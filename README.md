<div align="center">

<a href="https://github.com/InventraTech">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/InventraTech/.github/main/profile/assets/wordmark-dark.png" />
    <img src="https://raw.githubusercontent.com/InventraTech/.github/main/profile/assets/wordmark.png" alt="Inventra" width="220" />
  </picture>
</a>

# Engenharia e Qualidade de Software

Requisitos, casos de uso e documentação que orientam o desenvolvimento do **Inventra**,<br />
sistema de gestão de estoque para cozinhas institucionais e comerciais.

<a href="requisitos-sistema/Documento%20de%20Requisitos%20Funcionais%203.0%20-%20Inventra.pdf"><img src="https://img.shields.io/badge/Documento-Em_aprovação-FFDE3B?style=flat-square&labelColor=360082" alt="Documento em aprovação" /></a>
<a href="https://brasil.un.org/pt-br/sdgs/12"><img src="https://img.shields.io/badge/ODS_12-Consumo_e_Produção_Responsáveis-ECC506?style=flat-square&labelColor=360082" alt="ODS 12" /></a>
<a href="https://github.com/InventraTech/inventra-software-engineering-2/commits/main"><img src="https://img.shields.io/github/last-commit/InventraTech/inventra-software-engineering-2?style=flat-square&label=%C3%9Altimo%20commit&color=6A00FF&labelColor=360082" alt="Último commit" /></a>
<a href="LICENSE"><img src="https://img.shields.io/github/license/InventraTech/inventra-software-engineering-2?style=flat-square&label=Licen%C3%A7a&color=6A00FF&labelColor=360082" alt="Licença MIT" /></a>

<b>
<a href="#artefatos">Artefatos</a> ·
<a href="#o-sistema">O sistema</a> ·
<a href="#requisitos">Requisitos</a> ·
<a href="#casos-de-uso">Casos de uso</a> ·
<a href="#demandas-da-disciplina">Demandas</a> ·
<a href="#pendências">Pendências</a> ·
<a href="#como-contribuir">Como contribuir</a>
</b>

</div>

<br />

<table>
<tr>
<td align="center" width="25%"><b>26</b><br /><sub>requisitos funcionais</sub></td>
<td align="center" width="25%"><b>18</b><br /><sub>requisitos não funcionais</sub></td>
<td align="center" width="25%"><b>3</b><br /><sub>atores de negócio</sub></td>
<td align="center" width="25%"><b>7</b><br /><sub>casos de uso modelados</sub></td>
</tr>
</table>

