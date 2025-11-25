# Fase 4 - Análise dos dados coletados

## 1 - Introdução

A **Fase 4** detalha, de forma completa e rastreável, como foi realizada a coleta de dados para as características de qualidade selecionadas:  

- [**Adequação Funcional**](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)  
- [**Confiabilidade**](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)  

A coleta de dados foi feita utilizando uma ferramenta própria, explicada na página: [Ferramenta de Análise](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/) e contextualizada na [Fase 3](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/), sessão 5.2.2. O objetivo central da ferramenta é realizar uma coleta direcionada de dados do aplicativo **sougov** na loja brasileira (Play Store, Brasil), focando em dois conjuntos
de dados: as informações gerais do aplicativo e todas as avaliações publicadas durante o
ano de 2025.

Durante a análise, foram realizados os seguintes procedimentos:

- Criação de **gráficos** e **dashboards**.  
- Identificação dos **termos mais utilizados**, tanto de forma positiva quanto negativa.  
- Avaliação da **distribuição de estrelas** na loja de aplicativos do Google.  
- Análise de **sentimentos** aplicada aos dados coletados pela ferramenta.  

Para esta análise, foram processados **3.361 reviews** do aplicativo **SouGov.br**, abrangendo o período de **01/01/2025 a 17/11/2025**.


<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 1: Resumo dos Resultados da Ferramenta de Análise
</div>

<div style="text-align: center;">
  <img src="../assets/images/resumo_coleta.png" alt="Resumo Coleta" style="max-width: 100%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

??? info "Interpretação Geral dos Resultados da Ferramenta de Análise"

    - **A nota média de 4.40** indica uma alta percepção de qualidade na experiência geral dos usuários.
    - **Com 68.1% de reviews positivos**(4-5 estrelas), observa-se que a maior parte do público avalia bem o aplicativo.
    - **Os 22% de avaliações negativas**(1-2 estrelas) representam um volume considerável e merecem análise mais aprofundada, especialmente para as características de qualidade estudadas (**Adequação Funcional** e **Confiabilidade**).
    - **A taxa de reviews neutros (9.8%)**(3 estrelas) é típica e reflete usuários que nem elogiam nem criticam fortemente, mas oferecem oportunidades de melhoria.

<details>
  <summary>Versão SouGov Mobile (Android)</summary>
  Versão 5.573 — Versão mobile utilizada ao longo desta avaliação. O sistema operacional avaliado foi o Android.
</details>

## 2 - Análise Generalista da Fonte de dados
Análise de Sentimento e Qualidade do aplicativo SouGov.br, focando nos dados de
*reviews* e experiência do usuário extraídos dos comentários e avaliações.

### 2.1 - Distribuição de Notas de Avaliação e Evolução Mensal

<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 2: Notas das avaliações na App Store do Android
</div>

<div style="text-align: center;">
  <img src="../assets/images/grafico_avaliacoes.png" alt="grafico_avaliacoes" style="max-width: 60%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

??? "Distribuição de Notas de Avaliação"

    O gráfico apresenta a quantidade de avaliações para cada nota atribuída pelos usuários ao aplicativo. A distribuição é desigual, mostrando uma forte concentração nas extremidades, especialmente na nota máxima.
    Resumo das Quantidades por Nota

    - **1 estrela:** 331 avaliações  
    - **2 estrelas:** 68 avaliações  
    - **3 estrelas:** 85 avaliações  
    - **4 estrelas:** 331 avaliações  
    - **5 estrelas:** 2.546 avaliações

<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 3: Evolução Mensal da Quantidade de Comentários
</div>

<div style="text-align: center;">
  <img src="../assets/images/evolucao.png" alt="grafico_avaliacoes" style="max-width: 60%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

