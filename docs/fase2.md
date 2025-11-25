# Fase 2 — Especificação da Avaliação (Modelo GQM aplicado ao SouGov.br Mobile)

## 1. Introdução e Objetivos

  Esta fase tem como objetivo principal especificar a avaliação das características **Adequação Funcional** e **Confiabilidade** do aplicativo **SouGov.br**, conforme os critérios definidos na [**fase 1**](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/). A partir dessas definições iniciais, são estabelecidas as próximas etapas do processo de medição e análise de qualidade, das quais as três primeiras serão desenvolvidas nesta fase de especificação: 
.

1. **Definir Metas (Goals)** – Estabelecer os objetivos da avaliação, alinhados às características de qualidade selecionadas.

2. **Definir Questões (Questions)** – Formular perguntas baseadas nas metas da Fase 1, que direcionem a análise dos resultados.

3. **Definir Métricas (Metrics)** – Identificar indicadores quantitativos e qualitativos capazes de responder às questões propostas.

4. **Coletar Dados (Mensuração – Fase 3)** – Realizar a medição prática dos indicadores definidos.

5. **Analisar e Interpretar (Conclusões – Fase 4)** – Interpretar os resultados obtidos e utilizá-los como base para decisões de melhoria contínua.

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

| **Elemento**       | **Definição no GQM**   | **Objeto**             |
|--------------------|------------------------|------------------------|
| **Objeto** | O que será analisado | SouGov Mobile |
| **Propósito** | Por que será analisado | Avaliação e Diagnóstico de Satisfação |
| **Qualidade do foco** | Característica de interesse | Adequação Funcional e Confiabilidade (ISO 25010) |
| **Ponto de vista** | Quem vai utilizar os dados? | O Avaliador (Utilizando a Ferramenta de Análise PLN - Processamento de Linguagem Natural) |
| **Contexto** | Disciplina de Qualidade de Software 1 (FCTE - UnB) | Dados observacionais dos usuários em dispositivos móveis. |



## 3. Abordagem GQM: Definição de Metas, Questões e Métricas

  As métricas são categorizadas por característica de qualidade e subcaracterística, conforme o Modelo de Qualidade ISO/IEC 25010 da Fase 1.

### 3.1. Definição das Metas (Goals) do Projeto (Fase GQM - G)

Na metodologia GQM, o passo inicial (Fase 1) é a definição de Metas, o "G" de Goal. Embora a documentação da Fase 1 já tenha estabelecido o propósito e o escopo, formalizar as metas no formato GQM completo é crucial antes de mergulhar nas métricas.

  As metas (Goals) são formalizadas a partir do propósito da avaliação estabelecido na Fase 1, usando a estrutura do GQM: Propósito - Objeto - Qualidade do Foco - Ponto de Vista - Ambiente.

| Objeto (O que será analisado?) |	Propósito (Por que o objeto será analisado?) |	Qualidade do Foco (Propriedade do objeto)	| Ponto de Vista (Quem vai utilizar os dados?)	| Ambiente (Contexto da análise) |
| ------------------------------ | --------------------------------------------- | ------------------------------------------ | --------------------------------------------- | ------------------------------ |
| Aplicativo móvel SouGov.br | Avaliar a adequação funcional do sistema | Completude, correção e adequação à tarefa | Gestores de produto, analistas de QA(Quality Assurance) e usuários finais | Operação pública em dispositivos móveis, dados observáveis via monitoramento funcional |
| Aplicativo móvel SouGov.br e seus serviços de backend | Monitorar e prever falhas de estabilidade e disponibilidade | Maturidade, disponibilidade, recuperabilidade | Servidores Públicos, pensionistas, usuários finais | Execução real do aplicativo em dispositivos móveis com dependência de APIs(Application Programming Interfaces)  públicas |

#### Metas (Goals) Formalizadas 

  A partir do quadro GQM, podemos declarar as metas formais:

GOAL 1: Medir o nível de Adequação Funcional do aplicativo SouGov.br para identificar lacunas de completude, correção e adequação à tarefa nos módulos críticos (ex: Prova de Vida, Contracheque), do ponto de vista dos  usuários finais, no contexto de operação em dispositivos móveis, com o objetivo de priorizar a correção de defeitos e o desenvolvimento de funcionalidades ausentes.

GOAL 2: Controlar, monitorar e prever falhas de estabilidade e disponibilidade do Aplicativo móvel SouGov.br e seus serviços de backend, com foco na maturidade, disponibilidade, recuperabilidade, no ponto de vista dos usuários, no contexto da execução real do aplicativo em dispositivos móveis com dependência de APIs públicas.

### 3.2. Definição das Questões e Métricas (Abordagem GQM - Q e M)

Abaixo estão as Questões (Q) e as Métricas (M) detalhadas, alinhadas com as características de qualidade definidas na Fase 1 e nas Metas (G) estabelecidas.

#### 3.2.1. Adequação Funcional

