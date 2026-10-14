# Lançamento assistido de notas de serviço (NFS-e)

> **Área:** Financeiro · **Status:** Em uso · assistido (uma pessoa revisa e salva)

## Problema

Notas de serviço chegam como foto ou PDF e precisavam ser lidas e digitadas no contas a pagar do ERP, escolhendo fornecedor e conta contábil.

## Solução

O robô busca as notas pendentes, abre as imagens da nota e do boleto, extrai os dados com OCR (data, prestador, número, valor e código de barras), sugere fornecedor e conta contábil e deixa o formulário do ERP pré-preenchido. Uma pessoa revisa e salva. Depois de lançada, a nota é marcada e o fornecedor é memorizado para a próxima vez.

## Tecnologias

- Python
- Playwright
- OCR via Google Drive/Docs API
- PostgreSQL / Supabase (REST)

## Resultado

O trabalho de digitar caiu para revisar e salvar, e o sistema melhora a cada nota porque aprende os fornecedores.

## Minha atuação

Levantamento do processo real, definição das regras de negócio, desenvolvimento, testes, tratamento de falhas e ajustes de confiabilidade.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
