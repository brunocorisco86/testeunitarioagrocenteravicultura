# EA-G-OP-SO-AC-CVL-009 - Ativação funcional módulo Avicultura da AgroCenter

## Informações do Documento

| Campo | Valor |
|-------|-------|
| **Código do Documento** | EA-G-OP-SO-AC-CVL-009 |
| **Versão** | 1.0 |
| **Elaborado Por** | Larissa Ajala Batista |
| **Data de Revisão** | 05/11/2025 |
| **Aprovado Por** | - |
| **Status** | Em Revisão |

## Objetivo

O presente roteiro de testes tem como objetivo validar as funcionalidades do módulo Avicultura da plataforma AgroCenter, garantindo que as entregas estejam alinhadas aos objetivos de negócio e à experiência esperada pelo usuário final.

Além da validação técnica, o roteiro também tem a função de apoiar o usuário na ativação do sistema, facilitando o entendimento das suas funcionalidades, telas e fluxos operacionais. Dessa forma, busca-se assegurar que, ao chegar em ambiente de produção (PRD), o usuário esteja apto a utilizar o sistema de forma adequada, segura e consciente, aproveitando plenamente seus recursos e entregando valor às operações.

A execução dos testes deverá ocorrer em ambiente de homologação.

## Pré-requisitos

Antes de iniciar os testes, é necessário confirmar que:

- A organização do usuário possui o módulo de Avicultura habilitado e as telas liberadas.
- As permissões organizacionais e individuais necessárias estão corretamente configuradas.
- A tela Minha Organização esteja funcional.
- O usuário possui credenciais válidas, com acesso ativo a AgroCenter e ao módulo Avicultura.
- O ambiente de homologação encontra-se estável e operacional.
- Todas as integrações/conexões externas estão funcionando (SmartConnect, Windy).
- O SmartConnect está ancorado na nuvem C.Vale.

## Cenários de teste

### 1. Home

**Cenário:** Como consultor, quero acompanhar uma visão geral dos alertas atuais dos lotes e realizar orientações técnicas aos produtores de forma *on-line*, para ter uma gestão proativa e tomar decisões rápidas.

**Passo 1: Acessar a tela Home**
- Resultado esperado: A tela é íntegra.

**Passo 2: Validar a tabela de alertas**
- Resultado esperado 1: Todos os alertas da tabela estão categorizados corretamente, refletindo as condições reais dos lotes.
- Resultado esperado 2: O cabeçalho reflete os alertas para lotes em andamento e estão categorizados corretamente.

**Passo 3: Clicar em um alerta para visualizar detalhes**
- Resultado esperado: O detalhe do alerta é exibido corretamente, bem como as demais informações acompanhantes.

**Passo 4: Orientar o produtor *on-line***
- Resultado esperado: A funcionalidade de orientação técnica está disponível e todas as funcionalidades íntegras, sendo que esta deve chegar corretamente na tela de Avicultura de corte>Ocorrências>Orientações técnicas do eProdutor. OBS: Somente é possível criar orientações para lotes em andamento ou em espera.

**Passo 5: Aplicar filtros**
- Resultado esperado: A visualização da tabela e do mapa é atualizada conforme os filtros selecionados.

**Passo 6: Validar o mapa, clicando no ícone de mapa no canto superior direito da tabela**
- Resultado esperado 1: As funcionalidades do mapa funcionam adequadamente.
- Resultado esperado 2: As geolocalizações estão corretas.

### 2. Ocorrências

**Cenário:** Como consultor, quero acessar e baixar dados detalhados sobre ocorrências e realizar orientações técnicas aos produtores de forma *on-line*, para gerenciar situações atuais e históricas dos lotes de forma proativa.

**Passo 1: Acessar a tela Ocorrências**
- Resultado esperado: A tela é íntegra.

**Passo 2: Aplicar filtros**
- Resultado esperado: A lista de ocorrências e o mapa são atualizados conforme os filtros selecionados.

**Passo 3: Clicar em uma ocorrência de cada tipo para visualizar detalhes**
- Resultado esperado 1: Uma *pop-up* exibe informações detalhadas de cada ocorrência.
- Resultado esperado 2: As informações apresentadas condizem com àquelas lançadas na tela de ocorrências no eProdutor.

**Passo 4: Abrir o mapa, clicando no ícone de mapa no canto superior direito da tabela**
- Resultado esperado 1: As funcionalidades do mapa funcionam adequadamente.
- Resultado esperado 2: As geolocalizações estão corretas.

**Passo 5: Validar a última atualização**
- Resultado esperado: A última atualização condiz com a ocorrência mais recente.

