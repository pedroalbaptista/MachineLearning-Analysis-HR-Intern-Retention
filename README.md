<<<<<<< HEAD
<<<<<<< HEAD
# 🏢 HR Intern Retention Analysis | Análise de Retenção de Estagiários

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data-150458?style=flat&logo=pandas&logoColor=white)
![Methodology](https://img.shields.io/badge/Methodology-CRISP--DM-blue?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---
## English

### 📋 Context

Academic project developed as part of **AiDAPT01 – Cegid Academy**, aimed at analysing the factors that influence **intern retention** in a company, using the **CRISP-DM** methodology and Machine Learning techniques in Python.

The dataset contains **200 intern records** with variables such as age, university major, department, supervisor rating, salary, attendance, and retention indicator.

---

### 🎯 Objectives

- Identify the main **risk factors for intern departure**
- Build a **binary classification model** to predict retention (Retained: 0/1)
- Analyse **salary consistency** through supervised regression
- Discover **latent intern profiles** via unsupervised clustering
- Support **HR department decisions** grounded in empirical evidence

---

### ⚙️ Methodology: CRISP-DM

| Phase | Description |
|-------|-------------|
| 1️⃣ Business Understanding | Problem framing, success metrics and business criteria |
| 2️⃣ Data Understanding | Exploratory analysis, distributions and correlations |
| 3️⃣ Data Preparation | Cleaning, encoding, feature engineering and scaling |
| 4️⃣ Modeling | Training and comparison of multiple ML algorithms |
| 5️⃣ Evaluation | Business-oriented metric evaluation |
| 6️⃣ Deployment | Results export and HR recommendations |

---

### 🤖 Models Implemented

#### Classification (`Retained` target)
**Key metrics:**
- 🎯 **Recall (Class 0 – Left) ≥ 0.78** — minimise false negatives (lost talent)
- ⚖️ **F2-Score (Class 0)** — tiebreaker metric (double weight on Recall)
- 📈 **ROC AUC ≥ 0.60** — minimum discriminatory capacity
- ✅ Validated with **Stratified 5-Fold Cross-Validation**

#### Regression (`Salary` target)
No model outperformed the mean baseline — salary variance is largely unexplained by available features, suggesting high subjectivity in compensation decisions.

---

### 📊 Key Findings

- **Attendance**, **supervisor evaluation** and **internship duration** are the most impactful retention drivers
- The salary model confirms that compensation is not determined by objective merit metrics — external variables are likely at play
- The HR team can use the classification model as an **early warning system** for at-risk interns

---

### 🛠️ Tech Stack

- **Python 3.10+** · `pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn` · `Jupyter Notebook`

---

*Projeto académico — Cegid Academy AiDAPT01 | Academic project — Cegid Academy AiDAPT01*

---

---

## 🇵🇹 Português

### 📋 Contexto

Projeto académico desenvolvido no âmbito do curso **AiDAPT01 – Cegid Academy**, com o objetivo de analisar os fatores que influenciam a **retenção de estagiários** numa empresa, utilizando a metodologia **CRISP-DM** e técnicas de Machine Learning em Python.

O dataset contém **200 registos** de estagiários com variáveis como idade, curso universitário, departamento, avaliação do supervisor, salário, assiduidade e indicador de retenção.

---

### 🎯 Objetivos

- Identificar os principais **fatores de risco de saída** de estagiários
- Desenvolver um **modelo preditivo de classificação** (Retained: 0/1)
- Analisar a **consistência salarial** através de regressão supervisionada
- Descobrir **perfis latentes** de estagiários via clustering
- Apoiar decisões do **departamento de Recursos Humanos** com base em evidência empírica

---

### 🗂️ Estrutura do Projeto

```
hr-intern-retention-analysis/
│
├── 01_crisp_classification/         # Classificação — Retenção (Retained)
│   ├── 01_BusinessUnderstanding_class.ipynb
│   ├── 02_DataUnderstanding_class.ipynb
│   ├── 03_DataPreparation_class.ipynb
│   └── 04-05_Modeling_Evaluation_class.ipynb
│
├── 02_crisp_regression/             # Regressão — Salário (Salary)
│   ├── 01_BusinessUnderstanding_reg.ipynb
│   ├── 02_DataUnderstanding_reg.ipynb
│   ├── 03_DataPreparation_reg.ipynb
│   └── 04-05_Modeling_Evaluation_reg.ipynb
│
├── 03_crisp_clustering/             # Clustering — Perfis de Estagiários
│   └── CRISP-DM_Clustering.ipynb
│
└── README.md
```

---

### ⚙️ Metodologia: CRISP-DM

O projeto seguiu as 6 fases da metodologia **CRISP-DM**:

| Fase | Descrição |
|------|-----------|
| 1️⃣ Business Understanding | Definição do problema, métricas de sucesso e critérios de avaliação |
| 2️⃣ Data Understanding | Análise exploratória, distribuições e correlações entre variáveis |
| 3️⃣ Data Preparation | Limpeza, encoding, feature engineering e normalização |
| 4️⃣ Modeling | Treino e comparação de múltiplos algoritmos de ML |
| 5️⃣ Evaluation | Avaliação com métricas orientadas ao negócio |
| 6️⃣ Deployment | Exportação de resultados e recomendações ao RH |

---

### 🤖 Modelos Implementados

#### Classificação (Retenção — variável `Retained`)
| Modelo | Observação |
|--------|-----------|
| Logistic Regression | Baseline interpretável |
| Decision Tree | Captura de relações não-lineares |
| Random Forest | Modelo ensemble com melhor generalização |
| KNN | Comparação por vizinhança |

**Métricas principais:**
- 🎯 **Recall (Classe 0 – Sai) ≥ 0.78** — minimizar falsos negativos (talentos perdidos)
- ⚖️ **F2-Score (Classe 0)** — critério de desempate (penaliza mais o Recall)
- 📈 **ROC AUC ≥ 0.60** — capacidade discriminatória mínima
- ✅ Validação por **Stratified 5-Fold Cross-Validation**

#### Regressão (Salário — variável `Salary`)
| Modelo | MAE | RMSE | R² |
|--------|-----|------|----|
| Baseline (Média) | 261.69€ | 318.92€ | ~0.00 |
| Linear Regression | 277.06€ | 338.50€ | -0.13 |
| Decision Tree | 440.75€ | 514.75€ | -1.61 |
| Random Forest | 291.43€ | 355.15€ | -0.24 |

#### Clustering
- Análise de perfis latentes de estagiários com algoritmos não supervisionados

---

### 📊 Principais Conclusões

**Classificação:**
- Os fatores de maior impacto na retenção são a **assiduidade**, a **avaliação do supervisor** e a **duração do estágio**
- O modelo permite ao RH identificar antecipadamente estagiários em risco de saída, possibilitando intervenções preventivas
- A métrica Accuracy foi intencionalmente descartada dada a ligeira assimetria da target (61% Retained / 39% Sai)

**Regressão:**
- **Nenhum modelo superou a baseline da média** — o salário não é explicado pelas variáveis disponíveis
- Os R² negativos sugerem que a atribuição salarial tem um componente de **subjetividade ou negociação individual** elevado, não capturado nos dados
- Recomenda-se enriquecer o dataset com variáveis exógenas (ex.: benchmarks de mercado, dados de negociação)

**Recomendações ao RH:**
- Monitorizar continuamente assiduidade e avaliações como sinais precoces de saída
- Rever programas de estágio em departamentos com maior incidência de turnover
- Estruturar uma política salarial mais transparente e baseada em critérios objetivos

---

### 🛠️ Tecnologias Utilizadas

- **Python 3.10+**
- `pandas`, `numpy` — manipulação de dados
- `matplotlib`, `seaborn` — visualização
- `scikit-learn` — modelação e avaliação
- `Jupyter Notebook` — desenvolvimento interativo

---

### 📁 Dataset

| Campo | Descrição |
|-------|-----------|
| `Intern_ID` | Identificador único |
| `Age` | Idade do estagiário |
| `Major` | Curso universitário |
| `Internship_Duration_Months` | Duração do estágio (meses) |
| `Department` | Departamento |
| `Supervisor_Evaluation` | Avaliação do supervisor (1–5) |
| `Salary` | Remuneração mensal (€) |
| `Attendance_%` | Percentagem de assiduidade |
| `Retained` | 1 = Ficou, 0 = Saiu |
=======
# Analysis-HR-Intern-Retention
>>>>>>> daa1a6bb951c8e76e7318544bf8d91a60ba3c0a4
=======
# MachineLearning-Analysis-HR-Intern-Retention
>>>>>>> d8a3c6f2ce7c1b5393f60f129621d8574f0f79f7
