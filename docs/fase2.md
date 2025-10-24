# Fase 2 — Especificação da Avaliação (Modelo GQM aplicado ao SouGov.br Mobile)

## 1. Introdução

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
| **Objeto (O que será analisado)** | Processo, produto ou recurso |
| **Propósito (Por que será analisado)** | Avaliação, controle, melhoria |
| **Qualidade do foco** | Característica de interesse |
| **Ponto de vista** | Quem utilizará os resultados |
| **Ambiente** | Contexto da análise |



## 3. Abordagem GQM: Definição de Metas, Questões e Métricas

  As métricas são categorizadas por característica de qualidade e subcaracterística, conforme o Modelo de Qualidade ISO/IEC 25010 da Fase 1.

### 3.1. Definição das Metas (Goals) do Projeto (Fase GQM - G)

Na metodologia GQM, o passo inicial (Fase 1) é a definição de Metas, o "G" de Goal. Embora a documentação da Fase 1 já tenha estabelecido o propósito e o escopo, formalizar as metas no formato GQM completo é crucial antes de mergulhar nas métricas.

  As metas (Goals) são formalizadas a partir do propósito da avaliação estabelecido na Fase 1, usando a estrutura do GQM: Propósito - Objeto - Qualidade do Foco - Ponto de Vista - Ambiente.

| Objeto (O que será analisado?) |	Propósito (Por que o objeto será analisado?) |	Qualidade do Foco (Propriedade do objeto)	| Ponto de Vista (Quem vai utilizar os dados?)	| Ambiente (Contexto da análise) |
| ------------------------------ | --------------------------------------------- | ------------------------------------------ | --------------------------------------------- | ------------------------------ |
| Aplicativo móvel SouGov.br | Avaliar e melhorar a adequação funcional do sistema | Completude, correção e adequação à tarefa | Gestores de produto, analistas de QA e usuários finais | Operação pública em dispositivos móveis, dados observáveis via monitoramento funcional |
| Aplicativo móvel SouGov.br e seus serviços de backend | Controlar, monitorar e prever falhas de estabilidade e disponibilidade | Maturidade, disponibilidade, recuperabilidade | Usuários | Execução real do aplicativo em dispositivos móveis com dependência de APIs públicas |

#### Metas (Goals) Formalizadas 

  A partir do quadro GQM, podemos declarar as metas formais:

GOAL 1: Medir o nível de Adequação Funcional do aplicativo SouGov.br para identificar gaps de completude, correção e adequação à tarefa nos módulos críticos (ex: Prova de Vida, Contracheque), do ponto de vista dos gestores de produto e usuários finais, no contexto de operação em dispositivos móveis, com o objetivo de priorizar a correção de defeitos e o desenvolvimento de funcionalidades ausentes.

GOAL 2: Controlar, monitorar e prever falhas de estabilidade e disponibilidade do Aplicativo móvel SouGov.br e seus serviços de backend, com foco na maturidade, disponibilidade, recuperabilidade, no ponto de vista dos usuários, no contexto da execução real do aplicativo em dispositivos móveis com dependência de APIs públicas.

### 3.2. Definição das Questões e Métricas (Abordagem GQM - Q e M)

Abaixo estão as Questões (Q) e as Métricas (M) detalhadas, alinhadas com as características de qualidade definidas na Fase 1 e nas Metas (G) estabelecidas.

#### 3.2.1. Adequação Funcional

| Característica |	Subcaracterística |	Questão (Q)	| Métrica (M)	| Fonte de Dados (Onde buscar)	| Tipo de Análise |
| -------------- | ------------------ | ----------- | ----------- | ----------------------------- | ---------------- |
| Adequação Funcional	| Completude Funcional	| Q1: Os módulos críticos atendem a todos os requisitos e funções esperadas para cada perfil de usuário (Ativo, Aposentado, Pensionista)?	| M1: Cobertura de Requisitos Críticos por Módulo (Nrequisitos_atendidos​/Nrequisitos_totais​ em %)	| 1. Documentação Oficial do SouGov.br (MGI). 2. Registros de Chamados (Central de Ajuda/Suporte): Filtrar por "Funcionalidade Ausente".	| Análise de Documentação e Rastreabilidade	|	
| Adequação Funcional |	Correção Funcional	| Q2: Os resultados produzidos pelos serviços críticos (e.g., cálculo de contracheque, férias) estão corretos e em conformidade com as regras de negócio? |	M2: Taxa de Inconformidade Funcional (TIF) (Nerros_cálculo​/Ncálculos_auditados​ em %)	| 1. Registros de Chamados de Erro/Bug (Serpro/MGI): Filtrar por "Cálculo Incorreto" ou "Dados Divergentes". 2. Auditoria de Dados (Simulação): Comparação de 50 registros no SIAPE vs. SouGov.br.	| Teste de Caixa Preta e Auditoria |		
| Adequação Funcional |	Adequação à Tarefa	| Q3: As funções críticas (e.g., Prova de Vida Digital) permitem que os usuários concluam suas tarefas de forma eficiente, sem falhas de usabilidade?	| M3: Taxa de Sucesso na Conclusão de Tarefas Críticas (TSCTC) (Ntarefas_completadas​/Ntentativas_totais​ em %)	| 1. Pesquisas de Satisfação e Comentários (App Stores): Análise de feedback sobre dificuldades de uso. 2. Dados de Telemetria (Acesso restrito - Simular): Taxa de Abandono em Funções Chave (Ex: Prova de Vida). |	Testes de Usabilidade e Análise de Comportamento |

