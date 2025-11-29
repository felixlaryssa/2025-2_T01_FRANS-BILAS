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

| **Métrica** | **Descrição / Finalidade** | **Método de Coleta** | **Fonte de Dados** | **Frequência / Amostragem** | **Critério de Julgamento (da Fase 2)** |
|------------|-----------------------------|------------------------|---------------------|------------------------------|-----------------------------------------|
| **[M1 — Frequência de Lacunas Funcionais (FLF)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)** | Avalia a frequência com que funcionalidades esperadas estão ausentes ou incompletas em um sistema. | Contagem de N-grams em reviews neutros/negativos com termos de ausência (ex:“falta”, “não tem”, “precisava”).Para calcular a porcentagem, somamos o número de ocorrências dos dois N-Grams identificados e dividimos pelo total de citações.  | Reviews neutros e negativos contendo N-grams de ausência.( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.) | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≤ 5% / Bom: 6–15% / Regular: 16–25% / Insuficiente: > 25% |
| **[M2 — Proporção de Relatos de Incorreção (PRI)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)** | Avalia a correção funcional dos resultados do aplicativo (ex.: cálculo de contracheque, férias).A presença recorrente desses termos sugere que pode haver falhas no fluxo dessas funcionalidades. | Mapeamento via PLN e filtragem de N-grams que relatem incorreção funcional (“cálculo errado”, “valor diferente”).Para calcular a PRI, utilizamos o valor estimado dos dois termos que podem indicar incorreção funcional e dividimos pela quantidade de avaliações negativas que o aplicativo recebeu durante o período que as informações foram coletadas. Com a seguinte fórmula: PRI = (Total de ocorrências dos N-Grams indicativos) / (Total de avaliações negativas)  |  N-Grams presentes nos comentários neutros e negativos dos usuários, buscando termos que indiquem possíveis problemas na execução das funcionalidades.( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.)  | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≤ 5% / Bom: 6–15% / Regular: 16–25% / Insuficiente: > 25% |
| **[M3 — Índice de Fricção na Tarefa Crítica (IFTC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)** |  Indica a taxa de sucesso percebida pelo usuário em relação à realização de tarefas críticas no aplicativo. Quanto menor o índice, melhor a experiência do usuário. (ex.: Prova de Vida Digital). | Análise de N-grams de fricção (“não consigo finalizar”, “caminho confuso”, “tela sumiu”).Todos esses termos estão relacionados à tarefa crítica de acessar o aplicativo, essencial para a realização de qualquer outra funcionalidade dependente do SouGov. Calculo: Soma dos N-grams levados em consideração na métrica dividido pelo total de N-grams | Comentários e avaliações nas App Stores.( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.)  | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≤ 10% / Bom: 11–30% / Regular: 31–50% / Insuficiente: > 50% |


??? "Significado de N-Grams"
    N-Grams: Identifica as frases e termos mais frequentes (N-grams) em comentários
    positivos e negativos, após a remoção de espaço vazio e frases irrelevantes. Isso
    destaca o valor central percebido e os principais pontos de fricção.

### **4.2. Confiabilidade**

| **Métrica** | **Descrição / Finalidade** | **Método de Coleta** | **Fonte de Dados** | **Frequência / Amostragem** | **Critério de Julgamento (da Fase 2)** |
|------------|-----------------------------|------------------------|---------------------|------------------------------|-----------------------------------------|
| **[M4 — Frequência de Instabilidade Operacional (FIO)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)** | Avalia a estabilidade do sistema e a ocorrência de interrupções perceptíveis pelos usuários. | Mapeamento de Qualidade baseado em Processamento de Linguagem Natural (PLN), considerando termos indicativos de problemas, como:“travamentos”, “lentidão” e “instabilidade”. Cálculo pela fórmula: **FIO = (menções aos termos críticos) / (total de reviews)**. | Comentários de usuários que mencionem travamentos, lentidão ou instabilidade ( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.) | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≤ 2% / Bom: 3–5% / Regular: 6–10% / Insuficiente: > 10% |
| **[M5 — Índice de Recuperação Observável (IRO)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)** | Mede o tempo necessário para o sistema se recuperar de falhas críticas (TMPR). | Para isso, comparamos os relatos de falhas críticas identificadas nos N-Grams e reviews negativos com as informações de atualização do aplicativo na App Store do SouGov.br.O cálculo será feito a partir da estimativa de soma dos N-Grams para termos e reviews críticos e dividir esse valor pela soma das quantidades de avaliações 4 e 5 na App Store do Android, o resultado que der reduzimos de 1(correspondente a 100%), e esse resultado será o valor obtido para classificar a métrica: IRO = 1 - (Estimativa de N-Grams de termos e reviews críticos) / (Total de avaliações positivas, notas 4 e 5) | Comentários nas lojas de aplicativos e página oficial do aplicativo ( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.) | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≥ 80% / Bom: 60–79% / Regular: 40–59% / Insuficiente: < 40% |
| **[M6 — Densidade de Relatos de Bugs Críticos (DRBC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#323-confiabilidade)** | Mede a incidência de falhas percebidas pelos usuários (ex.: crash, erro de servidor). | Mapeamento de Qualidade (PLN) de termos como “bug”, “erro” e contagem da proporção de menções críticas no total de reviews. Fórmula: Densidade de Bugs Críticos = (Número de menções a Bugs/Erros) / (Total de reviews críticos) | Comentários nas lojas de aplicativos.( Ferramenta de análise utiliza as informações gerais do aplicativo e as avaliações publicadas em 2025.) | Comentários e avaliações de 2025 (01/01/2025 a 17/11/2025). | Excelente: ≤ 2% / Bom: 3–5% / Regular: 6–10% / Insuficiente: > 10% |


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
| **Coleta das Reviews**                            | Extração de reviews das lojas, limpeza dos dados, unificação das bases               | **Matheus, Laryssa, Giovana**              | Dia 1 Semana 1    |
| **Processamento NLP – Polaridade**                | Aplicação de análise de sentimento, cálculos de polaridade, identificação de padrões | **Matheus, Laryssa**              | Dia 2 Semana 1    |
| **Geração de N-grams (Unigram, Bigram, Trigram)** | Tokenização, remoção de stopwords, geração e validação dos N-grams                   | **Matheus,Ana Beatriz, Carlos**           | Dia 3 Semana 1    |
| **Identificação de Termos Críticos**              | Seleção de termos negativos, análise de frequência e relevância                      | **Matheus,Carlos, Giovana**               | Dia 3-4 Semana 1  |
| **Mapa de Calor de Sentimentos**                  | Cruzamento de emoções com funcionalidades, agrupamento por tópicos                   | **Matheus, Laryssa, Ana Beatriz**          | Dia 4 Semana 1    |
| **Análise de Correlação com Falhas**              | Relação entre reviews negativas e eventos de falha (camera, login, biometria etc.)   | **Matheus, Carlos**               | Dia 5 Semana 1    |
| **Síntese das Métricas Derivadas**                | Interpretação dos resultados (polaridade, termos críticos, N-grams)                  | **Matheus, Laryssa, Giovana, Ana Beatriz** | Dia 1 Semana 2    |
| **Redação da Conclusão Analítica**                | Construção das conclusões gerais a partir das evidências                             | **Todos**                       | Dia 2 Semana 2    |
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

## Tabela de Contribuição - Grupo Frans Bilas

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 4: Contribuições dos Membros do Grupo
</div>

| Matrícula | Nome do aluno | Atividade Realizada | % de Contribuição |
| --------- | ------------- | ------------------- | ----------------- |
| 200060783 | Ana Beatriz W. Massuh | Análise e Pesquisa | 20% |
| 190085584 | Carlos Eduardo Mendes |  Análise e Pesquisa | 20% |
| 231034707 | Giovana Ferreira Santos | Análise e Pesquisa | 20% |
| 231026840 | Laryssa Felix |  Análise e Pesquisa  | 20% |
| 202070064 | Matheus do Vale | Pesquisa e criação da ferramenta | 20% |

---------------------

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
| 4.0    | 19/11/2025  | Adição da explicação sobre a ferramenta escolhida(inicial) | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
| 5.0    | 23/11/2025  | Correções                                                  | [Laryssa Felix](https://github.com/felixlaryssa)                       |
