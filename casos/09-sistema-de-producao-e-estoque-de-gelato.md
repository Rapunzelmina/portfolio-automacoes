# Sistema de controle de produção e estoque de gelato

> **Área:** Operação e controle · **Status:** Em operação e em expansão

## Problema

O pedido das lojas à cozinha central, a produção, a pesagem do gelato e o envase do delivery eram acompanhados em planilhas separadas. Não havia registro de quem pesou o quê, nem comparação entre o que foi produzido, o que saiu e o que foi perdido.

## Solução

Um sistema web instalável, com cinco perfis de acesso (administrador, loja, confeiteiro, gelateiro e líder). **Pedido:** a loja recebe uma sugestão calculada de quantas BAGs pedir e registra o que foi enviado, com motivo quando muda a quantidade. **Produção:** a cozinha registra quantidade, peso e foto da balança. **Laboratório do gelato:** pesagem de cubas com foto, conferência por uma segunda pessoa (quem registra não confere a própria), tolerâncias, tara, perda de prova e descarte com motivo, resultando num mapa de produção por sabor e por loja, com ranking e ocorrências para o controle. O mapa do mês também é exportado para um Excel formatado, com painel e gráficos, mapa de calor por sabor, ranking semanal e uma aba por dia com as contas em fórmulas. **Delivery:** compara o gelato usado com os potes enchidos e a gramatura de cada tamanho. **Equipe e turnos:** acesso por PIN, com bloqueio após tentativas erradas. Também há cardápio do mês, consulta de compras e estoque, e importadores que trazem relatórios do ERP e planilhas para o banco, com sincronização diária agendada.

## Tecnologias

- JavaScript puro (módulos ES) e PWA, publicado na Vercel
- Supabase: PostgreSQL, Auth, Storage, funções e triggers, row level security (11 migrações)
- Python: importadores de relatórios e planilhas, sincronização diária agendada
- Playwright: robô que baixa relatórios do ERP
- Protótipo inicial em FastAPI + SQLite

## Resultado

Em poucas semanas o escopo saiu de pedido e produção de um único produto para um sistema de controle da operação, com mais de 11 mil linhas de código e 11 migrações de banco, e a sincronização diária já roda agendada. Custo de receita, baixa automática de insumos e reposição automática seguem em estudo.

## O que eu fiz

Entendi a rotina da cozinha e das lojas (pedido, produção, pesagem do gelato e envase do delivery) e a transformei em regras e telas. Desenhei os perfis e as permissões dentro do banco, criei os importadores que trazem os relatórios do ERP e das planilhas e separei o que já funciona do que ainda está em estudo.

---
*Código-fonte privado: contém integrações e informações do ambiente corporativo. Veja a nota de privacidade no [README principal](../README.md).*
