# Resumo dos Bugs Encontrados

## Objetivo

Este documento reúne os bugs encontrados durante a execução dos testes manuais do projeto QA Educabiz.

O objetivo é facilitar a leitura dos principais problemas identificados, agrupando os bugs por severidade e por módulo, além de manter referência para os registros criados no Jira.

## Status

Atualizado com os bugs registrados em 16/07/2026.

## Ambiente de Teste

| Item | Informação |
|---|---|
| Plataforma | Android |
| Dispositivo | OPPO A78 5G |
| Modelo | CPH2483 |
| Sistema operacional | ColorOS 15.0 |
| Aplicativo | Educabiz |
| Versão | 2.120.0 |

## Visão Geral

| Indicador | Quantidade |
|---|---:|
| Total de bugs encontrados | 6 |
| Bugs críticos | 1 |
| Bugs de severidade alta | 1 |
| Bugs de severidade média | 4 |
| Bugs de severidade baixa | 0 |
| Bugs abertos | 6 |
| Bugs resolvidos/fechados | 0 |

## Bugs por Severidade

| Severidade | Quantidade | Observação |
|---|---:|---|
| Crítica | 1 | Falha de permissão que permite ao responsável alterar documentos institucionais |
| Alta | 1 | Ação disponível direciona o usuário para uma tela vazia |
| Média | 4 | Problemas de navegação, layout, usabilidade e posicionamento de conteúdo |
| Baixa | 0 | Nenhum bug de baixa severidade registrado |

## Bugs por Módulo

| Módulo | Quantidade de bugs | Observação |
|---|---:|---|
| Autenticação | 0 | Nenhum bug registrado |
| Home / Feed | 3 | Problemas de navegação, layout em paisagem e visualização de imagem |
| Perfil do Aluno | 0 | Nenhum bug registrado |
| Mensagens | 0 | Nenhum bug registrado diretamente no módulo |
| Documentos | 1 | Falha crítica de permissão |
| Relatório Diário | 0 | Nenhum bug registrado |
| Galeria | 1 | Ação de edição abre tela vazia |
| Agenda | 1 | Agenda abre posicionada em datas passadas |

## Lista de Bugs

| ID | Jira | Módulo | Título | Severidade | Status | Caso de teste relacionado |
|---|---|---|---|---|---|---|
| EDUC-1 | [QE-23](https://dheborabeltrao.atlassian.net/browse/QE-23) | Home / Feed | Menu lateral não abre na tela de resposta de uma mensagem aberta pelo feed | Média | Aberto | CT-HOM-007 |
| EDUC-2 | [QE-22](https://dheborabeltrao.atlassian.net/browse/QE-22) | Home / Feed | Cabeçalho ocupa área excessiva da tela na orientação paisagem | Média | Aberto | CT-HOM-008 |
| EDUC-3 | [QE-21](https://dheborabeltrao.atlassian.net/browse/QE-21) | Documentos | Responsável consegue criar, editar, substituir e excluir documentos disponibilizados pela escola | Crítica | Aberto | CT-DOC-005 |
| EDUC-4 | [QE-24](https://dheborabeltrao.atlassian.net/browse/QE-24) | Galeria | Opção "Editar" de álbum direciona para tela vazia | Alta | Aberto | CT-GAL-007 |
| EDUC-5 | [QE-25](https://dheborabeltrao.atlassian.net/browse/QE-25) | Home / Feed | Zoom da fotografia aberta pelo Feed é limitado à área do card | Média | Aberto | CT-HOM-009 |
| EDUC-6 | [QE-26](https://dheborabeltrao.atlassian.net/browse/QE-26) | Agenda | Agenda abre posicionada em datas passadas | Média | Aberto | CT-AGE-003 |

## Principais Problemas Encontrados

### 1. Falha crítica de permissão em Documentos

O bug mais grave identificado foi no módulo **Documentos**. O perfil de responsável consegue criar, editar, substituir e excluir documentos disponibilizados pela escola.

Esse comportamento representa risco alto porque documentos institucionais deveriam estar disponíveis apenas para consulta e download pelo responsável. A alteração indevida desses arquivos pode comprometer a integridade das informações oficiais.

Bug relacionado: [QE-21](https://dheborabeltrao.atlassian.net/browse/QE-21)

### 2. Problemas recorrentes no Home / Feed

O módulo **Home / Feed** concentrou 3 dos 6 bugs encontrados. Os problemas envolveram:

- menu lateral que não abre em uma tela acessada pelo feed;
- cabeçalho ocupando espaço excessivo na orientação paisagem;
- zoom de imagem limitado à área do card.

Esses bugs afetam principalmente navegação e usabilidade, especialmente porque o Feed é uma das áreas mais acessadas pelos responsáveis.

Bugs relacionados: [QE-23](https://dheborabeltrao.atlassian.net/browse/QE-23), [QE-22](https://dheborabeltrao.atlassian.net/browse/QE-22), [QE-25](https://dheborabeltrao.atlassian.net/browse/QE-25)

### 3. Tela vazia ao editar álbum

No módulo **Galeria**, a opção de editar álbum fica disponível, mas direciona o usuário para uma tela vazia.

Mesmo que o responsável não tenha permissão para editar álbuns, o sistema deveria ocultar a ação ou exibir uma mensagem clara. Uma tela vazia prejudica a experiência e pode gerar impressão de travamento.

Bug relacionado: [QE-24](https://dheborabeltrao.atlassian.net/browse/QE-24)

### 4. Agenda posicionada em datas passadas

No módulo **Agenda**, a tela abre posicionada em eventos antigos, mesmo exibindo a data atual no cabeçalho.

Esse comportamento aumenta o esforço do usuário, que precisa rolar manualmente até encontrar eventos atuais ou futuros.

Bug relacionado: [QE-26](https://dheborabeltrao.atlassian.net/browse/QE-26)

## Análise Geral

A maior parte dos bugs encontrados está relacionada a **usabilidade, navegação e controle de permissões**.

O ponto mais crítico do projeto foi a falha no módulo **Documentos**, pois envolve permissão indevida para alterar informações institucionais. Já o módulo **Home / Feed** apresentou maior concentração de bugs, indicando que fluxos acessados a partir da tela inicial merecem atenção especial em regressões futuras.

## Links Úteis

| Artefato | Link |
|---|---|
| Board no Jira | [QA Project - Educabiz](https://dheborabeltrao.atlassian.net/jira/software/projects/QE/boards/2) |
| Bug crítico identificado | [QE-21](https://dheborabeltrao.atlassian.net/browse/QE-21) |
| Planilha de casos de teste | `outputs/planilha-projeto-qa-educabiz.xlsx` |
| Evidências dos bugs | Pasta de evidências no repositório |

## Conclusão

Durante a execução dos testes, foram registrados **6 bugs**, sendo **1 crítico**, **1 alto** e **4 médios**, e **6 casos de melhoria**.

Os resultados mostram que o aplicativo possui fluxos principais funcionais, mas apresenta pontos importantes de melhoria em permissões, navegação e experiência do usuário. Para um ciclo futuro de testes, a recomendação seria priorizar regressão no módulo **Documentos** e nos fluxos derivados do **Home / Feed**.
