# Features por Tela - Módulo Avicultura AgroCenter

Este documento detalha as funcionalidades (features) de cada tela do módulo de Avicultura da plataforma AgroCenter, extraídas do documento de ativação funcional EA-G-OP-SO-AC-CVL-009.

---

## 1. Home

**Objetivo:** Acompanhar visão geral dos alertas atuais dos lotes e realizar orientações técnicas aos produtores de forma online.

### Features:
- **Tabela de Alertas**
  - Exibição de alertas categorizados (crítico, moderado, etc.)
  - Cabeçalho com contadores de alertas por categoria
  - Filtros para lotes em andamento
  - Visualização de condições reais dos lotes
  
- **Detalhamento de Alertas**
  - Modal com informações detalhadas do alerta ao clicar
  - Exibição de informações complementares (temperatura, data, hora, estrutura, lote, fonte)
  
- **Orientação Técnica Online**
  - Funcionalidade para criar orientações técnicas diretamente na plataforma
  - Integração com eProdutor (Avicultura de corte > Ocorrências > Orientações técnicas)
  - Restrição: apenas para lotes em andamento ou em espera
  
- **Filtros**
  - Filtros por produtor, propriedade, lote, etc.
  - Atualização em tempo real da tabela e mapa conforme filtros aplicados
  
- **Mapa de Alertas**
  - Visualização geográfica dos alertas
  - Geolocalização precisa das propriedades
  - Funcionalidades interativas do mapa

---

## 2. Ocorrências

**Objetivo:** Acessar e baixar dados detalhados sobre ocorrências e realizar orientações técnicas aos produtores de forma online.

### Features:
- **Lista de Ocorrências**
  - Exibição de todas as ocorrências registradas
  - Visualização de ocorrências por tipo
  - Informações históricas dos lotes
  
- **Detalhamento de Ocorrências**
  - Pop-up com informações detalhadas de cada ocorrência
  - Sincronização com dados do eProdutor
  - Validação de consistência entre sistemas
  
- **Filtros**
  - Filtros por tipo de ocorrência, período, produtor, etc.
  - Atualização da lista e mapa conforme filtros
  
- **Mapa de Ocorrências**
  - Visualização geográfica das ocorrências
  - Geolocalização das propriedades
  - Funcionalidades interativas
  
- **Última Atualização**
  - Indicador de última atualização
  - Sincronização com a ocorrência mais recente
  
- **Orientação Técnica Online**
  - Criação de orientações técnicas vinculadas a ocorrências
  - Registro automático no eProdutor como "Orientação técnica"
  
- **Exportação de Dados**
  - Funcionalidade de download/exportação
  - Consistência entre dados exportados e exibidos em tela

---

## 3. Monitoramento - Sensores

**Objetivo:** Realizar consultas de sensores para identificar localização, nível de bateria e últimos envios.

### Features:
- **Lista de Sensores**
  - Exibição de todos os sensores cadastrados
  - Informações de localização
  - Nível de bateria
  - Data/hora dos últimos envios
  
- **Sincronização com eProdutor**
  - Comparação de dados entre AgroCenter e eProdutor
  - Validação de consistência (Sensores > Cadastro e consulta > Avicultura)
  
- **Detalhamento de Sensores**
  - Pop-up com últimas medidas do sensor (acionado pela lupa na coluna ações)
  - Informações detalhadas e íntegras
  - Dados condizentes com as medições reais
  
- **Filtros**
  - Filtros por tipo de sensor, localização, status, etc.
  - Atualização da lista conforme filtros aplicados

---

## 4. Monitoramento - Tempo Real

**Objetivo:** Visualizar em tempo real os dados de IoT provenientes de diferentes fontes, identificando facilmente quando um sensor estiver sem comunicação e se os valores mensurados estiverem dentro ou fora dos parâmetros de referência.

### Features:
- **Dashboard de Cards**
  - Card individual para cada lote com dados de IoT
  - Exibição de múltiplas variáveis por lote
  - Informações do cabeçalho dos cards (nome do lote, produtor, etc.)
  
- **Indicadores de Status**
  - Contador de alertas críticos
  - Contador de alertas moderados
  - Ícone de wi-fi desconectado (pisca em vermelho após 5h sem comunicação)
  
- **Alertas Visuais**
  - Linha amarela para variáveis com alerta moderado
  - Linha vermelha para variáveis com alerta crítico
  - Indicação visual clara de parâmetros fora da referência
  
- **Cabeçalho com Totalizadores**
  - Números totais por categoria de card
  - Correspondência exata com dados exibidos em tela
  
- **Filtros**
  - Filtros por produtor, propriedade, lote, etc.
  - Atualização dos cards conforme filtros
  
- **Busca**
  - Campo de busca por nome de produtor
  - Retorno imediato dos resultados

---

## 5. Monitoramento - Silos

