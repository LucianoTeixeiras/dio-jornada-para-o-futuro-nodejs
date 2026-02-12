# Guia de Estudos - Como Usar Este Repositório

## 📚 Filosofia de Aprendizado

Este repositório segue a metodologia **"Aprender Fazendo"**:
- Leitura mínima e focada nos conceitos essenciais
- Exercícios guiados passo a passo
- Projetos incrementais que evoluem a cada módulo
- Testes automatizados para validar o aprendizado
- Checklists para acompanhar o progresso

## 🚀 Como Começar

### 1. Clone o Repositório

```bash
git clone https://github.com/LucianoTeixeiras/dio-jornada-para-o-futuro-nodejs.git
cd dio-jornada-para-o-futuro-nodejs
```

### 2. Verifique os Pré-requisitos

Certifique-se de ter instalado:
- **Node.js** (versão 18 ou superior): [nodejs.org](https://nodejs.org)
- **Git**: [git-scm.com](https://git-scm.com)
- **Editor de código**: VS Code recomendado

Verifique as versões:
```bash
node --version
npm --version
git --version
```

### 3. Escolha um Módulo

Comece pelo **módulo 00-fundamentos** e siga em ordem sequencial.

## 📖 Estrutura de Cada Módulo

Cada módulo dentro de `modules/` segue a mesma estrutura:

```
XX-nome-modulo/
├── README.md           # Visão geral e objetivos do módulo
├── docs/
│   ├── concepts.md     # Conceitos essenciais (leitura mínima)
│   └── resources.md    # Links e recursos adicionais
├── exercises/
│   ├── 01-exercise/    # Exercícios guiados
│   ├── 02-exercise/
│   └── solutions/      # Soluções dos exercícios
├── project/            # Projeto incremental do módulo
│   ├── src/
│   ├── tests/
│   └── README.md
├── CHECKLIST.md        # Lista de verificação do aprendizado
└── package.json        # Dependências do módulo
```

## 🎯 Metodologia de Estudo

### Passo 1: Leia o README.md do Módulo
- Entenda os objetivos
- Veja o tempo estimado
- Identifique os pré-requisitos

### Passo 2: Estude os Conceitos (docs/concepts.md)
- Leitura focada de 20-30 minutos
- Apenas o essencial, sem sobrecarga de informação
- Anote dúvidas para explorar depois

### Passo 3: Faça os Exercícios Guiados
- Siga a ordem numérica
- Tente resolver sozinho primeiro
- Consulte as soluções se travar por mais de 15 minutos
- Entenda o "porquê", não apenas copie

### Passo 4: Desenvolva o Projeto Incremental
- Cada módulo adiciona features ao projeto
- Siga as instruções no README do projeto
- Escreva código limpo e bem documentado

### Passo 5: Execute os Testes
```bash
cd modules/XX-nome-modulo
npm install
npm test
```

### Passo 6: Complete o Checklist
- Marque cada item conforme completa
- Seja honesto com seu aprendizado
- Revise itens não compreendidos

## 🛠️ Convenções do Repositório

### Estilo de Código

- **JavaScript/TypeScript**: Seguimos o [Standard Style](https://standardjs.com/)
- **Indentação**: 2 espaços
- **Aspas**: Simples (`'`) para strings
- **Ponto-e-vírgula**: Sempre usar
- **Nomenclatura**:
  - `camelCase` para variáveis e funções
  - `PascalCase` para classes
  - `UPPER_SNAKE_CASE` para constantes

### Commits

```
tipo(escopo): descrição curta

Descrição mais detalhada se necessário

Tipos: feat, fix, docs, style, refactor, test, chore
Exemplo: feat(auth): adicionar validação JWT
```

### Branches

- `main`: código estável
- `develop`: desenvolvimento em andamento
- `feature/nome-da-feature`: novas funcionalidades
- `fix/nome-do-bug`: correções

## ⚙️ Como Rodar os Projetos

### Instalação de Dependências

Cada módulo é independente. Entre no diretório e instale:

```bash
cd modules/XX-nome-modulo
npm install
```

### Executar o Projeto

```bash
npm start          # Modo produção
npm run dev        # Modo desenvolvimento (com hot-reload)
```

### Executar Testes

```bash
npm test           # Todos os testes
npm run test:watch # Modo watch
npm run test:coverage # Com cobertura
```

### Linting e Formatação

```bash
npm run lint       # Verificar código
npm run lint:fix   # Corrigir automaticamente
npm run format     # Formatar código
```

## 🐛 Debug e Troubleshooting

### VS Code Debug

Cada módulo inclui configuração `.vscode/launch.json`:
1. Abra o arquivo que quer debugar
2. Coloque breakpoints (F9)
3. Pressione F5 para iniciar o debug

### Logs

Use o padrão:
```javascript
console.log('[INFO]', mensagem);
console.error('[ERROR]', erro);
console.warn('[WARN]', aviso);
```

### Problemas Comuns

**Erro de dependências não encontradas:**
```bash
rm -rf node_modules package-lock.json
npm install
```

**Porta já em uso:**
```bash
# Matar processo na porta 3000
npx kill-port 3000
```

## 📊 Acompanhamento de Progresso

### Checklist Global

Mantenha seu progresso atualizado:
- [ ] Módulo 00: Fundamentos
- [ ] Módulo 01: HTTP e REST
- [ ] Módulo 02: TypeScript
- [ ] Módulo 03: Autenticação

### Métricas de Sucesso

Para cada módulo, considere completo quando:
- ✅ Todos os exercícios resolvidos
- ✅ Projeto funcional com testes passando
- ✅ Checklist 100% marcado
- ✅ Código revisado e refatorado
- ✅ Conceitos principais dominados

## 💡 Dicas de Aprendizado

1. **Consistência > Intensidade**: 1h por dia é melhor que 7h em um dia
2. **Pratique primeiro, aprofunde depois**: Faça funcionar antes de otimizar
3. **Ensine para aprender**: Explique os conceitos para alguém (ou para você mesmo)
4. **Construa seu próprio projeto paralelo**: Aplique o que aprendeu
5. **Participe da comunidade**: Discord, fóruns, StackOverflow

## 🤝 Contribuindo

Encontrou um erro? Tem uma sugestão?
- Abra uma issue
- Envie um pull request
- Compartilhe seu feedback

## 📞 Suporte

- **Issues**: Para bugs e problemas técnicos
- **Discussions**: Para dúvidas e discussões
- **Wiki**: Para documentação adicional

---

**Boa jornada! 🚀**
