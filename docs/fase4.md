# Fase 4 - Análise dos dados coletados

## 1 - Introdução

A fase 4 detalha, de forma completa e rastreável, como foi feita a coleta de dados para as características de qualidade selecionadas: **[Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)** e **[Confiabilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)**, a coleta foi realizada utilizando ferramenta própria, explicada na [Fase 3](/docs/fase3.md) sessão 5.2.2, foram criados gráficos, dashboards, coletados os termos mais utilizados de forma positiva e de forma negativa, bem como a distribuição de estrelas na loja de aplicativos do google e uma análise de sentimentos em cima dos dados coletados pela ferramenta. Para esta análise, irão ser processados um total de 3361 reviews do aplicativo SouGov.br, abrangendo o período de 01/01/2025 a 17/11/2025.

![Figura 1 - Resumo dos resultados da ferramenta](../assets/images/resumo_coleta.png)

## 2 - Análise dos dados coletados para a característica Adequação Funcional

Essa sessão dedica-se a discutir sobre o que os dados coletados para as subcaracterísticas de Adequação Funcional no que diz respeito a qualidade evidenciam em relação às métricas definidas para validação nas fases [2](/docs/fase2.md) [3](/docs/fase3.md), mostrar onde falharam(se falharam), onde tiveram sucesso e onde o resultado foi neutro, adicionando o que a ferramenta conseguiu coletar por meio de fotos dos gráficos e dashboards produzidos, da análise de sentimentos e dos termos mais utilizados.

### 2.1 - Frequência de Lacunas Funcionais (FLF)

A ferramenta classificou os N-Grams de reviews Neutros(3) e Negativos(1 e 2), para fazer a análise dessa métricas precisamos encontrar termos que se assemelhem a "falta", "não tem" e "precisava", e ao olhar a tabela gerada:

![Figura 2 - N-Grams dos reviews neutros e negativos](../assets/images/ngrams_neutro_negativo.png)

Das frases presentes na figura 2, possuímos "não funcionando" e "não tenho" como representantes para essa métrica, o critério de julgamento é em porcentagem, sendo elas:

Excelente : menor ou igual a 5%
Bom: entre 6% a 15%
Regular: de 16% a 25%
Insuficiente: mais que 25%

Para achar a porcentagem, precisamos dividir o número de ocorrências em conjunto dos dois N-Grams que identificamos para a métrica e dividir pelo total de citações, como o gráfico não trouxe o valor exato, precisaremos fazer uma estimativa:

Quantidade total de N-Grams(estimativa): aproximadamente 460
Quantidade de N-Grams para a métrica(estimativa): aproximadamente 30

Fazendo o cálculo, chegamos a mais ou menos 6%, então a métrica está classificada como Bom, considerando que a margem de erro deve estar perto de 3% para mais ou para menos.

### 2.2 - Proporção de Relatos de Incorreção (PRI)

Essa métrica busca medir a correção funcional dos resultados, para isso precisamos identificar os N-Grams que podem ser relacionados a uma incorreção, utilizando do mesmo gráfico da figura 2 :

![Figura 2 - N-Grams dos reviews neutros e negativos](../assets/images/ngrams_neutro_negativo.png)

Ao analisar os N-Grams, encontramos duas que podem se enquadrar aqui, são elas "prova vida" e "reconhecimento facial", pois ter esses termos como amplamente citados pode indicar que existe algo de errado na execução do fluxo dessas funcionalidades. Precisamos então definir como enquadrar os resultados do cálculo desta métrica, que será feita pegando o valor estimado dos dois termos e dividindo pela quantidade de avaliações negativas que o aplicativo recebeu durante o período que as informações foram coletadas.

![Figura 3 - Nota das avaliações na App Store do Android](../assets/images/grafico_avaliacoes.png)

Critério de Julgamento:
Excelente - menor ou igual a 5%
Bom - entre 6% e 15%
Regular - entre 16% e 25%
Insuficiente - maior que 25%

Total de avaliações negativas(1 e 2) - 399 avaliações
Total estimado de N-Grams para "prova vida" e "reconhecimento facial" - aproximadamente 120

Fazendo o cálculo(120/399), encontramos o valor de 0.30, correspondente a 30%, sendo essa métrica então classificada como Insuficiente.

### 2.3 - Índice de Fricção na Tarefa Crítica(IFTC)

Essa métrica mede a taxa de sucesso percebida pelo usuário no feedback em relação a tarefas crítcas, fazendo a Análise em cima dos N-Grams de Fricção, utilizando do mesmo gráfico da figura 2:

![Figura 2 - N-Grams dos reviews neutros e negativos](../assets/images/ngrams_neutro_negativo.png)

Ao checarmos o gráfico por referências a tarefas críticas, encontramos uma série delas: "não funciona", "não abre", "não consigo acessar" e "não entra". Todos eles tem haver com a tarefa crítica de conseguir acessar o aplicativo, essencial para realizar toda e qualquer outra tarefa que dependa do SouGov.br. Para determinar como classificar o julgamento da métrica, utilizaremos a seguinte distribuição:

Excelente - menor ou igual a 10%
Bom - entre 11% e 30%
Regular - entre 31% e 50%
Insuficiente - acima de 50%

Para executar o cálculo, utilizaremos a estimativa da soma dos N-Grams destacados aqui e dividir pela quantidade total estimada de N-Grams:
Estimativa para total de N-Grams - aproximadamente 460
Estimativa para a junção dos 4 N-Grams levados em consideração aqui - aproximadamente 115
Cálculo da porcentagem - junção/total = 115/460 = 0.25 = 25%
Desta forma, a métrica fica classificada como Bom.

## 3 - Análise dos dados coletados para a característica de Confiabilidade

Essa sessão dedica-se a discutir o que os dados coletados para as subcaracterísticas de Confiabilidade no que diz respeito a qualidade evidenciam em relação às métricas definidas para validação nas fases [2](../fase2.md) e [3](../fase2.md), mostrar onde falharam(se falharam), onde tiveram sucesso e onde o resultado foi neutro, adicionando o que a ferramenta conseguiu coletar por meio de fotos dos gráficos e dashboards produzidos, da análise de sentimentos e dos termos mais utilizados.

### 3.1 - Frequência de Instabilidade Operacional (FIO)

Essa métrica mede a estabilidade do sistema e interrupções perceptíveis, utilizando do Mapeamento de Qualidade (PLN) em relação a termos como "Travamentos", "Lentidão" e "Instabilidade", utilizando como cálculo a frequência de menções em relação ao total de reviews(menções/reviews).

![Figura 4 - Mapeamento dos termos](../assets/images/mapa_termos.png)

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

![Figura 3 - Nota das avaliações na App Store do Android](../assets/images/grafico_avaliacoes.png)
![Figura 4 - Mapeamento dos termos](../assets/images/mapa_termos.png)
![Figura 5 - Mapeamento dos reviews críticos](../assets/images/reviews_criticos.png)

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

![Figura 4 - Mapeamento dos termos](../assets/images/mapa_termos.png)

![Figura 5 - Mapeamento dos reviews críticos](../assets/images/reviews_criticos.png)

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
| 3.0    | 23/11/2025  | Versão final da interpretação dos dados da fase 4(pendente revisão)     | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
