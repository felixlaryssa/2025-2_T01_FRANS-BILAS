# Fase 3 — Projetar a Avaliação

## 1. Introdução

A fase 3 detalha, de forma objetiva e sistemática, como as características de qualidade selecionadas: **[Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)** e **[Confiabilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)**, serão medidas e avaliadas no aplicativo **SouGov.br Mobile**, software que foi escolhido pelos membros anteriormente durante a [fase1].

<details>
  <summary>Versão SouGov Mobile</summary>
  Versão 5.573 — Versão mobile utilizada ao longo desta avaliação.
</details>

Este **Plano de Avaliação** traduz as definições da [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/) ([metas](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#31-definicao-das-metas-goals-do-projeto-fase-gqm-g), [questões](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#32-definicao-das-questoes-e-metricas-abordagem-gqm-q-e-m) e [métricas GQM](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#32-definicao-das-questoes-e-metricas-abordagem-gqm-q-e-m)) em um roteiro prático, contemplando:

- Métodos de coleta de dados
- Critérios de julgamento
- Recursos necessários
- Cronograma de execução

A elaboração segue as diretrizes da **ISO/IEC 25040**, garantindo que a avaliação seja rastreável, repetível e reprodutível, permitindo que os resultados obtidos sejam confiáveis e suportem decisões de melhoria contínua no sistema.

Esta fase garante que:

- Cada métrica esteja diretamente vinculada a uma meta de avaliação, evitando medições sem valor prático.
- Os métodos de análise permitam identificar lacunas

## 2. Objetivos da Avaliação

1. Avaliar o grau de correspondência entre as funcionalidades implementadas e as necessidades dos usuários ([Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)) .

2. Verificar a confiabilidade operacional do aplicativo, considerando falhas relatadas, estabilidade e comportamento sob condições normais de uso ([Confiabilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)).

## 3. Metodologia de Avaliação

A avaliação será conduzida de acordo com as cinco etapas do processo de avaliação da ISO/IEC 25040, que servem como referência metodológica:

- Estabelecimento dos requisitos de avaliação (já realizado na [Fase 1](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/));

- Especificação da avaliação (modelo GQM definido na [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/));

- Projetar a avaliação (fase atual);

- Executar a avaliação (coleta e mensuração prática dos dados);

- Concluir a avaliação (interpretação e julgamento dos resultados).

Nesta fase, são detalhados os procedimentos de coleta e análise para cada métrica GQM ([M1 a M6](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#32-definicao-das-questoes-e-metricas-abordagem-gqm-q-e-m)), bem como a estrutura operacional necessária para realizar a avaliação com consistência.

## 4. Planejamento das Métricas e Métodos de Coleta

As métricas a seguir derivam diretamente da [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/) e estão agrupadas conforme as duas características de qualidade priorizadas.

### **4.1. Adequação Funcional**

| **Métrica**                                                                                                                                               | **Descrição / Finalidade**                                                                         | **Método de Coleta**                                                                                                     | **Fonte de Dados**                                                                                                                                                                                                                                            | **Frequência / Amostragem**             | **Critério de Julgamento (da Fase 2)**                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- | ---------------------------------------------------------------- |
| **[M1 — Cobertura de Requisitos Críticos por Módulo](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**              | Mede a completude funcional, verificando se os módulos do SouGov atendem aos requisitos esperados. | Análise de rastreabilidade entre requisitos documentados e funcionalidades implementadas.                                | Documentação, lista de requisitos, base de chamados de suporte (“Funcionalidade Ausente”).                                                                                                                                                                    | Análise pontual sobre versão 5.573.     | ≥ 95% Excelente; 80–94% Bom; 60–79% Regular; < 60% Insuficiente. |
| **[M2 — Taxa de Inconformidade Funcional (TIF)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**               | Mede a correção funcional dos resultados (ex.: cálculo de contracheque, férias).                   | Análises de comentários de usuários relatando divergências (“meu valor no SouGov está diferente do Portal do Servidor”). | registros de chamados (“Cálculo Incorreto”) Comentários e avaliações nas App Stores. A partir de feedback de usuário fazer comparativos entre dados do SOUGOV e relatórios públicos (como o [Portal da Transparência](https://portaldatransparencia.gov.br/) ) | Avaliação sobre amostra representativa. | ≤ 5% Excelente; 6–15% Bom; 16–25% Regular; > 25% Insuficiente.   |
| **[M3 — Taxa de Sucesso na Conclusão de Tarefas Críticas (TSCTC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)** | Mede se os usuários conseguem completar tarefas essenciais (ex.: Prova de Vida Digital).           | Análise de comportamento do usuário + coleta de feedbacks.                                                               | Comentários e avaliações nas App Stores, telemetria de eventos de uso.                                                                                                                                                                                        | Coleta contínua durante 3 a 5 dias.    | ≥ 90% Excelente; 70–89% Bom; 50–69% Regular; < 50% Insuficiente. |

### **4.2. Confiabilidade**

| **Métrica**                                                                                                                                       | **Descrição / Finalidade**                                                                                | **Método de Coleta**                                                                                                                                                                                                                                                                                                                    | **Fonte de Dados**                                      | **Frequência / Amostragem**                            | **Critério de Julgamento (da Fase 2)**                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------- |
| **[M4 — Tempo Médio Entre Falhas (TMEF) / Disponibilidade (%)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)** | Mede a estabilidade operacional e o tempo médio de funcionamento do SouGov sem interrupções perceptíveis. | O avaliador realizará **sessões de uso simuladas** (mín. 30 min), em três dias distintos da semana,<br>simulando operações como **login**, **consulta de contracheque** e **atualização cadastral**.<br>Durante as sessões, serão anotadas falhas ou travamentos.<br>O cálculo da disponibilidade será feito com base nesses registros. | Sessões de uso simuladas                                | Coleta durante 3 a 5 dias                              | ≥ 99% Excelente; 95–98% Bom; 85–94% Regular; < 85% Insuficiente |
| **[M5 — Tempo Médio para Reparo/Recuperação (TMPR)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)**            | Mede o tempo necessário para o sistema se recuperar de falhas críticas relatadas por usuários.            | Análise de **20 comentários recentes** nas lojas (App Store e Play Store) que mencionem falhas funcionais.<br>Para cada relato, verifica-se se o problema foi **corrigido em versões posteriores**, com base nas notas oficiais.<br>O tempo entre o relato e a correção é usado para estimar o TMPR.                                    | Comentários de usuários e notas de atualização          | Avaliação do trimestre                                 | ≤ 1h Excelente; 1–3h Bom; 3–6h Regular; > 6h Insuficiente       |
| **[M6 — Frequência de Falhas Operacionais (FFO)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)**               | Mede a incidência de falhas percebidas pelos usuários e observadas durante o uso prático.                 | Coleta baseada em duas fontes:<br>(1) Comentários e avaliações das lojas, contabilizando menções de falhas.<br>(2) **Observação direta** das sessões realizadas para a métrica M4.<br>A proporção de interações que geraram falhas é convertida em percentual.                                                                          | Comentários das lojas e registros das sessões simuladas | Avaliações dos últimos 3 meses + observação por 3 dias | ≤ 2% Excelente; 3–5% Bom; 6–10% Regular; > 10% Insuficiente     |


## 5. Especificação dos Recursos

Os seguintes recursos são necessários para a execução completa e controlada do Plano de Avaliação:

### 5.1 Recursos Humanos

| Membro               | Responsabilidades                                |
| -------------------- | ------------------------------------------------ |
| Avaliadores (Equipe) | Execução dos testes, coleta e registro de dados. |

### 5.2 Materiais de Apoio e Ferramentas Técnicas

| Recurso                      | Função na Avaliação                                                               |
| ---------------------------- | --------------------------------------------------------------------------------- |
| Software Objeto de Avaliação | Aplicação SOUGOV (versão MOBILE).                                                 |
| Navegadores                  | Google Chrome e Firefox (ambientes de teste).                                     |
| Ferramentas de Software      | Ferramentas do Desenvolvedor (DevTools) e ferramentas de coleta e análise(5.2.1). |
| Registro                     | Planilha Eletrônica (Excel) para coleta de dados estraídos dos feedbacks.         |
| Documentação                 | Critérios de Avaliação Fase 2.                                                    |

#### 5.2.1 Ferramentas de coleta e análise em avaliação para uso

A equipe está atualmente analisando 3 ferramentas de coleta e análise de comentários nas lojas de sistema mobile mais comuns(google play store(android) e app store(apple)), de modo a determinar quais os prós e os contras de cada uma e qual será a melhor opção a ser utilizada, podendo ser definida apenas uma ferramenta como suficiente para o objetivo ou as 3 como complementares, a seguir trazemos uma análise inicial sobre cada uma das três selecionadas, respectivamente: [appbot](https://appbot.co), [appfollow](https://appfollow.io) e [iramuteq](https://sourceforge.net/projects/iramuteq/) ou [IRaMuTeQ](https://pratinaud.gitpages.huma-num.fr/iramuteq-website/), o segundo sendo a página oficial do desenvolvedor da aplicação, Pierre Ratinaud, porém escrito em francês, mas o google fornece tradução para a página.

##### 5.2.1.1 appbot

Em boa parte dos ranqueamentos de softwares empresariais, o appbot apareceu, sendo uma ferramenta útil para estar sendo utilizada por ter as funcionalidades que precisaremos utilizar, sendo elas análise de sentimentos e análise textual, a primeira seria feita para termos uma noção de como os usuários do SouGov se sentem ao utilizar o mesmo e o que falam sobre ao deixar avaliações nas lojas em que baixaram o mesmo, a segunda seria para termos uma noção de quais tópicos são os mais comentados sobre nas avaliações para trazer na coleta de dados e aplicação o que foi mais comentado que pode ser usado em conjunto com as métricas definidas.

Porém, o appbot é uma ferramenta **paga**, o que dificulta a avaliação continua dos comentários.

##### 5.2.1.2 appfollow

Também é uma das ferramentas que mais apareceram em ranqueamento para o que queríamos, realizando funções parelhas ao do appbot, porém trazendo também o feedback sobre aplicativos concorrentes, essa funcionalidade não possui utilidade para o grupo, pois o SouGov é disponibilizado pelo governo. A sua maior vantagem em relação ao appbot é possuir uma inscrição gratuita, garantindo uma reprodutibilidade da análise de forma mais coerente sem precisar se preocupar com conseguir uma conta de teste sempre que for refazer a avaliação de qualidade.

##### 5.2.1.3 iramuteq

O iramuteq é uma ferramenta(software) de análise de textos que utiliza o ambiente estatístico do software R e a linguagem python, viabilizando a análise de dados textuais que os comentários possuem, utilizando-se de diversos tipos de análises para cobrir o que vamos utilizar, podendo trazer um agrupamento de palavras que aparecem com maior frequência, palavras que aparecem juntas, dentre outras coisas que podem nos dar uma boa noção de quais são os principais pontos discutidos sobre o SouGov.

No entanto, o iramuteq não possui uma forma de fazer a análise de sentimento até onde observamos nas fontes que selecionamos para tentar entender o seu nicho de uso, sendo eles [IRAMUTEQ: um software gratuito para análise de dados textuais](https://pepsic.bvsalud.org/scielo.php?script=sci_arttext&pid=S1413-389X2013000200016), um artigo curto contando sobre o uso dele em alguns países e do início de sua utilização no Brasil, trazendo uma visão da utilidade do mesmo, as outras fontes foram a maioria em videos explicando o uso da ferramenta, portanto precisaremos de utilizar outra ferramenta para a análise de sentimento, podendo ser uma das citadas antes do IRAMUTEQ ou outra que o grupo venha a encontrar.


## 6. Cronograma de Ações

| **Métrica**                                   | **Atividades Resumidas**                                                                                 | **Responsável(is)**                       | **Período** |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------------------------- | ----------- |
| **[M1 – Cobertura de Requisitos Críticos por Módulo](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#31-adequacao-funcional)** | Levantamento de requisitos, rastreabilidade, análise de chamados, consolidação dos resultados            | **Laryssa, Matheus, Ana Beatriz**  | Dia 1-2 (Semana 1)       |
| **[M2 – TIF (Inconformidade Funcional)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#31-adequacao-funcional)**       | Coleta de comentários, análise de chamados, comparação com Portal da Transparência, cálculo final do TIF | **Giovana, Carlos, Matheus, Laryssa**     | Dia 1-2 (Semana 1)       |
| **[M3 – TSCTC (Sucesso nas Tarefas Críticas)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#31-adequacao-funcional)** | Coleta de avaliações, análise de comportamento, acompanhamento de tentativas, cálculo da taxa de sucesso | **Ana Beatriz, Giovana, Carlos, Laryssa** | 3 a 5 dias (Semana 1)      |
| **[M4 – TMEF / Disponibilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#32-confiabilidade)**               | 3 sessões de testes (dias diferentes) e consolidação dos dados                                           | **Matheus, Ana Beatriz, Carlos, Laryssa** | 3 dias distintos (Semana 1)       |
| **[M5 – TMPR (Tempo para Reparo)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#32-confiabilidade)**             | Coleta de relatos de falhas, análise de notas de atualização, cálculo do TMPR                            | **Giovana, Matheus, Laryssa**             | 3 dias (Semana 1)        |
| **[M6 – FFO (Frequência de Falhas)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#32-confiabilidade)**           | Coleta de avaliações, contagem de falhas, integração com sessões do M4, cálculo do FFO                   | **Ana Beatriz, Carlos, Giovana**          | Dia 1-2 (Semana 1)       |
| **Análise e Relatório**                       | Aplicação das pontuações GQM e redação do relatório final da Fase 3.	                                   |**Todos** |	Dia 1-2 (Semana 2) 

## 7. Garantia de Rastreabilidade e Reprodutibilidade

Para garantir a rastreabilidade e a reprodutibilidade dos resultados, cada métrica será acompanhada de um registro de medição padronizado, contendo:

- Data e versão do aplicativo analisado;

- Fonte de coleta (App Store, logs, documentação etc.);

- Método e ferramenta utilizada;

- Resultado numérico(quantitativo);

- Classificação segundo o critério de julgamento definido na [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/).

Esses registros servirão como evidência para auditoria e validação dos resultados.

## Bibliografia

> Ministério da Gestão e da Inovação em Serviços Públicos (MGI). _SouGov – Aplicativo oficial de serviços do servidor público federal_. Disponível em: <https://www.gov.br/servidor/pt-br/sou-gov>. Acesso em: 27 setembro 2025.

> Governo Federal. _Plataforma Gov.br – Serviços digitais para o cidadão_. Disponível em: <https://www.gov.br>. Acesso em: 27 setembro 2025.

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data       | Descrição                                           | Autor(a)                                                           |
| ------ | ---------- | --------------------------------------------------- | ------------------------------------------------------------------ |
| 1.0    | 10/11/2025 | Conteúdo da fase 3                                  | [Laryssa Felix](https://github.com/felixlaryssa)                   |
| 2.0    | 16/11/2025 | Adição de análise inicial das ferramentas de coleta | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita) |
| 2.1    | 16/11/2025 | Ajuste para deploy pages | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh) |
| 3.0    | 18/11/2025 | Ajustes no Alinhamento com a fase 2                 | [Laryssa Felix](https://github.com/felixlaryssa)                   |