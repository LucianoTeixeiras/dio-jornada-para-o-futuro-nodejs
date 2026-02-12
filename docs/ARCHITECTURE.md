# Arquitetura e Decisões Técnicas

## 🏗️ Visão Geral da Arquitetura

Este repositório é estruturado como um **monorepo didático**, onde cada módulo é uma unidade independente de aprendizado, mas todos compartilham convenções e padrões comuns.

## 📁 Estrutura de Diretórios

```
dio-jornada-para-o-futuro-nodejs/
├── docs/                      # Documentação central
│   ├── ROADMAP.md            # Trilha completa de aprendizado
│   ├── GUIDE.md              # Como estudar e usar o repo
│   └── ARCHITECTURE.md       # Este arquivo
├── modules/                   # Módulos de aprendizado
│   ├── 00-fundamentos/
│   ├── 01-http-rest/
│   ├── 02-typescript/
│   └── 03-auth/
├── .gitignore
├── LICENSE
└── README.md
```

## 🎯 Princípios de Design

### 1. Modularidade e Independência

**Decisão:** Cada módulo é auto-contido com suas próprias dependências.

**Razão:**
- Permite estudar módulos isoladamente
- Facilita atualização de dependências por módulo
- Evita conflitos de versão entre módulos
- Estudante pode deletar/recriar módulos sem afetar outros

**Implementação:**
```
modules/XX-nome/
└── package.json  # Dependências específicas do módulo
```

### 2. Progressão Incremental

**Decisão:** Cada módulo constrói sobre o anterior, mas pode ser estudado independentemente.

**Razão:**
- Reforça aprendizado cumulativo
- Permite revisão de conceitos anteriores
- Facilita identificar lacunas de conhecimento

**Implementação:**
- Módulos numerados sequencialmente (00, 01, 02...)
- Pré-requisitos claros em cada README
- Projeto incremental que evolui

### 3. Mínimo Viável de Leitura

**Decisão:** Documentação focada apenas no essencial.

**Razão:**
- Reduz sobrecarga cognitiva
- Foco em prática, não teoria excessiva
- Links para aprofundamento opcional

**Implementação:**
- `concepts.md`: Máximo 2-3 páginas por módulo
- `resources.md`: Links para aprofundamento

### 4. Aprendizado Orientado a Testes

**Decisão:** Cada módulo inclui testes automatizados.

**Razão:**
- Valida compreensão de forma objetiva
- Ensina TDD desde o início
- Feedback imediato sobre erros

**Implementação:**
```javascript
// Exemplo de estrutura de teste
describe('Módulo XX - Conceito', () => {
  it('deve demonstrar compreensão do conceito', () => {
    // Arrange, Act, Assert
  });
});
```

## 🔧 Decisões Técnicas

### Escolha de Ferramentas

| Ferramenta | Uso | Justificativa |
|------------|-----|---------------|
| **Node.js 18+** | Runtime | LTS, features modernas, estabilidade |
| **npm** | Gerenciador de pacotes | Nativo, amplamente adotado |
| **JavaScript/TypeScript** | Linguagens | Progressão natural JS → TS |
| **Express** | Framework web | Padrão da indústria, simples |
| **Jest** | Testes | Completo, fácil configuração |
| **ESLint** | Linting | Qualidade de código |
| **Prettier** | Formatação | Consistência automática |

### Padrões de Código

#### 1. Estrutura de Arquivos por Módulo

```
XX-nome-modulo/
├── src/              # Código fonte
│   ├── controllers/  # Lógica de controle
│   ├── models/       # Modelos de dados
│   ├── routes/       # Definição de rotas
│   ├── services/     # Lógica de negócio
│   ├── utils/        # Utilitários
│   └── index.js      # Entry point
├── tests/            # Testes
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── docs/             # Documentação do módulo
├── exercises/        # Exercícios práticos
├── package.json
└── README.md
```

#### 2. Padrão de Projeto: MVC/Clean Architecture

**Camadas:**

```
┌─────────────────────────────────┐
│         Controllers             │ ← Recebe requisições HTTP
│      (Express handlers)          │
└────────────┬────────────────────┘
             │
             ▼
┌─────────────────────────────────┐
│          Services               │ ← Lógica de negócio
│     (Business logic)             │
└────────────┬────────────────────┘
             │
             ▼
┌─────────────────────────────────┐
│           Models                │ ← Estrutura de dados
│      (Data structures)           │
└─────────────────────────────────┘
```

**Exemplo:**

```javascript
// controllers/userController.js
export const getUser = async (req, res) => {
  const user = await userService.findById(req.params.id);
  res.json(user);
};

// services/userService.js
export const findById = async (id) => {
  // Lógica de negócio
  return await User.findById(id);
};

// models/User.js
export class User {
  constructor(id, name, email) {
    this.id = id;
    this.name = name;
    this.email = email;
  }
}
```

#### 3. Tratamento de Erros

**Decisão:** Middleware centralizado de erros.