??? Evolução Mensal da Quantidade de Comentários

    - **Jan/25 → 286 comentários:** início do ano com volume moderado.
    - **Fev/25 → 202 comentários:** queda no engajamento.
    - **Mar/25 → 329 comentários:** aumento expressivo no volume de avaliações.
    - **Abr/25 → 744 comentários:** **pico absoluto do período**, indicando um evento significativo.
    - **Mai/25 → 492 comentários:** queda após o pico, mas ainda acima da média.
    - **Jun/25 → 338 comentários:** continuidade da tendência de queda.
    - **Jul/25 → 318 comentários:** estabilização próxima ao padrão.
    - **Ago/25 → 200 comentários:** queda mais acentuada.
    - **Set/25 → 150 comentários:** um dos menores volumes registrados.
    - **Out/25 → 191 comentários:** leve aumento.
    - **Nov/25 → 118 comentários:** menor valor do ano, indicando baixo engajamento.

    ### Interpretação Geral

    A evolução mensal revela um comportamento bastante oscilante, com destaque para:

    - **Um grande pico em abril (744 comentários)**, destoando dos demais meses.  
    - **Tendência geral de queda no segundo semestre.**  
    - **Últimos meses com volumes significativamente baixos**, sugerindo redução no engajamento ou diminuição de situações que motivam avaliações.



### 2.2 Sentimento Global (PLN)

<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 4: Análise de Sentimento Global (PLN)
</div>

<div style="text-align: center;">
  <img src="../assets/images/sentimento.png" alt="entimento" style="max-width: 60%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

??? "Análise de Sentimento Global (PLN)"

    - **A nota média de 4.40 estrelas** (sendo 5.0 o valor máximo)
    - **Com 68.1% de reviews positivos**(4-5 estrelas), 
    - **22% de avaliações negativas**(1-2 estrelas) 
    - **A taxa de reviews neutros (9.8%)**(3 estrelas) 

## 3 - Análise dos dados coletados para a característica Adequação Funcional

