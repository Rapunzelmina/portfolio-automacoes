# Margem de delivery por aplicativo

> **Área:** Comercial e delivery · **Status:** Em evolução · conceito em revisão com a gestão

## Problema

Existia visão de receita e quantidade de vendas por aplicativo de delivery, mas não do custo, então ninguém sabia a margem real de cada canal.

## Solução

Cruzamento automático entre vendas por produto e custo médio de cada produto (pelo código do produto, não pelo nome), calculando custo total, percentual de custo e margem por aplicativo, por loja e por mês. O resultado entra na planilha que a gerência já usava, com formatação por cor e um painel interativo (seletor de loja, indicadores e gráficos de tendência) feito só com recursos nativos do Excel.

## Tecnologias

- Python
- pandas
- Excel (fórmulas, formatação condicional, gráficos)

## Resultado

Passou a ser possível enxergar a tendência de margem de cada canal, o que antes não aparecia. O conceito segue em ajuste com a gestão.

## O que eu fiz

Validei a estrutura real de cada relatório do ERP (layout, colunas e casos especiais) antes de cruzar vendas e custo pelo código do produto, e tratei os casos em que um produto vendido não tem custo lançado no mês.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
