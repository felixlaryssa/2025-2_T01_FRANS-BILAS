# Fase 4 - Análise dos dados coletados

## 1 - Introdução

A fase 4 detalha, de forma completa e rastreável, como foi feita a coleta de dados para as características de qualidade selecionadas: **[Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)** e **[Confiabilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)**, a coleta foi realizada utilizando ferramenta própria, explicada na [Fase 3](/docs/fase3.md) sessão 5.2.2, foram criados gráficos, dashboards, coletados os termos mais utilizados de forma positiva e de forma negativa, bem como a distribuição de estrelas na loja de aplicativos do google e uma análise de sentimentos em cima dos dados coletados pela ferramenta. Para esta análise, irão ser processados um total de 3361 reviews do aplicativo SouGov.br, abrangendo o período de 01/01/2025 a 17/11/2025.

## 2 - Análise dos dados coletados para a característica Adequação Funcional

Essa sessão dedica-se a discutir sobre o que os dados coletados para as subcaracterísticas de Adequação Funcional no que diz respeito a qualidade evidenciam em relação às métricas definidas para validação nas fases [2](/docs/fase2.md) [3](/docs/fase3.md), mostrar onde falharam(se falharam), onde tiveram sucesso e onde o resultado foi neutro, adicionando o que a ferramenta conseguiu coletar por meio de fotos dos gráficos e dashboards produzidos, da análise de sentimentos e dos termos mais utilizados.

### 2.1 - Cobertura de Requisitos Críticos por Módulo

A análise de N-grams (termos recorrentes) identificou falhas na execução de tarefas críticas para o usuário.

Evidência: O termo "Reconhecimento Facial" foi citado 43 vezes como um ponto de fricção.

Análise: A funcionalidade de reconhecimento facial é um requisito crítico para o acesso aos serviços. A alta recorrência deste termo em contextos negativos indica que este módulo específico não está cobrindo adequadamente a necessidade do usuário de se autenticar de forma fluida.

### 2.2 - Taxa de Inconformidade Funcional(TIF)

### 2.3 - Taxa de Sucesso na Conclusão de Tarefas Críticas

## 3 - Análise dos dados coletados para a característica de Confiabilidade

Essa sessão dedica-se a discutir o que os dados coletados para as subcaracterísticas de Confiabilidade no que diz respeito a qualidade evidenciam em relação às métricas definidas para validação nas fases [2](/docs/fase2.md) e [3](/docs/fase2.md), mostrar onde falharam(se falharam), onde tiveram sucesso e onde o resultado foi neutro, adicionando o que a ferramenta conseguiu coletar por meio de fotos dos gráficos e dashboards produzidos, da análise de sentimentos e dos termos mais utilizados.

### 3.1 - Tempo Médio Entre Falhas (TMEF)/ Disponibilidade (%)

### 3.2 - Tempo Médio para Reparo/Reprodução (TMPR)

### 3.3 - Frequência de Falhas Operacionais (FFO)

Mede a quantidade de erros explícitos reportados.

Evidência: A categoria "Bugs/Erros" é a mais volumosa dentro dos riscos de confiabilidade, com cerca de 70 ocorrências registradas no gráfico de barras. O termo "Dá erro" foi identificado como a falha sistêmica mais recorrente.

Análise: A FFO é significativa. A recorrência da expressão "não funciona" (38 menções) reforça que o aplicativo apresenta comportamentos inesperados com frequência suficiente para ser estatisticamente relevante na análise de sentimento.

## Conclusão

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data        | Descrição                                            | Autor(a)                                                            |
| ------ | ----------- | ---------------------------------------------------- | ------------------------------------------------------------------- |
| 1.0    | 19/11/2025  | Versão inicial da fase 4                             | [Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita)  |
| 1.1    | 19/11/2025  | Adição de etapas iniciais extras a fase 4            | [Giovana Ferreira](https://github.com/gih7915)                      |
