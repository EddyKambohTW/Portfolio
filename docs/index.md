---
layout: default
title: Eddy Frank Fotsing Kamboh
---

**Data science & machine learning portfolio.** I build end-to-end ML pipelines and AI-powered data tools in Python, and practise applied statistics in R.

[LinkedIn](https://www.linkedin.com/in/eddyk1) · [GitHub](https://github.com/EddyKambohTW) · [RPubs](https://rpubs.com/kambonalytic)

**Contents:** [Projects](#projects) · [Articles](#articles) · [Coursework](#coursework) · [Skills](#skills)

---

## Projects

*The source code for these projects is in private GitHub repositories and is available on request.*

### Hilo (Hydro-Québec) energy consumption forecasting with responsible AI

Forecasts the next hour's total electricity consumption (kWh) for households in Hydro-Québec's **Hilo** demand-response program. Hilo can remotely reduce heating during winter peaks, so accurate hourly forecasts help plan peak events. Team project with Rami Alrishan.

- **Data:** 64,605 hourly records (3 substations, Jan 2022 – Jun 2024) pulled from the Hydro-Québec open-data API, covering consumption, connected clients, local weather and peak-event flags.
- **Feature engineering:** sine/cosine encoding of hour, weekday and month; 1 h and 24 h lags; rolling means and volatility; heating degree-hours (HDD) and cold-night interactions. Sensor errors are removed, and target leakage was found and eliminated.
- **Modelling:** a scikit-learn `HistGradientBoostingRegressor` predicts consumption *per client* (tree models can't extrapolate), with **monotonic constraints** on temperature. Hyperparameters were tuned with **Optuna** (Bayesian optimization), using a peak-weighted objective.
- **Evaluation:** a leak-free temporal split with 48 h gaps, tested on winter 2022–23. MAE is 23.3 kWh and **R² is 0.951**. Peak-hour error (above 1,000 kWh) is about **3× lower** than predicting total consumption directly (170 vs. 500 kWh). Quarterly blocked cross-validation (10 folds) gives R² = 0.924 ± 0.046.
- **Responsible AI:** fairness across substations and conditions with **Fairlearn**; explainability with **SHAP** and permutation importance; robustness tests; a STRIDE threat model and a privacy review.
- **MLOps:** reproducible **DVC** pipeline (Google Drive remote); **MLflow** experiment tracking and model registry; **Docker Compose**; Makefile and Typer CLI; Cookiecutter Data Science layout.

`Python` `scikit-learn` `Optuna` `SHAP` `Fairlearn` `pandas` `MLflow` `DVC` `Docker` `Jupyter`

### AutoML energy consumption forecasting (MLOps pipeline)

An end-to-end MLOps pipeline that predicts total hourly electricity consumption (kWh) from smart-thermostat data collected at three stations.

- **Data & features:** indoor, outdoor and set-point temperatures; weather (solar irradiation, humidity, wind, snow); connected clients and thermostats; calendar and peak-event indicators. Feature engineering adds lags, rolling means and outlier handling.
- **Modelling:** **H2O AutoML** trains and compares many regression models. The best one by RMSE is registered in **MLflow** as the `champion` model. RMSE, MAE and R² are tracked with **DVC**.
- **Serving:** a **FastAPI** prediction API loads the champion model. A **Streamlit** dashboard handles CSV upload, charts and metrics.
- **Ops:** **Docker Compose** runs the services with health checks. Data is versioned with **DVC** (Google Drive remote). **GitHub Actions** validates every push and regenerates features weekly.

`Python` `H2O AutoML` `MLflow` `DVC` `FastAPI` `Streamlit` `Docker` `GitHub Actions`

### AI data assistant: chat with your CSV (Streamlit + Ollama)

A Streamlit app for asking questions about a CSV file in plain language. Answers come from a **local LLM served by Ollama**, so the data never leaves your machine. Built for the course *420-C73-BB Processus et écosystèmes d'IA*.

- **Structure analysis:** row and column counts, data types
- **Data quality:** missing values and duplicates
- **Descriptive statistics:** mean, median, standard deviation and more
- **Automatic visualizations:** histograms, scatter plots
- **Code generation:** produces runnable Pandas code or SQL queries
- Runs on small local models: `qwen2.5-coder:1.5b`, `llama3.2:1b`, `qwen3:1.7b`, `gemma3:1b`

`Python` `Streamlit` `Ollama` `LLMs` `Pandas` `SQL`

---

## Articles

A five-part series of R tutorials based on [*Introduction to Statistical Thinking (With R, Without Calculus)*](http://pluto.huji.ac.il/~msby/StatThink/), originally published on [RPubs](https://rpubs.com/kambonalytic).

| # | Article | Topics | Published |
|---|---------|--------|-----------|
| 1 | [Statistics & Basic R](articles/statistical-thinking-chapter-1.md) | What statistics is, R objects, `c()`, `table()`, bar plots | Jun 2022 |
| 2 | [Data Frames & Frequency](articles/statistical-thinking-chapter-2.md) | Reading CSVs, `head()`/`tail()`, frequency, relative and cumulative frequency | Jun 2022 |
| 3 | [Descriptive Statistics](articles/statistical-thinking-chapter-3.md) | Histograms, box plots, skewness, mean vs. median, variance and standard deviation | Jun 2022 |
| 4 | [Probability & Random Variables](articles/statistical-thinking-chapter-4.md) | Populations, `summary()`, random sampling, sample space and distribution | Jun 2022 |
| — | [Loading the Data Sets](articles/loading-data-sets.md) | Loading all 20 course datasets into R from the web | Jun 2022 |

---

## Coursework

### [MATH 1280: Introduction to Statistics](https://sites.google.com/view/math-1280/chapter-1?authuser=1)

A chapter-by-chapter study site (Chapters 1–8) with notes and unit presentations for the course.

- Probability concepts that underpin statistics
- Presenting and summarizing data with tables, plots and numerical summaries
- Recognizing and interpreting variability
- Computing and plotting with R

### [MATH 1281: Statistical Inference](https://sites.google.com/view/math-1281)

- Point estimation, confidence intervals and hypothesis testing
- Models for describing relations between measurements
- Applying and interpreting the results of statistical inference
- The assumptions behind each inference procedure
- Using simulation to validate the probabilistic properties of inference procedures

---

## Skills

| Area | Tools |
|------|-------|
| **Languages** | Python, R, SQL |
| **Data analysis** | pandas, NumPy, Jupyter, seaborn, ydata-profiling, exploratory data analysis |
| **Machine learning** | scikit-learn (gradient boosting), H2O AutoML, regression, time-series forecasting, feature engineering (lags, rolling windows, cyclic encoding) |
| **Model evaluation** | Temporal train/test splits, blocked cross-validation, target-leakage detection, MAE / RMSE / R² / MAPE, error analysis by range |
| **Optimization** | Optuna (Bayesian hyperparameter tuning), monotonic constraints |
| **Responsible AI** | Fairlearn (fairness metrics), SHAP and permutation importance (explainability), robustness testing, STRIDE threat modeling, privacy review |
| **MLOps** | MLflow (tracking and model registry), DVC (data versioning and pipelines), Docker / Docker Compose, GitHub Actions, Makefile |
| **Apps & APIs** | FastAPI, Streamlit, Typer CLI, REST API data ingestion |
| **Generative AI** | Ollama, local LLMs (Qwen, Llama, Gemma) |
| **Statistics** | Descriptive statistics, probability, statistical inference, simulation |
| **Engineering practices** | Git, Cookiecutter Data Science project structure, Ruff (linting) |