#### 3.2.2. Confiabilidade

| Característica |	Subcaracterística |	Questão (Q)	| Métrica (M)	| Fonte de Dados (Onde buscar)	| Tipo de Análise |
| -------------- | ------------------ | ----------- | ----------- | ----------------------------- | ---------------- |
| Confiabilidade	| Maturidade e Disponibilidade	| Q4: Qual a estabilidade e o tempo de operação do sistema (uptime) para os serviços críticos, especialmente em integração?	| M4: Tempo Médio Entre Falhas (TMEF ou MTBF) (Tempo em Horas/Dias) e Disponibilidade Percentual (em %)	| 1. Acordos de Nível de Serviço (SLA) (Documentos MGI/Serpro): Metas de MTBF e Disponibilidade. 2. Logs de Infraestrutura (Serpro): Registros de uptime/downtime dos últimos 6 meses. | 	Monitoramento de Desempenho e Logs |		
| Confiabilidade |	Tolerância a Falhas e Recuperabilidade	| Q5: Em caso de falha de integração (e.g., SIAPE, Gov.br), o sistema consegue se recuperar e restaurar a operação em tempo hábil?	| M5: Tempo Médio Para Reparo/Recuperação (TMPR ou MTTR) (Tempo em Horas/Minutos)	| 1. Relatórios de Incidentes Críticos (Serpro): Registros de quanto tempo levou para restaurar a funcionalidade após uma falha crítica. 2. Logs de Integração: Análise de rollback e tempo de restauração.	| Análise de Incidentes e Resiliência	|	
| Confiabilidade |	Frequência de Falhas	| Q6: Qual a frequência de falhas operacionais que impactam diretamente o usuário final nos módulos críticos (e.g., crash do app, erro de servidor)?	| M6: Frequência de Falhas Operacionais (FFO) por Módulo (Nfalhas_operacionais​/Nsessões_usuário​ em % ou Taxa)	| 1. Registros Históricos de Incidentes (Serpro/MGI): Relatórios de Bug e Crash em Produção. 2. Logs de Servidor e Telemetria (Serpro/App Stores): Dados de erros críticos (crashes) reportados.	| Análise Estatística e de Logs de Erro	|	

### 3.3. Análise e Interpretação dos Resultados

Após a coleta de dados, a análise se concentrará em correlacionar os resultados das métricas com as questões definidas.

#### 3.3.1. Passos da Análise

1. Visualização: Criação de gráficos e dashboards (e.g., Taxa de Inconformidade Funcional por Objeto, MTBF por Mês).

2. Comparação:

Baseline: Comparar os resultados das métricas com os objetivos de qualidade preestabelecidos (e.g., meta de TIF ≤ 2%, meta de Disponibilidade ≥ 99.5%).

Tendência: Analisar a evolução dos resultados ao longo do tempo (últimos 6 meses) para identificar tendências de melhoria ou degradação.

3. Identificação de Causas Raiz: Para métricas que não atingirem as metas:

Analisar os logs de falha (M4, M5, M6) para identificar os módulos e as integrações mais instáveis.

Cruzar a baixa Taxa de Sucesso (M3) com as falhas de Correção Funcional (M2) para entender o impacto no usuário.

4. Conclusão da Fase: Gerar um relatório consolidado com a performance do SouGov.br em relação à Adequação Funcional e Confiabilidade.

---------------------

## Tabela de Contribuição - Grupo Frans Bilas

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 4: Contribuições dos Membros do Grupo
</div>

| Matrícula | Nome do aluno | Atividade Realizada | % de Contribuição |
| --------- | ------------- | ------------------- | ----------------- |
| 200060783 | Ana Beatriz W. Massuh | ... | % |
| 190085584 | Carlos Eduardo Mendes |  ... | % |
| 231034707 | Giovana Ferreira Santos | ... | % |
| 231026840 | Laryssa Felix |  ...  | % |
| 202070064 | Matheus do Vale | ... | % |

---------------------

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data       | Descrição                             | Autor(a) |
| ------ | ---------- | ------------------------------------- | -------- |
| 1.0    | 12/10/2025 | Versão inicial da fase 2 | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)   |
| 2.0    | 12/10/2025 | Complementar fase 2 | [Laryssa Felix](https://github.com/felixlaryssa) |
