# Modelo-Classificacao-churn

Este documento objetiva relatar como foi desenvolvido a solução de um problema de previsão de churn em uma plataforma de streaming.

A diretoria está preocupada com a alta taxa de cancelamento de assinaturas e deseja identificar antecipadamente os usuários com maior probabilidade de cancelar, a fim de tomar medidas para reduzir o churn.

O processo começa com a compreensão dos dados, utilizando métodos como describe, info e isna().sum() para entender a distribuição e a integridade dos dados. Em seguida, é feita a preparação dos dados, incluindo tratamento de valores nulos (fillna), remoção de entradas inválidas (dropna), substituição de valores categóricos por numéricos (replace) e conversão de tipos de dados (astype(int)), visando deixar a base pronta para modelagem.

Para a modelagem, são utilizados três abordagens principais: regressão logística, Random Forest e ajuste de hiperparâmetros (tuning). Cada uma dessas técnicas envolve etapas comuns, como codificação de variáveis categóricas (LabelEncoder, get_dummies), normalização de dados (MinMaxScaler), divisão da base em conjunto de treinamento e teste (train_test_split), ajuste do modelo aos dados de treinamento (fit) e previsão dos resultados utilizando os dados de teste (predict). Após a previsão, é realizada uma avaliação do modelo usando métricas como matriz de confusão (ConfusionMatrixDisplay) e outras métricas de desempenho, como acurácia.

O objetivo final é encontrar o modelo que ofereça a melhor acurácia na previsão do churn. Isso é feito através do ajuste dos hiperparâmetros dos modelos utilizando técnicas como grid_search e best_estimator_.get_params(), seguido pelo treinamento do modelo com os parâmetros otimizados e avaliação do desempenho.

Em resumo, este processo envolve uma combinação de compreensão dos dados, preparação dos dados e modelagem usando diferentes algoritmos, com o objetivo de identificar os usuários com maior probabilidade de cancelar suas assinaturas e tomar medidas proativas para reduzir o churn.
