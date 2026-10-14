# Entrada de NF-e de mercadoria com apoio de IA

> **Área:** Compras e estoque · **Status:** Em uso · assistido (uma pessoa confere e salva)

## Problema

A cada nota de mercadoria recebida, era preciso manifestar o recebimento no sistema fiscal e dar entrada manual no ERP, convertendo cada item para a unidade usada no estoque.

## Solução

As lojas escaneiam a chave da nota pelo celular; o robô pega a fila, faz a manifestação do destinatário, abre a entrada de mercadoria, importa a NF-e e preenche os campos. A conversão de quantidade segue uma ordem: tabela de conversões já aprendidas, depois regras por texto e, só por último, a API do Claude (IA). O robô respeita o limite de consultas por hora do órgão fiscal e **para antes de salvar**, para um humano conferir.

## Tecnologias

- Python
- Playwright
- PostgreSQL / Supabase
- API da Anthropic (Claude) para inferir conversões de unidade
- Expressões regulares

## Resultado

Menos digitação e menos erro de unidade, com a decisão final sempre nas mãos de uma pessoa.

## O que eu fiz

Descobri as regras do órgão fiscal, como o limite de consultas por hora, e desenhei a ordem de conversão (tabela aprendida, regras, IA por último), guiando a IA com instruções precisas e deixando sempre uma pessoa com a decisão final.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
