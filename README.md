<div align="center">

# Jai Indra Reddy Jonnala

### Graduate Student, M.S. Data Science (Mathematics & Statistics) — University at Albany

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

</div>

---

## About

I'm a graduate student studying Data Science, Mathematics, and Statistics, focused on
building research projects that are **actually run end-to-end** rather than described in
the abstract — every result in every repo below comes from code that executes, trains, and
evaluates for real. I care about getting the methodology right: honest baselines, held-out
evaluation, confounding handled explicitly, and limitations stated plainly rather than
glossed over.

My work sits across four areas that overlap more than people expect:

- **Artificial Intelligence** — retrieval systems, representation learning, architecture comparisons (CNN vs. attention-based models)
- **Data Science** — forecasting, experimentation, statistical inference, reproducible research pipelines
- **Causal Inference & Business Analytics** — recovering true effects from confounded observational data, translating model output into business recommendations
- **Systems-minded ML engineering** — pairing Python research code with faster compiled components (Go, Rust) for data generation and simulation, and SQL for real analytical querying

---

## Research Focus Areas

| Area | What I work on |
|---|---|
| 🔎 **Information Retrieval / NLP** | Retrieval evaluation methodology for RAG systems — comparing sparse (BM25), dense-ish (LSA), and hybrid retrievers with standard IR metrics (Precision@k, Recall@k, MRR, nDCG) |
| 📈 **Time-Series Forecasting** | Classical statistical models (Holt-Winters, SARIMA) vs. ML regressors on demand/sales data, with rigorous train/test splits and ablations |
| 🧮 **Causal Inference** | Regression adjustment, Inverse Propensity Weighting, and doubly-robust estimation — validated against known ground-truth treatment effects in simulation |
| 🧠 **Computer Vision Research** | Architecture comparisons (CNN vs. Vision-Transformer-style attention) with multi-seed statistical rigor, not single-run anecdotes |
| 📊 **Business Analytics** | Cohort/retention analysis, revenue-at-risk modeling, and churn prediction — grounded in real SQL queries against structured data |

---

## Featured Research Repositories

### 🔎 [rag-eval-framework](https://github.com/jaiindrareddy23/rag-eval-framework)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)

A Retrieval-Augmented Generation **retrieval evaluation framework**: TF-IDF, BM25, LSA, and
a hybrid retriever benchmarked on a synthetic knowledge-base corpus with labeled
ground-truth queries, plus a chunking-strategy ablation study.

> **Result:** the hybrid BM25+LSA retriever won every metric (MRR 0.923); smaller chunks
> roughly doubled precision but cut recall@5 from 0.955 to 0.510 — a real, measured
> precision/recall tradeoff.

### 📈 [timeseries-forecast-lab](https://github.com/jaiindrareddy23/timeseries-forecast-lab)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white)

A Go CLI generates and validates a synthetic daily-demand series (trend + weekly/yearly
seasonality + noise); Python then benchmarks naive, seasonal-naive, Holt-Winters, and
gradient-boosting forecasts on a 90-day held-out split.

> **Result:** Holt-Winters won decisively — MAE 21.96 vs. 102+ for the naive baselines — and
> a training-window ablation showed the ML model's error kept dropping with more history
> while the statistical model stayed flat.

### 🧮 [causal-inference-marketing](https://github.com/jaiindrareddy23/causal-inference-marketing)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/-Rust-000000?style=flat-square&logo=rust&logoColor=white)

A Rust simulator generates confounded observational marketing data with a **known true
treatment effect** baked in; Python then compares naive, regression-adjusted, IPW, and
doubly-robust estimators against that ground truth.

> **Result:** the naive comparison was biased by +$45 due to confounding; regression, IPW,
> and doubly-robust estimation all recovered the true $25 effect within ~$1.60.

### 🧠 [vision-transformer-study](https://github.com/jaiindrareddy23/vision-transformer-study)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

A small CNN vs. a from-scratch patch + self-attention Vision-Transformer-style model,
trained on scikit-learn's digits dataset and evaluated over 3 random seeds for a
statistically honest comparison (not a single lucky run).

> **Result:** the CNN won by ~1.7pp (98.5% vs. 96.8% mean test accuracy) despite having 3x
> fewer parameters — consistent with its locality/translation-equivariance inductive bias
> mattering more than capacity at this scale.

### 📊 [churn-analytics-ba](https://github.com/jaiindrareddy23/churn-analytics-ba)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

Synthetic subscription data loaded into SQLite; real SQL queries drive cohort-retention and
revenue-at-risk analysis, feeding a logistic-regression/gradient-boosting churn model and a
static Chart.js dashboard.

> **Result:** ROC-AUC 0.78; SQL analysis surfaced one segment (month-to-month, fiber) with
> $73,803/month in revenue at risk — roughly 2x the next-largest segment.

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=jaiindrareddy23&show_icons=true&theme=default&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=jaiindrareddy23&layout=compact&hide_border=true&theme=default)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=jaiindrareddy23&hide_border=true&theme=default)

</div>

---

## Other Projects

| Repo | Language |
|---|---|
| [EDA-Project](https://github.com/jaiindrareddy23/EDA-Project) — Exploratory and predictive analysis of traffic violations in the USA | Jupyter Notebook |
| [Fraud-Analysis](https://github.com/jaiindrareddy23/Fraud-Analysis) | Python |
| [RiskLens](https://github.com/jaiindrareddy23/risklens) | Python |
| [chargeback-defense](https://github.com/jaiindrareddy23/chargeback-defense) | TypeScript |
| [EcoSynapse](https://github.com/jaiindrareddy23/ecosynapse) | TypeScript |
| [EcoSense](https://github.com/jaiindrareddy23/ecosense) | Python |
| [Project-MindBridge](https://github.com/jaiindrareddy23/Project-MindBridge) | Python |
| [Jarvis — The AI Assistant](https://github.com/jaiindrareddy23/Jarvis---The-AI-Assistant) | Python |

---

## Education

**M.S. Data Science (Mathematics & Statistics)** — University at Albany

---

## Skills

**Languages:** `Python` `SQL` `Go` `Rust`
**ML / Data:** `scikit-learn` `PyTorch` `statsmodels` `pandas` `NumPy`
**Methodology:** `Statistical Inference` `Causal Inference` `Experiment Design` `Model Evaluation`
**Tools:** `Git` `Jupyter` `SQLite` `Linux`

<div align="center">

*Every number on this profile's pinned repos came from code that was actually run — no placeholder metrics.*

</div>
