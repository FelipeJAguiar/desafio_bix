# Projeto de Redução de Custos de Manutenção dos Caminhões

## Descrição do Projeto

Este projeto foi desenvolvido para uma empresa terceirizada de transporte com o objetivo de ser uma solução inicial para reduzir os custos de manutenção dos caminhões. Uma aplicação de machine learning que busca identificar caminhões que tiveram falhas no sistema de ar, desenvolvida para o processo seletivo de Data Science da Bix.

## Estrutura do Projeto

O projeto está estruturado da seguinte forma:

```
├── data
│   ├── air_system_previous_years.csv
│   ├── air_system_present_year.csv
├── notebooks
│   ├── desafio_bix.ipynb
├── README.md
├── requirements.txt
```

## Dados

### air_system_previous_years.csv

Contém todas as informações do setor de manutenção dos anos anteriores a 2022, com 171 colunas.

### air_system_present_year.csv

Contém todas as informações do setor de manutenção deste ano.

## Pré-processamento dos Dados

1. Exclusão de valores 'na'.
2. Conversão de tipos de dados conforme necessário.
3. Reescala de valores
4. Aplicação de Extra Trees para feature importance. 

## Modelagem

Modelos aplicados:
- Random Forest
- KNN
- Logistic Regression
- XGBoost
- Extra Trees Classifier

## Métricas de Avaliação

Para avaliar o desempenho dos modelos, utilizamos as seguintes métricas:
- Precision
- Recall
- F1-Score
- Accuracy

Essas métricas foram calculadas tanto para a classe "pos" (caminhões com defeito no sistema de ar) quanto para a classe "neg" (caminhões sem defeito no sistema de ar).

## Resultados

O melhor modelo foi selecionado com base nas métricas de precisão e recall. Após ajustar o threshold de decisão, o modelo apresentou os seguintes resultados:

- Precision: 0.8167539267015707
- Recall: 0.78
- F1-Score: 0.7979539641943735

## Previsões

Para prever os dados do novo dataset:

1. Carregue o novo dataset.
2. Aplique as mesmas etapas de pré-processamento.
3. Use o modelo treinado para fazer previsões.
4. Aplique o threshold para obter as classes preditas.

## Conclusão

Foi possível prever os caminhões mais propensos de forma consideravelmente assertiva, atendendo as demandas de negócio e propondo uma solução inicial para o problema de custos do clientes. 
