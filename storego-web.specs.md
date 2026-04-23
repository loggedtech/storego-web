# STOREGO WEB - Especificação Técnica do Frontend

## 1. VISÃO GERAL DO FRONTEND

### 1.1 Objetivos
- Interface responsiva e acessível
- Experiência de usuário intuitiva
- Integração eficiente com API REST
- Suporte a múltiplos módulos de negócio

### 1.2 Stack Tecnológica

| Camada | Tecnologia |
|--------|------------|
| Build Tool | Vite |
| Framework | React + TypeScript |
| Estado Global | React Hooks |
| Server State | TanStack Query |
| Componentes | Shadcn/ui |
| Estilização | Tailwind CSS |
| Formulários | React Hook Form + Zod |
| Testes | Vitest + Playwright |

---

## 2. ESTRUTURA DE PASTAS

```
src/
├── app/                    # Configuração principal
├── components/            # Componentes reutilizáveis
│   ├── ui/              # Componentes base (Shadcn)
│   └── layout/           # Componentes de layout
├── features/             # Funcionalidades por módulo
│   ├── auth/
│   ├── tasks/
│   ├── assets/
│   ├── temperature/
│   ├── maintenance/
│   ├── field-force/
│   └── subscriptions/
├── lib/                  # Utilitários
├── hooks/                # Hooks personalizados
├── types/                # Tipos TypeScript
└── styles/               # Estilos
```

---

*Versão do Documento: 1.1*  
*Última Atualização: 2026-04-23*  
*Autor: Equipa Técnica StoreGo*