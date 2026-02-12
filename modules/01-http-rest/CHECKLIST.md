# Checklist de Aprendizado - Módulo 01: HTTP e REST APIs

## 📋 Protocolo HTTP

### HTTP Fundamentals
- [ ] Entendo o que é o protocolo HTTP
- [ ] Sei a diferença entre HTTP e HTTPS
- [ ] Conheço o modelo cliente-servidor
- [ ] Entendo o conceito de stateless protocol

### HTTP Methods
- [ ] Entendo GET (recuperar recursos)
- [ ] Entendo POST (criar recursos)
- [ ] Entendo PUT (atualizar recurso completo)
- [ ] Entendo PATCH (atualizar parcialmente)
- [ ] Entendo DELETE (remover recursos)
- [ ] Conheço outros métodos (HEAD, OPTIONS, etc.)
- [ ] Sei quando usar cada método

### Status Codes
- [ ] Conheço os principais códigos 2xx (sucesso)
- [ ] Conheço os principais códigos 3xx (redirecionamento)
- [ ] Conheço os principais códigos 4xx (erro do cliente)
- [ ] Conheço os principais códigos 5xx (erro do servidor)
- [ ] Sei escolher o status code apropriado

### Headers e Body
- [ ] Entendo o que são HTTP headers
- [ ] Conheço headers comuns (Content-Type, Authorization, etc.)
- [ ] Sei trabalhar com request body
- [ ] Entendo diferentes content types (JSON, form-data, etc.)

## 🌐 Servidor HTTP Nativo

### Node.js HTTP Module
- [ ] Sei criar servidor HTTP com módulo nativo
- [ ] Entendo req (request) e res (response)
- [ ] Consigo parsear URL e query parameters
- [ ] Sei lidar com diferentes métodos HTTP
- [ ] Consigo retornar JSON como resposta

## ⚡ Express.js

### Setup e Configuração
- [ ] Sei instalar e configurar Express
- [ ] Entendo a estrutura básica de uma app Express
- [ ] Conheço app.listen() e porta do servidor
- [ ] Sei configurar o ambiente (development/production)

### Routing
- [ ] Sei criar rotas com Express
- [ ] Entendo route parameters (:id)
- [ ] Sei trabalhar com query strings (?page=1)
- [ ] Conheço route handlers
- [ ] Sei organizar rotas em arquivos separados (Router)

### Request e Response
- [ ] Sei acessar dados com req.body, req.params, req.query
- [ ] Consigo enviar respostas com res.send(), res.json()
- [ ] Sei definir status codes com res.status()
- [ ] Entendo res.redirect() e res.render()

## 🔧 Middlewares

### Conceitos
- [ ] Entendo o que são middlewares
- [ ] Compreendo a ordem de execução
- [ ] Sei a importância de next()
- [ ] Conheço a assinatura (req, res, next)

### Built-in Middlewares
- [ ] Sei usar express.json() para parsear JSON
- [ ] Sei usar express.urlencoded() para forms
- [ ] Conheço express.static() para arquivos estáticos

### Third-party Middlewares
- [ ] Sei usar cors para Cross-Origin Resource Sharing
- [ ] Conheço morgan para logging
- [ ] Sei usar helmet para segurança
- [ ] Entendo compression para compressão de respostas

### Custom Middlewares
- [ ] Sei criar middlewares customizados
- [ ] Consigo aplicar middleware globalmente
- [ ] Sei aplicar middleware em rotas específicas
- [ ] Implemento logging personalizado
- [ ] Crio middleware de autenticação básico

## 🏗️ Arquitetura REST

### REST Principles
- [ ] Entendo o que é REST
- [ ] Conheço os princípios RESTful
- [ ] Sei estruturar URLs como recursos
- [ ] Entendo stateless communication
- [ ] Conheço HATEOAS (opcional)

### Resource Design
- [ ] Sei nomear recursos (plural vs singular)
- [ ] Estruturo URLs hierárquicas (/users/:id/posts)
- [ ] Evito verbos em URLs
- [ ] Uso substantivos para recursos

