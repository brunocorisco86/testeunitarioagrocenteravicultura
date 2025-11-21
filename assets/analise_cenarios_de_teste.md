# Análise dos Testes de Validação (QAS) - Módulo Avicultura

Este documento consolida a análise quantitativa e qualitativa dos resultados da fase de validação (QAS) do Módulo Avicultura do AgroCenter.

## 1. Resumo Quantitativo dos Testes

A tabela abaixo apresenta um resumo do resultado dos 37 cenários de teste executados.

| Cenario                                             | Sucesso | Problema | Total | %Sucesso | Status   |
| --------------------------------------------------- | ------- | -------- | ----- | -------- | -------- |
| 1:Home                                              | 8       | 0        | 8     | 100,00%  | OK       |
| 2:Ocorrencias                                       | 9       | 0        | 9     | 100,00%  | OK       |
| 3:Monitoramento-Sensores                            | 6       | 0        | 6     | 100,00%  | OK       |
| 4:Monitoramento – Tempo Real                        | 11      | 0        | 11    | 100,00%  | OK       |
| 5:Monitoramento – Silos                             | 6       | 0        | 6     | 100,00%  | OK       |
| 6:Monitoramento – Copiloto                          | 3       | 2        | 5     | 60,00%   | Problema |
| 7:Monitoramento – Doenças                           | 5       | 0        | 5     | 100,00%  | OK       |
| 8:Monitoramento – Controle de Acesso                | 4       | 0        | 4     | 100,00%  | OK       |
| 9:Ranking                                           | 4       | 1        | 5     | 80,00%   | Problema |
| 10:Analise – Comparativo                            | 4       | 1        | 5     | 80,00%   | Problema |
| 11:Analise – Predicao de Peso                       | 5       | 1        | 6     | 83,33%   | Problema |
| 12:Analise – Predicao de Peso                       | 7       | 3        | 10    | 70,00%   | Problema |
| 13:Solicitacoes                                     | 5       | 1        | 6     | 83,33%   | Problema |
| 14:Relatorio – Acompanhamento Diário                | 7       | 0        | 7     | 100,00%  | OK       |
| 15:Configuracoes – Detalhada                        | 6       | 0        | 6     | 100,00%  | OK       |
| 16:Configuracoes – Atribuicao                       | 5       | 0        | 5     | 100,00%  | OK       |
| 17:Configuracoes – Tags                             | 7       | 0        | 7     | 100,00%  | OK       |
| 18:Configuracoes – Setores                          | 7       | 0        | 7     | 100,00%  | OK       |
| 19:Configuracoes – Periodo de Contagio              | 5       | 0        | 5     | 100,00%  | OK       |
| 20:Perfil – Produtores                              | 6       | 0        | 6     | 100,00%  | OK       |
| 21:Perfil – Consultores                             | 5       | 0        | 5     | 100,00%  | OK       |
| 22:Perfil do Consultor – Dashboard                  | 5       | 0        | 5     | 100,00%  | OK       |
| 23:Perfil do Consultor – Agenda                     | 7       | 0        | 7     | 100,00%  | OK       |
| 24:Perfil do Consultor – Relatorio                  | 6       | 0        | 6     | 100,00%  | OK       |
| 25:Perfil do Consultor – Copiloto                   | 1       | 5        | 6     | 16,67%   | Problema |
| 26:Perfil do Produtor – Linha do Tempo              | 6       | 0        | 6     | 100,00%  | OK       |
| 27:Perfil do Produtor – Analise                     | 4       | 3        | 7     | 57,14%   | Problema |
| 28:Perfil do Produtor – Resumo Diario               | 3       | 3        | 6     | 50,00%   | Problema |
| 29:Perfil do Produtor – Copiloto – Monitoramento    | 5       | 0        | 5     | 100,00%  | OK       |
| 30:Perfil do Produtor – Copiloto – Recomendacoes    | 5       | 0        | 5     | 100,00%  | OK       |
| 31:Perfil do Produtor – Doenças                     | 5       | 0        | 5     | 100,00%  | OK       |
| 32:FAQ                                              | 6       | 0        | 6     | 100,00%  | OK       |
| 33:Conexoes/Avicultura                              | 1       | 5        | 6     | 16,67%   | Problema |
| 34:Cadastro de Novos Usuarios na Plataforma         | 6       | 0        | 6     | 100,00%  | OK       |
| 35:Convite a Novos Membros de Equipe da Organizacao | 7       | 0        | 7     | 100,00%  | OK       |
| 36:Convite a Novos Produtores da Organizacao        | 5       | 2        | 7     | 71,43%   | Problema |
| 37:Atribuicao de Permissoes e Perfis de Usuarios    | 8       | 0        | 8     | 100,00%  | OK       |

### Análise Geral dos Resultados

| Análise das Etapas | Contagem | Percentual |
| :--- | :--- | :--- |
| **Total de Etapas** | **37** | **100,00%** |
| Etapas com Sucesso | 26 | 70,27% |
| Etapas com Falhas | 11 | 29,73% |

| Análise dos Passos | Contagem | Percentual |
| :--- | :--- | :--- |
| **Total de Passos** | **232** | **100,00%** |
| Passos com Sucesso | 205 | 88,36% |
| Passos com Falhas | 27 | 11,64% |

Dos **37 cenários** de teste, **11 (29,73%) apresentaram problemas**. Os cenários com menor taxa de sucesso e que requerem maior atenção são:
- **Perfil do Consultor – Copiloto (16,67%)**
- **Conexoes/Avicultura (16,67%)**
- **Perfil do Produtor – Resumo Diario (50,00%)**
- **Perfil do Produtor – Analise (57,14%)**