(Aguardando extração detalhada da documentação)

---

## 6. Monitoramento - Copiloto

(Aguardando extração detalhada da documentação)

---

## 7. Monitoramento - Doenças

(Aguardando extração detalhada da documentação)

---

## 8. Monitoramento - Controle de Acesso

(Aguardando extração detalhada da documentação)

---

## 9. Ranking

(Aguardando extração detalhada da documentação)

---

## 10. Análise - Comparativo

(Aguardando extração detalhada da documentação)

---

## 11. Análise - Predição de Peso

**Objetivo:** Realizar análises preditivas de peso dos lotes.

### Features:
- **Interface de Predição**
  - Tela íntegra para análise de predição de peso
  
- **Filtros**
  - Aplicação de filtros para análise
  
- **Inserção de Dados**
  - Botão "+ Insira o primeiro item" para adicionar dados

---

## 12. Análise - Predição de Ração

(Aguardando extração detalhada da documentação)

---

## 13. Solicitações

**Objetivo:** Gerenciar solicitações relacionadas aos lotes.

### Features:
- **Lista de Solicitações**
  - Tela íntegra para visualização de solicitações
  
- **Filtros**
  - Filtros íntegros para refinamento da lista
  - Atualização da visualização conforme filtros aplicados

---

## 14. Relatório - Acompanhamento Diário

**Objetivo:** Acompanhar diariamente a evolução dos lotes.

### Features:
- **Gráficos**
  - Gráfico de peso
  - Gráfico de mortalidade
  - Validação de dados apresentados

---

## 15. Configurações - Detalhada

**Objetivo:** Configurar parâmetros detalhados do sistema.

### Features:
- **Interface de Configuração**
  - Tela íntegra para configurações detalhadas
  
- **Filtros**
  - Filtro por Tipo
  - Filtro por Referência (dependente do tipo selecionado)
  - Renderização correta das opções

---

## 16. Configurações - Atribuição

**Objetivo:** Gerenciar atribuições de responsabilidades.

### Features:
- **Interface de Atribuição**
  - Tela íntegra para gerenciamento de atribuições
  
- **Filtros**
  - Filtros para refinamento
  - Renderização correta das filtragens aplicadas

---

## 17. Configurações - Tags

**Objetivo:** Gerenciar tags do sistema.

### Features:
- **Gerenciamento de Tags**
  - Tela íntegra para visualização de tags
  
- **Criação de Tags**
  - Botão "Adicionar" para criar novas tags
  - Formulário de criação

---

## 18. Configurações - Setores

**Objetivo:** Gerenciar setores da organização.

### Features:
- **Gerenciamento de Setores**
  - Tela íntegra para visualização de setores
  
- **Criação de Setores**
  - Botão "Adicionar" para criar novos setores
  - Formulário de criação

---

## 19. Configurações - Período de Contágio

**Objetivo:** Configurar períodos de contágio para controle sanitário.

### Features:
- **Interface de Configuração**
  - Tela íntegra para configuração de períodos
  
- **Atribuição de Período**
  - Funcionalidade para atribuir período de contágio
  - Validação de dados inseridos

---

## 20. Perfil - Produtores

**Objetivo:** Visualizar lista de produtores, suas fazendas e informações associadas.

### Features:
- **Lista de Produtores**
  - Visualização completa de produtores
  - Informações de fazendas associadas
  - Dados detalhados de cada produtor

---

## 21. Perfil - Consultores

**Objetivo:** Visualizar lista de consultores para acessar detalhes de sua assessoria aos produtores.

### Features:
- **Lista de Consultores**
  - Visualização completa de consultores
  - Informações de assessoria
  - Detalhes de atuação

---

## 22. Perfil do Consultor - Dashboard

**Objetivo:** Visualizar dashboard consolidado do consultor.

### Features:
- **Dashboard de Produtores**
  - Tela íntegra com visão geral
  - Validação de dados apresentados
  - Métricas consolidadas

---

## 23. Perfil do Consultor - Agenda

**Objetivo:** Gerenciar agenda de atendimentos do consultor.

### Features:
- **Visualização de Agenda**
  - Tela íntegra com calendário/lista de atendimentos
  
- **Criação de Atendimentos**
  - Botão "Adicionar > Atendimento"
  - Formulário de criação de atendimento
  - Validação de agendamento

---

## 24. Perfil do Consultor - Relatório

**Objetivo:** Visualizar relatórios de visitas do consultor.

### Features:
- **Dashboard de Relatórios**
  - Tela íntegra com relatório de visitas
  - Validação de dados apresentados
  - Métricas de visitas realizadas

---

## 25. Perfil do Consultor - Copiloto

**Objetivo:** Gerenciar sugestões do copiloto para consultores.

### Features:
- **Interface de Copiloto**
  - Tela íntegra para visualização de sugestões
  
