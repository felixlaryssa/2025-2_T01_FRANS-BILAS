# Fase 2 — Especificação da Avaliação (Modelo GQM aplicado ao SouGov.br Mobile)

## 1. Introdução e Objetivos

  Esta fase tem como objetivo principal especificar a avaliação das características **Adequação Funcional** e **Confiabilidade** do aplicativo **SouGov.br**, conforme os critérios definidos na [**fase 1**](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/). A partir dessas definições iniciais, são estabelecidas as próximas etapas do processo de medição e análise de qualidade, das quais as três primeiras serão desenvolvidas nesta fase de especificação: 
.

1. **Definir Metas (Goals)** – Estabelecer os objetivos da avaliação, alinhados às características de qualidade selecionadas.

2. **Definir Questões (Questions)** – Formular perguntas baseadas nas metas da Fase 1, que direcionem a análise dos resultados.

3. **Definir Métricas (Metrics)** – Identificar indicadores quantitativos e qualitativos capazes de responder às questões propostas.

4. **Coletar Dados (Mensuração – Fase 3)** – Realizar a medição prática dos indicadores definidos.

5. **Analisar e Interpretar (Conclusões – Fase 3)** – Interpretar os resultados obtidos e utilizá-los como base para decisões de melhoria contínua.

  O foco da medição está voltado para os objetos de avaliação (módulos e serviços críticos) e para os escopos de usuários definidos no contexto do aplicativo SouGov.br (versão mobile).

<details>
  <summary>Versão SouGov Mobile</summary>
  Versão 5.573 — Versão mobile utilizada ao longo desta avaliação.
</details>

## 2. Metodologia - Modelo Goal Question Metric (GQM)

O modelo **Goal Question Metric (GQM)** define que cada **meta de avaliação (Goal)** deve ser desdobrada em **questões (Questions)** que reflitam aspectos observáveis do sistema, e em **métricas (Metrics)** que respondam a essas questões de forma objetiva. A aplicação do GQM assegura que cada métrica esteja diretamente relacionada a um objetivo de negócio, evitando medições sem valor prático.


<div style="text-align: center;">
  <img src="../assets/images/gqm.png" alt="SouGov.br" style="max-width: 100%; height: auto;">
</div>
<div style="text-align: center; margin: 0; font-size: 14px;">
  Imagem 1:  Modelo Goal Question Metric (GQM)
</div>

### Estrutura Analítica (modelo base)

| **Elemento**       | **Definição no GQM**                |
|--------------------|------------------------------------|
| **Objeto (O que será analisado)** | SouGov Mobile |
| **Propósito (Por que será analisado)** | Avaliação, controle, melhoria |
| **Qualidade do foco** | Característica de interesse |
| **Ponto de vista** | Servidores Públicos, pensionistas |
| **No contexto da** | Disciplina de Qualidade de Software 1 (FCTE - UnB) |



## 3. Abordagem GQM: Definição de Metas, Questões e Métricas

  As métricas são categorizadas por característica de qualidade e subcaracterística, conforme o Modelo de Qualidade ISO/IEC 25010 da Fase 1.

### 3.1. Definição das Metas (Goals) do Projeto (Fase GQM - G)

Na metodologia GQM, o passo inicial (Fase 1) é a definição de Metas, o "G" de Goal. Embora a documentação da Fase 1 já tenha estabelecido o propósito e o escopo, formalizar as metas no formato GQM completo é crucial antes de mergulhar nas métricas.

  As metas (Goals) são formalizadas a partir do propósito da avaliação estabelecido na Fase 1, usando a estrutura do GQM: Propósito - Objeto - Qualidade do Foco - Ponto de Vista - Ambiente.

