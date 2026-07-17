# Relatório Final do Projeto QA Educabiz

## 1. Objetivo do Projeto

O objetivo deste projeto foi realizar testes manuais no aplicativo de creche **Educabiz**, simulando um fluxo real de trabalho de QA.

O projeto foi criado como parte de um portfólio para vaga de **QA Júnior**, com foco em demonstrar:

- planejamento de testes;
- definição de escopo;
- criação de casos de teste;
- execução manual;
- registro de bugs no Jira;
- documentação dos resultados no GitHub.

A proposta foi manter um escopo profissional, mas viável para uma pessoa executar sozinha em aproximadamente um mês.

## 2. Fonte dos Dados

As informações deste relatório foram extraídas da planilha:

`planilha-projeto-qa-educabiz.xlsx`

A planilha contém as abas:

- Resumo
- Mapeamento
- Checklist Geral
- Casos de Teste
- Relatório de Bugs
- Melhorias

## 3. Ferramentas Utilizadas

| Ferramenta | Uso no projeto |
|---|---|
| GitHub | Documentação e versionamento do projeto |
| Jira | Organização do Kanban e registro dos bugs |
| Excel | Documentação e execução dos casos de teste |
| Android | Ambiente de execução dos testes |
| Capturas de tela | Evidências dos testes e bugs encontrados |

## 4. Ambiente de Teste

| Item | Informação |
|---|---|
| Plataforma | Android |
| Dispositivo | OPPO A78 5G |
| Modelo | CPH2483 |
| Sistema operacional | ColorOS 15.0 |
| Aplicativo | Educabiz |
| Versão | 2.120.0 |

## 5. Escopo Testado

O escopo foi reduzido para os módulos mais importantes do aplicativo, priorizando os fluxos mais relevantes para pais e responsáveis.

| Módulo | Quantidade de casos |
|---|---:|
| Autenticação | 7 |
| Home / Feed | 9 |
| Perfil do Aluno | 4 |
| Mensagens | 8 |
| Documentos | 5 |
| Relatório Diário | 9 |
| Galeria | 9 |
| Agenda | 4 |

Total: **55 casos de teste**.

## 6. Módulos Fora do Escopo

Os seguintes módulos e funcionalidades ficaram fora do escopo para manter o projeto viável:

- Produtos e Serviços
- Pagamentos
- Relatórios de Progresso
- Dados Clínicos, exceto bug evidente
- Contactos
- Minha Conta
- Permissões por perfil em profundidade
- Multi-filho
- Auditoria
- Testes offline
- Acessibilidade
- Push notifications
- Upload de documentos
- Upload de fotos
- Exportação
- Múltiplos perfis

## 7. Resumo da Execução

| Indicador | Quantidade |
|---|---:|
| Casos de teste criados | 55 |
| Casos de teste executados | 55 |
| Casos aprovados | 47 |
| Casos reprovados | 6 |
| Casos classificados como sugestão/melhoria | 2 |
| Bugs encontrados | 6 |
| Melhorias registradas | 6 |

## 8. Resultado por Módulo

| Módulo | Total | Aprovados | Reprovados | Sugestão/Melhoria |
|---|---:|---:|---:|---:|
| Autenticação | 7 | 7 | 0 | 0 |
| Home / Feed | 9 | 6 | 3 | 0 |
| Perfil do Aluno | 4 | 4 | 0 | 0 |
| Mensagens | 8 | 8 | 0 | 0 |
| Documentos | 5 | 4 | 1 | 0 |
| Relatório Diário | 9 | 9 | 0 | 0 |
| Galeria | 9 | 6 | 1 | 2 |
| Agenda | 4 | 3 | 1 | 0 |

## 9. Bugs Encontrados

Durante a execução dos testes, foram registrados **6 bugs** no Jira.

