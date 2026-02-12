# Checklist de Aprendizado - Módulo 02: TypeScript

## 📋 Fundamentos do TypeScript

### Introdução e Setup
- [ ] Entendo o que é TypeScript e seus benefícios
- [ ] Sei a diferença entre TypeScript e JavaScript
- [ ] Instalei TypeScript globalmente (npm install -g typescript)
- [ ] Sei usar o compilador tsc
- [ ] Consigo criar e configurar tsconfig.json
- [ ] Entendo as opções principais do tsconfig.json

### Tipos Básicos
- [ ] Sei usar tipos primitivos (string, number, boolean)
- [ ] Trabalho com arrays (number[], Array<string>)
- [ ] Entendo any, unknown, never, void
- [ ] Sei usar null e undefined
- [ ] Conheço o tipo object
- [ ] Entendo type inference

### Anotações de Tipo
- [ ] Sei anotar variáveis com tipos
- [ ] Tipo parâmetros de funções
- [ ] Especifico tipos de retorno de funções
- [ ] Uso anotações em arrow functions
- [ ] Entendo quando TypeScript infere tipos

## 🔧 Tipos Avançados

### Arrays e Tuples
- [ ] Trabalho com arrays tipados
- [ ] Entendo tuples e seus usos
- [ ] Sei usar readonly em arrays
- [ ] Conheço array methods tipados

### Union e Intersection
- [ ] Sei usar Union Types (string | number)
- [ ] Entendo Intersection Types (Type1 & Type2)
- [ ] Uso type guards para Union Types
- [ ] Implemento discriminated unions

### Type Aliases
- [ ] Sei criar type aliases
- [ ] Uso aliases para tipos complexos
- [ ] Entendo quando usar type vs interface
- [ ] Crio aliases para unions e intersections

### Enums
- [ ] Sei criar numeric enums
- [ ] Trabalho com string enums
- [ ] Entendo const enums
- [ ] Uso enums para valores fixos

## 🏗️ Interfaces e Classes

### Interfaces
- [ ] Sei criar interfaces para objetos
- [ ] Uso propriedades opcionais (?)
- [ ] Implemento readonly properties
- [ ] Defino index signatures
- [ ] Estendo interfaces (extends)
- [ ] Uso interfaces para funções

### Classes
- [ ] Crio classes em TypeScript
- [ ] Uso modificadores de acesso (public, private, protected)
- [ ] Implemento constructors tipados
- [ ] Trabalho com getters e setters
- [ ] Uso static members
- [ ] Implemento abstract classes

### Interfaces vs Types
- [ ] Entendo diferenças entre interface e type
- [ ] Sei quando usar cada um
- [ ] Conheço declaration merging em interfaces

## ⚡ Generics

### Generics Básicos
- [ ] Entendo o conceito de generics
- [ ] Sei criar funções genéricas
- [ ] Uso generics com arrays
- [ ] Implemento classes genéricas
- [ ] Trabalho com interfaces genéricas

### Constraints
- [ ] Sei adicionar constraints a generics
- [ ] Uso extends para limitar tipos
- [ ] Implemento multiple type parameters
- [ ] Uso default generic types

## 🛠️ Utility Types

### Built-in Utilities
- [ ] Uso Partial<T> para propriedades opcionais
- [ ] Uso Required<T> para tornar tudo obrigatório
- [ ] Uso Readonly<T> para imutabilidade
- [ ] Uso Pick<T, K> para selecionar propriedades
- [ ] Uso Omit<T, K> para excluir propriedades
- [ ] Uso Record<K, T> para mapear tipos
- [ ] Conheço Exclude, Extract, NonNullable

### Custom Utilities
- [ ] Sei criar utility types personalizados
- [ ] Uso mapped types
- [ ] Implemento conditional types

## 🔍 Type Guards e Assertions

### Type Guards
- [ ] Uso typeof para primitive types
- [ ] Uso instanceof para classes
- [ ] Implemento custom type guards (is)
- [ ] Uso in operator para objects

