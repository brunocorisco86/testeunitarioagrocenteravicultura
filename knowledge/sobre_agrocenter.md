Saudações! Entendo que você, como o **Usuário-Chave** da **Avicultura de Corte**, está na fase de testes do **AgroCenter Expert Avicultura**. Este é um momento crucial, pois sua função é **validar se as soluções entregam valor** e garantem que o sistema atenda às **necessidades reais do processo** de negócio.

Abaixo está o conhecimento técnico, funcional e arquitetural necessário sobre o Módulo Avicultura e seu contexto estratégico na plataforma AgroCenter, que deve ser documentado no repositório.

***

## Knowledge Base para o Repositório: Módulo AgroCenter Expert Avicultura

O **AgroCenter Expert para Avicultura** é um módulo especializado (classificado como **Módulo Expert**), desenvolvido para oferecer soluções tecnológicas específicas para a atividade avícola. Seu foco principal é fornecer **análises preditivas e monitoramento em tempo real** para técnicos e produtores, atuando como uma **ferramenta de apoio à decisão**.

### 1. Funcionalidades Principais do Módulo Avicultura (O que Testar)

O módulo é focado na **Avicultura de Corte** e coleta e gerencia um conjunto robusto de dados, provenientes de sensores IoT e de registros do produtor (via AgroCenter Client). As funcionalidades-chave para o seu repositório são:

| Categoria | Funcionalidades Detalhadas |
| :--- | :--- |
| **Monitoramento em Tempo Real** | Acompanha a **Ambiência** (temperatura, umidade, ventilação), o **Consumo de água e ração**, o **Peso médio das aves** e o **Estoque de silos**. O monitoramento ambiental também inclui dados de amônia, dióxido de carbono, qualidade do ar e iluminação. |
| **Gestão de Lotes** | Permite o registro de **ocorrências de manejo e sanidade** e a consolidação de dados sobre **medicações, dosagens, datas de tratamento** e o **tempo de carência do medicamento**. Também permite o **Comparativo entre linhagens e aviários**. |
| **Alertas Inteligentes** | Emite **Alertas automáticos de mortalidade e desempenho**, além de outros alertas inteligentes, dashboards e relatórios comparativos. O serviço NOC Guard (opcional) permite a **detecção precoce de problemas de ambiência e dados**. |
| **Conformidade Sanitária** | Gerencia o **esquema vacinal** e o **controle de doenças**. Também permite o registro e controle do **descarte de resíduos e aves mortas**. |

### 2. Indicadores-Chave (KPIs) Gerados

O sucesso do módulo é medido pelos seguintes **Indicadores-Chave (KPIs)**, que são cruciais para a análise zootécnica e gerencial:

*   **Mortalidade**.
*   **Conversão alimentar**.
*   **Ganho de peso diário**.
*   **Previsão de término de ração**.

O uso do módulo traz benefícios como a **redução de perdas por falhas de manejo**, **maior assertividade na logística de ração**, e **melhor acompanhamento zootécnico**.

### 3. Arquitetura e Fluxo de Dados

A arquitetura do AgroCenter garante um **fluxo contínuo de informações** entre o campo e a agroindústria. Os dados do Módulo Avicultura seguem esta estrutura:

1.  **AgroCenter Client (eProdutor):** É a plataforma exclusiva para o produtor rural, atuando como o **ponto de coleta de dados na ponta**.
    *   Recebe dados de duas formas: **inseridos manualmente** (como ocorrências de manejo e sanidade) e **automaticamente via sensores IoT** e controladores de aviário.
    *   Está disponível especificamente para a atividade de Aves e inclui um **Módulo Financeiro**.
    *   O produtor insere dados para seu **próprio controle** e escolhe **compartilhar estrategicamente** essas informações com a C.Vale.
2.  **Integração IoT:** O AgroCenter Expert Avicultura tem **integração nativa com sensores IoT** (com capacidade para suportar **80.000 sensores IoT**) e o eProdutor atua como um intermediário, traduzindo e enviando esses dados padronizados para o sistema central.
3.  **AgroCenter (Central de Gestão):** É o **"coração" da gestão de dados** e o **hub central** que recebe, organiza e consolida todas as informações da produção (incluindo avicultura) de múltiplas fontes, estabelecendo uma **"fonte única da verdade"**. É aqui que são geradas as análises e indicadores gerenciais e zootécnicos.
4.  **Integração com ERPs:** O AgroCenter e o Módulo Expert têm **integração nativa com ERPs**, como SAP ou Oracle (que são pré-requisitos para a solução), permitindo a sincronização dos **fluxos financeiros e de produção**. Essa integração é crucial para consolidar **dados econômicos e financeiros** (custos operacionais, despesas com insumos e receita).