| ID | Jira | Módulo | Título | Severidade | Status |
|---|---|---|---|---|---|
| EDUC-1 | [QE-23](https://dheborabeltrao.atlassian.net/browse/QE-23) | Home / Feed | Menu lateral não abre na tela de resposta de uma mensagem aberta pelo feed | Média | Aberto |
| EDUC-2 | [QE-22](https://dheborabeltrao.atlassian.net/browse/QE-22) | Home / Feed | Cabeçalho ocupa área excessiva da tela na orientação paisagem | Média | Aberto |
| EDUC-3 | [QE-21](https://dheborabeltrao.atlassian.net/browse/QE-21) | Documentos | Responsável consegue criar, editar, substituir e excluir documentos disponibilizados pela escola | Crítica | Aberto |
| EDUC-4 | [QE-24](https://dheborabeltrao.atlassian.net/browse/QE-24) | Galeria | Opção "Editar" de álbum direciona para tela vazia | Alta | Aberto |
| EDUC-5 | [QE-25](https://dheborabeltrao.atlassian.net/browse/QE-25) | Home / Feed | Zoom da fotografia aberta pelo Feed é limitado à área do card | Média | Aberto |
| EDUC-6 | [QE-26](https://dheborabeltrao.atlassian.net/browse/QE-26) | Agenda | Agenda abre posicionada em datas passadas | Média | Aberto |

Mais detalhes estão documentados em [Resumo dos Bugs Encontrados](./bugs-resumo.md).

## 10. Bugs por Severidade

| Severidade | Quantidade |
|---|---:|
| Crítica | 1 |
| Alta | 1 |
| Média | 4 |
| Baixa | 0 |

## 11. Bugs por Módulo

| Módulo | Quantidade de bugs |
|---|---:|
| Home / Feed | 3 |
| Documentos | 1 |
| Galeria | 1 |
| Agenda | 1 |
| Autenticação | 0 |
| Perfil do Aluno | 0 |
| Mensagens | 0 |
| Relatório Diário | 0 |

## 12. Módulos com Maior Risco

### Documentos

O módulo **Documentos** apresentou o bug de maior severidade do projeto.

O perfil de responsável conseguiu criar, editar, substituir e excluir documentos disponibilizados pela escola. Esse comportamento representa risco crítico, pois envolve controle de permissão e integridade de documentos institucionais.

### Home / Feed

O módulo **Home / Feed** concentrou a maior quantidade de bugs encontrados, com 3 registros.

Os problemas identificados envolveram navegação, adaptação de layout e visualização de imagem. Como a Home é uma das telas mais acessadas pelos responsáveis, esses problemas têm impacto direto na experiência de uso.

### Galeria

Na **Galeria**, a opção de editar álbum direcionou o usuário para uma tela vazia. Além disso, dois casos foram classificados como sugestão/melhoria, indicando oportunidades de aprimoramento na experiência do usuário.

### Agenda

Na **Agenda**, a tela abriu posicionada em datas passadas, exigindo esforço manual para encontrar eventos atuais. Esse comportamento impacta a usabilidade, principalmente para responsáveis que consultam a agenda com frequência.

## 13. Melhorias Registradas

A planilha contém **6 melhorias registradas** em aba própria.

Essas melhorias foram separadas dos bugs para diferenciar falhas funcionais de oportunidades de evolução da experiência do usuário.

Essa separação ajuda a demonstrar uma prática importante de QA: nem toda observação encontrada durante os testes é necessariamente um bug. Algumas descobertas podem ser tratadas como sugestão de melhoria, dependendo da regra de negócio e do impacto para o usuário.

## 14. Aprendizados do Projeto

Este projeto ajudou a reforçar aprendizados importantes de QA manual:

- A importância de definir um escopo realista antes de começar a testar.
- Como transformar capturas de tela em mapa de funcionalidades e casos de teste.
- Como priorizar fluxos principais em vez de tentar cobrir todo o aplicativo superficialmente.
- Como registrar bugs com passos reproduzíveis, resultado esperado, resultado obtido, severidade e evidência.
- Como usar o Jira para organizar o andamento do projeto em Kanban.
- Como documentar resultados no GitHub de forma clara para portfólio.
- Como diferenciar bug de sugestão de melhoria.
- Como identificar riscos além do comportamento visual, especialmente em permissões e dados sensíveis.

## 15. Conclusão Final

O projeto QA Educabiz atingiu o objetivo proposto: criar um estudo de testes manuais organizado, executável e adequado para portfólio de QA Júnior.

Foram criados e executados **55 casos de teste**, cobrindo os principais fluxos do aplicativo. Durante a execução, foram encontrados **6 bugs**, incluindo uma falha crítica relacionada a permissões no módulo Documentos.

O resultado demonstra não apenas a execução de testes, mas também a capacidade de planejar, priorizar, documentar evidências, analisar riscos e comunicar os resultados de forma clara.

Este projeto pode ser apresentado como exemplo prático de um ciclo completo de QA manual: planejamento, criação de casos, execução, registro de bugs, identificação de melhorias e documentação final.
