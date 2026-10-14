# Fechamento semanal de vendas e metas

> **Área:** Comercial e metas · **Status:** Em produção · roda sozinho todos os dias

## Problema

O acompanhamento de vendas contra metas, loja por loja, era feito à mão: baixar relatórios do ERP, somar por categoria, atualizar planilhas e montar PDFs para a diretoria e para as lojas. Podia consumir uma semana de trabalho a cada fechamento.

## Solução

Um robô entra sozinho no ERP, baixa o relatório de vendas de cada loja, soma por categoria, atualiza as planilhas de meta e gera os PDFs (um para a diretoria e um por loja). Vira o mês sozinho no fechamento, avisa no celular quando termina e cria um evento na agenda compartilhada para aprovação. Mais recentemente passou a enviar os mesmos números para um banco de dados na nuvem, que alimenta um painel de metas, e ganhou uma carga única de histórico para popular o painel. Para ser confiável, o robô refaz sozinho a loja que falha logo após o login (comum quando o ERP devolve uma página de erro), protege a virada de mês (uma unidade que não fechou o mês fica de fora e a equipe recebe um alerta de prioridade alta, em vez de herdar um mês incompleto), gera um PDF completo no último ciclo do mês, lê de volta as metas digitadas no aplicativo da empresa para gravá-las nas planilhas e nos PDFs, e a tarefa agendada acorda o computador e roda ao retornar quando o horário é perdido.

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

## O que eu fiz

Identifiquei o gargalo nos relatórios semanais de vendas e inspecionei as telas do ERP (botões, filtros e o caminho de cada relatório) para descobrir como automatizar um sistema sem API. Traduzi as regras do fechamento (categorias, checkpoints, virada de mês) em código e testei com os números reais antes de deixar rodar sozinho. Depois, lendo os logs, investiguei uma falha recorrente (uma unidade que errava na primeira carga do ERP), criei a nova tentativa automática e a proteção da virada de mês, e ajustei o agendador do Windows para a tarefa não perder o dia quando o computador dorme.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