| Objeto (O que será analisado?) |	Propósito (Por que o objeto será analisado?) |	Qualidade do Foco (Propriedade do objeto)	| Ponto de Vista (Quem vai utilizar os dados?)	| Ambiente (Contexto da análise) |
| ------------------------------ | --------------------------------------------- | ------------------------------------------ | --------------------------------------------- | ------------------------------ |
| Aplicativo móvel SouGov.br | Avaliar a adequação funcional do sistema | Completude, correção e adequação à tarefa | Gestores de produto, analistas de QA e usuários finais | Operação pública em dispositivos móveis, dados observáveis via monitoramento funcional |
| Aplicativo móvel SouGov.br e seus serviços de backend | Monitorar e prever falhas de estabilidade e disponibilidade | Maturidade, disponibilidade, recuperabilidade | Servidores Públicos, pensionistas, usuários finais | Execução real do aplicativo em dispositivos móveis com dependência de APIs públicas |

#### Metas (Goals) Formalizadas 

  A partir do quadro GQM, podemos declarar as metas formais:

GOAL 1: Medir o nível de Adequação Funcional do aplicativo SouGov.br para identificar gaps de completude, correção e adequação à tarefa nos módulos críticos (ex: Prova de Vida, Contracheque), do ponto de vista dos gestores de produto e usuários finais, no contexto de operação em dispositivos móveis, com o objetivo de priorizar a correção de defeitos e o desenvolvimento de funcionalidades ausentes.

GOAL 2: Controlar, monitorar e prever falhas de estabilidade e disponibilidade do Aplicativo móvel SouGov.br e seus serviços de backend, com foco na maturidade, disponibilidade, recuperabilidade, no ponto de vista dos usuários, no contexto da execução real do aplicativo em dispositivos móveis com dependência de APIs públicas.

### 3.2. Definição das Questões e Métricas (Abordagem GQM - Q e M)

Abaixo estão as Questões (Q) e as Métricas (M) detalhadas, alinhadas com as características de qualidade definidas na Fase 1 e nas Metas (G) estabelecidas.

#### 3.2.1. Adequação Funcional

| Característica      | Subcaracterística    | Questão (Q)                                                                                                                                             | Métrica (M)                                                                                                   | Fonte de Dados / Onde buscar                                                                                     | Tipo de Análise                                  | Hipóteses (H)                                                                                                                                                                                    |
| ------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Adequação Funcional | Completude Funcional | Q1: Os módulos críticos atendem a todos os requisitos e funções esperadas para cada perfil de usuário?                                                  | M1: Cobertura de Requisitos Críticos por Módulo (Nrequisitos_atendidos / Nrequisitos_totais em %)             | 1. Documentação Oficial SouGov.br (MGI) <br> 2. Chamados de Suporte: filtrar "Funcionalidade Ausente"            | Análise de Documentação / Rastreabilidade        | H1a: ≥ 95% dos requisitos críticos atendidos <br> H1b: 80–94% dos requisitos atendidos, indicando necessidade de melhorias pontuais                                                              |
| Adequação Funcional | Correção Funcional   | Q2: Os resultados produzidos pelos serviços críticos, como cálculo de contracheque e férias, estão corretos e em conformidade com as regras de negócio? | M2: Taxa de Inconformidade Funcional (TIF) (Nerros_cálculo / Ncálculos_auditados em %)                        | 1. Chamados de Erro/Bug (filtrar "Cálculo Incorreto") <br> 2. Auditoria: comparar 50 registros SIAPE x SouGov.br | Teste de Caixa Preta                  | H2a: TIF ≤ 5%, indicando alta conformidade <br> H2b: TIF entre 6% e 15%, sugerindo ocorrência de erros que exigem correção                                                                       |
| Adequação Funcional | Adequação à Tarefa   | Q3: As funções críticas, como Prova de Vida Digital, permitem que os usuários concluam suas tarefas de forma eficiente, sem falhas de usabilidade?      | M3: Taxa de Sucesso na Conclusão de Tarefas Críticas (TSCTC) (Ntarefas_completadas / Ntentativas_totais em %) | 1. Pesquisas de Satisfação e Comentários nas App Stores <br> 2. Telemetria: taxa de abandono em funções-chave    | Testes de Usabilidade / Análise de Comportamento | H3a: ≥ 90% das tentativas de concluir tarefas críticas são bem-sucedidas <br> H3b: Entre 70% e 89% das tentativas são bem-sucedidas, apontando necessidade de ajustes na interface ou nos fluxos |




