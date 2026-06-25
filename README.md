# 🚀 Modelo de Classificação de Score de Crédito - Quantum Finance

## 📌 Sobre o Projeto
Este projeto prático de Aprendizado de Máquina foi desenvolvido como parte do MBA em Data Science e IA da FIAP. Atuando no papel de analista de dados da **Quantum Finance**, o objetivo principal é explorar uma base de dados financeira e criar um sistema de classificação supervisionada para prever o score de crédito de indivíduos (Good, Standard ou Poor).

Os dados utilizados neste projeto foram disponibilizados originalmente no Kaggle: [Credit Score Classification](https://www.kaggle.com/datasets/parisrohan/credit-score-classification).

## 🎯 Etapas e Metodologia
1. **Análise Exploratória de Dados (EDA):** Inspeção da base de dados, identificação de valores ausentes (ex: `Monthly_Inhand_Salary`, `Type_of_Loan`) e análise das distribuições e correlações para entender o comportamento das features numéricas e categóricas.
2. **Modelagem de Machine Learning:** Construção de um pipeline de classificação testando três algoritmos robustos:
   - Random Forest
   - XGBoost
   - LightGBM
3. **Otimização:** Ajuste de hiperparâmetros utilizando `GridSearchCV`.
4. **Avaliação:** Utilização da métrica `f1_weighted` para garantir uma avaliação justa e robusta diante do desequilíbrio de classes presente na variável alvo.

## 📊 Principais Resultados e Insights
- 🏆 **LightGBM:** Apresentou o melhor desempenho geral, alcançando o maior `f1_weighted` (**0.74**) no conjunto de teste. O modelo demonstrou consistência na previsão de todas as três classes (0.68 para 'Good', 0.72 para 'Poor' e 0.77 para 'Standard').
- 🥈 **XGBoost:** Obteve o segundo melhor desempenho, com um `f1_weighted` de **0.70**.
- ⚠️ **Random Forest:** Apresentou a performance mais baixa (**0.55**), com extrema dificuldade em prever a classe 'Good' (recall de apenas 0.03).
- **Conclusão:** Os modelos baseados em *boosting* (XGBoost e LightGBM) provaram ser significativamente mais adequados e eficazes para este problema específico de score de crédito. 

## 🛠️ Tecnologias Utilizadas
- **Linguagem:** Python
- **Manipulação de Dados:** Pandas, NumPy
- **Visualização de Dados:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn, XGBoost, LightGBM
