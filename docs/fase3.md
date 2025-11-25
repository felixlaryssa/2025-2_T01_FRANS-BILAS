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

| **Métrica**                                                                                                                                                | **Descrição / Finalidade**                                                                          | **Método de Coleta**                                                                                                      | **Fonte de Dados**                                                                                                                                                                                                                                             | **Frequência / Amostragem**              | **Critério de Julgamento (da Fase 2)**                            |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ----------------------------------------------------------------- |
| **[M1 — Frequência de Lacunas Funcionais (FLF)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**               | Mede a completude funcional, identificando requisitos ausentes.  | Análise de rastreabilidade entre requisitos documentados e funcionalidades implementadas.                                 | Contagem de N-grams em reviews Neutros/Negativos que contenham termos de ausência ("falta", "não tem", "precisava"). | Comentários e avaliações de 2025     | Excelente: ≤ 5% / Bom: 6-15% / Regular: 16-25% / Insuficiente: > 25%  |
| **[M2 — Proporção de Relatos de Incorreção (PRI)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**                    | Mede a correção funcional dos resultados (ex.: cálculo de contracheque, férias).                    | Mapeamento de Qualidade (PLN) e filtragem de N-Grams que relatem incorreção funcional ("cálculo errado", "valor diferente")  | Comentários e avaliações de 2025   | Avaliação sobre amostra representativa do ano de 2025 | Excelente: PRI ≤ 5% / Bom: 6-15% / Regular: 16-25% / Insuficiente: > 25%    |
| **[M3 — Índice de Fricção na Tarefa Crítica (IFTC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**  | Mede a usabilidade e a taxa de sucesso percebida pelo usuário em tarefas críticas (ex.: Prova de Vida Digital).            | Análise de N-grams de Fricção ("não consigo finalizar", "caminho confuso", "tela sumiu").                                                              | Comentários e avaliações nas App Stores                                                                                                                                                                                         | Comentários e avaliações de 2025       | Excelente: PRI ≤ 5% / Bom: 6-15% / Regular: 16-25% / Insuficiente: > 25%  |

### **4.2. Confiabilidade**

| **Métrica**                                                                                                                                        | **Descrição / Finalidade**                                                                                 | **Método de Coleta**                                                                                                                                                                                                                                                                                                                                                                                                 | **Fonte de Dados**                                                                  | **Frequência / Amostragem**                                                                                                      | **Critério de Julgamento (da Fase 2)**                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **[M4 — Frequência de Instabilidade Operacional (FIO)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)**  | Mede a estabilidade operacional e o tempo médio de funcionamento do SouGov sem interrupções perceptíveis.  | Mapeamento de Qualidade (PLN) em termos de "Travamentos", "Lentidão" e "Instabilidade". Utiliza a Frequência de menções em relação ao total de reviews. | Comentários de usuários e Notas de Atualização (publicadas).  | Comentários e avaliações de 2025    | Excelente: ≤ 2% / Bom: 3-5% / Regular: 6-10% / Insuficiente: < 10%|
| **[M5 — Índice de Recuperação Observável (IRO)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)**             | Mede o tempo necessário para o sistema se recuperar de falhas críticas (TMPR)          | Análise de Correlação: Cruzamento da data de relatos de falha crítica (N-Grams/Mapeamento) com as Notas Oficiais de Atualização (Release Notes) | Avaliação do trimestre, considerando o histórico de versões lançadas.| Coleta das avaliações e comentáarios dos do ano de 2025                                                             |Excelente: IRO ≥ 80% / Bom: 60-79% / Regular: 40-59% / Insuficiente: < 40%     |
| **[M6 — Densidade de Relatos de Bugs Críticos (DRBC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)**                | Mede a incidência de falhas percebidas pelos usuários e observadas durante o uso prático do aplicativo. (crash, erro de servidor)   | Mapeamento de Qualidade (PLN) em "Bugs/Erros" e contagem da proporção de menções críticas no total de reviews.   | Comentários nas lojas de aplicativos    | Coleta das avaliações e comentáarios dos do ano de 2025                                            | Excelente: DRBC ≤ 2% / Bom: 3-5% / Regular: 6-10% / Insuficiente: DRBC > 10%    |

## 5. Especificação dos Recursos

Os seguintes recursos são necessários para a execução completa e controlada do Plano de Avaliação:

### 5.1 Recursos Humanos

| Membro                | Responsabilidades                                |
| --------------------- | ------------------------------------------------ |
| Avaliadores (Equipe)  | Execução dos testes, coleta e registro de dados. |

### 5.2 Materiais de Apoio e Ferramentas Técnicas

| Recurso                       | Função na Avaliação                                                                |
| ----------------------------- | ---------------------------------------------------------------------------------- |
| Software Objeto de Avaliação  | Aplicação SOUGOV (versão 5.573 MOBILE ANDROID ).                                                  |                                   |
|Ferramentas de Coleta (Scrapers) | Utilizadas para extrair os dados públicos de  (Play Store e Notas de Atualização.)  |
| Ferramentas de Análise PLN      | [Ferramenta de análise](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/)(5.2.2). Execução do Mapeamento de Qualidade, N-Grams e classificação de Sentimento.  |
| Registro                      | Planilha Eletrônica (Excel) para coleta de dados estraídos dos feedbacks.          |
| Documentação                  | Critérios de Avaliação Fase 2.                                                     |

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

#### 5.2.2 Ferramenta de coleta definida para uso

Com base nos problemas citados na sessão 5.2.1, o grupo optou por produzir uma ferramenta própria para a coleta de dados, onde conseguisse realizar tudo o que precisávamos sem depender de unir mais de um software ou pagar uma licença para uso da ferramenta. Mais infromações a respeito da ferramenta, estão na página  [Ferramenta de análise](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/).

## 6. Cronograma de Ações

| **Etapa / Métrica**                               | **Atividades Resumidas**                                                             | **Responsável(is)**               | **Período**       |
| ------------------------------------------------- | ------------------------------------------------------------------------------------ | --------------------------------- | ----------------- |
| **Coleta das Reviews**                            | Extração de reviews das lojas, limpeza dos dados, unificação das bases               | **Laryssa, Giovana**              | Dia 1 Semana 1    |
| **Processamento NLP – Polaridade**                | Aplicação de análise de sentimento, cálculos de polaridade, identificação de padrões | **Matheus, Laryssa**              | Dia 2 Semana 1    |
| **Geração de N-grams (Unigram, Bigram, Trigram)** | Tokenização, remoção de stopwords, geração e validação dos N-grams                   | **Ana Beatriz, Carlos**           | Dia 3 Semana 1    |
| **Identificação de Termos Críticos**              | Seleção de termos negativos, análise de frequência e relevância                      | **Carlos, Giovana**               | Dia 3-4 Semana 1  |
| **Mapa de Calor de Sentimentos**                  | Cruzamento de emoções com funcionalidades, agrupamento por tópicos                   | **Laryssa, Ana Beatriz**          | Dia 4 Semana 1    |
| **Análise de Correlação com Falhas**              | Relação entre reviews negativas e eventos de falha (camera, login, biometria etc.)   | **Matheus, Carlos**               | Dia 5 Semana 1    |
| **Síntese das Métricas Derivadas**                | Interpretação dos resultados (polaridade, termos críticos, N-grams)                  | **Laryssa, Giovana, Ana Beatriz** | Dia 1 Semana 2    |
| **Redação da Conclusão Analítica**                | Construção das conclusões gerais a partir das evidências                             | **Laryssa**                       | Dia 2 Semana 2    |
| **Consolidação do Relatório Final**               | Revisão, formatação e organização de todo o conteúdo analisado                       | **Todos**                         | Final da Semana 2 |


## 7. Garantia de Rastreabilidade e Reprodutibilidade

Para garantir a rastreabilidade e a reprodutibilidade dos resultados, cada métrica será acompanhada de um registro de medição padronizado, contendo:

- Versão do aplicativo analisado;

- Fonte de coleta (App Store, documentação etc.);

- Método e ferramenta utilizada;

- Resultado numérico(quantitativo);

- Classificação segundo o critério de julgamento definido na [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/).

Esses registros servirão como evidência para validação dos resultados.

## Bibliografia

> Ministério da Gestão e da Inovação em Serviços Públicos (MGI). _SouGov – Aplicativo oficial de serviços do servidor público federal_. Disponível em: <https://www.gov.br/servidor/pt-br/sou-gov>. Acesso em: 27 setembro 2025.

> Governo Federal. _Plataforma Gov.br – Serviços digitais para o cidadão_. Disponível em: <https://www.gov.br>. Acesso em: 27 setembro 2025.

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data        | Descrição                                                  | Autor(a)                                                               |
| ------ | ----------- | ---------------------------------------------------------- | ---------------------------------------------------------------------- |
| 1.0    | 10/11/2025  | Conteúdo da fase 3                                         | [Laryssa Felix](https://github.com/felixlaryssa)                       |
| 2.0    | 16/11/2025  | Adição de análise inicial das ferramentas de coleta        | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)     |
| 2.1    | 16/11/2025  | Ajuste para deploy pages                                   | [Ana Beatriz Massuh](https://github.com/AnaBeatrizMassuh)              |
| 3.0    | 18/11/2025  | Ajustes no Alinhamento com a fase 2                        | [Laryssa Felix](https://github.com/felixlaryssa)                       |
| 4.0    | 19/11/2025  | Adição da explicação sobre a ferramenta escolhida(inicial) | [Carlos Eduardo](<(https://github.com/CarlosEduardoMendesdeMesquita)>) |
| 5.0    | 23/11/2025  | Correções                       | [Laryssa Felix](https://github.com/felixlaryssa)                       |
