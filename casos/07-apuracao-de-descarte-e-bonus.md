# Apuração de descarte e bônus de equipe

> **Área:** Operação e controle · **Status:** Em produção · roda no fechamento do mês

## Problema

Medir a perda de produtos por loja, compará-la com as vendas e calcular o bônus de cada equipe exigia reunir dezenas de planilhas e PDFs e aplicar as regras na mão, a cada mês.

## Solução

Um pipeline lê os relatórios de estoque e de metas de cada loja, consolida o descarte, compara com as vendas, aplica as regras de bonificação (metas atingidas e melhora no índice de perda) e gera a planilha consolidada e os PDFs para impressão, loja por loja. Uma tarefa agendada confere o calendário e só roda no dia certo do fechamento.

## Tecnologias

- Python
- pandas
- OpenPyXL
- pdfplumber
- Geração de PDFs
- Windows Task Scheduler

## Resultado

Fechamento mensal reproduzível, com as regras documentadas em código e os mesmos números para todas as lojas.

## O que eu fiz

Levantei as regras de bonificação com a gestão (metas atingidas e melhora no índice de perda), traduzi tudo em código e documentei de onde vem cada número para que qualquer pessoa consiga conferir o resultado.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
