# Relatório Detalhado do Trabalho: Redes Neurais Aplicadas a Ataques Cibernéticos

## 1. Introdução

O objetivo deste trabalho foi implementar e avaliar redes neurais para a classificação da gravidade (Severity Level) de ataques cibernéticos. Para isso, foi utilizado um conjunto de dados com 25 métricas e cerca de 40.000 registros. A análise foi realizada em etapas, incluindo o pré-processamento dos dados, construção de modelos de redes neurais, treinamento e avaliação.

## 2. Descrição e Pré-processamento dos Dados

### 2.1 Carregamento dos Dados
A inspeção inicial permitiu identificar os tipos de dados e a presença de valores ausentes. Esta etapa é importante para garantir que as etapas seguintes de análise e modelagem sejam feitas com dados limpos e consistentes.

### 2.2 Tratamento de Valores Faltantes
Colunas Numéricas: Para variáveis contínuas (como métricas de ataques), valores ausentes foram preenchidos com a média da coluna. Esta abordagem minimiza a introdução de viés.

Colunas Categóricas: Para variáveis qualitativas (ex: tipos de ataques ou categorias de alvos), valores ausentes foram preenchidos com a string 'desconhecido'. Isso evita perda de dados e permite posterior codificação numérica.

### 2.3 Transformação de Variáveis Categóricas
As redes neurais requerem entradas numéricas. Portanto, as colunas categóricas foram transformadas utilizando LabelEncoder, que converte cada categoria em um número único. 

Por exemplo: ["baixo", "médio", "alto"] → [0, 1, 2].

### 2.4 Processamento de Datas
A coluna de timestamp foi tratada para obtermos dados úteis:

Ano, Mês, Dia e Dia da Semana: Essas informações podem revelar padrões nos ataques.

### 2.5 Normalização dos Dados
Os dados numéricos foram normalizados com o StandardScaler, que ajusta todas as variáveis para uma escala similar. Isso é importante porque sem a normalização, variáveis com valores muito altos poderiam ter mais influência no modelo do que as variáveis com valores menores.

### 2.6 Tratamento de Outliers
Os outliers foram tratados usando o método de truncamento. Nesse método, definimos limites baseados nos percentuais 1% e 99%. Valores abaixo de 1% foram ajustados para o limite mínimo, e valores acima de 99% foram ajustados para o limite máximo. Isso ajuda a evitar que esses valores extremos, que podem ser erros ou casos muito incomuns, prejudiquem o treinamento do modelo, garantindo que o aprendizado se concentre nos padrões gerais dos dados.

## 3. Construção e Treinamento das Redes Neurais
### 3.1 Divisão do Conjunto de Dados
Para avaliar o desempenho das redes neurais, os dados foram divididos em dois conjuntos:

Treinamento (70%): Utilizado para ajustar os pesos das redes neurais.
Teste (30%): Utilizado para avaliar o desempenho em dados desconhecidos.

### 3.2 Estruturas dos Modelos
Três redes neurais foram implementadas, cada uma com diferentes configurações para comparar seu desempenho:

Modelo 1: Uma rede simples com uma camada oculta e 64 neurônios.
Objetivo: Estabelecer uma base de desempenho.
Função de Ativação: ReLU (Rectified Linear Unit), que é eficiente para capturar não linearidades em redes neurais.

Modelo 2: Uma rede com duas camadas ocultas (128 e 64 neurônios) e Dropout.
Objetivo: Testar a capacidade de aprendizado em uma estrutura mais profunda e avaliar o efeito do dropout.
Dropout: Durante o treinamento, desativa aleatoriamente neurônios para evitar overfitting. Essa técnica força o modelo a generalizar melhor.

Modelo 3: Uma rede mais complexa com três camadas ocultas (256, 128 e 64 neurônios).
Objetivo: Capturar padrões mais complexos no conjunto de dados.

## 4. Resultados e Avaliação
Os três modelos apresentaram resultados parecidos, com acurácia em torno de 33%. Isso mostra que os modelos não foram capazes de aprender os padrões relevantes no conjunto de dados. Além disso, alterar o número de camadas, neurônios e dropout não foi suficiente para melhorar os resultados.