---

## 2. Análise Qualitativa das Considerações

A seguir, um resumo detalhado das observações, erros e sugestões coletadas, com base nos arquivos de descrição encontrados em `docs/CONSIDERACOES_FEITAS_NOS_CENARIOS/`.

As observações foram agrupadas nas seguintes categorias:

1.  [Bugs de Funcionalidade](#21-bugs-de-funcionalidade)
2.  [Sugestões de Melhoria (UX/UI)](#22-sugestões-de-melhoria-uxui)
3.  [Problemas de Dados](#23-problemas-de-dados)
4.  [Requisições de Novas Features e Validações](#24-requisições-de-novas-features-e-validações)
5.  [Questões sobre Regras de Negócio](#25-questões-sobre-regras-de-negócio)

### 2.1. Bugs de Funcionalidade

Erros que impedem o funcionamento esperado de uma tela ou funcionalidade.

-   **Análise Comparativa:**
    -   A tela não responde ao tentar editar o intervalo de datas para filtro.
    -   Não é possível gerar a plotagem da análise.
-   **Predição de Peso:**
    -   A extração de dados em CSV não inclui todos os aviários que aparentam estar selecionados.
-   **Solicitações:**
    -   O filtro de data não funciona corretamente (um pedido criado no dia não aparece ao filtrar pelo dia).
-   **Perfil do Consultor:**
    -   Não foi possível concluir uma operação por não conseguir selecionar um aviário.
-   **Resumo Diário do Produtor:**
    -   Os dados de IoT não foram carregados para o aviário testado (erro de integração/carregamento).
-   **Linha do Tempo do Produtor:**
    -   A descrição da doença que acometeu as aves não está visível na legenda do gráfico.
-   **Convite de Novos Produtores:**
    -   O texto do convite parece incorreto, direcionando a um consultor em vez de um produtor e levando a uma tela de cadastro extenso.
-   **Monitoramento de Silos:**
    -   Dados incorretos (erros) estão sendo exibidos na tela de operação, o que pode causar problemas operacionais.
-   **Monitoramento Copiloto:**
    -   O sistema não encontrou uma regra válida para sugerir, impedindo o teste do fluxo de aceitação no eProdutor.

### 2.2. Sugestões de Melhoria (UX/UI)

Recomendações para tornar a interface mais intuitiva e amigável.

-   **Ordenação Alfabética:**
    -   Ordenar a lista de "grandezas" por ordem alfabética nas telas de **Análise Comparativa**, **Análise do Produtor** e **Copiloto Monitoramento**.
-   **Exportação de Análises:**
    -   Adicionar a funcionalidade de exportar a análise/gráfico na tela de **Análise Comparativa**.
-   **Visualização de Dados:**
    -   Na **Predição de Peso**, exibir o peso atual do lote diretamente na tela principal, sem a necessidade de clicar em cada lote.
    -   No **Ranking**, truncar valores para exibir números inteiros quando aplicável (ex: "36 UN" em vez de "36.00 UN").
    -   Na tela de **Doenças**, utilizar um gráfico de barras empilhadas para mostrar a contagem de cada tipo de doença, facilitando a análise.
-   **Filtros e Classificação:**
    -   No **Monitoramento em Tempo Real**, permitir a classificação ou filtro por "grandeza" na tabela principal.
-   **FAQ:**
    -   Adicionar links para vídeos e documentação detalhada sobre o uso de cada tela, similar à "Academia eProdutor".

### 2.3. Problemas de Dados

Inconsistências e erros encontrados nos dados apresentados.

-   **Dados Duplicados:**
    -   Foram encontrados aviários duplicados nos filtros das telas de **Predição de Peso** e **Predição de Ração**.
    -   Silos aparecem em duplicata ao filtrar por aviário no **Monitoramento de Silos**.
-   **Dados Inconsistentes:**
    -   Na **Predição de Ração**, as demandas de ração são todas idênticas, o que indica um provável erro no cálculo ou na extração dos dados.
-   **Outliers:**
    -   Na tela de **Ranking**, valores muito discrepantes (outliers) estão sendo classificados entre os melhores, sugerindo a necessidade de um tratamento (ETL) nos dados antes da exibição.

### 2.4. Requisições de Novas Features e Validações

Sugestões de novas funcionalidades ou regras de validação para aumentar a robustez do sistema.

-   **Validação de Dados (Constraints):**
    -   Aplicar regras de validação (constraints) no campo de pesagem para evitar a inserção de dados incorretos.
    -   Alertar sobre dados incorretos de sensores na tela de **Monitoramento de Silos** em vez de exibi-los.
-   **Novas Funcionalidades:**
    -   No **Dashboard do Consultor**, adicionar um filtro ou agrupamento por semana de vida das aves para facilitar o manejo.
    -   Registrar e exibir o nome do usuário que realizou o registro no eProdutor para fins de rastreabilidade.

### 2.5. Questões sobre Regras de Negócio

Dúvidas sobre o funcionamento e o fluxo de processos do sistema.

-   **Status de Ocorrências:**
    -   Foi levantado um questionamento geral sobre a lógica de status "Em andamento" para diversos tipos de ocorrências (Movimento de Ração, Checklist, Doenças), que parecem não ter um fluxo de mudança de status definido.
    -   Para **Orientações Técnicas**, sugere-se um fluxo de status mais claro (ex: Recebido, Ciente, Aplicado).
-   **Ordem de Rações:**
    -   Questiona-se se a ordem de utilização de ração no lote deve ser respeitada pelo sistema.