- **Criação de Sugestões**
  - Botão "Adicionar" para nova sugestão
  - Tipo "rascunho" disponível
  - Formulário com informações requisitadas
  - Botão "Salvar como rascunho"
  - Validação de criação

---

## 26. Perfil do Produtor - Linha do Tempo

**Objetivo:** Visualizar linha do tempo de eventos do produtor.

### Features:
- **Linha do Tempo**
  - Tela íntegra com eventos cronológicos
  
- **Filtros**
  - Filtros para refinamento da visualização
  - Atualização conforme filtros aplicados

---

## 27. Perfil do Produtor - Análise

**Objetivo:** Realizar análises gráficas dos dados do produtor.

### Features:
- **Interface de Análise**
  - Tela íntegra para projeção de gráficos
  
- **Criação de Gráficos**
  - Botão "Adicionar" para novo gráfico
  - Modal com seleções requisitadas
  - Validação de projeção em tela

---

## 28. Perfil do Produtor - Resumo Diário

**Objetivo:** Visualizar resumo diário das atividades do produtor.

### Features:
- **Dashboard de Resumo**
  - Tela íntegra com resumo diário
  
- **Filtros**
  - Filtro por aviário
  - Filtro por lote
  - Atualização conforme filtros

---

## 29. Perfil do Produtor - Copiloto - Monitoramento

**Objetivo:** Monitorar sugestões do copiloto para o produtor.

### Features:
- **Interface de Monitoramento**
  - Tela íntegra com sugestões de copiloto
  
- **Filtros**
  - Filtros para refinamento
  - Atualização conforme filtros aplicados

---

## 30. Perfil do Produtor - Copiloto - Recomendações

**Objetivo:** Gerenciar recomendações do copiloto para o produtor.

### Features:
- **Interface de Recomendações**
  - Tela íntegra com recomendações
  
- **Filtros**
  - Filtros para refinamento
  - Atualização conforme filtros
  
- **Criação de Sugestões**
  - Botão "Adicionar" para nova sugestão
  - Tipo "rascunho" disponível
  - Formulário com informações requisitadas
  - Botão "Salvar como rascunho"
  - Validação de criação

---

## 31. Perfil do Produtor - Doenças

**Objetivo:** Monitorar doenças e situação sanitária do produtor.

### Features:
- **Dashboard de Visão Geral**
  - Tela íntegra com visão geral de doenças
  - Validação de dados apresentados
  - Indicadores sanitários

---

## 32. FAQ

**Objetivo:** Fornecer respostas a dúvidas frequentes.

### Features:
- **FAQ - Objetivo das Telas**
  - Tela íntegra com explicações sobre objetivos das telas
  
- **FAQ - Dúvidas Gerais**
  - Tela íntegra com respostas a dúvidas gerais
  - Navegação entre seções

---

## 33. Conexões/Avicultura

**Objetivo:** Gerenciar conexões do SmartConnect no módulo Avicultura.

### Features:
- **Gerenciamento de Conexões**
  - Adição de novas conexões SmartConnect
  - Exclusão de conexões existentes
  - Validação de fluxo sem falhas

---

## 34. Cadastro de Novos Usuários na Plataforma

**Objetivo:** Cadastrar novos usuários na plataforma AgroCenter.

### Features:
- **Login com Microsoft Azure**
  - Acesso via conta Microsoft Azure
  - Fluxo de autenticação
  - Validação de acesso concluído com sucesso
  - URL: https://qas-agrocenter.cvale.com.br/

---

## 35. Convite a Novos Membros de Equipe da Organização

**Objetivo:** Validar fluxo de convite e ingresso de novos membros na equipe.

### Features:
- **Convite de Membros**
  - Acesso via Minha organização > Equipe > Convidar
  - Opção por E-mail
  - Opção por Telefone
  - Envio de convite
  - Gerenciamento na tela de convites da organização
  - Validação de fluxo completo

---

## 36. Convite a Novos Produtores da Organização

**Objetivo:** Validar fluxo de convite de novos produtores.

### Features:
- **Convite de Produtores**
  - Acesso via Minha organização > Produtores > Convidar
  - Opção por E-mail
  - Opção por Telefone
  - Envio de convite
  - Recebimento pelo produtor
  - Compartilhamento de dados produtivos com a organização
  - Validação de fluxo completo

---

## 37. Atribuição de Permissões e Perfis de Usuários

**Objetivo:** Validar atribuição de níveis de acesso e alteração de permissões internas.

### Features:
- **Gerenciamento de Permissões**
  - Acesso via Minha organização > Equipe > Ícone de três pontos
  - Atribuição de nível de acesso:
    - Owner
    - Master
    - Basic
  - Alteração de permissões internas
  - Validação de fluxo adequado

---

**Fonte:** Documento EA-G-OP-SO-AC-CVL-009 - Ativação funcional módulo Avicultura da AgroCenter