### CRUD Operations
- [ ] Implemento Create (POST)
- [ ] Implemento Read (GET)
- [ ] Implemento Update (PUT/PATCH)
- [ ] Implemento Delete (DELETE)
- [ ] Retorno status codes apropriados

## ✅ Validação e Sanitização

### Input Validation
- [ ] Sei validar dados com express-validator
- [ ] Valido tipos de dados (string, number, email, etc.)
- [ ] Valido tamanhos e formatos
- [ ] Implemento validações customizadas
- [ ] Retorno erros de validação claros

### Data Sanitization
- [ ] Sei sanitizar inputs para prevenir XSS
- [ ] Normalizo dados (trim, lowercase, etc.)
- [ ] Escapo caracteres especiais quando necessário

## 🛡️ Segurança e Best Practices

### Segurança Básica
- [ ] Implemento CORS corretamente
- [ ] Uso helmet para headers de segurança
- [ ] Valido e sanitizo todas as entradas
- [ ] Implemento rate limiting básico
- [ ] Sei prevenir injection attacks

### Error Handling
- [ ] Implemento middleware de erro centralizado
- [ ] Crio classes de erro customizadas
- [ ] Trato erros de forma consistente
- [ ] Não exponho stack traces em produção
- [ ] Logo erros adequadamente

### Best Practices
- [ ] Separo código em camadas (routes, controllers, services)
- [ ] Uso variáveis de ambiente (.env)
- [ ] Implemento logging adequado
- [ ] Versiono minha API (/api/v1/)
- [ ] Implemento paginação em listas

## 📚 Documentação

### API Documentation
- [ ] Sei usar Swagger/OpenAPI
- [ ] Documento todos os endpoints
- [ ] Especifico schemas de request/response
- [ ] Documento códigos de erro
- [ ] Gero documentação interativa

### Code Documentation
- [ ] Uso JSDoc para funções
- [ ] Mantenho README atualizado
- [ ] Documento decisões arquiteturais

## 💻 Exercícios Práticos

- [ ] **Exercício 01**: HTTP Server - Servidor nativo
- [ ] **Exercício 02**: Express Basics - Primeira app Express
- [ ] **Exercício 03**: Middlewares - Criar e usar middlewares
- [ ] **Exercício 04**: REST API - CRUD completo

## 🚀 Projeto: Task Manager API

### Setup
- [ ] Projeto inicializado com Express
- [ ] Dependências instaladas
- [ ] Estrutura de pastas organizada
- [ ] Variáveis de ambiente configuradas

### Endpoints Implementados
- [ ] GET /api/tasks - Listar tarefas
- [ ] GET /api/tasks/:id - Obter tarefa específica
- [ ] POST /api/tasks - Criar tarefa
- [ ] PUT /api/tasks/:id - Atualizar tarefa
- [ ] DELETE /api/tasks/:id - Deletar tarefa
- [ ] GET /api/tasks/status/:status - Filtrar por status

### Features
- [ ] Validação de dados implementada
- [ ] Tratamento de erros centralizado
- [ ] Paginação funcionando
- [ ] Filtros e ordenação
- [ ] CORS configurado
- [ ] Segurança básica (helmet)

### Documentação
- [ ] Swagger/OpenAPI configurado
- [ ] Todos os endpoints documentados
- [ ] Schemas definidos
- [ ] Exemplos de request/response
- [ ] README com instruções de uso

### Testes
- [ ] Testes de integração escritos
- [ ] Todos os endpoints testados
- [ ] Casos de erro testados
- [ ] Validações testadas

## 🎓 Conhecimento Consolidado

### Auto-Avaliação
- [ ] Consigo criar uma API REST do zero
- [ ] Entendo profundamente o protocolo HTTP
- [ ] Sei estruturar uma aplicação Express
- [ ] Implemento segurança básica em APIs
- [ ] Documento APIs adequadamente
- [ ] Estou pronto para o próximo módulo

## 📝 Notas e Dúvidas

_Use este espaço para anotar conceitos que precisa revisar ou dúvidas a esclarecer_

---

**Data de início:** ___/___/___  
**Data de conclusão:** ___/___/___  
**Tempo total investido:** ___ horas
