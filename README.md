# StoreGo Web

Frontend Web para o sistema StoreGo - Plataforma SaaS multi-organizacional para gestão empresarial.

## Stack Tecnológica

| Tecnologia | Descrição |
|------------|------------|
| Vite | Build tool |
| React | Framework UI |
| TypeScript | Linguagem |
| TanStack Query | Server state |
| Shadcn/ui | Componentes |
| Tailwind CSS | Estilização |
| React Hook Form | Formulários |
| Zod | Validação |
| Biome | Linting |
| Vitest | Testes |

## Começando

### Instalação

```bash
# Instalar dependências
bun install

# Configurar variáveis de ambiente
cp .env.example .env

# Iniciar desenvolvimento
bun run dev
```

### Variáveis de Ambiente

Consulte `.env.example` para todas as variáveis necessárias.

## Estrutura

```
src/
├── app/           # App root, router, providers
├── components/    # Componentes reutilizáveis
├── features/      # Funcionalidades por módulo
├── lib/          # Utilitários
├── hooks/        # Hooks personalizados
├── types/        # Tipos TypeScript
└── styles/       # Estilos globais
```

## Documentação

- [Especificação Técnica](./storego-web.specs.md)
- [Requisitos](./storego.specs.md)

## Licença

MIT