# Análise sobre Cenários de Teste e Considerações

Este documento resume as observações, erros e sugestões coletadas durante a fase de validação (QAS) do Módulo Avicultura do AgroCenter.

**Nota:** Não foi possível realizar a leitura e análise do arquivo `Resumo_Acompanhamento_Testes - EA-G-OP-SO-AC-CVL-009 - 2025-11-21.ods` por ser um formato de planilha. A análise a seguir é baseada exclusivamente no conteúdo dos arquivos `descricao.md` encontrados na pasta `docs/CONSIDERACOES_FEITAS_NOS_CENARIOS/`.

## Sumário das Considerações

As observações foram agrupadas nas seguintes categorias:

1.  [Bugs de Funcionalidade](#1-bugs-de-funcionalidade)
2.  [Sugestões de Melhoria (UX/UI)](#2-sugestões-de-melhoria-uxui)
3.  [Problemas de Dados](#3-problemas-de-dados)
4.  [Requisições de Novas Features e Validações](#4-requisições-de-novas-features-e-validações)
5.  [Questões sobre Regras de Negócio](#5-questões-sobre-regras-de-negócio)

---

### 1. Bugs de Funcionalidade

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

### 2. Sugestões de Melhoria (UX/UI)

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

### 3. Problemas de Dados

Inconsistências e erros encontrados nos dados apresentados.

-   **Dados Duplicados:**
    -   Foram encontrados aviários duplicados nos filtros das telas de **Predição de Peso** e **Predição de Ração**.
    -   Silos aparecem em duplicata ao filtrar por aviário no **Monitoramento de Silos**.
-   **Dados Inconsistentes:**
    -   Na **Predição de Ração**, as demandas de ração são todas idênticas, o que indica um provável erro no cálculo ou na extração dos dados.
-   **Outliers:**
    -   Na tela de **Ranking**, valores muito discrepantes (outliers) estão sendo classificados entre os melhores, sugerindo a necessidade de um tratamento (ETL) nos dados antes da exibição.

### 4. Requisições de Novas Features e Validações

Sugestões de novas funcionalidades ou regras de validação para aumentar a robustez do sistema.

-   **Validação de Dados (Constraints):**
    -   Aplicar regras de validação (constraints) no campo de pesagem para evitar a inserção de dados incorretos.
    -   Alertar sobre dados incorretos de sensores na tela de **Monitoramento de Silos** em vez de exibi-los.
-   **Novas Funcionalidades:**
    -   No **Dashboard do Consultor**, adicionar um filtro ou agrupamento por semana de vida das aves para facilitar o manejo.
    -   Registrar e exibir o nome do usuário que realizou o registro no eProdutor para fins de rastreabilidade.

### 5. Questões sobre Regras de Negócio

Dúvidas sobre o funcionamento e o fluxo de processos do sistema.

-   **Status de Ocorrências:**
    -   Foi levantado um questionamento geral sobre a lógica de status "Em andamento" para diversos tipos de ocorrências (Movimento de Ração, Checklist, Doenças), que parecem não ter um fluxo de mudança de status definido.
    -   Para **Orientações Técnicas**, sugere-se um fluxo de status mais claro (ex: Recebido, Ciente, Aplicado).
-   **Ordem de Rações:**
    -   Questiona-se se a ordem de utilização de ração no lote deve ser respeitada pelo sistema.
