# 🧪 Ensaio de Machine Learning

Este projeto compara o desempenho de diversos algoritmos de **Classificação**, **Regressão** e **Agrupamento (Clusterização)**, avaliando o impacto do ajuste de hiperparâmetros e o equilíbrio entre aprendizado e generalização (overfitting vs. underfitting).

---

## 🛠️ Metodologia (Holdout)

A validação foi feita dividindo os dados em três etapas:

1. **Treino (60%):** Aprendizado inicial dos modelos.
2. **Validação (20%):** Ajuste fino de hiperparâmetros.
3. **Teste (20%):** Avaliação final da capacidade de generalização.

---

## 🧰 Algoritmos e Métricas

* **Classificação:** KNN, Árvores de Decisão, Random Forest e Regressão Logística.  
  * *Métricas:* Acurácia, Precisão, Recall e F1-Score.
* **Regressão:** Regressão Linear, Árvores de Decisão, Random Forest, Regressão Polinomial e variações com regularização (Lasso, Ridge, Elastic Net).  
  * *Métricas:* R², MSE, RMSE, MAE e MAPE.
* **Agrupamento:** K-Means e Affinity Propagation.  
  * *Métricas:* Silhouette Score.

---

## 🏆 Melhores Resultados (Dados de Teste)

| Tarefa | Melhor Algoritmo | Métrica Principal | Resultado |
|---|---|---|---|
| **Classificação** | Decision Tree / Random Forest | Accuracy / F1-Score | **0.8950 / 0.8948** |
| **Regressão** | Polinomial Regression | R² / MAPE | **0.9919 / 0.3610** |
| **Agrupamento** | K-Means | Silhouette Score | **0.7283** |

---

## 💡 Principais Conclusões

1. **Árvores de Decisão exigem limite de profundidade:** Sem limitação (`max_depth`), o modelo decora os dados de treino e perde capacidade de generalizar.
2. **Modelos lineares foram altamente eficazes em Regressão:** Tiveram desempenho excelente ($R^2 \approx 0.992$) e estável em todas as etapas.
3. **Ajuste de hiperparâmetros alavancou o K-Means:** O ajuste de clusters aumentou o Silhouette Score de $0.4746$ para $0.7283$.

---

## 💻 Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas:** Pandas, NumPy e Scikit-Learn
