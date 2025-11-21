# Roteiro para Criação de Testes Unitários - Módulo Avicultura AgroCenter

Este roteiro foi elaborado com base no documento de ativação funcional **EA-G-OP-SO-AC-CVL-009** e tem como objetivo guiar a criação de testes unitários para as funcionalidades do módulo de Avicultura da plataforma AgroCenter.

## Estrutura dos Testes

Para cada funcionalidade, os testes devem ser divididos da seguinte forma:

- **Testes de Componente:** Validam a renderização e o comportamento de componentes individuais da interface (botões, tabelas, filtros, etc.).
- **Testes de Integração:** Validam a interação entre diferentes componentes e a comunicação com a API.
- **Testes de Regra de Negócio:** Validam a lógica de negócio e os resultados esperados para cada ação do usuário.

## Cenários de Teste por Funcionalidade

### 1. Home

- **Componentes:**
  - Testar a renderização da tabela de alertas.
  - Testar a renderização do mapa de alertas.
  - Testar a renderização dos filtros (produtor, propriedade, etc.).
- **Integração:**
  - Testar se a aplicação dos filtros atualiza a tabela e o mapa.
  - Testar se o clique em um alerta abre o modal de detalhes.
  - Testar se a orientação técnica é enviada corretamente para a API.
- **Regra de Negócio:**
  - Testar se os alertas são categorizados corretamente (crítico, moderado, etc.).
  - Testar se o cabeçalho reflete o número correto de alertas.
  - Testar se a orientação técnica só pode ser criada para lotes em andamento ou em espera.

### 2. Ocorrências

- **Componentes:**
  - Testar a renderização da lista de ocorrências.
  - Testar a renderização do mapa de ocorrências.
  - Testar a funcionalidade de download (botão Exportar).
- **Integração:**
  - Testar se a aplicação de filtros atualiza a lista e o mapa.
  - Testar se o clique em uma ocorrência abre o pop-up de detalhes.
  - Testar se a orientação técnica é enviada para a API e registrada no eProdutor.
- **Regra de Negócio:**
  - Testar se os detalhes da ocorrência correspondem aos dados do eProdutor.
  - Testar se a data da última atualização está correta.
  - Testar se o arquivo exportado contém os dados corretos.

### 3. Monitoramento - Sensores

- **Componentes:**
  - Testar a renderização da lista de sensores.
  - Testar a funcionalidade de busca e filtros.
- **Integração:**
  - Testar se a busca por um sensor retorna o resultado esperado.
  - Testar se o clique na lupa abre o pop-up com as últimas medidas.
- **Regra de Negócio:**
  - Testar se os dados dos sensores são consistentes com os dados do eProdutor.
  - Testar se as informações no pop-up de medidas estão corretas e condizentes.

### 4. Monitoramento - Tempo Real

- **Componentes:**
  - Testar a renderização dos cards de lote.
  - Testar a renderização dos ícones de status (online, offline, alerta).
- **Integração:**
  - Testar se os filtros atualizam os cards exibidos.
  - Testar se a busca por produtor funciona corretamente.
- **Regra de Negócio:**
  - Testar se os números no cabeçalho correspondem aos dados em tela.
  - Testar se o ícone de wi-fi desconectado aparece após 5 horas sem comunicação.
  - Testar se a cor da linha da variável muda de acordo com o nível de alerta (amarelo para moderado, vermelho para crítico).

### Demais Funcionalidades

O mesmo padrão de testes (Componentes, Integração, Regra de Negócio) deve ser aplicado para as demais funcionalidades listadas no documento, como:

- Monitoramento - Silos
- Monitoramento - Copiloto
- Monitoramento - Doenças
- Monitoramento - Controle de acesso
- Ranking
- Análise - Comparativo
- Análise - Predição de Peso
- Análise - Predição de Ração
- Solicitações
- Relatório - Acompanhamento Diário
- Configurações (Detalhada, Atribuição, Setores, Período de Contágio)
- Perfis (Produtores e Consultores)
- Administração de usuários (Cadastro, Convite, Permissões)
