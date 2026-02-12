# Checklist de Aprendizado - Módulo 03: Autenticação e Autorização

## 📋 Conceitos Fundamentais

### Autenticação vs Autorização
- [ ] Entendo a diferença entre autenticação e autorização
- [ ] Sei quando aplicar cada conceito
- [ ] Conheço diferentes estratégias de autenticação
- [ ] Entendo o fluxo básico de auth

### Segurança Básica
- [ ] Entendo hashing vs encryption
- [ ] Sei por que nunca armazenar senhas em plain text
- [ ] Conheço salt e sua importância
- [ ] Entendo o conceito de token-based authentication

## 🔐 Hashing de Senhas

### Bcrypt
- [ ] Sei instalar e configurar bcrypt
- [ ] Entendo como bcrypt funciona
- [ ] Sei gerar hash de senha
- [ ] Consigo comparar senha com hash
- [ ] Entendo salt rounds e seu impacto
- [ ] Sei escolher salt rounds apropriado

### Implementação
- [ ] Hasheo senhas no registro de usuário
- [ ] Comparo senhas no login
- [ ] Trato erros de hashing adequadamente
- [ ] Nunca exponho hashes em responses

## 🎫 JSON Web Tokens (JWT)

### Fundamentos JWT
- [ ] Entendo o que é JWT
- [ ] Conheço a estrutura (Header, Payload, Signature)
- [ ] Sei a diferença entre JWT e session-based auth
- [ ] Entendo quando usar JWT

### Trabalhando com JWT
- [ ] Sei gerar tokens com jsonwebtoken
- [ ] Configuro payload com dados necessários
- [ ] Defino expiração de tokens
- [ ] Assino tokens com secret seguro
- [ ] Verifico e decodifico tokens
- [ ] Trato tokens inválidos ou expirados

### Token Management
- [ ] Implemento access tokens
- [ ] Entendo refresh tokens
- [ ] Sei invalidar tokens (opcional com blacklist)
- [ ] Armazeno secrets em variáveis de ambiente

## 🔒 Sistema de Autenticação

### Registro de Usuários
- [ ] Valido dados de entrada (email, senha, etc.)
- [ ] Verifico se usuário já existe
- [ ] Hasheo senha antes de salvar
- [ ] Retorno resposta apropriada
- [ ] Trato erros de registro

### Login
- [ ] Valido credenciais
- [ ] Busco usuário por email
- [ ] Comparo senha com hash
- [ ] Gero JWT após login bem-sucedido
- [ ] Retorno token para o cliente
- [ ] Trato tentativas de login inválidas

### Logout
- [ ] Implemento logout no cliente (remover token)
- [ ] Considero invalidação de tokens no servidor (opcional)
- [ ] Limpo sessões ou tokens expirados

### Recuperação de Senha
- [ ] Implemento fluxo de "esqueci minha senha" (opcional)
- [ ] Gero token temporário para reset
- [ ] Valido token de reset
- [ ] Permito definir nova senha

## 🛡️ Middleware de Autenticação

### Proteção de Rotas
- [ ] Crio middleware de autenticação
- [ ] Extraio token do header (Authorization: Bearer)
- [ ] Verifico validade do token
- [ ] Adiciono dados do usuário ao req
- [ ] Retorno erro 401 se não autenticado
- [ ] Aplico middleware em rotas protegidas

### Error Handling
- [ ] Trato token ausente
- [ ] Trato token inválido
- [ ] Trato token expirado
- [ ] Retorno mensagens de erro claras

## 👥 Autorização e Permissões

### Roles (Papéis)
- [ ] Implemento sistema de roles (Admin, User, etc.)
- [ ] Armazeno role do usuário
- [ ] Incluo role no JWT payload
- [ ] Crio middleware para verificar roles

### RBAC (Role-Based Access Control)
- [ ] Implemento controle de acesso por role
- [ ] Defino permissões por endpoint
- [ ] Verifico permissões no middleware
- [ ] Retorno 403 Forbidden quando não autorizado

### Autorização Granular
- [ ] Usuários só acessam seus próprios recursos
- [ ] Implemento verificação de ownership
- [ ] Admins têm acesso a todos os recursos
- [ ] Aplico regras de negócio na autorização

