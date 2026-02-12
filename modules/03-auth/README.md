# Módulo 03: Autenticação e Autorização

## 🎯 Objetivos de Aprendizado

Ao completar este módulo, você será capaz de:

- ✅ Entender conceitos de autenticação e autorização
- ✅ Implementar JWT (JSON Web Tokens)
- ✅ Hash de senhas com bcrypt
- ✅ Criar sistema de registro e login
- ✅ Implementar middleware de autenticação
- ✅ Gerenciar permissões e roles
- ✅ Aplicar boas práticas de segurança
- ✅ Configurar CORS e rate limiting

## ⏱️ Tempo Estimado

**15-20 horas** (distribuídas em 5-7 dias)

## 📋 Pré-requisitos

- ✅ Módulo 00: Fundamentos concluído
- ✅ Módulo 01: HTTP e REST concluído
- ✅ Módulo 02: TypeScript concluído
- Compreensão básica de segurança web

## 📚 Estrutura do Módulo

```
03-auth/
├── README.md              # Este arquivo
├── CHECKLIST.md           # Lista de verificação do aprendizado
├── docs/
│   ├── concepts.md        # Conceitos essenciais
│   └── resources.md       # Links e recursos adicionais
├── exercises/             # Exercícios práticos (a ser criado)
│   ├── 01-bcrypt/
│   ├── 02-jwt/
│   ├── 03-auth-flow/
│   ├── 04-rbac/
│   └── solutions/
└── project/               # Projeto: Secure Task Manager API (a ser criado)
    ├── src/
    ├── tests/
    └── README.md
```

## 🗺️ Roteiro de Estudo

### Semana 1: Fundamentos de Segurança

#### Dia 1-2: Autenticação vs Autorização
- Conceitos fundamentais
- Diferentes estratégias de autenticação
- Hashing vs Encryption
- **Exercício**: Hash de senhas com bcrypt

#### Dia 3-4: JSON Web Tokens (JWT)
- O que são JWTs
- Estrutura (Header, Payload, Signature)
- Geração e validação de tokens
- **Exercício**: Implementar JWT

#### Dia 5-7: Fluxo de Autenticação
- Registro de usuários
- Login e geração de token
- Refresh tokens
- **Exercício**: Sistema de login completo

### Semana 2: Autorização e Segurança Avançada

#### Dia 8-10: Middleware de Autenticação
- Proteger rotas
- Extrair e validar tokens
- Error handling em auth
- **Exercício**: Middleware de proteção

#### Dia 11-12: Roles e Permissões (RBAC)
- Role-Based Access Control
- Implementar diferentes níveis de acesso
- Autorização granular
- **Exercício**: Sistema de permissões

#### Dia 13-15: Projeto Final
- **Projeto**: Secure Task Manager API
- Autenticação completa
- Autorização por roles
- Boas práticas de segurança

## 🚀 Projeto do Módulo

**Secure Task Manager API**

API de gerenciamento de tarefas com autenticação e autorização completas:

**Features de Autenticação:**
- Registro de usuários com validação
- Login com email e senha
- JWT tokens (access + refresh)
- Logout e invalidação de tokens
- Recuperação de senha (opcional)

**Features de Autorização:**
- Roles: Admin, User, Guest
- Usuários só veem suas próprias tarefas
- Admins podem ver todas as tarefas
- Permissões granulares por endpoint

**Segurança:**
- Senhas hasheadas com bcrypt
- Tokens JWT seguros
- Rate limiting
- CORS configurado
- Helmet para headers de segurança
- Validação e sanitização de inputs

**Tecnologias:**
- bcrypt ou bcryptjs
- jsonwebtoken
- express-rate-limit
- helmet
- cors

## 📖 Conceitos-Chave

1. **Authentication**: Verificar identidade do usuário
2. **Authorization**: Verificar permissões do usuário
3. **Hashing**: Armazenamento seguro de senhas
4. **JWT**: Tokens stateless para autenticação
5. **RBAC**: Controle de acesso baseado em roles
6. **Security Headers**: Proteção contra ataques comuns
7. **Rate Limiting**: Prevenção de abuso
8. **CORS**: Controle de acesso cross-origin

## ✅ Critérios de Conclusão

Você completou este módulo quando:

- [ ] Entende diferença entre autenticação e autorização
- [ ] Implementa JWT corretamente
- [ ] Hash senhas com bcrypt
- [ ] Cria sistema de registro/login funcional
- [ ] Protege rotas com middleware
- [ ] Implementa roles e permissões
- [ ] Aplica boas práticas de segurança
- [ ] Projeto Secure API funcional
- [ ] Todos os testes passam
- [ ] Completou o CHECKLIST.md

## 🔗 Próximos Passos

Após concluir este módulo, você domina os fundamentos de Node.js e está pronto para:
- **Módulo 04**: Bancos de Dados
- **Módulo 05**: Testes Automatizados
- **Módulo 06**: Docker e Containerização
- **Módulo 07**: Deploy e CI/CD

## 📚 Recursos Adicionais

- [JWT.io](https://jwt.io/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [bcrypt npm](https://www.npmjs.com/package/bcrypt)
- [Express Security Best Practices](https://expressjs.com/en/advanced/best-practice-security.html)

---

**Bons estudos! 🚀**
