# Módulo 02: TypeScript

## 🎯 Objetivos de Aprendizado

Ao completar este módulo, você será capaz de:

- ✅ Entender os benefícios do TypeScript
- ✅ Trabalhar com tipos básicos e avançados
- ✅ Criar interfaces e types
- ✅ Utilizar generics
- ✅ Configurar TypeScript em projetos Node.js
- ✅ Integrar TypeScript com Express
- ✅ Implementar type safety em APIs

## ⏱️ Tempo Estimado

**15-20 horas** (distribuídas em 5-7 dias)

## 📋 Pré-requisitos

- ✅ Módulo 00: Fundamentos concluído
- ✅ Módulo 01: HTTP e REST concluído
- Conhecimento sólido de JavaScript ES6+

## 📚 Estrutura do Módulo

```
02-typescript/
├── README.md              # Este arquivo
├── CHECKLIST.md           # Lista de verificação do aprendizado
├── docs/
│   ├── concepts.md        # Conceitos essenciais
│   └── resources.md       # Links e recursos adicionais
├── exercises/             # Exercícios práticos (a ser criado)
│   ├── 01-basics/
│   ├── 02-interfaces/
│   ├── 03-generics/
│   ├── 04-express-ts/
│   └── solutions/
└── project/               # Projeto: Migração da API para TS (a ser criado)
    ├── src/
    ├── tests/
    └── README.md
```

## 🗺️ Roteiro de Estudo

### Semana 1: TypeScript Fundamentals

#### Dia 1-2: Introdução ao TypeScript
- O que é TypeScript e por que usar
- Configuração e setup (tsc, tsconfig.json)
- Tipos básicos (string, number, boolean, etc.)
- **Exercício**: Primeiros scripts TypeScript

#### Dia 3-4: Tipos Avançados
- Arrays e Tuples
- Enums
- Union e Intersection Types
- Type Aliases
- **Exercício**: Trabalhar com tipos complexos

#### Dia 5-7: Interfaces e Classes
- Interfaces vs Types
- Classes e modificadores de acesso
- Herança e abstração
- **Exercício**: Modelagem de dados com interfaces

### Semana 2: TypeScript em Produção

#### Dia 8-10: Generics e Utilitários
- Generics básicos
- Utility Types (Partial, Pick, Omit, etc.)
- Type Guards
- **Exercício**: Funções genéricas

#### Dia 11-12: TypeScript com Node.js/Express
- Configuração de projeto TS + Express
- Tipagem de Request/Response
- Middlewares tipados
- **Exercício**: API Express com TypeScript

#### Dia 13-15: Projeto Final
- **Projeto**: Migrar Task Manager API para TypeScript
- Adicionar tipos completos
- Refatorar com boas práticas TS

## 🚀 Projeto do Módulo

**Task Manager API - TypeScript Version**

Migração completa da API do módulo anterior para TypeScript:

**Objetivos:**
- Converter todo código JavaScript para TypeScript
- Adicionar interfaces para todos os modelos
- Tipar requests, responses e middlewares
- Implementar enums para status e prioridades
- Usar generics para funções utilitárias
- Configurar build pipeline com TypeScript

**Tecnologias:**
- TypeScript 5+
- ts-node-dev (desenvolvimento)
- @types/express, @types/node
- TSLint ou ESLint + TypeScript

## 📖 Conceitos-Chave

1. **Static Typing**: Benefícios da tipagem estática
2. **Type Inference**: TypeScript infere tipos automaticamente
3. **Interfaces**: Contratos de estrutura de dados
4. **Generics**: Código reutilizável e type-safe
5. **Type Guards**: Runtime type checking
6. **tsconfig.json**: Configuração do compilador
7. **Utility Types**: Transformação de tipos
8. **Integration**: TypeScript com Node.js e Express

## ✅ Critérios de Conclusão

Você completou este módulo quando:

- [ ] Entende os benefícios do TypeScript
- [ ] Sabe trabalhar com tipos básicos e avançados
- [ ] Cria interfaces e types adequadamente
- [ ] Utiliza generics de forma efetiva
- [ ] Configurou TypeScript em projeto Node.js
- [ ] Migrou API para TypeScript com sucesso
- [ ] Todos os testes passam
- [ ] Completou o CHECKLIST.md

## 🔗 Próximo Módulo

Após concluir este módulo, você estará pronto para:
→ **Módulo 03: Autenticação e Autorização**

## 📚 Recursos Adicionais

- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/)
- [TypeScript Deep Dive](https://basarat.gitbook.io/typescript/)
- [TypeScript with Express](https://www.digitalocean.com/community/tutorials/typescript-express-getting-started)

---

**Bons estudos! 🚀**