```javascript
// middlewares/errorHandler.js
export const errorHandler = (err, req, res, next) => {
  const statusCode = err.statusCode || 500;
  const message = err.message || 'Erro interno do servidor';
  
  res.status(statusCode).json({
    success: false,
    error: message,
    ...(process.env.NODE_ENV === 'development' && { stack: err.stack })
  });
};

// Custom error classes
export class AppError extends Error {
  constructor(message, statusCode) {
    super(message);
    this.statusCode = statusCode;
  }
}
```

#### 4. Configuração e Variáveis de Ambiente

**Decisão:** Uso de `.env` para configurações.

```
# .env.example
NODE_ENV=development
PORT=3000
DATABASE_URL=mongodb://localhost:27017/myapp
JWT_SECRET=your-secret-key
```

```javascript
// config/index.js
import dotenv from 'dotenv';
dotenv.config();

export const config = {
  env: process.env.NODE_ENV || 'development',
  port: process.env.PORT || 3000,
  database: {
    url: process.env.DATABASE_URL
  },
  jwt: {
    secret: process.env.JWT_SECRET
  }
};
```

#### 5. Segurança

**Decisões de Segurança:**

- ✅ Sanitização de inputs
- ✅ Validação de dados
- ✅ Rate limiting
- ✅ Helmet.js para headers seguros
- ✅ CORS configurado adequadamente
- ✅ Senhas com bcrypt (hash + salt)
- ✅ JWTs com expiração
- ✅ Validação de tokens
- ✅ Proteção contra SQL Injection (quando aplicável)
- ✅ Proteção contra XSS

```javascript
// Exemplo de middleware de segurança
import helmet from 'helmet';
import rateLimit from 'express-rate-limit';
import cors from 'cors';

app.use(helmet());
app.use(cors({
  origin: process.env.ALLOWED_ORIGINS?.split(',') || '*'
}));

const limiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutos
  max: 100 // limite de requisições
});
app.use('/api/', limiter);
```

## 📊 Estratégia de Testes

### Pirâmide de Testes

```
       /\
      /  \
     / E2E\     ← Poucos testes end-to-end
    /------\
   /  Inte  \   ← Testes de integração moderados
  /  gration \
 /------------\
/    Unit      \ ← Muitos testes unitários
/   Tests       \
------------------
```

### Tipos de Testes por Módulo

1. **Testes Unitários**: Funções, classes, utilitários isolados
2. **Testes de Integração**: APIs, banco de dados, serviços
3. **Testes E2E**: Fluxos completos (apenas em módulos avançados)

### Exemplo de Estrutura de Teste

```javascript
// tests/unit/services/userService.test.js
import { findById } from '../../../src/services/userService';

describe('UserService', () => {
  describe('findById', () => {
    it('deve retornar usuário quando ID é válido', async () => {
      const user = await findById('123');
      expect(user).toBeDefined();
      expect(user.id).toBe('123');
    });

    it('deve lançar erro quando ID é inválido', async () => {
      await expect(findById('invalid')).rejects.toThrow();
    });
  });
});
```

## 🔄 Versionamento e Evolução

### Semantic Versioning

Seguimos [SemVer](https://semver.org/):
- **MAJOR**: Mudanças incompatíveis
- **MINOR**: Novas funcionalidades compatíveis
- **PATCH**: Correções de bugs

### Changelog

Mantemos `CHANGELOG.md` para rastrear mudanças importantes.

## 🚀 Deploy e Ambientes

### Ambientes

1. **Development**: Desenvolvimento local
2. **Testing**: Para testes automatizados
3. **Production**: Simulação de produção (módulos avançados)

### Variáveis por Ambiente

```javascript
// config/environments/
├── development.js
├── testing.js
└── production.js
```

## 📝 Documentação

### Níveis de Documentação

1. **README.md**: Overview do módulo
2. **concepts.md**: Conceitos essenciais
3. **JSDoc**: Documentação inline no código
4. **API Docs**: Swagger/OpenAPI (para APIs)

### Exemplo de JSDoc

```javascript
/**
 * Busca usuário por ID
 * @param {string} id - ID do usuário
 * @returns {Promise<User>} Usuário encontrado
 * @throws {AppError} Quando usuário não é encontrado
 */
export const findById = async (id) => {
  // implementação
};
```

## 🎓 Filosofia Pedagógica

### Aprendizado Progressivo

1. **Conceitos básicos primeiro**: Fundamentos antes de abstrações
2. **Do simples ao complexo**: Incrementar complexidade gradualmente
3. **Prática > Teoria**: Código antes de explicação extensa
4. **Feedback rápido**: Testes imediatos, iteração rápida

### Anti-padrões Evitados

- ❌ Over-engineering prematuro
- ❌ Abstrações excessivas para iniciantes
- ❌ Frameworks complexos antes dos fundamentos
- ❌ Documentação extensa sem prática
- ❌ Projetos irrealistas ou muito complexos

## 🔮 Roadmap de Evolução

### Versão 1.0 (Atual)
- Módulos 00-03
- Estrutura base
- Exercícios e projetos

### Versão 2.0 (Futuro)
- Módulos 04-07 (Database, Testing, Docker, Deploy)
- Projeto final integrado
- Vídeos complementares

### Versão 3.0 (Futuro)
- Módulos 08-10 (Microservices, GraphQL, Real-time)
- Certificação automatizada
- Comunidade e gamificação

---

**Última atualização:** 2026-02-12