Esta seção tem como objetivo analisar os dados coletados referentes às subcaracterísticas de [Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#71-adequacao-funcional), no contexto da qualidade do sistema. Serão avaliadas as [métricas](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/#41-adequacao-funcional) definidas para validação nas fases: [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/), [Fase 3](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/), destacando:

- Pontos em que houve falhas;

- Pontos em que se obteve sucesso;

- Pontos com resultado neutro.

Além disso, serão apresentados os dados coletados pela ferramenta, incluindo: fotos dos gráficos e dashboards gerados e os termos mais utilizados pelos usuários.

### 3.1 - M1 Frequência de Lacunas Funcionais (FLF)

A ferramenta classificou os N-Grams das avaliações **neutras** (nota 3) e **negativas** (notas 1 e 2).  
Para analisar essas métricas, é necessário identificar termos que expressem carência ou insatisfação, como *“falta”*, *“não tem”* e *“precisava”*. A M1 – Frequência de Lacunas Funcionais (FLF) é uma métrica de adequação funcional que avalia a frequência com que funcionalidades esperadas estão ausentes ou incompletas em um sistema.

Ao observar a tabela gerada, podemos verificar esses padrões:
<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 5: N-Grams dos reviews neutros e negativos
</div>

<div style="text-align: center;">
  <img src="../assets/images/ngrams_neutro_negativo.png" alt="ngrams_neutro_negativo" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

Das frases presentes na **Figura 5**, identificamos os N-Grams *“não funcionando”* e *“não tenho”* como representativos desta métrica.  

??? "O **critério de avaliação da Frequência de Lacunas Funcionais (FLF)** é baseado em porcentagem:"  

    - **Excelente (0% a 5%)**  
      Indica que o sistema possui muito poucas ou quase nenhuma lacuna funcional. A maioria das funcionalidades esperadas está presente e funcionando corretamente. O impacto na experiência do usuário ou na operação do sistema é mínimo ou nulo.
    - **Bom (6% a 15%)**  
      Significa que existem algumas lacunas funcionais, mas elas são relativamente poucas. O sistema ainda atende bem aos objetivos, embora algumas funcionalidades esperadas possam estar ausentes ou incompletas. O impacto é perceptível, mas não crítico.
    - **Regular (16% a 25%)**  
      Indica que há uma quantidade significativa de lacunas funcionais. Um número considerável de funcionalidades esperadas está ausente ou incompleto, o que pode afetar a eficiência do usuário e comprometer parte das operações do sistema.
    - **Insuficiente (> 25%)**  
      Mostra que mais de um quarto das funcionalidades esperadas estão faltando ou incompletas. O sistema apresenta sérias deficiências funcionais, comprometendo sua utilidade e dificultando o cumprimento dos objetivos para os quais foi projetado.

Para calcular a porcentagem, somamos o número de ocorrências dos dois N-Grams identificados e dividimos pelo total de citações. Como o gráfico não apresenta valores exatos, utilizamos uma estimativa:  

- **Quantidade total de N-Grams (estimativa)**: ~460  
- **Quantidade de N-Grams para a métrica (estimativa)**: ~30  


#### Resultado da Análise :
O cálculo aproximado resulta em **6,52%**, classificando a métrica como **Bom**, considerando uma margem de erro estimada de ±3%. Significa que existem algumas lacunas funcionais, mas elas são relativamente poucas. O sistema ainda atende bem aos objetivos, embora algumas funcionalidades esperadas possam estar ausentes ou incompletas. O impacto é perceptível, mas não crítico.


??? info "Significado de N-Grams"
    N-Grams: Identifica as frases e termos mais frequentes (N-grams) em comentários
    positivos e negativos, após a remoção de espaço vazio e frases irrelevantes. Isso
    destaca o valor central percebido e os principais pontos de fricção.

### 3.2 - Proporção de Relatos de Incorreção (PRI)

A **Proporção de Relatos de Incorreção (PRI)** é uma métrica que busca avaliar a **correção funcional** dos resultados do aplicativo. Para isso, analisamos os **N-Grams** presentes nos comentários neutros e negativos dos usuários, buscando termos que indiquem possíveis problemas na execução das funcionalidades.

No gráfico da Figura 6, podemos observar os N-Grams mais frequentes:


<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 6: N-Grams dos reviews neutros e negativos
</div>

<div style="text-align: center;">
  <img src="../assets/images/ngrams_neutro_negativo.png" alt="ngrams_neutro_negativo" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

No gráfico da figura 7, podemos observar o total de avaliações negativas (1 e 2 estrelas):
<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 7: Nota das avaliações na App Store do Android
</div>


<div style="text-align: center;">
  <img src="../assets/images/grafico_avaliacoes.png" alt="grafico_avaliacoes" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

Ao analisar os N-Grams, identificamos dois termos que podem indicar **incorreções funcionais**:

- **"prova vida"**  
- **"reconhecimento facial"**

A presença recorrente desses termos sugere que pode haver falhas no fluxo dessas funcionalidades.  

??? "Critérios de Julgamento da Proporção de Relatos de Incorreção (PRI)"

    A **Proporção de Relatos de Incorreção (PRI)** indica a frequência de relatos de problemas funcionais pelos usuários. Quanto menor a PRI, melhor é a percepção de correção funcional do aplicativo. Os critérios de julgamento são os seguintes:

    - **Excelente (≤ 5%)**: Indica que muito poucos usuários relataram problemas. O aplicativo apresenta alta confiabilidade e quase não há relatos de falhas nas funcionalidades.

    - **Bom (6% a 15%)**: Mostra que há alguns relatos de incorreções, mas ainda dentro de níveis aceitáveis. O aplicativo funciona bem na maior parte do tempo, com pequenas falhas pontuais.

    - **Regular (16% a 25%)**: Indica que uma quantidade significativa de usuários identificou problemas funcionais. É necessário revisar e corrigir as funcionalidades críticas para melhorar a experiência.

    - **Insuficiente (> 25%)**: Reflete que uma parte considerável dos usuários enfrenta falhas no aplicativo. Há problemas importantes que comprometem a confiabilidade e exigem ação corretiva imediata.

Para calcular a PRI, utilizamos o valor estimado dos dois termos e dividindo pela quantidade de avaliações negativas que o aplicativo recebeu durante o período que as informações foram coletadas. Com a seguinte fórmula:

PRI = (Total de ocorrências dos N-Grams indicativos) / (Total de avaliações negativas)
PRI = 120 / 399 ≈ 0,30 (30%) 

- **Total de avaliações negativas (1 e 2 estrelas):** 399  
- **Total estimado de N-Grams para "prova vida" e "reconhecimento facial":** 120  



#### Resultado da Análise : 

- Fazendo o cálculo \(120 / 399\), obtemos o valor de **0,30**, correspondente a **30%**.  

- Esse percentual indica que quase um terço das avaliações negativas mencionou problemas funcionais em funcionalidades críticas, como "prova vida" e "reconhecimento facial".  

- De acordo com os critérios de julgamento da **PRI**, esse valor se enquadra na classificação **Insuficiente**, evidenciando que há uma quantidade significativa de relatos de falhas. Isso aponta que o aplicativo apresenta problemas relevantes que impactam diretamente a experiência dos usuários.  

Em resumo, a métrica demonstra que funcionalidades essenciais não estão funcionando corretamente para uma parcela considerável dos usuários, sinalizando a necessidade de correções urgentes e melhorias no fluxo dessas funcionalidades.


### 3.3 - Índice de Fricção na Tarefa Crítica(IFTC)

O **Índice de Fricção na Tarefa Crítica (IFTC)** mede a **taxa de sucesso percebida pelo usuário** em relação à realização de tarefas críticas no aplicativo, com base nos feedbacks coletados. Para isso, analisamos os **N-Grams de fricção**, utilizando o mesmo gráfico da Figura 8.


<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 8: Nota das avaliações na App Store do Android
</div>

<div style="text-align: center;">
  <img src="../assets/images/ngrams_neutro_negativo.png" alt="grafico_avaliacoes" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

Ao analisarmos o gráfico em busca de **referências a tarefas críticas**, identificamos os N-Grams:

- "não funciona"  
- "não abre"  
- "não consigo acessar"  
- "não entra"  

Todos esses termos estão relacionados à **tarefa crítica de acessar o aplicativo**, essencial para a realização de qualquer outra funcionalidade dependente do SouGov.

??? "Critérios de Julgamento do  Índice de Fricção na Tarefa Crítica(IFTC)"
    O **Índice de Fricção na Tarefa Crítica (IFTC)** indica a taxa de sucesso percebida pelo usuário em relação à realização de tarefas críticas no aplicativo. Quanto menor o índice, melhor a experiência do usuário. Os critérios de julgamento são:

    - **Excelente (≤ 10%)**: Indica que praticamente todos os usuários conseguem realizar a tarefa crítica sem encontrar dificuldades significativas. A experiência de uso é fluida e confiável.

    - **Bom (11% a 30%)**: Mostra que uma parcela moderada de usuários relata algum nível de fricção, mas a maioria consegue concluir a tarefa com sucesso. Pequenas melhorias podem tornar a experiência ainda mais eficiente.

    - **Regular (31% a 50%)**: Indica que uma quantidade considerável de usuários enfrenta dificuldades ao realizar a tarefa crítica. É necessário investigar os pontos de fricção e implementar melhorias para reduzir barreiras e aumentar a taxa de sucesso.

    - **Insuficiente (> 50%)**: Reflete que mais da metade dos usuários encontra obstáculos ao tentar completar a tarefa crítica. Isso compromete a experiência geral do aplicativo, tornando urgente a correção de falhas e ajustes no fluxo da funcionalidade.

Para executar o cálculo, utilizaremos a estimativa da soma dos N-Grams destacados aqui e dividir pela quantidade total estimada de N-Grams:

- **Estimativa para total de N-Grams** - aproximadamente 460
- **Estimativa para a junção dos 4 N-Grams levados em consideração aqui** - aproximadamente 115
- Cálculo da porcentagem - junção/total = 115/460 = 0.25 = 25%

#### Resultado da Análise : 

- Com base nesse cálculo, **25% das menções indicam fricção** na execução da tarefa crítica.  

- Portanto, o **IFTC é classificado como "Bom"**, indicando que, embora exista algum nível de dificuldade relatada pelos usuários, a maioria consegue realizar a tarefa crítica de acessar o aplicativo sem grandes problemas.  

Em resumo, a métrica evidencia que a **experiência de acesso ao SouGov.br é satisfatória para a maior parte dos usuários**, mas ainda há espaço para melhorias em pontos críticos.

## 3 - Análise dos dados coletados para a característica de Confiabilidade

Essa sessão dedica-se a discutir o que os dados coletados para as subcaracterísticas de Confiabilidade no que diz respeito a qualidade evidenciam em relação às métricas definidas para validação nas fases [2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/) e [3](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase3/), mostrar onde falharam(se falharam), onde tiveram sucesso e onde o resultado foi neutro, adicionando o que a ferramenta conseguiu coletar por meio de fotos dos gráficos e dashboards produzidos, da análise de sentimentos e dos termos mais utilizados.

### 3.1 - Frequência de Instabilidade Operacional (FIO)

Essa métrica mede a estabilidade do sistema e interrupções perceptíveis, utilizando do Mapeamento de Qualidade (PLN) em relação a termos como "Travamentos", "Lentidão" e "Instabilidade", utilizando como cálculo a frequência de menções em relação ao total de reviews(menções/reviews).


<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 4: Nota das avaliações na App Store do Android
</div>

<div style="text-align: center;">
  <img src="../assets/images/mapa_termos.png" alt="grafico_avaliacoes" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

Os valores definidos para os Critérios de Julgamento são:

Excelente - menor ou igual a 2%
Bom - entre 3% e 5%
Regular - de 6% até 10%
Insuficiente - acima de 10%

Estimativa da frequência de aparição dos termos "Travamentos", "Lentidão" e "Instabilidade" - aproximadamente 105
Total de reviews analisadas, contando as positivas também - 3361
Cálculo - 105/3361 = 0,03 = 3%
Desta forma, essa métrica é classificada como Bom.

### 3.2 - Índice de Recuperação Observável (IRO)

Essa métrica tem como objetivo mensurar o tempo necessário para o sistema se recuperar de uma falha crítica, de forma que precisamos comparar os relatos de falha crítica com as notas oficiais de atualização, ao checar a página oficial do souGov.br na App Store, a última atualização só cita ter melhorado o controle de uso da câmera, mas não cita ter arrumado outros problemas que apareceram nos N-Grams ou nos relatos de falha crítica, portanto, para essa métrica utilizaremos a estimativa de N-Grams negativos referentes aos termos e aos reviews críticos e dividir pelo total de avaliações positivas recebidas pela ferramenta

<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 5: Nota das avaliações na App Store do Android
</div>

<div style="text-align: center;">
  <img src="../assets/images/grafico_avaliacoes.png" alt="grafico_avaliacoes" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>
<!-- ![Figura 4 - Mapeamento dos termos](../assets/images/mapa_termos.png)
![Figura 5 - Mapeamento dos reviews críticos](../assets/images/reviews_criticos.png) -->

Os Critérios de Julgamento são:
Excelente - maior ou igual a 80%
Bom - entre 60% e 79%
Regular - entre 40% e 59%
Insuficiente - menor que 40%

O cálculo será feito a partir da estimativa de soma dos N-Grams para termos e reviews críticos e dividir esse valor pela soma das quantidades de avaliações 4 e 5 na App Store do Android, o resultado que der reduzimos de 1(correspondente a 100%), e esse resultado será o valor obtido para classificar a métrica:
Estimativa da soma dos N-Grams de termos e de reviews críticos - aproximadamente 474
Soma avaliações 4 e 5: 2877
Cálculo final - 1 - (474/2877) = 1 - 0,16 = 0,84 = 84%

Desta forma, definimos que pelos Critérios de Julgamento, essa métrica se classifica como Excelente.

### 3.3 - Densidade de Relatos de Bugs Críticos

Essa métrica mede a incidência de falhas operacionais que impactam diretamente o usuário final(como crash e erro de servidor), seu cálculo é feito a partir do Mapeamento de Qualidade (PLN) em "Bugs/Erros" e a contagem de menções críticas no total de reviews.

<!-- <img src="../assets/images/mapa_termos.png" alt="Mapa Termos" style="max-width: 80%; height: auto;">

<img src="../assets/images/reviews_criticos.png" alt="Reviews_criticos" style="max-width: 80%; height: auto;"> -->

<div style="text-align: center; margin: 0; font-size: 16px;">
  Imagem 5: Nota das avaliações na App Store do Android
</div>

<div style="text-align: center;">
  <img src="../assets/images/reviews_criticos.png" alt="reviews_criticos" style="max-width: 80%; height: auto;">
</div>

<div style="text-align: center; margin: 0; font-size: 14px;">
  Fonte: <a href="https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/funcionamentodaferramenta/" target="_blank">Ferramenta Própria</a>
</div>

Os valores determinados para os Critérios de Julgamento dessa métrica são:
Excelente - menor ou igual a 2%
Bom - entre 3% e 5%
Regular - entre 6% e 10%
Insuficiente - acima de 10%

Estimativa para Bugs/Erros - aproximadamente 72
Estimativa reviews críticos - aproximadamente 300
Cálculo - 72/300 = 0,24 = 24%
Portanto, a classificação desta métrica é Insuficiente.

## Conclusão

Após a análise dos dados recolhidos pela ferramenta, foi possível ver que 1 das 6 métricas alcançou o nível Excelente e outras 3 das 6 métricas estabelecidas passaram classificadas como Bom pelos Critérios de Julgamento, portanto existem melhorias a serem feitas, e pelo levantamenton dos N-Grams, termos críticos e nota das reviews, é perceptível que o maior problema do souGov reside em funcionalidades que necessitem do uso da câmera dos celulares, o que é algo bem subjetivo e difícil de se analisar como resolver, pois é necessário levar em conta que uma boa parte dos usuários não vão ter uma qualidade de imagem alta com as câmeras dos seus aparelhos, outros podem não ter a coordenação motora para fazer o reconhecimento facial, dentre muitos outros problemas que precisam ser resolvidos.
Para finalizar, a equipe recomenda que no próximo ciclo de QA da aplicação os realizadores desse processo se atentem mais aos mapas, N-Grams, notas e reviews de forma mais aprofundada, assim garantindo que conseguirão sanar ao menos parte dos problemas que foram encontrados.

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data        | Descrição                                                               | Autor(a)                                                            |
| ------ | ----------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------- |
| 1.0    | 19/11/2025  | Versão inicial da fase 4                                                | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
| 1.1    | 19/11/2025  | Adição de etapas iniciais extras a fase 4                               | [Giovana Ferreira](https://github.com/gih7915)                      |
| 2.0    | 22/11/2025  | Versão intermediária da interpretação dos dados da fase 4(pendência m5) | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
| 3.0    | 23/11/2025  | Versão final da interpretação dos dados da fase 4     | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
| 4.0    | 24/11/2025 | Ajusta imagens, descrição e fonte | [Laryssa Felix](https://github.com/felixlaryssa)  |
| 5.0    | 24/11/2025 | Reorganização e adição de informações | [Laryssa Felix](https://github.com/felixlaryssa)  |