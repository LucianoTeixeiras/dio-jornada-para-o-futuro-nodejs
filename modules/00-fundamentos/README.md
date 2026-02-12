# Módulo 00: Fundamentos do Node.js

## 🎯 Objetivos de Aprendizado

Ao completar este módulo, você será capaz de:

- ✅ Entender o que é Node.js e como funciona
- ✅ Trabalhar com Event Loop e programação assíncrona
- ✅ Gerenciar pacotes com NPM
- ✅ Criar e usar módulos (CommonJS e ES Modules)
- ✅ Manipular arquivos com o módulo `fs`
- ✅ Trabalhar com Streams e Buffers
- ✅ Debugar aplicações Node.js

## ⏱️ Tempo Estimado

**15-20 horas** (distribuídas em 5-7 dias)

## 📋 Pré-requisitos

- Conhecimento básico de JavaScript (ES6+)
- Familiaridade com terminal/linha de comando
- Node.js 18+ instalado
- Editor de código (VS Code recomendado)

## 📚 Estrutura do Módulo

```
00-fundamentos/
├── README.md              # Este arquivo
├── CHECKLIST.md           # Lista de verificação do aprendizado
├── docs/
│   ├── concepts.md        # Conceitos essenciais
│   └── resources.md       # Links e recursos adicionais
├── exercises/             # Exercícios práticos (a ser criado)
│   ├── 01-hello-node/
│   ├── 02-modules/
│   ├── 03-async/
│   ├── 04-fs/
│   └── solutions/
└── project/               # Projeto: CLI Tool (a ser criado)
    ├── src/
    ├── tests/
    └── README.md
```

## 🗺️ Roteiro de Estudo

### Semana 1: Conceitos Fundamentais

#### Dia 1-2: Introdução ao Node.js
- O que é Node.js
- Diferenças entre Browser JavaScript e Node.js
- Event Loop e arquitetura não-bloqueante
- **Exercício**: Hello World e primeiros scripts

#### Dia 3-4: Módulos e NPM
- Sistema de módulos (CommonJS vs ES Modules)
- NPM: instalação e uso
- package.json e versionamento semântico
- **Exercício**: Criar e usar módulos próprios

#### Dia 5-7: Assincronia
- Callbacks, Promises e Async/Await
- Error handling em código assíncrono
- **Exercício**: Operações assíncronas

### Semana 2: Aplicações Práticas

#### Dia 8-10: Sistema de Arquivos
- Módulo `fs` (filesystem)
- Leitura e escrita de arquivos
- Operações síncronas vs assíncronas
- **Exercício**: Manipulação de arquivos

#### Dia 11-12: Streams e Buffers
- O que são Streams
- Readable, Writable, Duplex, Transform
- Buffers e manipulação de dados binários
- **Exercício**: Processamento de arquivos grandes

#### Dia 13-15: Projeto Final
- **Projeto**: CLI Tool para manipulação de arquivos
- Aplicação prática de todos os conceitos
- Testes e debugging

## 🚀 Projeto do Módulo

**CLI Tool - File Manager**

Um aplicativo de linha de comando para:
- Listar arquivos e diretórios
- Criar, copiar, mover e deletar arquivos
- Buscar conteúdo em arquivos
- Estatísticas de uso de disco

**Tecnologias:**
- Node.js core modules (fs, path, os)
- Commander.js (CLI framework)
- Chalk (colorir output)

## 📖 Conceitos-Chave

1. **Event Loop**: Como Node.js gerencia operações assíncronas
2. **Non-blocking I/O**: Modelo de I/O não-bloqueante
3. **Módulos**: Organização e reutilização de código
4. **NPM**: Gerenciamento de dependências
5. **Assincronia**: Callbacks, Promises, Async/Await
6. **Streams**: Processamento eficiente de dados

## ✅ Critérios de Conclusão

Você completou este módulo quando:

- [ ] Entende como o Event Loop funciona
- [ ] Sabe criar e usar módulos
- [ ] Domina async/await e error handling
- [ ] Consegue manipular arquivos com fs
- [ ] Implementou o projeto CLI Tool
- [ ] Todos os testes passam
- [ ] Completou o CHECKLIST.md

## 🔗 Próximo Módulo

Após concluir este módulo, você estará pronto para:
→ **Módulo 01: HTTP e REST APIs**

## 📚 Recursos Adicionais

- [Documentação oficial do Node.js](https://nodejs.org/docs)
- [Node.js Event Loop Explained](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/)
- [NPM Documentation](https://docs.npmjs.com/)

---

**Bons estudos! 🚀**