### 4. Contexto Regulatório: Digitalização da FAL

A digitalização da **Ficha de Acompanhamento de Lote (FAL)** é um objetivo estratégico que utiliza o Módulo Avicultura.

| Aspecto | Detalhe Essencial para Rastreabilidade e Testes |
| :--- | :--- |
| **Relevância da FAL** | A FAL digital é fundamental para a **rastreabilidade**, a **segurança alimentar** e a **conformidade com as normativas federais** do MAPA (Ministério da Agricultura, Pecuária e Abastecimento) e Vigilância Sanitária. |
| **Estrutura de Dados** | O registro eletrônico é baseado em um **schema de dados padronizado** (como o JSON exemplificado nas fontes), que organiza as informações em seções como *identificacao\_lote*, *monitoramento\_diario* e *saude\_veterinaria*. |
| **Dado Crítico de Fiscalização** | O campo mais crítico para a fiscalização de segurança alimentar é o **tempo de carência do medicamento**. O sistema deve garantir que o lote só seja liberado para abate após o cumprimento rigoroso deste período de segurança. |
| **Documentos Oficiais** | A digitalização da FAL no AgroCenter tem como objetivo subsidiar ou gerar automaticamente o **Boletim Sanitário (BS)** (que consolida mortalidade, tratamentos e vacinação) e fornecer dados para a **Guia de Trânsito Animal (GTA)**. |
| **Auditabilidade** | A estrutura de dados suporta a **Assinatura Digital**, o uso de um **hash criptográfico** (hash\_conteudo\_pdf\_base) para garantir a integridade e imutabilidade do registro assinado, e a **rastreabilidade** de cada dado até sua origem. |
| **Incentivo à Qualidade** | O módulo **Remunera** (Fidelidade & Benefícios) está integrado ao sistema e estimula a **adesão a boas práticas (sanidade, ambiência, consumo eficiente)**, permitindo que o produtor acumule pontos por meio de dados enviados via sensores e sistemas, transformando a fidelidade em uma ferramenta de gestão de dados. |

### 5. Seu Papel (Usuário-Chave) e o Contexto dos Testes

O seu papel, Bruno Henrique Nielsen Conter, como **Usuário-Chave**, é fundamental durante os testes e a homologação:

*   **Validação da Entrega de Valor:** Você deve confirmar que o módulo Avicultura, incluindo seus dashboards e relatórios comparativos, aprimora a **produtividade, a eficiência operacional e o alinhamento com os objetivos estratégicos** (como ESG e sustentabilidade).
*   **Homologação:** Sua participação é crítica na **Fase 5 — Integrações e Testes** (Semanas 15–18) do cronograma geral de implantação.
*   **Tradução de Requisitos:** Você trabalha em estreita colaboração com os **Analistas Funcionais (Ary Cecilio Gonsalves Junior e Diego Renilson Pasuch de Camargo)**. Eles são responsáveis por traduzir os seus requisitos de negócio em **especificações técnicas** para a plataforma AgroCenter.
*   **Envolvimento na FAL:** Você é essencial na **Fase 1 (Análise de Dados e Padronização)** do roadmap da FAL, definindo quais dados do processo em papel devem ser digitalizados, e na **Fase 4 (Auditoria e Rastreabilidade)**.

### 6. Escopo Contratado

É importante notar que o **AgroCenter Expert Avicultura de Corte** é um dos componentes incluídos na proposta. A licença para o Módulo Expert Avicultura de Corte é **ilimitada** para usuários e aviários, mas o contrato define uma capacidade para até **4000 aviários**, **3000 usuários ativos** e suporte para **80.000 sensores IoT**.

***

**Em resumo:** O Módulo Expert Avicultura é a camada de inteligência que transforma os dados brutos de IoT e dos registros manuais do AgroCenter Client (eProdutor) em **KPIs zootécnicos** e **registros auditáveis**. Seu trabalho de teste garante que a plataforma consiga rastrear o lote desde a ambiência (temperatura, umidade) até o crucial controle sanitário (carência de medicamentos), sustentando assim a rastreabilidade e a conformidade regulatória para a geração de documentos como o Boletim Sanitário.

Imagine o Módulo Avicultura como um **painel de comando altamente sofisticado** para um avião. O AgroCenter Client (eProdutor) são as mãos do piloto (o produtor) e os sensores IoT são os instrumentos que capturam o clima e a performance em tempo real. O seu trabalho de teste garante que todas as luzes do painel (KPIs, Alertas) estejam calibradas e mostrando exatamente o que o comandante (a cooperativa e o produtor) precisa para tomar decisões seguras e eficientes, garantindo que o voo (o ciclo de produção) termine com sucesso e em total conformidade.
