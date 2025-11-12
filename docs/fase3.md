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

1. Avaliar o grau de correspondência entre as funcionalidades implementadas e as necessidades dos usuários ([Adequação Funcional](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)
).

2. Verificar a confiabilidade operacional do aplicativo, considerando falhas relatadas, estabilidade e comportamento sob condições normais de uso ([Confiabilidade](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/#7-modelo-de-qualidade)).

## 3. Metodologia de Avaliação

A avaliação será conduzida de acordo com as cinco etapas do processo de avaliação da ISO/IEC 25040, que servem como referência metodológica:

- Estabelecimento dos requisitos de avaliação (já realizado na [Fase 1]((https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase1/)));

- Especificação da avaliação (modelo GQM definido na [Fase 2]((https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/) ));

- Projetar a avaliação (fase atual);

- Executar a avaliação (coleta e mensuração prática dos dados);

- Concluir a avaliação (interpretação e julgamento dos resultados).

Nesta fase, são detalhados os procedimentos de coleta e análise para cada métrica GQM ([M1 a M6]((https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#32-definicao-das-questoes-e-metricas-abordagem-gqm-q-e-m))), bem como a estrutura operacional necessária para realizar a avaliação com consistência.

## 4. Planejamento das Métricas e Métodos de Coleta

As métricas a seguir derivam diretamente da [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/) e estão agrupadas conforme as duas características de qualidade priorizadas.

### **3.1. Adequação Funcional**

| **Métrica**                                                       | **Descrição / Finalidade**                                                                         | **Método de Coleta**                                                                      | **Fonte de Dados**                                                                                       | **Frequência / Amostragem**                   | **Critério de Julgamento (da Fase 2)**                                   |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | --------------------------------------------- | ------------------------------------------------------------------------ |
| **[M1 — Cobertura de Requisitos Críticos por Módulo](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)**              | Mede a completude funcional, verificando se os módulos do SouGov atendem aos requisitos esperados. | Análise de rastreabilidade entre requisitos documentados e funcionalidades implementadas. | Documentação, lista de requisitos, base de chamados de suporte (“Funcionalidade Ausente”). | Análise pontual sobre versão 5.573.           | ≥ 95% Excelente; 80–94% Bom; 60–79% Regular; < 60% Insuficiente. |
| **[M2 — Taxa de Inconformidade Funcional (TIF)]((https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional))**                   | Mede a correção funcional dos resultados (ex.: cálculo de contracheque, férias).                   | Análises de comentários de usuários relatando divergências (“meu valor no SouGov está diferente do Portal do Servidor”).  |  registros de chamados (“Cálculo Incorreto”) Comentários e avaliações nas App Stores. A partir de feedback de usuário fazer comparativos entre dados do SOUGOV e relatórios públicos (como o [Portal da Transparência](https://portaldatransparencia.gov.br/))                                                | Avaliação sobre amostra representativa. | ≤ 5% Excelente; 6–15% Bom; 16–25% Regular; > 25% Insuficiente.   |
| **[M3 — Taxa de Sucesso na Conclusão de Tarefas Críticas (TSCTC)](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/#321-adequacao-funcional)** | Mede se os usuários conseguem completar tarefas essenciais (ex.: Prova de Vida Digital).           | Análise de comportamento do usuário + coleta de feedbacks.                                | Comentários e avaliações nas App Stores, telemetria de eventos de uso.                                   | Coleta contínua durante alguns dias.              | ≥ 90% Excelente; 70–89% Bom; 50–69% Regular; < 50% Insuficiente. |

### **3.2. Confiabilidade**

| **Métrica**                                                    | **Descrição / Finalidade**                                                                                | **Método de Coleta**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | **Fonte de Dados**                                                                                                            | **Frequência / Amostragem**                                         | **Critério de Julgamento (da Fase 2)**                                   |
| -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **M4 — Tempo Médio Entre Falhas (TMEF) / Disponibilidade (%)** | Mede a estabilidade operacional e o tempo médio de funcionamento do SouGov sem interrupções perceptíveis. | O avaliador realizará **sessões de uso contínuo** do aplicativo (mínimo de 30 minutos), em três dias distintos da semana, simulando operações típicas como **login, consulta de contracheque e atualização cadastral**. Durante as sessões, serão anotadas falhas ou travamentos. O cálculo da disponibilidade percentual média será feito com base nesses registros. | Sessões de uso simuladas; | Coleta semanal durante 3 semanas consecutivas.                      | ≥ 99% Excelente; 95–98% Bom; 85–94% → Regular; < 85% → Insuficiente. |
| **M5 — Tempo Médio para Reparo/Recuperação (TMPR)**            | Mede o tempo necessário para o sistema se recuperar de falhas críticas relatadas por usuários.            | Serão analisados **20 comentários recentes** de usuários na App Store e Play Store que mencionem falhas funcionais (ex: “não abre”, “erro no login”, “não carrega”). Para cada relato, será verificado se o problema foi **corrigido em versões posteriores**, com base nas **notas de atualização oficiais**. O tempo médio entre o relato e a correção observada será estimado como o TMPR.                                                                                                                              | Comentários de usuários nas lojas de aplicativos e notas de atualização do SouGov.                                            | Avaliação trimestral, considerando o histórico de versões lançadas. | ≤ 1h Excelente; 1–3h Bom; 3–6h Regular; > 6h Insuficiente.       |
| **M6 — Frequência de Falhas Operacionais (FFO)**               | Mede a incidência de falhas percebidas pelos usuários e observadas durante o uso prático do aplicativo.   | A coleta será baseada em **duas fontes**: (1) análise de comentários e avaliações nas lojas de aplicativos, contabilizando menções de falhas (“fecha sozinho”, “erro”, “não abre”); e (2) **observação direta** durante as sessões de teste realizadas para a métrica M4. A proporção de interações que resultaram em falhas será calculada e convertida em percentual de falhas operacionais.                                                                                                                             | Comentários nas lojas de aplicativos e registros das sessões de uso simuladas.                                                | Coleta mensal contínua  | ≤ 2% Excelente; 3–5% Bom; 6–10% Regular; > 10% Insuficiente.     |

# 5. Especificação dos Recursos

Os seguintes recursos são necessários para a execução completa e controlada do Plano de Avaliação:

## 4.1 Recursos Humanos

| Membro          | Responsabilidades                                     |
|-----------------|-------------------------------------------------------|
| Avaliadores (Equipe) | Execução dos testes, coleta e registro de dados. |

## 4.2 Materiais de Apoio e Ferramentas Técnicas

| Recurso                  | Função na Avaliação                                                |
|---------------------------|-------------------------------------------------------------------|
| Software Objeto de Avaliação | Aplicação SOUGOV (versão MOBILE).                    |
| Navegadores               | Google Chrome e Firefox (ambientes de teste).            |
| Ferramentas de Software   | Ferramentas do Desenvolvedor (DevTools).                        |
| Registro                  | Planilha Eletrônica (Excel) para coleta de dados estraídos dos feedbacks.               |
| Documentação              | Critérios de Avaliação Fase 2.                                   |


## 6. Garantia de Rastreabilidade e Reprodutibilidade

Para garantir a rastreabilidade e a reprodutibilidade dos resultados, cada métrica será acompanhada de um registro de medição padronizado, contendo:

- Data e versão do aplicativo analisado;

- Fonte de coleta (App Store, logs, documentação etc.);

- Método e ferramenta utilizada;

- Resultado numérico(quantitativo);

- Classificação segundo o critério de julgamento definido na [Fase 2](https://felixlaryssa.github.io/2025-2_T01_FRANS-BILAS/fase2/).

Esses registros servirão como evidência para auditoria e validação dos resultados.

## Bibliografia

> Ministério da Gestão e da Inovação em Serviços Públicos (MGI). *SouGov – Aplicativo oficial de serviços do servidor público federal*. Disponível em: <https://www.gov.br/servidor/pt-br/sou-gov>. Acesso em: 27 setembro 2025.

> Governo Federal. *Plataforma Gov.br – Serviços digitais para o cidadão*. Disponível em: <https://www.gov.br>. Acesso em: 27 setembro 2025.

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data       | Descrição                             | Autor(a) |
| ------ | ---------- | ------------------------------------- | -------- |
| 1.0    | 10/11/2025 | Conteúdo da fase 3 | [Laryssa Felix](https://github.com/felixlaryssa)   |