### Type Assertions
- [ ] Sei fazer type casting com as
- [ ] Uso angle-bracket syntax (<Type>)
- [ ] Entendo quando assertions são necessárias
- [ ] Evito usar any desnecessariamente

## 🌐 TypeScript com Node.js

### Setup e Configuração
- [ ] Configurei projeto Node.js + TypeScript
- [ ] Instalei @types/node
- [ ] Configurei ts-node ou ts-node-dev
- [ ] Setup de build scripts
- [ ] Configurei source maps

### Módulos
- [ ] Uso ES modules (import/export) em TS
- [ ] Entendo module resolution
- [ ] Configurei paths em tsconfig
- [ ] Trabalho com default e named exports

## 🚀 TypeScript com Express

### Setup Express + TypeScript
- [ ] Configurei projeto Express com TS
- [ ] Instalei @types/express
- [ ] Tipei aplicação Express
- [ ] Configurei hot-reload com ts-node-dev

### Tipagem de Rotas
- [ ] Tipo Request e Response
- [ ] Uso RequestHandler type
- [ ] Tipo route parameters
- [ ] Tipo query strings
- [ ] Tipo request body

### Middlewares Tipados
- [ ] Crio middlewares com tipos corretos
- [ ] Tipo error handling middleware
- [ ] Estendo Request com propriedades customizadas
- [ ] Uso NextFunction corretamente

### Models e DTOs
- [ ] Crio interfaces para modelos
- [ ] Implemento DTOs (Data Transfer Objects)
- [ ] Uso validation com tipos
- [ ] Separo types em arquivos dedicados

## 🧪 Boas Práticas

### Code Organization
- [ ] Organizo tipos em arquivos .d.ts
- [ ] Uso barrel exports (index.ts)
- [ ] Separo interfaces de implementação
- [ ] Mantenho tipos próximos ao uso

### Type Safety
- [ ] Evito any sempre que possível
- [ ] Uso unknown ao invés de any quando necessário
- [ ] Habilito strict mode no tsconfig
- [ ] Trato null/undefined adequadamente

### Performance
- [ ] Uso const enums quando apropriado
- [ ] Entendo compilation vs runtime
- [ ] Otimizo imports para tree shaking

## 💻 Exercícios Práticos

- [ ] **Exercício 01**: Basics - Tipos primitivos e funções
- [ ] **Exercício 02**: Interfaces - Modelar dados complexos
- [ ] **Exercício 03**: Generics - Funções e classes genéricas
- [ ] **Exercício 04**: Express TS - API com TypeScript

## 🚀 Projeto: Task Manager API (TypeScript)

### Migração
- [ ] Projeto configurado com TypeScript
- [ ] Todos os arquivos .js convertidos para .ts
- [ ] Dependencies com @types instaladas
- [ ] Build pipeline funcionando

### Tipagem Implementada
- [ ] Interfaces para Task model
- [ ] DTOs para request/response
- [ ] Enums para status e prioridade
- [ ] Tipos para controllers
- [ ] Tipos para services
- [ ] Middlewares tipados

### Qualidade
- [ ] Strict mode habilitado
- [ ] Sem uso de any
- [ ] Type safety em toda aplicação
- [ ] Validações com tipos
- [ ] Código mais legível e manutenível

### Build e Deploy
- [ ] npm run build funciona
- [ ] dist/ gerado corretamente
- [ ] Source maps configurados
- [ ] Scripts de desenvolvimento e produção

## 🎓 Conhecimento Consolidado

### Auto-Avaliação
- [ ] Entendo profundamente o sistema de tipos do TS
- [ ] Consigo tipar aplicações complexas
- [ ] Sei configurar projetos TypeScript do zero
- [ ] Uso generics de forma efetiva
- [ ] Aplico TypeScript em projetos reais
- [ ] Estou pronto para o próximo módulo

## 📝 Notas e Dúvidas

_Use este espaço para anotar conceitos que precisa revisar ou dúvidas a esclarecer_

---

**Data de início:** ___/___/___  
**Data de conclusão:** ___/___/___  
**Tempo total investido:** ___ horas
