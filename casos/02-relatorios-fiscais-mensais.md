# Relatórios fiscais mensais para a contabilidade

> **Área:** Contabilidade e fiscal · **Status:** Em produção · roda sozinho no 1º dia útil do mês

## Problema

No começo de cada mês, alguém precisava entrar no ERP, gerar o relatório de cupons fiscais de cada loja e entregar os arquivos organizados para a contabilidade.

## Solução

Um robô detecta o primeiro dia útil do mês, gera o relatório do mês anterior para todas as unidades e salva cada arquivo na pasta certa, com nome padronizado, na nuvem da contabilidade. Registra logs de cada passo e avisa no celular.

## Tecnologias

- Python
- Playwright
- Requests
- Windows Task Scheduler
- Notificações push

## Resultado

Rotina mensal que não depende mais de ninguém lembrar de fazer, com nomes e pastas sempre padronizados.

## O que eu fiz

Inspecionei a página do relatório ao vivo e descobri que ele tem URL própria e um formulário de filtro direto, o que evitou o caminho mais frágil pela lista de relatórios. Defini a regra do primeiro dia útil e o padrão de nomes e pastas com a contabilidade.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