**Passo 6: Orientar o produtor *on-line***
- Resultado esperado: A funcionalidade de orientação técnica está disponível e operacional, sendo que esta deve chegar corretamente na tela de ocorrências do eProdutor (ocorrência "Orientação técnica").

**Passo 7: Realizar um download, clicando em Exportar**
- Resultado esperado: Os arquivos baixados estão consistentes com os dados exibidos em tela.

### 3. Monitoramento - Sensores

**Cenário:** Como consultor, quero realizar consultas de sensores para identificar sua localização, o nível de bateria e últimos envios.

**Passo 1: Acessar a aba Monitoramento - Sensores**
- Resultado esperado: A tela é íntegra.

**Passo 2: Comparar os dados da tela com o eProdutor>Sensores>Cadastro e consulta>Avicultura**
- Resultado esperado: Informações que constam em ambos os sistemas são semelhantes.

**Passo 3: Clicar sobre a lupa na coluna ações**
- Resultado esperado 1: Uma *pop-up* se abre contendo informações sobre as últimas medidas dos sensores.
- Resultado esperado 2: As informações possuem escrita íntegra.
- Resultado esperado 3: Os dados apresentados são condizentes.

**Passo 4: Aplicar filtros**
- Resultado esperado: A lista de sensores é atualizada conforme os filtros selecionados.

### 4. Monitoramento - Tempo Real

**Cenário:** Eu, como consultor, quero visualizar em tempo real os dados de IoT provenientes de diferentes fontes, identificando facilmente quando um sensor estiver sem comunicação e se os valores mensurados estiverem dentro ou fora dos parâmetros de referência.

**Passo 1: Acessar a aba Monitoramento - Tempo Real**
- Resultado esperado: A tela é íntegra.

**Passo 2: Validar os números exibidos no cabeçalho**
- Resultado esperado: Os valores apresentados em cada categoria de card devem corresponder exatamente aos dados exibidos em tela.

**Passo 3: Aplicar filtros**
- Resultado esperado 1: Os filtros são íntegros.
- Resultado esperado 2: A tela é atualizada conforme os filtros selecionados.

**Passo 4: Digitar o nome de um produtor no campo de buscas**
- Resultado esperado: A tela retorna o nome digitado.

**Passo 5: Validar os cards e as informações exibidas**
- Resultado esperado 1: A tela deve apresentar um card para cada lote que possua dados de IoT, contemplando as diferentes variáveis disponíveis.
- Resultado esperado 2: As informações do cabeçalho dos cards estão corretas.
- Resultado esperado 3: As informações de número de alertas críticos e moderados estão corretas.
- Resultado esperado 4: Se um sensor permanecer sem enviar dados para uma variável por 5 horas ou mais, um ícone de wi-fi desconectado deve ser exibido e piscar na cor vermelha, indicando a perda de comunicação.
- Resultado esperado 5: Se uma variável apresenta alerta moderado, a linha da variável é pintada de amarelo.
- Resultado esperado 6: Se uma variável apresenta alerta crítico, a linha da variável é pintada de vermelho.

---

**Observação:** Este documento contém 37 cenários de teste no total. Os cenários adicionais incluem:

5. Monitoramento - Silos
6. Monitoramento - Copiloto
7. Monitoramento - Doenças
8. Monitoramento - Controle de acesso
9. Ranking
10. Análise - Comparativo
11. Análise - Predição de Peso
12. Análise - Predição de Ração
13. Solicitações
14. Relatório - Acompanhamento Diário
15. Configurações - Detalhada
16. Configurações - Atribuição
18. Configurações - Setores
19. Configurações - Período de Contágio
20. Perfil - Produtores
21. Perfil - Consultores
22. Perfil do Consultor - Dashboard
23. Perfil do Consultor - Agenda
24. Perfil do Consultor - Relatório
25. Perfil do Consultor - Copiloto
26. Perfil do Produtor - Linha do Tempo
27. Perfil do Produtor - Análise
28. Perfil do Produtor - Resumo Diário
29. Perfil do Produtor - Copiloto - Monitoramento
30. Perfil do Produtor - Copiloto - Recomendações
31. Perfil do Produtor - Doenças
32. FAQ
33. Conexões/Avicultura
34. Cadastro de novos usuários na plataforma
35. Convite a novos membros de equipe da organização
36. Convite a novos produtores da organização
37. Atribuição de permissões e perfis de usuários

---

**Fonte:** https://docs.eaware.io/books/agrocenter/page/ea-g-op-so-ac-cvl-009-ativacao-funcional-modulo-avicultura-da-agrocenter
