# Módulo 01: HTTP e REST APIs

## 🎯 Objetivos de Aprendizado

Ao completar este módulo, você será capaz de:

- ✅ Entender o protocolo HTTP e seus métodos
- ✅ Criar servidores HTTP com Node.js nativo
- ✅ Desenvolver APIs REST com Express.js
- ✅ Implementar middlewares customizados
- ✅ Criar rotas e controllers organizados
- ✅ Validar dados de entrada
- ✅ Tratar erros de forma centralizada
- ✅ Documentar APIs com Swagger/OpenAPI

## ⏱️ Tempo Estimado

**15-20 horas** (distribuídas em 5-7 dias)

## 📋 Pré-requisitos

- ✅ Módulo 00: Fundamentos concluído
- Conhecimento de HTTP básico
- Familiaridade com JSON
- Ferramentas: Postman ou Insomnia

## 📚 Estrutura do Módulo

```
01-http-rest/
├── README.md              # Este arquivo
├── CHECKLIST.md           # Lista de verificação do aprendizado
├── docs/
│   ├── concepts.md        # Conceitos essenciais
│   └── resources.md       # Links e recursos adicionais
├── exercises/             # Exercícios práticos (a ser criado)
│   ├── 01-http-server/
│   ├── 02-express-basics/
│   ├── 03-middlewares/
│   ├── 04-rest-api/
│   └── solutions/
└── project/               # Projeto: Task Manager API (a ser criado)
    ├── src/
    ├── tests/
    └── README.md
```

## 🗺️ Roteiro de Estudo

### Semana 1: HTTP e Express Fundamentals

#### Dia 1-2: Protocolo HTTP
- HTTP methods (GET, POST, PUT, DELETE, PATCH)
- Status codes e seus significados
- Headers e body
- **Exercício**: Servidor HTTP nativo

#### Dia 3-4: Express.js Basics
- Setup e configuração inicial
- Rotas básicas
- Request e Response objects
- **Exercício**: Primeira aplicação Express

#### Dia 5-7: Middlewares
- O que são middlewares
- Ordem de execução
- Middlewares built-in vs customizados
- Error handling middleware
- **Exercício**: Criar middlewares próprios

### Semana 2: REST APIs

#### Dia 8-10: REST API Design
- Princípios REST
- Estrutura de URLs (resources)
- CRUD operations
- **Exercício**: API de produtos

#### Dia 11-12: Validação e Segurança
- Validação de dados (express-validator)
- Sanitização de inputs
- CORS e segurança básica
- **Exercício**: Validações em API

#### Dia 13-15: Projeto Final
- **Projeto**: Task Manager API completa
- Documentação com Swagger
- Testes de integração

## 🚀 Projeto do Módulo

**Task Manager API**

Uma API REST completa para gerenciamento de tarefas:

**Endpoints:**
- `GET /api/tasks` - Listar todas as tarefas
- `GET /api/tasks/:id` - Obter uma tarefa
- `POST /api/tasks` - Criar nova tarefa
- `PUT /api/tasks/:id` - Atualizar tarefa
- `DELETE /api/tasks/:id` - Deletar tarefa
- `GET /api/tasks/status/:status` - Filtrar por status

**Features:**
- Validação de dados
- Tratamento de erros
- Paginação
- Filtros e ordenação
- Documentação Swagger

**Tecnologias:**
- Express.js
- express-validator
- swagger-ui-express
- cors
- helmet

## 📖 Conceitos-Chave

1. **HTTP Protocol**: Métodos, headers, status codes
2. **REST Architecture**: Princípios e boas práticas
3. **Express.js**: Framework web minimalista
4. **Middlewares**: Pipeline de processamento de requisições
5. **Routing**: Organização de endpoints
6. **Validation**: Segurança e integridade de dados
7. **Error Handling**: Tratamento centralizado de erros
8. **API Documentation**: Swagger/OpenAPI

## ✅ Critérios de Conclusão

Você completou este módulo quando:

- [ ] Entende o protocolo HTTP profundamente
- [ ] Sabe criar APIs REST com Express
- [ ] Implementa middlewares customizados
- [ ] Valida dados de entrada adequadamente
- [ ] Trata erros de forma centralizada
- [ ] Documentou sua API com Swagger
- [ ] Projeto Task Manager API funcional
- [ ] Todos os testes passam
- [ ] Completou o CHECKLIST.md

## 🔗 Próximo Módulo

Após concluir este módulo, você estará pronto para:
→ **Módulo 02: TypeScript**

## 📚 Recursos Adicionais

- [Express.js Documentation](https://expressjs.com/)
- [HTTP Status Codes](https://httpstatuses.com/)
- [REST API Best Practices](https://restfulapi.net/)
- [Swagger/OpenAPI](https://swagger.io/specification/)

---

**Bons estudos! 🚀**
