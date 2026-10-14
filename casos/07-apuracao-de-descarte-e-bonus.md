# Apuração de descarte e bônus de equipe

> **Área:** Operação e controle · **Status:** Em produção · roda no fechamento do mês

## Problema

Medir a perda de produtos por loja, compará-la com as vendas e calcular o bônus de cada equipe exigia reunir dezenas de planilhas e PDFs e aplicar as regras na mão, a cada mês.

## Solução

Um pipeline copia os arquivos da pasta do mês na nuvem, lê os relatórios de estoque e os controles semanais (massa de waffle, produção própria, café, torta e gelato vendido × utilizado), consolida o descarte, compara com as vendas, aplica as regras de bonificação e gera a planilha consolidada e os PDFs para impressão, loja por loja. Uma tarefa agendada confere o calendário e só roda no dia certo do fechamento, e cada execução termina num resumo com checklist de diagnóstico: arquivos que faltam e valores fora da curva ficam visíveis em vez de passarem despercebidos. As regras de bônus (meta de faturamento como condição, pontos por categoria e ajuste pela faixa de descarte) estão documentadas, e eu preparei documentos de decisão para a diretoria comparando alternativas de regra.

## Tecnologias

- Python
- pandas
- OpenPyXL
- pdfplumber
- Geração de PDFs e documentos Word
- Windows Task Scheduler

## Resultado

Fechamento mensal reproduzível, com as regras documentadas em código e os mesmos números para todas as lojas. O último fechamento rodou com avisos de arquivos faltando, que o próprio resumo apontou e que foram completados na mesma manhã. A regra de bonificação está em validação com a diretoria.

## O que eu fiz

Levantei as regras de bonificação com a gestão, traduzi tudo em código e documentei de onde vem cada número para que qualquer pessoa consiga conferir. Quando a regra precisou ser decidida, preparei documentos comparando as alternativas para a diretoria, e deixei o resumo de cada fechamento apontando o que faltou.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