#### 3.2.2. Diagrama GQM - Adequação Funcional

<img width="741" height="311" alt="AdequacaoFuncional_Diagrama" src="https://github.com/user-attachments/assets/30544782-a139-40cd-b11d-c0140fda5561" />

#### 3.2.3. Confiabilidade

| Característica | Subcaracterística                      | Questão (Q)                                                                                                                                       | Métrica (M)                                                                                                   | Fonte de Dados / Onde buscar                                                                                                                                                            | Tipo de Análise                       | Hipóteses (H)                                                                                                                                                            |
| -------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Confiabilidade | Maturidade e Disponibilidade           | Q4: Qual a estabilidade e o tempo de operação do sistema (uptime) para os serviços críticos, especialmente em integração?                         | M4: Tempo Médio Entre Falhas (TMEF ou MTBF) (horas/dias) e Disponibilidade Percentual (%)                     | 1. Acordos de Nível de Serviço (SLA) (Documentos MGI/Serpro): metas de MTBF e disponibilidade <br> 2. Logs de Infraestrutura (Serpro): registros de uptime/downtime dos últimos 6 meses | Monitoramento de Desempenho e Logs    | H4a: MTBF elevado e disponibilidade ≥ 99%, indicando alta estabilidade do sistema. <br> H4b: MTBF médio e disponibilidade entre 95% e 98%, sugerindo melhorias pontuais. |
| Confiabilidade | Tolerância a Falhas e Recuperabilidade | Q5: Em caso de falha de integração (ex.: SIAPE, Gov.br), o sistema consegue se recuperar e restaurar a operação em tempo hábil?                   | M5: Tempo Médio Para Reparo/Recuperação (TMPR ou MTTR) (horas/minutos)                                        | 1. Relatórios de Incidentes Críticos (Serpro): tempo para restaurar a funcionalidade após falhas críticas <br> 2. Logs de Integração: análise de rollback e tempo de restauração        | Análise de Incidentes e Resiliência   | H5a: TMPR ≤ 1 hora, indicando alta capacidade de recuperação. <br> H5b: TMPR entre 1 e 3 horas, mostrando necessidade de ajustes nos procedimentos de recuperação.       |
| Confiabilidade | Frequência de Falhas                   | Q6: Qual a frequência de falhas operacionais que impactam diretamente o usuário final nos módulos críticos (ex.: crash do app, erro de servidor)? | M6: Frequência de Falhas Operacionais (FFO) por módulo (Nfalhas_operacionais / Nsessões_usuário em % ou taxa) | 1. Registros históricos de incidentes (Serpro/MGI): relatórios de bug e crash em produção <br> 2. Logs de Servidor e Telemetria (Serpro/App Stores): dados de erros críticos reportados | Análise Estatística e de Logs de Erro | H6a: FFO ≤ 2%, indicando baixa ocorrência de falhas críticas. <br> H6b: FFO entre 3% e 5%, sugerindo necessidade de melhorias de estabilidade.                           |


#### 3.2.4. Diagrama GQM - Confiabilidade

<img width="741" height="311" alt="Confiabilidade_Diagrama" src="https://github.com/user-attachments/assets/18928250-7a8e-4d50-aba5-45a3c541c1ac" />


### 3.3 Níveis de Pontuação e Critérios para Julgamento

Os níveis de pontuação e critérios de julgamento foram definidos para cada métrica de acordo com as hipóteses estabelecidas, permitindo mensurar o grau de alcance das metas de forma objetiva e coerente com os objetivos de qualidade. As faixas de avaliação (Excelente, Bom, Regular e Insuficiente) possibilitam verificar o desempenho funcional do SouGov.br sob a perspectiva da adequação funcional e confiabilidade, com base em dados quantitativos e observáveis.

#### Adequação Funcional


**Subcaracterística 1:** Completude Funcional

Métrica: Cobertura de Requisitos Críticos por Módulo (%)

Hipóteses:

- H1a: ≥ 95% dos requisitos críticos atendidos

