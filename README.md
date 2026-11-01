# Inventra — Engenharia e Qualidade de Software

Documentos da disciplina de **Engenharia e Qualidade de Software** do projeto interdisciplinar **Inventra**, um sistema de gestão de estoque para cozinhas industriais com cozinhas, produtos, lotes, requisições e fornecedores.

Aqui ficam os requisitos, os diagramas UML, a divisão de funções da equipe e os extras de padrões de projeto e de testes. O código está nos outros repositórios da [InventraTech](https://github.com/InventraTech).

## Sumário

- [Entregas](#entregas)
- [Estrutura](#estrutura)
- [Acompanhamento do projeto](#acompanhamento-do-projeto)
- [Repositórios do projeto](#repositórios-do-projeto)
- [Como contribuir](#como-contribuir)

## Entregas

| Requisito | Documento |
|:----------|:----------|
| M1. Acompanhamento do projeto com o professor incluído | Jira, projeto `INV2` (veja [Acompanhamento do projeto](#acompanhamento-do-projeto)) |
| M2. Documento de requisitos funcionais | [Documento de Requisitos Funcionais 3.0](requisitos-sistema/Documento%20de%20Requisitos%20Funcionais%203.0%20-%20Inventra.pdf) e [planilha de requisitos](requisitos-sistema/requisitos_estoque_cozinha.xlsx) |
| M3. Diagrama de casos de uso | [use-case-model-inventra.png](requisitos-sistema/use-case-model-inventra.png) |
| M4. Diagramas de atividades | [Diagramas de Atividades](diagramas-atividades/Diagramas%20de%20Atividades%20-%20Inventra.pdf) |
| M5. Dinâmica de trabalho e responsáveis | [Divisão de Funções Técnicas 2.1](divisao-funcoes/Divisao_de_Funcoes_Tecnicas_Inventra2.1.pdf) |
| E1. Padrão de projeto: onde e para quê | [Padrões de Projeto](padroes-projeto/Inventra%20-%20Padroes%20de%20Projeto.pdf) |
| E2. Padrão de testes (TDD): onde e como | [TDD](testes-tdd/Inventra%20-%20TDD.pdf) |

## Estrutura

```
requisitos-sistema/      requisitos funcionais, planilha e diagrama de casos de uso
diagramas-atividades/    diagramas de atividades dos processos
divisao-funcoes/         divisão de funções técnicas da equipe
padroes-projeto/         padrões de projeto usados no app mobile
testes-tdd/              padrão de testes com TDD no app mobile
```

**Padrões de projeto e TDD.** Os dois documentos mostram o código do [app mobile](https://github.com/InventraTech/inventra-mobile-development-2). O de padrões de projeto cobre o Repository, que é o padrão principal, e também Factory, Chain of Responsibility e Observer. O de TDD mostra 4 ciclos de teste, implementação e refatoração, cada etapa num commit da branch [`feat/estado-rotacao`](https://github.com/InventraTech/inventra-mobile-development-2/commits/feat/estado-rotacao).

## Acompanhamento do projeto

- **Jira:** projeto [`INV2`](https://inventraoficial.atlassian.net/jira/software/projects/INV2/boards). As entregas desta disciplina estão no épico [`INV2-10`](https://inventraoficial.atlassian.net/browse/INV2-10).
- **Miro:** os diagramas de casos de uso e de atividades foram feitos no [quadro do projeto](https://miro.com/app/board/uXjVHM8iiGc=/). O acesso é restrito à equipe; as versões finais estão nos PDFs e PNGs deste repositório.

## Repositórios do projeto

| Repositório | Conteúdo |
|:------------|:---------|
| [inventra-api-2](https://github.com/InventraTech/inventra-api-2) | API REST em Java com Spring |
| [inventra-mobile-development-2](https://github.com/InventraTech/inventra-mobile-development-2) | App Android em Kotlin com Jetpack Compose |
| [inventra-dynamic-applications-2](https://github.com/InventraTech/inventra-dynamic-applications-2) | Front-end web em React, TypeScript e Tailwind CSS |
| [inventra-artificial-intelligence-2](https://github.com/InventraTech/inventra-artificial-intelligence-2) | Back-end de IA em FastAPI, LangGraph e LangChain |
| [inventra-database-2](https://github.com/InventraTech/inventra-database-2) | Bancos de dados do projeto |
| [inventra-database-rpa-2](https://github.com/InventraTech/inventra-database-rpa-2) | RPAs do time |

## Como contribuir

- Trabalhe numa branch a partir da `main` e abra uma **Pull Request**, usando o [template da organização](https://github.com/InventraTech/.github/blob/main/PULL_REQUEST_TEMPLATE.md).
- Cada documento fica numa pasta própria. Uma versão nova substitui a anterior no mesmo commit, e o número da versão vai no nome do arquivo.
- As mensagens de commit seguem o *Conventional Commits*, por exemplo `docs(atividades): adiciona os diagramas de atividades`.