> [!NOTE]
> **Situação atual:** o documento de requisitos está entregue e em aprovação. O diagrama de casos de uso e o acompanhamento no Jira estão parciais, e ainda faltam os diagramas de atividades e o documento de dinâmica da equipe. Os detalhes estão em [Demandas da disciplina](#demandas-da-disciplina).

## Artefatos

Este repositório guarda apenas documentação. O código do sistema está nos [repositórios de implementação](#onde-o-sistema-é-implementado).

| Artefato | Conteúdo |
|:---------|:---------|
| [Documento de Requisitos Funcionais](requisitos-sistema/Documento%20de%20Requisitos%20Funcionais%203.0%20-%20Inventra.pdf) | Identificação, escopo, atores, requisitos funcionais e não funcionais, e glossário |
| [Planilha de requisitos](requisitos-sistema/requisitos_estoque_cozinha.xlsx) | Os mesmos requisitos em duas abas (RF e RNF), com código, título e descrição, para filtrar e rastrear |
| [Diagrama de casos de uso](requisitos-sistema/use-case-model-inventra.png) | Atores e casos de uso já modelados |

## O sistema

O Inventra faz a gestão de estoque e o controle de movimentações (entradas e saídas) de insumos e ingredientes em cozinhas institucionais ou comerciais. Com ele, a equipe monitora os níveis de estoque e requisita novos produtos quando necessário. O projeto é interdisciplinar e está alinhado ao ODS 12 da ONU, com foco na redução do desperdício de alimentos.

### Atores

| Ator | Responsabilidade |
|:-----|:-----------------|
| **Supervisor** | Acompanha indicadores e métricas no dashboard, gera relatórios de consumo, desperdício e disponibilidade, gerencia alertas e autoriza requisições |
| **Estoquista** | Registra movimentações (entradas, saídas, transferências), faz ajustes manuais de inventário e executa contagens periódicas |
| **Comprador** | Gerencia fornecedores, analisa pedidos de compra automáticos e aprova aquisições baseadas em previsões de consumo |

### Glossário

| Termo | Definição |
|:------|:----------|
| **Estoque físico** | Quantidade real de produtos disponível fisicamente na cozinha |
| **Estoque registrado** | Quantidade de produtos registrada no sistema |
| **Ponto de pedido** | Nível mínimo de estoque que dispara a geração automática de pedido de compra |
| **Lote** | Conjunto de produtos com a mesma data de fabricação/validade |
| **Perda** | Produto que não pode ser utilizado por motivos diversos (vencimento, avaria etc.) |
| **Auditoria** | Processo de verificação e rastreamento das movimentações realizadas no sistema |

## Requisitos

As fontes oficiais são o [PDF](requisitos-sistema/Documento%20de%20Requisitos%20Funcionais%203.0%20-%20Inventra.pdf) e a [planilha](requisitos-sistema/requisitos_estoque_cozinha.xlsx). As listas abaixo são uma cópia para leitura no GitHub.

<details>
<summary><b>Requisitos funcionais</b> (RF01 a RF26)</summary>
<br />

| Código | Título | Descrição |
|:-------|:-------|:----------|
| RF01 | Cadastro de cozinhas | Permitir cadastrar cozinhas no sistema. |
| RF02 | Cadastro de usuários | Permitir cadastrar usuários com diferentes níveis de acesso. |
| RF03 | Cadastro de produtos | Permitir cadastrar itens de estoque com nome, categoria, validade e fornecedor. |
| RF04 | Cadastro de categorias | Permitir cadastrar categorias de produtos. |
| RF05 | Entrada de produtos | Permitir registrar entrada de produtos no estoque. |
| RF06 | Saída de produtos | Permitir registrar retirada e consumo de produtos. |
| RF07 | Ajuste manual de inventário | Permitir correções manuais de estoque. |
| RF08 | Comparação de estoque | Comparar estoque físico e registrado. |
| RF09 | Histórico de inventário | Armazenar histórico das contagens realizadas. |
| RF10 | Controle de validade | Controlar datas de validade dos produtos. |
| RF11 | Alertas de vencimento | Emitir alertas para produtos próximos do vencimento. |
| RF12 | Registro de perdas | Permitir registrar perdas e desperdícios. |
| RF13 | Relatórios de estoque | Gerar relatórios de disponibilidade e falta de produtos. |
| RF14 | Relatórios de consumo | Apresentar consumo por período. |
| RF15 | Relatórios de desperdício | Gerar relatórios de perdas e desperdícios. |
| RF16 | Dashboard gerencial | Apresentar indicadores e métricas do estoque. |
| RF17 | Autenticação | Permitir login com usuário e senha. |
| RF18 | Controle de permissões | Restringir funcionalidades conforme perfil do usuário. |
| RF19 | Registro de auditoria | Registrar ações realizadas pelos usuários. |
| RF20 | Requisição de compra | Gerar pedido de compra para fornecedores baseado em ponto de pedido (estoque mínimo) e consumo médio. |
| RF21 | Revisão de pedidos | Revisar produtos e suas quantidades antes de fazer a requisição. |
| RF22 | Notificações push/e-mail | Enviar alertas de vencimento, estoque baixo, auditoria pendente e movimentações suspeitas. |
| RF23 | Exportação em lote | Permitir exportar produtos, movimentações e inventários via CSV/Excel. |
| RF24 | Gestão de fornecedores | Cadastrar fornecedores com dados de contato, prazos de entrega, produtos fornecidos e histórico de performance. |
| RF25 | Motivo de movimentação | Obrigar ou permitir registrar motivo na saída (ex: consumo, perda, doação, devolução a fornecedor). |
| RF26 | Alerta de produto vencido | Alertar fortemente se produto estiver vencido ou perto da data de validade. |

</details>

<details>
<summary><b>Requisitos não funcionais</b> (RNF01 a RNF18)</summary>
<br />

| Código | Título | Descrição |
|:-------|:-------|:----------|
| RNF01 | Usuários simultâneos | O sistema deve suportar múltiplos usuários simultaneamente. |
| RNF02 | Criptografia | As senhas devem ser armazenadas de forma criptografada. |
| RNF03 | Autenticação e autorização | O sistema deve possuir controle de autenticação e autorização. |
| RNF04 | Logs | O sistema deve registrar logs de acesso e alterações. |
| RNF05 | Usabilidade | A interface deve ser intuitiva e fácil de utilizar. |
| RNF06 | Responsividade | O sistema deve funcionar em tablets e celulares. |
| RNF07 | Rapidez operacional | O sistema deve permitir operação rápida na rotina da cozinha. |
| RNF08 | Backup | O sistema deve possuir mecanismo de backup automático. |
| RNF09 | Escalabilidade | O sistema deve suportar múltiplas cozinhas/unidades. |
| RNF10 | Manutenibilidade | O sistema deve possuir arquitetura modular. |
| RNF11 | Padronização | O código deve seguir padrões de desenvolvimento e documentação. |
| RNF12 | Compatibilidade | O sistema deve funcionar nos principais dispositivos. |
| RNF13 | Rastreabilidade | Cada movimentação deve permitir rastrear qual usuário, data/hora, terminal/IP e motivo – com cadeia de auditoria imutável. |
| RNF14 | API REST documentada | Expor API para integração com sistemas de compras, ERP, PDV ou fiscal. |
| RNF15 | Versionamento de dados | Manter histórico completo de alterações em produtos e movimentações (quem mudou, de/para). |
| RNF16 | Testabilidade | Cobertura de testes automatizados mínima de 80%. |
| RNF17 | Acessibilidade | Pesquisar Acessibilidades para Mobile |
| RNF18 | Atualização automática do estoque | Atualizar automaticamente o estoque após movimentações. |

</details>

## Casos de uso

O diagrama está em construção. Os 7 casos de uso modelados cobrem 8 dos 26 requisitos funcionais.

<p align="center">
  <img src="requisitos-sistema/use-case-model-inventra.png" alt="Diagrama de casos de uso do Inventra: Estoquista, Supervisor e Comprador ligados aos sete casos de uso modelados" width="520" />
</p>

| Caso de uso | Atores | Requisitos atendidos |
|:------------|:-------|:---------------------|
| Registrar Entrada | Estoquista, Supervisor | RF05 |
| Registrar Saída | Estoquista, Supervisor | RF06, RF25 |
| Ajuste Manual | Estoquista, Supervisor | RF07 |
| Cadastrar Cozinha | Supervisor | RF01 |
| Cadastrar Usuário | Supervisor | RF02 |
| Cadastrar Produto | Supervisor | RF03 |
| Requisição Compra | Comprador | RF20 |

**Ainda sem caso de uso:** RF04, RF08 a RF19, RF21 a RF24 e RF26. O ator `Sistema` aparece no diagrama, mas não está ligado a nenhum caso de uso.

## Demandas da disciplina

Checklist de Engenharia de Software, conforme as solicitações por disciplina de maio de 2026.

### Mínimo para o 7,0

| Item | Demanda | Status | Situação | Onde |
|:-----|:--------|:-------|:---------|:-----|
| **M1** | Mecanismo de acompanhamento do projeto, com o professor incluído | 🟡 Parcial | O planejamento está no board **INV2** do Jira. Falta registrar o acompanhamento desta disciplina e confirmar o acesso do professor | [Board INV2](https://inventraoficial.atlassian.net/jira/software/projects/INV2/boards/81) |
| **M2** | Documento com os requisitos funcionais | ✅ Feito | Documento com escopo, atores, RF, RNF e glossário, acompanhado da planilha | [PDF](requisitos-sistema/Documento%20de%20Requisitos%20Funcionais%203.0%20-%20Inventra.pdf), [planilha](requisitos-sistema/requisitos_estoque_cozinha.xlsx) |
| **M3** | Diagrama com todos os casos de uso, relacionados aos RF | 🟡 Parcial | Cobre 8 dos 26 RF. A relação com os RF está na [tabela deste README](#casos-de-uso), ainda não no diagrama | [Diagrama](requisitos-sistema/use-case-model-inventra.png) |
| **M4** | Diagrama de atividades de 2 processos | ❌ Não feito | Nenhum diagrama de atividades neste repositório | |
| **M5** | Dinâmica de trabalho da equipe e responsáveis por back, front, banco de dados etc. | ❌ Não feito | A divisão por frentes aparece no [perfil da organização](https://github.com/InventraTech), mas sem responsáveis por papel | |

### Extras

| Item | Demanda | Status | Situação | Onde |
|:-----|:--------|:-------|:---------|:-----|
| **E1** | Padrão de projeto, indicando onde foi usado e com que finalidade | 🟡 Não documentado | O código usa interfaces `UseCase` com implementações na API e o padrão *Repository* no app, mas falta registrar onde e por quê | [API](https://github.com/InventraTech/inventra-api-2/tree/main/src/main/java/com/inventra/api/core/service), [app](https://github.com/InventraTech/inventra-mobile-development-2/tree/main/app/src/main/java/com/inventraoficial/inventra/data/repository) |
| **E2** | Padrão de testes (como TDD), indicando onde e como será usado | 🟡 Não documentado | Há testes automatizados na API e no app, mas a estratégia não está descrita e o uso de TDD não está registrado | [API](https://github.com/InventraTech/inventra-api-2/tree/main/src/test), [app](https://github.com/InventraTech/inventra-mobile-development-2/tree/main/app/src/test) |

## Pendências

**Entregas da disciplina**

- [ ] **M4:** elaborar os diagramas de atividades de 2 processos, como a saída de produto com baixa por lote e a requisição de compra com aprovação.
- [ ] **M5:** documentar a dinâmica de trabalho e o responsável por back, front, banco de dados e demais frentes.
- [ ] **M3:** incluir os casos de uso que faltam, ligar o ator `Sistema` e citar os códigos dos RF no próprio diagrama.
- [ ] **M1:** registrar aqui o acompanhamento da disciplina no Jira e confirmar o acesso do professor ao board.
- [ ] **E1 e E2:** documentar os padrões de projeto (com local e finalidade) e a estratégia de testes.

**Revisão do documento de requisitos**

- [ ] **Versão:** o arquivo se chama *3.0*, mas o cabeçalho do PDF indica **versão 2.0**, de 23/06/2026. Alinhar os dois e atualizar o status.
- [ ] **Transferências:** o papel do Estoquista as inclui e a [API](https://github.com/InventraTech/inventra-api-2) as implementa, mas nenhum RF as descreve.
- [ ] **Aprovação de requisições:** o Supervisor autoriza e o Comprador aprova, mas nenhum RF define esse fluxo. O RF21 cobre apenas a revisão do pedido.
- [ ] **Cadastros:** o diagrama os atribui ao Supervisor, mas a descrição do ator no documento não os menciona.
- [ ] **Redação dos requisitos:** o RNF17 descreve uma tarefa de pesquisa, e não um critério verificável. O RF11 e o RF26 se sobrepõem. O RNF18 descreve um comportamento funcional.
- [ ] **Planilha:** o RF19 tem um asterisco na coluna D, sem legenda.
- [ ] **Fontes editáveis:** versionar os arquivos que geram o PDF e o diagrama, hoje disponíveis só no formato final.
- [ ] **RNF16:** acompanhar a meta de 80% de cobertura de testes nos relatórios da API e do app.

## Onde o sistema é implementado

| Repositório | Frente | Conteúdo |
|:------------|:-------|:---------|
| [`inventra-api-2`](https://github.com/InventraTech/inventra-api-2) | Desenvolvimento | API REST em Java e Spring Boot |
| [`inventra-mobile-development-2`](https://github.com/InventraTech/inventra-mobile-development-2) | Desenvolvimento Mobile | Aplicativo Android em Kotlin e Jetpack Compose |
| [`inventra-dynamic-applications-2`](https://github.com/InventraTech/inventra-dynamic-applications-2) | Aplicações Dinâmicas | Front-end em React, TypeScript e Tailwind CSS |
| [`inventra-artificial-intelligence-2`](https://github.com/InventraTech/inventra-artificial-intelligence-2) | Inteligência Artificial | Assistente multiagente IAI, com FastAPI e LangGraph |
| [`inventra-database-2`](https://github.com/InventraTech/inventra-database-2) | Arte e Modelagem de Dados | Bancos PostgreSQL, MongoDB e Redis |
| [`inventra-database-rpa-2`](https://github.com/InventraTech/inventra-database-rpa-2) | Arte e Modelagem de Dados | Automações (RPA) |
| [`inventra-gitops`](https://github.com/InventraTech/inventra-gitops) | Operações Ágeis | Implantação em produção com Argo CD e Argo Rollouts |

## Como contribuir

1. Abra um Pull Request usando o [template da organização](https://github.com/InventraTech/.github/blob/main/PULL_REQUEST_TEMPLATE.md).
2. Ao alterar um requisito, atualize **o PDF e a planilha juntos**, além das listas deste README, e ajuste a versão e o status no cabeçalho do documento.
3. Ao incluir ou mudar um caso de uso, atualize o diagrama e a [tabela de rastreabilidade](#casos-de-uso).
4. Escreva as mensagens de commit em português, seguindo o *Conventional Commits* (por exemplo, `docs: adiciona planilha de requisitos`).

## Licença

Distribuído sob a [licença MIT](LICENSE).
