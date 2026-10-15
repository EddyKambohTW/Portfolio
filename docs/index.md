---
layout: default
title: Eddy Frank Fotsing Kamboh
---

**Data science & machine learning portfolio.** I build end-to-end ML pipelines and AI-powered data tools in Python, and practise applied statistics in R.

[LinkedIn](https://www.linkedin.com/in/eddyk1) · [GitHub](https://github.com/EddyKambohTW) · [RPubs](https://rpubs.com/kambonalytic)

**Contents:** [Projects](#projects) · [Articles](#articles) · [Coursework](#coursework) · [Skills](#skills)

---

## Projects

### [AutoML energy consumption forecasting (MLOps pipeline)](https://github.com/EddyKambohTW/projet-automl-energy-peak--002-)

An end-to-end MLOps pipeline that predicts total hourly electricity consumption (kWh) from smart-thermostat data collected at three stations.

- **Data & features:** indoor, outdoor and set-point temperatures; weather (solar irradiation, humidity, wind, snow); connected clients and thermostats; calendar and peak-event indicators. Feature engineering adds lags, rolling means and outlier handling.
- **Modelling:** **H2O AutoML** trains and compares many regression models. The best one by RMSE is registered in **MLflow** as the `champion` model. RMSE, MAE and R² are tracked with **DVC**.
- **Serving:** a **FastAPI** prediction API loads the champion model. A **Streamlit** dashboard handles CSV upload, charts and metrics.
- **Ops:** **Docker Compose** runs the services with health checks. Data is versioned with **DVC** (Google Drive remote). **GitHub Actions** validates every push and regenerates features weekly.

`Python` `H2O AutoML` `MLflow` `DVC` `FastAPI` `Streamlit` `Docker` `GitHub Actions`

### [AI data assistant: chat with your CSV (Streamlit + Ollama)](https://github.com/EddyKambohTW/03-tp-03-assistant-ia-csv-streamlit-ollama)

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

A five-part series of R tutorials based on *Introduction to Statistical Thinking (With R, Without Calculus)*, originally published on [RPubs](https://rpubs.com/kambonalytic).

| # | Article | Topics | Published |
|---|---------|--------|-----------|
| 1 | [Statistics & Basic R](articles/statistical-thinking-chapter-1.html) | What statistics is, R objects, `c()`, `table()`, bar plots | Jun 2022 |
| 2 | [Data Frames & Frequency](articles/statistical-thinking-chapter-2.html) | Reading CSVs, `head()`/`tail()`, frequency, relative and cumulative frequency | Jun 2022 |
| 3 | [Descriptive Statistics](articles/statistical-thinking-chapter-3.html) | Histograms, box plots, skewness, mean vs. median, variance and standard deviation | Jun 2022 |
| 4 | [Probability & Random Variables](articles/statistical-thinking-chapter-4.html) | Populations, `summary()`, random sampling, sample space and distribution | Jun 2022 |
| — | [Loading the Data Sets](articles/loading-data-sets.html) | Loading all 20 course datasets into R from the web | Jun 2022 |

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
| **Machine learning** | H2O AutoML, regression, feature engineering |
| **MLOps** | MLflow, DVC, Docker / Docker Compose, GitHub Actions |
| **Apps & APIs** | FastAPI, Streamlit |
| **Generative AI** | Ollama, local LLMs (Qwen, Llama, Gemma) |
| **Statistics** | Descriptive statistics, probability, statistical inference, simulation |
