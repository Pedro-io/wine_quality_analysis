# Análise da Qualidade de Vinhos Tintos

Este projeto realiza uma análise exploratória de dados sobre a qualidade de vinhos tintos, com o objetivo de entender as relações entre as propriedades físico-químicas do vinho e sua avaliação de qualidade. O estudo é conduzido utilizando um dataset contendo medidas de diversas variáveis relacionadas à produção de vinho tinto.

## Dataset

O dataset utilizado é proveniente do arquivo `winequality-red.csv`. Ele contém 11 variáveis físico-químicas e uma variável de qualidade (score). As variáveis são:

1. **fixed acidity**: medida da acidez devido à presença de ácidos orgânicos de baixa volatilidade.
2. **volatile acidity**: medida da acidez devido a ácidos de baixo peso molecular.
3. **citric acid**: medida de ácido cítrico no vinho.
4. **residual sugar**: medida de açúcar residual no vinho após a fermentação.
5. **chlorides**: medida de cloretos (íons de cloro) no vinho.
6. **free sulfur dioxide**: medida de dióxido de enxofre livre no vinho.
7. **total sulfur dioxide**: medida de dióxido de enxofre total no vinho.
8. **density**: medida da densidade do vinho.
9. **pH**: medida do pH do vinho.
10. **sulphates**: medida de sulfatos no vinho.
11. **alcohol**: medida da graduação alcoólica do vinho.
12. **quality**: score numérico de qualidade (de 0 a 10), baseado em dados sensoriais.

## Objetivos

O principal objetivo deste projeto é:

*   Realizar uma análise exploratória dos dados.
*   Analisar a distribuição das variáveis numéricas e verificar a presença de outliers.
*   Estudar a distribuição da variável resposta (qualidade) e, se possível, discretizá-la.
*   Avaliar a correlação das variáveis descritivas com a variável resposta.
*   Visualizar intervalos de confiança para a média das variáveis físico-químicas, agrupadas por níveis de qualidade.

## Estrutura do Notebook

O Jupyter Notebook segue uma estrutura de análise exploratória de dados, dividido nas seguintes etapas:

1.  **Importação de bibliotecas:** Carregamento de bibliotecas necessárias para análise (pandas, numpy, matplotlib, seaborn).
2.  **Carregamento e visão geral dos dados:**
    *   Leitura do arquivo `winequality-red.csv` para um DataFrame do pandas.
    *   Exibição do número de linhas e colunas do dataset.
    *   Identificação dos tipos de dados em cada coluna.
    *   Verificação da existência de dados nulos.
3.  **Distribuição das variáveis numéricas:**
    *   Cálculo de estatísticas descritivas (média, mediana, quartis, etc.) e dispersão (desvio padrão, IQR, etc.) para cada variável numérica.
    *   Visualização das distribuições através de histogramas.
4.  **Análise de Outliers:**
    *   Identificação de outliers em cada variável numérica usando o método do quartil (IQR).
5.  **Análise da variável resposta (quality):**
    *   Determinação se a variável é contínua ou discreta.
    *   Análise da distribuição das notas de qualidade.
    *   Discretização da variável `quality` em duas categorias ("bom" e "ruim") utilizando um ponto de corte em 5.
    *   Visualização da distribuição dos níveis de qualidade discretizados.
6.  **Correlação entre variáveis:**
    *   Cálculo e visualização da matriz de correlação de todas as variáveis.
    *   Cálculo e ordenação da correlação da variável resposta com as variáveis descritivas.
7.  **Intervalos de Confiança:**
    *   Visualização dos intervalos de confiança de 90% para as médias de cada variável físico-química, agrupadas pelos níveis da variável resposta (`quality_bin`).

## Resultados

Através desta análise, foi possível verificar:

*   A distribuição das variáveis numéricas e a identificação de outliers.
*   A distribuição das notas de qualidade e a necessidade de transformá-la em uma variável binária (bom/ruim) para uma análise mais focada.
*   A correlação de cada variável com a qualidade, mostrando que o álcool é a variável com maior influência positiva, enquanto a acidez volátil tem a maior influência negativa.
*   Os intervalos de confiança para as médias das variáveis físico-químicas, agrupadas por nível de qualidade, sugerem que as variáveis estão distribuídas de maneira diferente para vinhos considerados bons e ruins.

Um arquivo CSV contendo a variável `quality` binarizada é salvo como `winequality-red-binary.csv`.

## Conclusões

Este projeto demonstra como realizar uma análise exploratória de dados de forma sistemática para:

*   Caracterizar o dataset inicial.
*   Identificar comportamentos e padrões nos dados.
*   Preparar a base de dados para futuras análises preditivas.
*   Gerar visualizações úteis para entender melhor o problema a ser resolvido.

## Próximos Passos

Os próximos passos do projeto incluem:

*   Investigar o uso das variáveis com maior correlação para construir modelos preditivos de classificação da qualidade do vinho.
*   Explorar outras abordagens para discretizar a variável de qualidade e avaliar seus efeitos nos resultados.
*   Utilizar outras técnicas de tratamento de outliers e avaliar o impacto nos modelos preditivos.
