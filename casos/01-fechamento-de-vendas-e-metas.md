# Fechamento semanal de vendas e metas

> **Área:** Comercial e metas · **Status:** Em produção · roda sozinho todos os dias

## Problema

O acompanhamento de vendas contra metas, loja por loja, era feito à mão: baixar relatórios do ERP, somar por categoria, atualizar planilhas e montar PDFs para a diretoria e para as lojas. Podia consumir uma semana de trabalho a cada fechamento.

## Solução

Um robô entra sozinho no ERP, baixa o relatório de vendas de cada loja, soma por categoria, atualiza as planilhas de meta e gera os PDFs (um para a diretoria e um por loja). Vira o mês sozinho no fechamento, avisa no celular quando termina e cria um evento na agenda compartilhada para aprovação. Mais recentemente passou a enviar os mesmos números para um banco de dados na nuvem, que alimenta um painel de metas, e ganhou uma carga única de histórico para popular o painel.

## Tecnologias

- Python
- Playwright
- OpenPyXL / Excel
- LibreOffice (PDF)
- Google Calendar API
- PostgreSQL via API REST
- Windows Task Scheduler

## Resultado

O processo, que podia levar uma semana de trabalho, passou a rodar automaticamente em cerca de 5 minutos. Veja também o [caso público original](https://github.com/Rapunzelmina/Sales-Closing-Automation).

## Minha atuação

Levantamento do processo real, definição das regras de negócio, desenvolvimento, testes, tratamento de falhas e ajustes de confiabilidade.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
