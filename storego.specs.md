# STOREGO - Documento de Especificação de Requisitos

## 1. INTRODUÇÃO

### 1.1 Propósito do Documento

Este documento estabelece a especificação completa de requisitos para o sistema **StoreGo**, uma plataforma SaaS multi-organizacional para gestão empresarial integrada com controle de assinaturas, gamificação e gestão de força de campo.

### 1.2 Escopo do Sistema (6 Módulos + Super Administrador)

| Módulo | Descrição | Prioridade |
|--------|----------|------------|
| **Módulo de Tarefas** | Gestão de tarefas, equipes, projetos, visualizações | Must |
| **Módulo de Temperatura** | Equipamentos, ambientes, veículos, alertas | Must |
| **Módulo de Gestão de Ativos** | Cadastro, inventário, auditoria, baixa | Must |
| **Módulo de Manutenção** | Ordens de serviço com workflow de aprovação, SLA, custos | Should |
| **Módulo de Assinaturas** | Gestão de planos, cobranças, gamificação | Must |
| **Módulo de Força de Campo** | Presença de promotores, escalas, dashboard | Must |
| **Super Administrador** | Gestão global do sistema | Must |

### 1.3 Diagrama de Contexto do Sistema

```
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                           SISTEMA STOREGO                           │
│  ┌─────────────────────────────────────────────────────────────────┐  │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐       │  │
│  │  │ Módulo   │  │ Módulo   │  │ Módulo   │  │ Módulo   │       │  │
│  │  │ Tarefas  │  │Temperatura│  │ Ativos   │  │Manutenção│       │  │
│  │  └──────────┘  └──────────┘  └──────────┘  └──────────┘       │  │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐                      │  │
│  │  │ Módulo   │  │ Módulo   │  │ Super    │                      │  │
│  │  │Assinaturas│  │Campo     │  │ Admin    │                      │  │
│  │  └──────────┘  └──────────┘  └──────────┘                      │  │
│  └─────────────────────────────────────────────────────────────────┘  │
└────────────────────────────────────────────────────────────────────┘
```

### 1.4 Atores Externos

| Ator | Descrição | Tipo |
|------|-----------|------|
| **Usuário Administrador** | Gerencia organização | Primário |
| **Usuário Gestor** | Cria projetos | Primário |
| **Promotor de Campo** | Realiza check-in | Primário |
| **Sensor IoT** | Envia temperatura | Sistema |
| **Stripe** | Pagamentos | Sistema |

### 1.5 Restrições do Projeto

| Aspecto | Definição |
|---------|----------|
| Prazo | 3 meses |
| Equipe | 1-2 desenvolvedores |
| Ambientes | Dev, Homologação, Produção |

---

## 2. STACK TECNOLÓGICA

### 2.1 Visão Geral

| Camada | Tecnologia |
|--------|------------|
| Runtime | Bun |
| Backend | Elysia + TypeScript |
| Frontend | React + TypeScript |
| Banco de Dados | PostgreSQL |
| ORM | Drizzle ORM |
| Cache | Redis |
| Armazenamento | AWS S3 |
| Gateway de Pagamento | Stripe |
| Linting | Biome |
| Logging | Pino |

---

## 3. MÓDULOS

### 3.1 Módulo de Tarefas
- Gestão de tarefas com visualizações Kanban, Lista e Timeline
- Equipes e Projetos
- Subtarefas, Checklists, Dependências
- Notificações

### 3.2 Módulo de Temperatura
- Sensores IoT
- Equipamentos (frozen, refrigerated, hot, ambient)
- Alertas automáticos (normal, alerta, crítico)
- Integração com manutenção

### 3.3 Módulo de Ativos
- Cadastro e categorização
- QR Code para auditoria
- Workflow de baixa
- Cálculo de depreciação

### 3.4 Módulo de Manutenção
- Ordens de serviço
- Workflow com gatekeeper
- SLA por prioridade
- Controle de custos

### 3.5 Módulo de Assinaturas
- Planos por loja
- Stripe integração
- Trial de 14 dias
- Gamificação

### 3.6 Módulo de Força de Campo
- Cadastro de promotores
- Check-in por QR Code
- GPS validação
- Dashboard de presença

### 3.7 Super Administrador
- Gestão global
- Métricas (MRR, Churn)
- Intervenção em pagamentos

---

*Versão do Documento: 1.1*  
*Última Atualização: 2026-04-23*  
*Autor: Equipa Técnica StoreGo*