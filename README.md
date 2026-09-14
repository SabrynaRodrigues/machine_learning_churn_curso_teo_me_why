<h1 align="center">Machine Learning — Curso Tell Me Why</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F793E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
</p>

<p align="center">
  Anotações, códigos e um projeto completo de <strong>Machine Learning</strong> desenvolvidos
  durante o curso gratuito do canal <strong>Tell Me Why</strong> no YouTube.
</p>

---

## Sobre o repositório

Este repositório reúne o material produzido ao longo do curso, cobrindo desde os
fundamentos do ciclo analítico até a construção, avaliação e deploy de um modelo
de classificação aplicado a um problema real de **churn de clientes**.

---

## Conteúdo abordado

<table>
  <tr>
    <td><strong>Ciclo Analítico</strong></td>
    <td>Etapas de um projeto de ciência de dados, do entendimento do problema até a entrega do modelo</td>
  </tr>
  <tr>
    <td><strong>Regressão Linear</strong></td>
    <td>Regressão linear simples e múltipla</td>
  </tr>
  <tr>
    <td><strong>Árvores de Regressão</strong></td>
    <td>Modelos baseados em árvores para variáveis contínuas</td>
  </tr>
  <tr>
    <td><strong>Regressão Logística</strong></td>
    <td>Classificação binária e interpretação de coeficientes</td>
  </tr>
  <tr>
    <td><strong>Naive Bayes</strong></td>
    <td>Classificador probabilístico baseado no Teorema de Bayes</td>
  </tr>
  <tr>
    <td><strong>Random Forest</strong></td>
    <td>Ensemble de árvores de decisão com amostragem aleatória</td>
  </tr>
  <tr>
    <td><strong>Métricas de Ajuste</strong></td>
    <td>Acurácia, precisão, especificidade e recall</td>
  </tr>
  <tr>
    <td><strong>Matriz de Confusão</strong></td>
    <td>Análise detalhada de erros e acertos do modelo</td>
  </tr>
  <tr>
    <td><strong>Curva ROC e AUC</strong></td>
    <td>Avaliação comparativa entre treino, teste e out-of-time</td>
  </tr>
  <tr>
    <td><strong>Feature Engineering</strong></td>
    <td>Discretização (binning) e One-Hot Encoding com <code>feature-engine</code></td>
  </tr>
  <tr>
    <td><strong>Pipelines</strong></td>
    <td>Encapsulamento de etapas de pré-processamento e modelo com <code>sklearn.pipeline</code></td>
  </tr>
  <tr>
    <td><strong>Tuning</strong></td>
    <td>Grid Search com validação cruzada para otimização de hiperparâmetros</td>
  </tr>
  <tr>
    <td><strong>MLflow</strong></td>
    <td>Rastreamento de experimentos, métricas e versionamento de modelos</td>
  </tr>
  <tr>
    <td><strong>Serialização</strong></td>
    <td>Persistência do modelo treinado com <code>pickle</code> para uso futuro</td>
  </tr>
</table>

---

## Projeto de Churn — Metodologia SEMMA

O projeto principal do repositório aplica a metodologia **SEMMA** na construção de
um modelo de previsão de churn:

### 🔹 Sample — Amostragem
- Separação da base em **treino**, **teste** e **out-of-time** (safra mais recente)
- Split estratificado 80/20 para preservar a proporção da variável resposta
- Verificação da taxa da variável resposta entre as amostras

### 🔹 Explore — Exploração
- Análise de valores ausentes
- Análise bivariada entre features e a variável target
- Importância das features com Árvore de Decisão
- Seleção das melhores features por importância acumulada

### 🔹 Modify — Transformação
- **Discretização (Binning)** com `DecisionTreeDiscretiser`
- **One-Hot Encoding** das variáveis discretizadas
- Encapsulamento em pipelines reutilizáveis

### 🔹 Model — Modelagem
- Regressão Logística
- Naive Bayes (Bernoulli)
- Random Forest
- Tuning com `GridSearchCV` (critério, `min_samples_leaf`, `n_estimators`)

### 🔹 Assess — Avaliação
- Acurácia e AUC em treino, teste e out-of-time
- Curvas ROC comparativas
- Registro de experimentos no **MLflow**
- Serialização do pipeline final com `pickle`

---

## Estrutura dos notebooks

| Notebook | Descrição |
|----------|-----------|
| `project_churn_semma.ipynb` | Projeto completo seguindo as etapas SEMMA, com EDA, feature engineering, modelagem, tuning e integração com MLflow |
| `predict_final_file.ipynb` | Carrega o modelo serializado (`model_churn_rf.pkl`) e realiza predições de probabilidade de churn sobre uma amostra da base |

---

## Tecnologias

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F793E?style=flat-square&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/feature--engine-4B8BBE?style=flat-square" />
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat-square" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white" />
</p>

---

## Créditos

Conteúdo baseado no curso gratuito do canal **Tell Me Why** no YouTube.
Todo o mérito do material didático é do professor e do canal.

<p>
  <a href="https://www.youtube.com/watch?v=oz_rZ92Tmls&list=PLvlkVRRKOYFR6_LmNcJliicNan2TYeFO2&index=1">
    <img src="https://img.shields.io/badge/YouTube-Curso%20de%20Machine%20Learning-FF0000?style=for-the-badge&logo=youtube&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <img src="https://img.shields.io/badge/Status-Em%20estudo-4CAF50?style=for-the-badge" />
</p>
