# Futebol FDS

Aplicação web construída com **Next.js (App Router)**. O projeto está na fase inicial: a página atual ainda é o template gerado pelo `create-next-app`, pronta para receber as funcionalidades.

## Tecnologias

| Tecnologia | Versão | Uso |
| --- | --- | --- |
| [Next.js](https://nextjs.org) | 16.4.3 | Framework React com App Router, Cache Components e Partial Prefetching |
| [React](https://react.dev) | 19.3.0 | Interface, com **React Compiler** ativado |
| [TypeScript](https://www.typescriptlang.org) | 5.x | Tipagem estática |
| [Tailwind CSS](https://tailwindcss.com) | 4.x | Estilização (via `@tailwindcss/turbopack`) |
| [Turbopack](https://nextjs.org/docs/app/api-reference/turbopack) | — | Bundler de desenvolvimento e build |
| [ESLint](https://eslint.org) | 9.x | Lint com `eslint-config-next` |
| [Geist](https://vercel.com/font) | — | Fontes Geist Sans e Geist Mono via `next/font` |

Configurações relevantes em [next.config.ts](next.config.ts): `cacheComponents`, `partialPrefetching` e `reactCompiler` habilitados.

## Pré-requisitos

- Node.js 20 ou superior
- npm

## Como rodar

```bash
# instalar dependências
npm install

# servidor de desenvolvimento
npm run dev
```

Acesse [http://localhost:3000](http://localhost:3000).

## Scripts

| Comando | Descrição |
| --- | --- |
| `npm run dev` | Inicia o servidor de desenvolvimento |
| `npm run build` | Gera o build de produção |
| `npm run start` | Executa o build de produção |
| `npm run lint` | Roda o ESLint |

## Estrutura do projeto

```
futebol-fds/
├── app/
│   ├── layout.tsx      # Layout raiz (fontes Geist, metadata)
│   ├── page.tsx        # Página inicial
│   └── globals.css     # Estilos globais e Tailwind
├── public/             # Arquivos estáticos
├── next.config.ts      # Configuração do Next.js
├── eslint.config.mjs   # Configuração do ESLint
├── tsconfig.json       # Configuração do TypeScript
├── AGENTS.md           # Instruções para agentes de IA
└── claude.md           # Convenções do projeto para o Claude Code
```

## Convenções

- **Server Components por padrão**: use `'use client'` apenas quando precisar de hooks, eventos ou APIs do navegador.
- Rotas ficam em `app/`, componentes reutilizáveis em `components/` e helpers em `lib/`.
- Esta versão do Next.js tem mudanças em relação às anteriores. Consulte a documentação em `node_modules/next/dist/docs/` antes de usar APIs novas.

## Skills de IA

O repositório inclui skills para agentes de código (Claude Code, Aider) em `.claude/skills/`, `.agents/skills/` e `.aider-desk/skills/`:

- `vercel-react-best-practices`: boas práticas de performance para React e Next.js
- `web-design-guidelines`: diretrizes de design e acessibilidade para web

## Deploy

A forma mais simples de publicar é pela [Vercel](https://vercel.com/new). Veja também a [documentação de deploy do Next.js](https://nextjs.org/docs/app/getting-started/deploying).
