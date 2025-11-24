# Funcionamento da ferramenta desenvolvida pelo integrante Matheus do Vale

## Introdução

Como citado na [fase 3](../docs/fase3.md), a equipe optou pelo desenvolvimento de uma ferramenta própria para coletar as informações que iríamos precisar para fazer a análise de qualidade em relação a Adequação Funcional e Confiabilidade, pois as opções atuais do mercado ou não possuem tudo o que precisávamos para uma análise completa a utilizando, tornando necessário o uso de outro secundária, ou custavam entre 40 e 100 **dólares**, um valor que convertido para real(cotação do dia 23/11/2025, horário 16:26, segundo calculadora do Windows 11 em modo de conversão : 5,4028), varia de 216,11 reais a 540,28 reais, o que dá uma média de 378,19(cálculo de média padrão), que daria cerca de 75,63 reais por membro para adquirir um que estivesse no valor médio em dólar, que seria 70.
Ao percebermos a inviabilidade de conseguir uma ferramenta para isso, o integrante do grupo [Matheus Do Vale](https://github.com/delvale412) optou por produzir uma própria, que foi a que utilizamos para executar nossa fase 4, ela é um Dashboard de Análise de Sentimento e Qualidade que processa as avaliações ou _reviews_, como preferir chamar de modo a fornecer inferências ou _insights_ sobre a saúde e performance de um aplicativo

# 1 - O que a Ferramenta Analisa e Como Calcula as Estatísticas

A análise da ferramenta é **híbrida**, combinando inteligência de PLN(Processamento de Linguagem Natural) com regras de negócio e contagem de dados para transformar textos em métricas claras.

## 1.1 - Análise de Sentimento(PLN)

Foi utilizado o modelo BERT para classificar o texto de cada _review_ e determinar a polaridade, caso queira saber mais sobre o BERT, ao fim do 1.1 estaremos disponibilizando um link para acessar uma explicação do modelo pelo site Hugging Face. As etapas realizadas pela ferramenta são:

- **Classificação:** A previsão original de 1 a 5 estrelas do modelo BERT é consolidada em três categorias: **Negativo(1-2 estrelas)**, **Neutro(3 estrelas)** e **Positivo(4-5 estrelas)**;
- **Cálculo de KPIs:** As métricas de polaridade(exemplo: "Positivos(4-5)") são calculadas como a proporção da contagem de _reviews_ em cada categoria de sentimento em relação ao total de _reviews_ analisados.

[Hugging Face - BERT](https://huggingface.co/docs/transformers/model_doc/bert)

## 1.2 - Análise Qualitativa de Tópicos

A ferramenta realiza uma análise de conteúdo para identificar os temas mais críticos e os pontos fortes:

- **N-Grams:** Identifica as frases e termos mais frequentes (N-grams) em comentários positivos e negativos, após a remoção de _espaço vazio_ e frases irrelevantes. Isso destaca o **valor central percebido** e os **principais pontos de fricção**.
- **Mapeamento de Qualidade (ISO 25010):** _Reviews_ com baixa pontuação(Score > 3) são mapeados contra categorias de qualidade predefinidas(como **Confiabilidade** e **Adequação Funcional**), quantificando explicitamente a frequência de menções a bugs, travamentos ou problemas de acesso.

# 2 - Resultados, Fontes de Dados e Margem de Erro

Aqui falaremos sobre as etapas supracitadas.

## 2.1 - Fonte de Dados e Estatísticas

- **Fonte:** Todas as métricas de performance(_Total Reviews_, Nota Média, Distribuições Gráficas) são calculadas diretamente a partir da base de dados de _reviews_ carregada pelo usuário
- **Ficha Técnica:** As informações sobre o aplicativo(Desenvolvedor,Downloads,Classificação,Descrição) são usadas para contextualizar o relatório, sendo extraídas de um arquivo separado (Metadados do App).

## 2.2 - Margem de Erro na Análise

A ferramenta processa **100% da amostra** fornecida. Portanto, o erro principal não é estatístico, mas sim **erro de classificação** do PLN.

**Margem de Erro por Classificação:** o modelo BERT tem uma precisão média de 90%, a incerteza nos KPIs de sentimento é aproximadamente 10%;
**Falsos Resultados**: A ferramenta está sujeita a **Falsos Positivos**(um _review_ sarcástico é classificado como positivo) ou **Falsos Negativos**. O **Mapeamento de Qualidade** atua como uma validação, focando em palavras-chave objetivas para mitigar o impacto do erro de classificação global no diagnóstico técnico.

# 3 - Fluxo de Trabalho e Coleta de Dados

A execução da ferramenta segue três etapas principais.

## 3.1 - Preparação e Configuração

- **Criação de Diretório:** Inicialmente, a ferramenta garante que um local de armazenamento será utilizado. Se o diretório não existir, ele é criado automáticamente para organizar os resultados;
- **Definição do Alvo:** O código é configurado para buscar dados do aplicativo com o identificador ID;
- **Definição do Período::** É estabelecido o intervalo de datas de interesse para o recolhimento de dados, no escopo do nosso projeto, o ano de 2025(1° de janeiro a 31 de dezembro de 2025).

## 3.2 - Coleta de Informações Gerais do Aplicativo

Nesta etapa, a ferramenta se conecta à Google Play Store para extrair os detalhes sobre o aplicativo alvo. Esses detalhes incluem:

- Nome do aplicativo;
- Descrição
- Desenvolvedor
- Data de última atualização
- Estatísticas de avaliação(nota média, número de avaliações, etc).
  Todos os dados coletados são imediatamente organizados em formato tabular.

## 3.3 - Coleta e Filtragem de Reviews(Avaliações)

Esta é a etapa mais complexa, focada em obter as opiniões dos usuários:

1. **Busca Interativa:** A ferramenta inicia a busca por avaliações, começando pelas mais **recentes**(ordenadas por data). Ela busca os _reviews_ em lotes(200 por vez);
2. **Paginação:** Para garantir que todos os _reviews_ relevantes sejam encontrados, a ferramenta utiliza um mecanismo de "continuação" que move a busca para a próxima página de resultados, simulando a navegação na loja;
3. **Critério de Parada:** O processo de busca é otimizado para parar de forma eficiente. A coleta continua de página em página até que a ferramenta encontre um _review_ com data anterior ao determinado pelo usuário, no nosso caso, anterior a 1° de janeiro de 2025. Ao atingir essa data, o processo é interrompido, pois o critério de tempo foi atendido;
4. **Processamento:** Após a coleta bruta, os _reviews_ são processados. Mesmo que a coleta tenha parado após encontrar um review de 2024, por exemplo, é realizado um filtro final para garantir que **somente** os _reviews_ com datas estritamente dentro do período de 2025 sejam mantidos. É o mesmo processo de verificação para outras estipulações de datas.

## 4 - Arquivos Gerados

Ao final da execução, dois arquivos de planilha são gerados dentro do diretório:

1. **informacoes_app_xlsx:** Contém as informações gerais do aplicativo(Título, Desenvolvedor, Notas, etc.) em uma planilha de duas colunas(Campo e Valor);
2. **reviews_2025_xlsx:** Contém uma lista detalhada de todas as avaliações de usuários coletadas e filtradas, incluindo data, texto do comentário, nota dada pelo usuário e outras métricas, limitadas estritamente ao tempo estipulado pelo usuário, no escopo do projeto, 2025.

## Histórico de versão

<div style="text-align: center; margin: 0; font-size: 14px;">
  Tabela 5: Tabela de Versionamento
</div>

| Versão | Data        | Descrição                                                 | Autor(a)                                                                                                                         |
| ------ | ----------- | --------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 1.0    | 23/11/2025  | Transcrição da explicação dada pelo Matheus para o github | [Matheus Do Vale](https://github.com/delvale412), transcrição:[Carlos Eduardo](https://github.com/CarlosEduardoMendesdeMesquita) |
