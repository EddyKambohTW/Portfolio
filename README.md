# Portfolio: Eddy Frank Fotsing Kamboh

My data science and machine learning portfolio, published with GitHub Pages.

**Live site:** https://eddykambohtw.github.io/Portfolio/

## What's inside

- **Projects:** Hilo (Hydro-Québec) energy forecasting with responsible AI (scikit-learn, Optuna, SHAP, Fairlearn), an AutoML/MLOps energy-forecasting pipeline (H2O, MLflow, DVC, FastAPI, Docker) and a local-LLM CSV assistant (Streamlit + Ollama)
- **Articles:** a five-part *Statistical Thinking* R tutorial series, migrated from [RPubs](https://rpubs.com/kambonalytic)
- **Coursework:** MATH 1280 (Introduction to Statistics) and MATH 1281 (Statistical Inference)

## Structure

```
docs/
├── _config.yml        # Jekyll config (Cayman theme, site title)
├── index.md           # Portfolio home page
└── articles/
    ├── *.md           # R tutorial articles
    └── images/        # Plots from the articles
```

## Local preview

GitHub Pages builds the `docs/` folder automatically on every push to `main`. To preview locally (requires Ruby):

```bash
gem install bundler jekyll github-pages
cd docs
jekyll serve
```

Then open http://localhost:4000.

## Contact

Reach me on [LinkedIn](https://www.linkedin.com/in/eddyk1).
