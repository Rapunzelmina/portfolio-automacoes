# Margem de delivery por aplicativo

> **Área:** Comercial e delivery · **Status:** Em evolução · painel refeito, automação e cupom pendentes

## Problema

Existia visão de receita e quantidade de vendas por aplicativo de delivery, mas não do custo, então ninguém sabia a margem real de cada canal.

## Solução

Um pipeline lê dois relatórios do ERP por loja e por mês (vendas por produto e custo médio), cruza pelo código do produto e pela loja, considera só os aplicativos de delivery, valida o total contra o do robô de vendas e sinaliza anomalias (preço unitário muito baixo, quantidade muito alta). Grava custo total, custo médio por unidade, percentual de custo e margem em cada aba de loja, sem mudar o endereço das células, para que o robô de vendas continue escrevendo nos mesmos lugares. O painel foi refeito só com fórmulas, sem valores fixos: seletor de loja, indicadores, evolução mensal, desempenho por aplicativo, comparativo entre as lojas com ranking e destaques gerados por fórmula, com formatação condicional e gráficos nativos.

## Tecnologias

- Python
- pandas
- OpenPyXL
- pdfplumber
- Excel (fórmulas, formatação condicional, gráficos de barras, linhas e rosca)

## Resultado

Passou a ser possível enxergar a tendência de margem de cada canal, o que antes não aparecia. Depois do feedback da gestão sobre o painel, o layout foi reconstruído; as regras de cálculo se mantiveram. Ainda faltam unificar tudo numa rotina única, automatizar a extração dos relatórios e incluir cupom e desconto.

## O que eu fiz

Validei a estrutura real de cada relatório do ERP (layout, colunas e casos especiais) antes de cruzar vendas e custo, e escrevi um roteiro com as regras, os pontos de verificação e o que não pode mudar para trabalhar com a IA com segurança. Reconstruí o painel depois do feedback da gestão sem mexer nos endereços que o robô usa.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