- H1b: 80–94% dos requisitos atendidos

| Nível            | Critério de Julgamento                  | Interpretação                                                                    |
| ---------------- | --------------------------------------- | -------------------------------------------------------------------------------- |
| **Excelente**    | ≥ 95% dos requisitos críticos atendidos | O sistema cobre praticamente todos os requisitos críticos esperados.             |
| **Bom**          | 80% – 94%                               | Há boa cobertura, mas pequenas lacunas funcionais precisam de correção.          |
| **Regular**      | 60% – 79%                               | Cobertura parcial; funções essenciais ausentes ou incompletas.                   |
| **Insuficiente** | < 60%                                   | Baixa cobertura dos requisitos críticos; falhas severas de completude funcional. |

**Subcaracterística 2:** Correção Funcional

Métrica: Taxa de Inconformidade Funcional (TIF = erros em %)

Hipóteses:

- H2a: TIF ≤ 5%

- H2b: TIF entre 6% e 15%

| Nível            | Critério de Julgamento | Interpretação                                                       |
| ---------------- | ---------------------- | ------------------------------------------------------------------- |
| **Excelente**    | TIF ≤ 5%               | Alta conformidade com regras de negócio e cálculos corretos.        |
| **Bom**          | 6% – 15%               | Pequenos desvios que não comprometem significativamente a operação. |
| **Regular**      | 16% – 25%              | Ocorrência frequente de erros que impactam a confiabilidade.        |
| **Insuficiente** | > 25%                  | Elevada taxa de erros; o sistema compromete os resultados críticos. |

**Subcaracterística 3:** Adequação à Tarefa

Métrica: Taxa de Inconformidade Funcional (TIF = erros em %)

Hipóteses:

- H2a: TIF ≤ 5%

- H2b: TIF entre 6% e 15%

| Nível            | Critério de Julgamento                   | Interpretação                                                                                |
| ---------------- | ---------------------------------------- | -------------------------------------------------------------------------------------------- |
| **Excelente**    | ≥ 90% das tarefas concluídas com sucesso | Fluxos e interface otimizados; alta eficiência do usuário.                                   |
| **Bom**          | 70% – 89%                                | Boas condições de uso, mas ainda há barreiras em tarefas críticas.                           |
| **Regular**      | 50% – 69%                                | Dificuldades significativas na execução de tarefas; usabilidade limitada.                    |
| **Insuficiente** | < 50%                                    | Falhas graves de adequação à tarefa; usuários não conseguem completar atividades essenciais. |

#### Confiabilidade

**Subcaracterística 1:** Maturidade e Disponibilidade

Métrica: Tempo Médio Entre Falhas (TMEF ou MTBF) e Disponibilidade Percentual (%)

Hipóteses:

- H4a: MTBF elevado e disponibilidade ≥ 99%

- H4b: MTBF médio e disponibilidade entre 95% e 98%

| **Nível**        | **Critério de Julgamento**                                          | **Interpretação**                                                                        |
| ---------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| **Excelente**    | MTBF elevado (acima do esperado no SLA) e **disponibilidade ≥ 99%** | Sistema altamente estável, praticamente sem interrupções perceptíveis ao usuário.        |
| **Bom**          | MTBF médio e **disponibilidade entre 95% e 98%**                    | Boa estabilidade, com falhas ocasionais que não afetam o serviço de forma significativa. |
| **Regular**      | MTBF baixo e **disponibilidade entre 85% e 94%**                    | Interrupções recorrentes e degradação perceptível do serviço.                            |
| **Insuficiente** | MTBF muito baixo e **disponibilidade < 85%**                        | Sistema instável, com falhas frequentes e impacto direto na confiabilidade percebida.    |

**Subcaracterística 2:** Tolerância a Falhas e Recuperabilidade

Métrica: Tempo Médio Para Reparo/Recuperação (TMPR ou MTTR)

Hipóteses:

- H5a: TMPR ≤ 1 hora

- H5b: TMPR entre 1 e 3 horas