## 🔐 Segurança Avançada

### CORS
- [ ] Entendo o que é CORS
- [ ] Configurei CORS adequadamente
- [ ] Defino origens permitidas
- [ ] Configuro headers permitidos
- [ ] Trato preflight requests

### Rate Limiting
- [ ] Implemento rate limiting
- [ ] Configuro limites por IP
- [ ] Aplico limites em endpoints sensíveis (login, registro)
- [ ] Retorno erro 429 quando limite excedido

### Security Headers (Helmet)
- [ ] Uso helmet para headers de segurança
- [ ] Entendo cada header que helmet configura
- [ ] Customizo configuração quando necessário

### Validação e Sanitização
- [ ] Valido todos os inputs
- [ ] Sanitizo dados para prevenir XSS
- [ ] Previno SQL Injection (quando aplicável)
- [ ] Uso bibliotecas de validação (express-validator)

## 🏗️ Boas Práticas

### Secrets e Configuração
- [ ] JWT_SECRET em variável de ambiente
- [ ] Nunca commito secrets no código
- [ ] Uso .env para configurações sensíveis
- [ ] Mantenho .env.example atualizado

### Token Security
- [ ] Tokens têm tempo de expiração razoável
- [ ] Uso algoritmos seguros (HS256, RS256)
- [ ] Não incluo informações sensíveis no payload
- [ ] Implemento refresh token strategy

### Password Security
- [ ] Exijo senhas fortes (validação)
- [ ] Uso salt rounds adequado (10-12)
- [ ] Nunca faço log de senhas
- [ ] Implemento rate limiting em login

### Error Handling
- [ ] Não exponho detalhes de implementação em erros
- [ ] Mensagens de erro genéricas para segurança
- [ ] Logo tentativas de autenticação falhadas
- [ ] Monitoro atividades suspeitas

## 💻 Exercícios Práticos

- [ ] **Exercício 01**: Bcrypt - Hash e comparação de senhas
- [ ] **Exercício 02**: JWT - Gerar e validar tokens
- [ ] **Exercício 03**: Auth Flow - Sistema de login completo
- [ ] **Exercício 04**: RBAC - Implementar roles e permissões

## 🚀 Projeto: Secure Task Manager API

### Autenticação
- [ ] Endpoint POST /auth/register implementado
- [ ] Endpoint POST /auth/login implementado
- [ ] Endpoint POST /auth/logout implementado
- [ ] Senhas hasheadas com bcrypt
- [ ] JWT gerado no login
- [ ] Tokens com expiração configurada

### Autorização
- [ ] Middleware de autenticação implementado
- [ ] Rotas protegidas com middleware
- [ ] Sistema de roles implementado
- [ ] Usuários só veem suas tarefas
- [ ] Admins veem todas as tarefas
- [ ] Autorização granular funcionando

### Segurança
- [ ] CORS configurado
- [ ] Helmet implementado
- [ ] Rate limiting em auth endpoints
- [ ] Validação de inputs completa
- [ ] Sanitização de dados
- [ ] Secrets em variáveis de ambiente

### Endpoints Protegidos
- [ ] GET /api/tasks - Requer autenticação
- [ ] POST /api/tasks - Requer autenticação
- [ ] PUT /api/tasks/:id - Requer ownership ou admin
- [ ] DELETE /api/tasks/:id - Requer ownership ou admin
- [ ] GET /api/admin/* - Requer role admin

### Testes
- [ ] Testes de registro de usuário
- [ ] Testes de login
- [ ] Testes de rotas protegidas
- [ ] Testes de autorização por role
- [ ] Testes de segurança

## 🎓 Conhecimento Consolidado

### Auto-Avaliação
- [ ] Entendo profundamente autenticação e autorização
- [ ] Consigo implementar JWT de forma segura
- [ ] Sei aplicar boas práticas de segurança
- [ ] Implemento RBAC adequadamente
- [ ] Conheço principais vulnerabilidades e como preveni-las
- [ ] Pronto para construir aplicações seguras

## 📝 Notas e Dúvidas

_Use este espaço para anotar conceitos que precisa revisar ou dúvidas a esclarecer_

---

**Data de início:** ___/___/___  
**Data de conclusão:** ___/___/___  
**Tempo total investido:** ___ horas
