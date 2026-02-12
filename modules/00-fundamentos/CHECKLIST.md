# Checklist de Aprendizado - Módulo 00: Fundamentos

## 📋 Conceitos Fundamentais

### Node.js Basics
- [ ] Entendo o que é Node.js e sua relação com V8
- [ ] Sei a diferença entre JavaScript no browser e no Node.js
- [ ] Compreendo o conceito de runtime JavaScript
- [ ] Conheço os use cases principais do Node.js

### Event Loop
- [ ] Entendo como funciona o Event Loop
- [ ] Sei a diferença entre código síncrono e assíncrono
- [ ] Compreendo o conceito de non-blocking I/O
- [ ] Entendo a ordem de execução: Call Stack, Callback Queue, Event Loop

### Módulos
- [ ] Sei criar módulos com CommonJS (module.exports, require)
- [ ] Sei criar módulos com ES Modules (import/export)
- [ ] Entendo a diferença entre CommonJS e ES Modules
- [ ] Sei quando usar cada sistema de módulos
- [ ] Conheço os módulos core do Node.js (fs, path, os, http, etc.)

## 🔧 NPM e Gerenciamento de Pacotes

### NPM Fundamentals
- [ ] Sei inicializar um projeto com npm init
- [ ] Entendo a estrutura do package.json
- [ ] Sei instalar dependências (dependencies vs devDependencies)
- [ ] Conheço semantic versioning (^, ~, etc.)
- [ ] Sei usar npm scripts

### Trabalhando com Pacotes
- [ ] Sei buscar pacotes no npmjs.com
- [ ] Consigo instalar pacotes localmente e globalmente
- [ ] Entendo o que é node_modules e package-lock.json
- [ ] Sei remover e atualizar dependências

## ⚡ Programação Assíncrona

### Callbacks
- [ ] Entendo o padrão de callbacks em Node.js
- [ ] Sei lidar com erros em callbacks (error-first pattern)
- [ ] Conheço o problema do "callback hell"

### Promises
- [ ] Sei criar e consumir Promises
- [ ] Entendo os estados de uma Promise (pending, fulfilled, rejected)
- [ ] Sei usar .then(), .catch() e .finally()
- [ ] Consigo encadear Promises

### Async/Await
- [ ] Sei usar async/await para código assíncrono
- [ ] Entendo que async functions retornam Promises
- [ ] Sei tratar erros com try/catch em async functions
- [ ] Consigo usar Promise.all(), Promise.race(), etc.

## 📁 Sistema de Arquivos (fs)

### Operações Básicas
- [ ] Sei ler arquivos (fs.readFile, fs.readFileSync)
- [ ] Sei escrever arquivos (fs.writeFile, fs.writeFileSync)
- [ ] Sei trabalhar com diretórios (fs.mkdir, fs.readdir)
- [ ] Entendo a diferença entre operações síncronas e assíncronas
- [ ] Sei usar fs.promises para operações com async/await

### Operações Avançadas
- [ ] Sei copiar, mover e deletar arquivos
- [ ] Consigo obter informações de arquivos (fs.stat)
- [ ] Sei trabalhar com caminhos usando o módulo path
- [ ] Entendo file descriptors e fs.open/fs.close

## 🌊 Streams e Buffers

### Buffers
- [ ] Entendo o que são Buffers
- [ ] Sei criar e manipular Buffers
- [ ] Conheço métodos básicos (Buffer.from, toString, etc.)

### Streams
- [ ] Entendo o conceito de Streams
- [ ] Conheço os tipos: Readable, Writable, Duplex, Transform
- [ ] Sei usar fs.createReadStream e fs.createWriteStream
- [ ] Entendo o conceito de piping (.pipe())
- [ ] Sei quando usar Streams vs carregar arquivo completo

## 🐛 Debugging

### Técnicas de Debug
- [ ] Sei usar console.log efetivamente
- [ ] Conheço o debugger do Node.js (node inspect)
- [ ] Sei debugar com VS Code
- [ ] Entendo como usar breakpoints
- [ ] Sei inspecionar variáveis e call stack

### Error Handling
- [ ] Sei criar e lançar erros (throw new Error)
- [ ] Entendo try/catch para código síncrono
- [ ] Sei tratar erros em Promises e async/await
- [ ] Conheço o objeto Error e suas propriedades

## 💻 Exercícios Práticos

- [ ] **Exercício 01**: Hello Node - Primeiro script Node.js
- [ ] **Exercício 02**: Módulos - Criar e importar módulos
- [ ] **Exercício 03**: Async - Trabalhar com Promises e async/await
- [ ] **Exercício 04**: File System - Manipular arquivos e diretórios
- [ ] **Exercício 05**: Streams - Processar arquivo grande com streams

## 🚀 Projeto: CLI Tool

### Setup e Estrutura
- [ ] Projeto inicializado com npm init
- [ ] Dependências instaladas (commander, chalk, etc.)
- [ ] Estrutura de diretórios criada
- [ ] README do projeto escrito

### Funcionalidades Implementadas
- [ ] Comando para listar arquivos (ls)
- [ ] Comando para criar arquivo (touch)
- [ ] Comando para ler arquivo (cat)
- [ ] Comando para copiar arquivo (cp)
- [ ] Comando para mover arquivo (mv)
- [ ] Comando para deletar arquivo (rm)
- [ ] Comando para buscar em arquivos (grep)
- [ ] Comando para estatísticas (stats)

### Qualidade e Testes
- [ ] Código está organizado e legível
- [ ] Tratamento de erros implementado
- [ ] Testes básicos escritos
- [ ] Documentação das funções (JSDoc)
- [ ] CLI funciona corretamente

## 🎓 Conhecimento Consolidado

### Auto-Avaliação
- [ ] Consigo explicar como Node.js funciona para outra pessoa
- [ ] Me sinto confortável criando scripts Node.js
- [ ] Entendo quando usar código síncrono vs assíncrono
- [ ] Sei organizar código em módulos
- [ ] Consigo debugar problemas básicos
- [ ] Estou pronto para o próximo módulo

## 📝 Notas e Dúvidas

_Use este espaço para anotar conceitos que precisa revisar ou dúvidas a esclarecer_

---

**Data de início:** ___/___/___  
**Data de conclusão:** ___/___/___  
**Tempo total investido:** ___ horas
