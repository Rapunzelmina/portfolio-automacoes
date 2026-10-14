# Projetos, automação e melhoria de processos

**Analista de projetos e automação.** Mapeio o processo, encontro o gargalo, construo a solução (robô, aplicativo ou IA) e acompanho até ela rodar em produção.

*Melhoria de processos · Automação (RPA) · IA aplicada · Robôs · Gestão de projetos*

[English version](README.en.md)

Em uma rede de lojas do setor de alimentação, passei por várias áreas da empresa e, em cada uma, descobri onde havia trabalho manual e criei a solução. São 9 projetos, e o fio condutor é o mesmo: **entender o processo real, transformar as regras em código e deixar sempre uma pessoa com a decisão final.**

## Resultados em destaque

- **De até uma semana de trabalho para cerca de 5 minutos** no fechamento semanal de vendas e metas.
- **9 projetos em 6 áreas da empresa:** financeiro, contabilidade, comercial e metas, compras e estoque, operação e controle e delivery.
- **6 rotinas agendadas** no Windows rodando sem ninguém apertar um botão.
- **Um sistema de produção e estoque com mais de 11 mil linhas de código**, construído em poucas semanas e já em operação.
- **IA aplicada com responsabilidade:** sempre depois das regras e sempre com revisão humana antes de gravar.
- **Segurança por perfil dentro do banco de dados** (row level security) em três sistemas.

## Projetos

| Área | Projeto | Tipo | Status |
|---|---|---|---|
| Comercial e metas | [Fechamento semanal de vendas e metas](casos/01-fechamento-de-vendas-e-metas.md) | Robô (RPA) | Em produção |
| Contabilidade e fiscal | [Relatórios fiscais mensais para a contabilidade](casos/02-relatorios-fiscais-mensais.md) | Robô (RPA) | Em produção |
| Financeiro | [Contas a pagar: da extração à aprovação e ao borderô](casos/03-contas-a-pagar-aprovacao-e-bordero.md) | Robô + banco de dados | Em produção |
| Compras e estoque | [Entrada de NF-e de mercadoria com apoio de IA](casos/04-entrada-de-nfe-com-ia.md) | Robô + IA | Em uso |
| Financeiro | [Lançamento assistido de notas de serviço (NFS-e)](casos/05-lancamento-assistido-de-nfse.md) | Robô + IA | Em uso |
| Financeiro e operação das lojas | [App de recebimento e financeiro (PWA)](casos/06-app-de-recebimento-e-financeiro.md) | Aplicativo | Em produção |
| Operação e controle | [Apuração de descarte e bônus de equipe](casos/07-apuracao-de-descarte-e-bonus.md) | Dados e relatórios | Em produção |
| Comercial e delivery | [Margem de delivery por aplicativo](casos/08-margem-de-delivery-por-app.md) | Dados e relatórios | Em evolução |
| Operação e controle | [Sistema de controle de produção e estoque de gelato](casos/09-sistema-de-producao-e-estoque-de-gelato.md) | Aplicativo + robôs | Em operação e em expansão |

## Casos em repositório próprio

Os projetos mais completos também têm um repositório só deles, com diagrama:

- [Entrada de NF-e com IA](https://github.com/Rapunzelmina/AI-Assisted-Invoice-Entry): regras primeiro, IA por último, uma pessoa sempre decide
- [App de recebimento e financeiro](https://github.com/Rapunzelmina/Receiving-Finance-PWA): aprovação, tesouraria (conciliação OFX) e painel de metas
- [Contas a pagar, aprovação e borderô](https://github.com/Rapunzelmina/Accounts-Payable-Approval-Workflow): do ERP ao fluxo de aprovação, com segurança por perfil no banco
- [Sistema de controle de produção e estoque](https://github.com/Rapunzelmina/Production-Stock-Control-System): pedido, produção, laboratório com pesagem conferida, delivery e exportação para Excel
- [Fechamento de vendas e metas](https://github.com/Rapunzelmina/Sales-Closing-Automation): de até uma semana para cerca de 5 minutos

## Melhoria de processos: antes e depois

| Processo | Antes | Depois |
|---|---|---|
| Fechamento de vendas e metas | Manual, podia levar uma semana | Automático, cerca de 5 minutos |
| Relatórios fiscais | Gerados loja a loja, à mão | Gerados e organizados sozinhos no 1º dia útil |
| Aprovação de pagamentos | Uma lista dentro do ERP | Fila de aprovação com histórico e borderô |
| Entrada de notas de mercadoria | Digitação e conversão de unidade à mão | Assistida, com IA só como último recurso e revisão humana |
| Notas de serviço | Leitura e digitação | OCR com formulário pré-preenchido e revisão humana |
| Conciliação bancária | Extrato e pagamentos em planilhas separadas | Importação do extrato e conciliação automática |
| Descarte e bônus | Dezenas de planilhas e PDFs a cada mês | Pipeline reproduzível, com diagnóstico do que falta |
| Produção e estoque | Planilhas separadas, sem saber quem pesou o quê | Sistema com rastreabilidade e conferência por uma segunda pessoa |
| Margem de delivery | Só receita e quantidade | Receita, custo e margem por canal (em evolução) |

## Como conduzo um projeto

1. **Descubro o processo e o gargalo** conversando com quem opera a área.
2. **Inspeciono o sistema.** Quando não há API, analiso as telas (botões, formulários, URLs e o caminho de cada relatório) até entender como automatizar.
3. **Pesquiso e escolho a tecnologia** e o caminho de execução.
4. **Conduzo a IA com instruções precisas.** Eu defino o problema e as regras; o Claude (Anthropic) é meu parceiro de programação e eu reviso o que ele escreve.
5. **Testo com dados reais**, trato as falhas e só então deixo rodar sozinho.
6. **Acompanho depois de entregar:** leio os logs, corrijo o que falha e ajusto o que mudou no processo.
7. **Mantenho uma pessoa com a decisão final** onde há risco.

## Próximos passos (roadmap)

Em estudo ou em andamento, ainda sem código pronto:

- Rotina de baixa de pagamentos, fluxo de caixa e DRE, integrados à tesouraria.
- Sistema de produção e estoque: custo da receita, baixa automática de insumos e reposição automática.
- Margem de delivery: incluir cupom e desconto, automatizar a extração e unificar tudo numa rotina única.

## Habilidades

- **Projetos e processos:** levantamento de requisitos, mapeamento de processos, melhoria contínua, priorização, validação com as áreas, acompanhamento pós-entrega
- **Automação e robôs (RPA):** Python, Playwright, integração com sistemas sem API, rotinas agendadas, logs, tratamento de falhas e notificações
- **IA aplicada:** OCR, conversão de unidades e apoio à decisão com o Claude, com revisão humana
- **Dados e relatórios:** pandas, Excel avançado (fórmulas, painéis, gráficos), PDF
- **Banco de dados e segurança:** PostgreSQL, SQL, triggers, row level security
- **Aplicativos web:** PWA instalável em JavaScript puro, com autenticação, perfis e funcionamento offline

## Privacidade e segurança

Os repositórios e documentos deste portfólio não contêm:

- código-fonte das implementações originais;
- credenciais, senhas, chaves ou tokens;
- dados de clientes, funcionários ou pessoais;
- CNPJs, nomes de lojas ou fornecedores;
- URLs e caminhos internos;
- arquivos, planilhas ou números da empresa.

O código original permanece privado por conter integrações e informações do ambiente corporativo. Os projetos são apresentados como *cases* técnicos de portfólio.
