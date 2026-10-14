# App de recebimento e financeiro (PWA)

> **Área:** Financeiro e operação das lojas · **Status:** Em produção

## Problema

As lojas recebiam notas e boletos em papel, WhatsApp e e-mail, sem um registro único. Aprovação de pagamentos, borderô, conciliação bancária e acompanhamento de metas viviam em planilhas separadas.

## Solução

Um aplicativo instalável no celular, num único lugar, com login por usuário e perfis de acesso. Na loja: leitura do código de barras da nota (chave de 44 dígitos) e fotos da nota e do boleto. Para o financeiro: fila de aprovação com regras de roteamento, borderô de pagamentos, **tesouraria** (importa o extrato do banco em OFX e concilia automaticamente com o que o ERP marcou como pago, separando o que bateu, o que está só no banco e o que está só no ERP) e **painel de metas** (cada loja vê a sua meta e a diretoria cadastra metas novas).

## Tecnologias

- HTML, CSS e JavaScript puro (PWA)
- Supabase (Auth, PostgreSQL, Storage, row level security)
- zxing-wasm (código de barras)
- PDF.js e SheetJS
- Vercel

## Resultado

Um registro único das notas, aprovação com histórico, conciliação bancária e metas acessíveis no celular, com cada pessoa vendo só o que o seu perfil permite.

## O que eu fiz

Desenhei as telas e os perfis a partir da rotina real das lojas e do financeiro, e pesquisei e implementei a leitura de código de barras, a importação de extrato OFX para a conciliação e o painel de metas.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