| Característica | Subcaracterística | Questão (Q) | Métrica (M) | Fonte de Dados / Método de Coleta (Alinhado à Fase 3) | Critério de Julgamento (Nível) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Adequação Funcional | Completude Funcional | Q1: Os módulos críticos atendem a todas as funções esperadas? | M1: Frequência de Lacunas Funcionais (FLF) **(N de N-grams de Ausência / N de reviews Negativos) em %** | Comentários nas App Stores. **Método:** Análise de N-grams (termos como "falta", "não tem", "deveria ter"). | Excelente: ≤ 5% / Bom: 6-15% / Regular: 16-25% / Insuficiente: > 25% |
| Adequação Funcional | Correção Funcional | Q2: Os resultados produzidos pelos serviços críticos (cálculo, regras de negócio) estão corretos? | **M2:  Proporção de Relatos de Incorreção (PRI) ** (N de relatos de cálculo incorreto / N de reviews Negativos) em % | Comentários nas App Stores. **Método:** Mapeamento de Qualidade em termos de "Cálculo", "Incorreto", "Regra de Negócio". | Excelente: PRI ≤ 5% / Bom: 6-15% / Regular: 16-25% / Insuficiente: > 25% |
| Adequação Funcional | Adequação à Tarefa | Q3: As funções críticas permitem que os usuários concluam tarefas de forma eficiente, sem falhas de usabilidade? | **M3:  Índice de Fricção na Tarefa Crítica (IFTC)** (N de N-grams de Fricção / N de reviews Neutros/Negativos) em % | Comentários nas App Stores. **Método:** Análise de N-grams de Fricção (e.g., "não consigo finalizar", "caminho confuso"). | Excelente: ≤ 10% / Bom: 11-30% / Regular: 31-50% / Insuficiente: > 50% |

#### 3.2.2. Diagrama GQM - Adequação Funcional

<img width="741" height="311" alt="AdequacaoFuncional_Diagrama" src="https://github.com/felixlaryssa/2025-2_T01_FRANS-BILAS/blob/main/docs/assets/images/G1.png" />

#### 3.2.3. Confiabilidade

| Característica | Subcaracterística | Questão (Q) | Métrica (M) | Fonte de Dados / Método de Coleta (Alinhado à Fase 3) | Critério de Julgamento (Nível) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Confiabilidade | Maturidade e Disponibilidade | Q4: Qual a estabilidade e o tempo de operação do sistema (uptime) para os serviços críticos, especialmente em integração? | **M4: Frequência de Instabilidade Operacional (FIO)**  (N de relatos de falha/travamento / N de reviews totais) em % | Comentários nas App Stores. **Método:** Mapeamento de Qualidade em "Travamentos", "Lentidão", "Instabilidade" (PLN). | Excelente: ≤ 2% / Bom: 3-5% / Regular: 6-10% / Insuficiente: > 10% |
| Confiabilidade | Tolerância a Falhas e Recuperabilidade | Q5:Em caso de falha de integração, o sistema consegue se recuperar e restaurar a operação em tempo hábil? | **M5: Índice de Recuperação Observável (IRO) ** (N de correções/versão / N de relatos críticos) | Comentários de Usuários (App Stores) e Notas de Atualização. **Método:** Correlação (N-grams de falha desaparecem após nova versão). | Excelente: 90-100% / Bom: 70-89% / Regular: 50-69% / Insuficiente: ≤ 50% |
| Confiabilidade | Frequência de Falhas | Q6:Qual a frequência de falhas operacionais que impactam diretamente o usuário final (crash do app, erro de servidor)? | **M6: Densidade de Relatos de Bugs Críticos (DRBC)**  (N de relatos Bug/Erro / N de reviews totais) em %) | Comentários nas App Stores. **Método:** Mapeamento de Qualidade em "Bugs/Erros" (PLN). | Excelente: DRBC ≤ 2% / Bom: 3-5% / Regular: 6-10% / Insuficiente: DRBC > 10% |


#### 3.2.4. Diagrama GQM - Confiabilidade

<img width="741" height="311" alt="Confiabilidade_Diagrama" src="https://github.com/felixlaryssa/2025-2_T01_FRANS-BILAS/blob/main/docs/assets/images/G2.png" />

### 3.3 Análise e Interpretação dos Resultados

Após a coleta de dados, a análise se concentrará em correlacionar os resultados das métricas com as questões definidas.

#### 3.3.1. Passos da Análise

 **Visualização:** Criação de gráficos e dashboards (painéis de controle) (e.g., Taxa de Inconformidade Funcional por Objeto, MTBF - Tempo Médio Entre Falhas por Mês).

 **Comparação:**

- Baseline: Comparar os resultados das métricas com os objetivos de qualidade preestabelecidos (Critérios de Julgamento).

- Tendência: Analisar a evolução dos resultados ao longo do tempo (últimos 6 meses) para identificar tendências de melhoria ou degradação.

**Identificação de Causas Raiz (PLN e Correlação)** Para métricas que não atingirem as metas:

- Utilizar os N-Grams mais frequentes em reviews negativos para validar e localizar a causa raiz da falha na aplicação.

- Cruzar a baixa IFTC (M3) com a alta DRBC (M6) para entender o impacto no usuário.
  
**Conclusão da Fase:** Gerar um relatório consolidado com a performance do SouGov.br em relação à Adequação Funcional e Confiabilidade.


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
|5.0     | 19/11/2025 | Adequação as outras fases | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)   |
|6.0     | 24/11/2025 | Readequação as outras fases | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)   |


