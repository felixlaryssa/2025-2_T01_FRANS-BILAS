# Fase 2 — Medição e análise (Abordagem GQM)

## 1. Introdução

  Esta fase tem como objetivo principal medir as características de qualidade definidas na Fase 1 (Adequação Funcional e Confiabilidade) e analisar os dados coletados. O processo segue o segundo e terceiro passos do modelo GQM:

1. Definir Questões (Baseadas nos Objetivos da Fase 1).

2. Definir Métricas (Para responder às Questões).

3. Coletar Dados (Mensuração).

4. Analisar e Interpretar (Conclusão e Base para a Fase 3).

  O foco da medição está nos Objetos de Avaliação (Módulos/Serviços críticos) e nos Escopos de Usuários definidos para o aplicativo SouGov.br (Mobile).

## 2. Abordagem GQM: Definição de Questões e Métricas

  As métricas são categorizadas por característica de qualidade e subcaracterística, conforme o Modelo de Qualidade ISO/IEC 25010 da Fase 1.

### 2.1. Definição das Metas (Goals) do Projeto (Fase GQM - G)

Na metodologia GQM, o passo inicial (Fase 1) é a definição de Metas, o "G" de Goal. Embora a documentação da Fase 1 já tenha estabelecido o propósito e o escopo, formalizar as metas no formato GQM completo é crucial antes de mergulhar nas métricas.

  As metas (Goals) são formalizadas a partir do propósito da avaliação estabelecido na Fase 1, usando a estrutura do GQM: Propósito - Objeto - Qualidade do Foco - Ponto de Vista - Ambiente.

| Objeto (O que será analisado?) |	Propósito (Por que o objeto será analisado?) |	Qualidade do Foco (Propriedade do objeto)	| Ponto de Vista (Quem vai utilizar os dados?)	| Ambiente (Contexto da análise) |
| ------------------------------ | --------------------------------------------- | ------------------------------------------ | --------------------------------------------- | ------------------------------ |
| Módulos Críticos do SouGov.br Mobile (Contracheque, Prova de Vida Digital, Férias/Licenças) |	Avaliação e Melhoria |	Adequação Funcional (Completude e Correção)	| Usuários Finais (Servidores Ativos, Aposentados, Pensionistas)	| No contexto do Serviço Público Digital Federal |
| Integrações Sistêmicas Críticas (Com SIAPE, Gov.br e Prova de Vida Digital)	| Avaliação e Acompanhamento	| Confiabilidade (Maturidade, Disponibilidade e Tolerância a Falhas) |	Fornecedor/Desenvolvedor (Serpro) e Gestor (MGI)	| No contexto do Projeto de Modernização Governamental |
| Processo de Suporte e Manutenção do SouGov.br |	Controle e Melhoria |	Correção/Confiabilidade (Redução de Falhas Operacionais e de Cálculo) |	Gestor Sênior (MGI) e Órgãos de Controle (CGU, TCU)	| No contexto dos Problemas de performance e incidentes |

#### Metas (Goals) Formalizadas

  A partir do quadro GQM, podemos declarar as metas formais:

GOAL 1: Avaliar os Módulos Críticos do SouGov.br Mobile (Contracheque, Prova de Vida, Férias) com o propósito de melhoria, focando na Adequação Funcional (Completude e Correção), do ponto de vista dos Usuários Finais, no contexto do Serviço Público Digital Federal.

GOAL 2: Acompanhar as Integrações Sistêmicas Críticas (SIAPE, Gov.br) com o propósito de controle e avaliação, focando na Confiabilidade (Disponibilidade e MTBF), do ponto de vista do Fornecedor/Desenvolvedor (Serpro) e Gestor (MGI), no contexto do Projeto de Modernização Governamental.

### 2.2. Definição das Medição e Análise (Abordagem GQM - Q e M)

Abaixo estão as Questões (Q) e as Métricas (M) detalhadas, alinhadas com as características de qualidade definidas na Fase 1 e nas Metas (G) estabelecidas.

#### 2.2.1. Adequação Funcional

| Característica |	Subcaracterística |	Questão (Q)	| Métrica (M)	| Fonte de Dados (Onde buscar)	| Tipo de Análise |
| -------------- | ------------------ | ----------- | ----------- | ----------------------------- | ---------------- |
| Adequação Funcional	| Completude Funcional	| Q1: Os módulos críticos atendem a todos os requisitos e funções esperadas para cada perfil de usuário (Ativo, Aposentado, Pensionista)?	| M1: Cobertura de Requisitos Críticos por Módulo (Nrequisitos_atendidos​/Nrequisitos_totais​ em %)	| 1. Documentação Oficial do SouGov.br (MGI). 2. Registros de Chamados (Central de Ajuda/Suporte): Filtrar por "Funcionalidade Ausente".	| Análise de Documentação e Rastreabilidade	|	
| Adequação Funcional |	Correção Funcional	| Q2: Os resultados produzidos pelos serviços críticos (e.g., cálculo de contracheque, férias) estão corretos e em conformidade com as regras de negócio? |	M2: Taxa de Inconformidade Funcional (TIF) (Nerros_caˊlculo​/Ncaˊlculos_auditados​ em %)	| 1. Registros de Chamados de Erro/Bug (Serpro/MGI): Filtrar por "Cálculo Incorreto" ou "Dados Divergentes". 2. Auditoria de Dados (Simulação): Comparação de 50 registros no SIAPE vs. SouGov.br.	| Teste de Caixa Preta e Auditoria |		
| Adequação Funcional |	Adequação à Tarefa	| Q3: As funções críticas (e.g., Prova de Vida Digital) permitem que os usuários concluam suas tarefas de forma eficiente, sem falhas de usabilidade?	| M3: Taxa de Sucesso na Conclusão de Tarefas Críticas (TSCTC) (Ntarefas_completadas​/Ntentativas_totais​ em %)	| 1. Pesquisas de Satisfação e Comentários (App Stores): Análise de feedback sobre dificuldades de uso. 2. Dados de Telemetria (Acesso restrito - Simular): Taxa de Abandono em Funções Chave (Ex: Prova de Vida). |	Testes de Usabilidade e Análise de Comportamento |

#### 2.2.2. Confiabilidade

| Versão | Data       | Descrição                             | Autor(a) |
| ------ | ---------- | ------------------------------------- | -------- |
| 1.0    | 12/10/2025 | Versão inicial da fase 2 | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)   |