| **Nível**        | **Critério de Julgamento** | **Interpretação**                                                                                 |
| ---------------- | -------------------------- | ------------------------------------------------------------------------------------------------- |
| **Excelente**    | TMPR ≤ 1 hora         | Elevada capacidade de recuperação; falhas solucionadas rapidamente sem afetar o serviço.          |
| **Bom**          | 1 < TMPR ≤ 3 horas     | Boa resposta a falhas; pequenos atrasos pontuais na restauração.                                  |
| **Regular**      | 3 < TMPR ≤ 6 horas     | Recuperação lenta; impacto moderado nas operações.                                                |
| **Insuficiente** | TMPR > 6 horas         | Recuperação ineficiente; tempo de inatividade prolongado e falhas críticas sem resposta imediata. |

**Subcaracterística 3:** Frequência de Falhas

Métrica: Frequência de Falhas Operacionais (FFO)

Hipóteses:

- H6a: FFO ≤ 2%

- H6b: FFO entre 3% e 5%

| **Nível**        | **Critério de Julgamento** | **Interpretação**                                                       |
| ---------------- | -------------------------- | ----------------------------------------------------------------------- |
| **Excelente**    | FFO ≤ 2%               | Sistema altamente confiável; falhas raras e bem controladas.            |
| **Bom**          | 3% ≤ FFO ≤ 5%          | Pequena ocorrência de falhas, com impacto mínimo no uso.                |
| **Regular**      | 6% ≤ FFO ≤ 10%*        | Falhas ocasionais perceptíveis; necessidade de ajustes de estabilidade. |
| **Insuficiente** | FFO > 10%              | Alta taxa de falhas; experiência do usuário comprometida.               |

### 3.4 Análise e Interpretação dos Resultados

Após a coleta de dados, a análise se concentrará em correlacionar os resultados das métricas com as questões definidas.

#### 3.4.1. Passos da Análise

 Visualização: Criação de gráficos e dashboards (e.g., Taxa de Inconformidade Funcional por Objeto, MTBF por Mês).

 Comparação:

- Baseline: Comparar os resultados das métricas com os objetivos de qualidade preestabelecidos (e.g., meta de TIF ≤ 2%, meta de Disponibilidade ≥ 99.5%).

- Tendência: Analisar a evolução dos resultados ao longo do tempo (últimos 6 meses) para identificar tendências de melhoria ou degradação.

 Identificação de Causas Raiz: Para métricas que não atingirem as metas:

- Analisar os logs de falha (M4, M5, M6) para identificar os módulos e as integrações mais instáveis.

- Cruzar a baixa Taxa de Sucesso (M3) com as falhas de Correção Funcional (M2) para entender o impacto no usuário.

 Conclusão da Fase: Gerar um relatório consolidado com a performance do SouGov.br em relação à Adequação Funcional e Confiabilidade.


## Tabela de Contribuição - Grupo Frans Bilas

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 4: Contribuições dos Membros do Grupo
</div>

| Matrícula | Nome do aluno | Atividade Realizada | % de Contribuição |
| --------- | ------------- | ------------------- | ----------------- |
| 200060783 | Ana Beatriz W. Massuh | Pesquisa e documentação | 20% |
| 190085584 | Carlos Eduardo Mendes |  Pesquisa | 20% |
| 231034707 | Giovana Ferreira Santos | Pesquisa e documentação | 20% |
| 231026840 | Laryssa Felix |  Pesquisa e documentação  | 20% |
| 202070064 | Matheus do Vale | Pesquisa | 20% |

---------------------

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data       | Descrição                             | Autor(a) |
| ------ | ---------- | ------------------------------------- | -------- |
| 1.0    | 12/10/2025 | Versão inicial da fase 2 | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)   |
| 2.0    | 12/10/2025 | Complementar fase 2 | [Laryssa Felix](https://github.com/felixlaryssa) |
| 3.0    | 24/10/2025 | Revisão e Alteração após PC2 | [Giovana Ferreira](https://github.com/gih7915) |
| 4.0    | 24/10/2025 | Hipóteses Níveis de pontuação | [Laryssa Felix](https://github.com/felixlaryssa) |


