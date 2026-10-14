# Contas a pagar: da extração à aprovação e ao borderô

> **Área:** Financeiro · **Status:** Em produção · roda sozinho todos os dias

## Problema

O contas a pagar vivia dentro do ERP, sem uma fila clara de aprovação nem uma visão consolidada do que pagar e quando.

## Solução

Todo dia um robô extrai as contas a pagar (janela de 90 dias para trás e para frente) e grava num banco PostgreSQL, sem duplicar registros. Sobre esses dados foram construídos a fila de aprovação, regras de roteamento por fornecedor, categorias automáticas para fornecedores novos e o borderô de pagamentos, tudo com controle de acesso por perfil no próprio banco (row level security).

## Tecnologias

- Python
- Playwright
- PostgreSQL / Supabase (REST, triggers, RLS)
- SQL
- Windows Task Scheduler

## Resultado

O que antes era uma lista dentro do ERP virou um fluxo com aprovador, histórico e borderô, atualizado todo dia sem intervenção.

## Minha atuação

Levantamento do processo real, definição das regras de negócio, desenvolvimento, testes, tratamento de falhas e ajustes de confiabilidade.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
