<p align="center">
  <h1 align="center">🚀 AutoPilot-ML</h1>
  <p align="center">
    <strong>Production-Grade Automated Data Science & MLOps Engine</strong><br/>
    <em>Proprietary, enterprise-grade automated modeling and pipeline suite with interactive dashboard.</em>
  </p>
  <p align="center">
    <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.9+">
    <img src="https://img.shields.io/badge/AutoGluon-v1.5-FF6F00?style=for-the-badge" alt="AutoGluon v1.5">
    <img src="https://img.shields.io/badge/MLflow-Tracking-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow">
    <img src="https://img.shields.io/badge/BERTopic-NLP-00B2A9?style=for-the-badge" alt="BERTopic">
    <img src="https://img.shields.io/badge/Validation-256_Tests_/_4k+_Lines-2ea44f?style=for-the-badge" alt="Validation Assertion Count">
  </p>
  <br/>
  <img src="Assets/AutoPilot-ML.png" alt="AutoPilot-ML Banner" width="100%">
</p>

---

## 🌟 Executive Summary

**AutoPilot-ML** is a modular, enterprise-grade data science automation suite designed to execute the entire data lifecycle — from raw web data extraction to production-ready predictive models. The architecture separates the highly optimized, proprietary core engines from the public API layer, presenting a clean interface for data scientists, ML engineers, and technical stakeholders.

The public interface is showcased through interactive Jupyter Notebooks, demonstrating the capabilities of the automated engines in data ingestion, deep statistical profiling, deterministic data cleansing, and multi-domain model optimization.

| User Role | Ecosystem Deliverables |
|---|---|
| **🔬 Data Scientist** | Unified AutoML execution with SHAP explainability matrices, Optuna-tuned clustering models, and MLflow experiment tracking across 4 machine learning domains. |
| **📊 Business Analyst** | Interactive HTML dashboards, auto-generated Entity-Relationship diagrams, and plain-language data quality action plans. |
| **🤖 ML Engineer** | Deterministic, reproducible pipelines with memory-safe O(1) sampling, hardware-aware resource allocation, and exportable model artifacts. |

> **📐 System Capacity:** Powered by a proprietary engine comprising ~30,000 lines of highly optimized code, validated by a rigorous 4,000+ line automated test specification matrix (256 test cases) to ensure production stability.

---

## ✨ Headline Features

### 🧠 Automated Insight Generation
The statistical profiling engine translates complex numerical metrics into human-readable, actionable recommendations. It automatically compiles an **LLM-ready Markdown context file** mapping the schema:

- 🔗 **Auto-detected Entity Relationships** visualized as Mermaid ER diagrams.
- 📏 **Data Quality Scores** (0–100) based on completeness, uniqueness, and semantic type consistency.
- 🎯 **Prioritized Action Plans** classifying quality warnings by severity (CRITICAL / WARNING / INFO) per column.
- 🧩 **Semantic Type Inference** auto-detecting 18 semantic types (including email, IP, URL, phone, MAC, UUID, hash, binary, count, temporal, coordinate, continuous, primary/foreign key candidates).

### 📊 Premium Visual Dashboards
Each module generates a dark-themed, responsive HTML dashboard embedded directly inside Jupyter Notebooks or saved as standalone HTML assets:
- Model performance leaderboards with metric card visualizations.
- TreeSHAP feature importance plots and feature importance bar charts.
- Binary classification decision threshold calibration curves.
- Step-by-step cleaning audit logs and execution timelines.
- Unsupervised cluster archetype profiles with comparisons to global distributions.

### 🛡️ Production-Grade Safety
A defensive engineering layer protects pipelines against silent data corruption:

| Protection | MLOps Safety Safeguard |
|---|---|
| **Target Variable Shielding** | Labels are protected from imputation, clipping, or transforms to preserve ground truth. |
| **Foreign Key Protection** | Join keys are blocked from statistical coercion, imputation, or encoding to maintain relational integrity. |
| **O(1) Memory Sampling** | High-cardinality operations (MICE/KNN imputation, multicollinearity checks) automatically use bounded sampling budgets to prevent OOM errors. |
| **Temporal Leakage Quarantine** | Features recorded after the target anchor timestamp are quarantined to prevent leakage. |
| **Inf-Safe Imputation** | Upstream infinite values (`np.inf`) are neutralized before computing descriptive statistics. |
| **Hardware-Aware Allocations** | Resources are dynamically throttled based on system CPU/GPU/RAM availability to avoid local execution failure. |

### Audit-Hardened Safeguards
The pipeline contains strict enforcement rules:
- **Extension-aware loading**: Path verification for CSV, Excel, JSON, and Parquet files prior to execution.
- **Input Validation**: Strict schema checks for holdout size, forecast horizons, URLs, selector methods, and crawler timing parameters.
- **Degenerate Input Isolation**: Safely handles tiny, empty, constant, or non-finite datasets in modeling and visualization tasks.
- **Batch Inference Schema Verifications**: Prevents inference on mismatched schemas or missing features during batch scoring.
- **Context Sanity**: Generates aggregate-only AI summaries and falls back to local narrative generation if network-based API endpoints are unavailable.

### 🔗 Modular Pipeline Architecture
The execution steps feed into one another sequentially, though each module can be executed standalone:

```
🕷️ Scrape  ──→  🔍 Profile  ──→  🧹 Clean  ──→  🤖 Model
     │               │               │              │
     ▼               ▼               ▼              ▼
  Raw HTML /     Quality Report   ML-Ready Data   Trained Models
  Google Play    → Action Plan    → Cleaned CSV   → Predictions
  → CSV/JSONL    → Mermaid ERD                     → HTML Dashboard
                 → LLM Context                     → MLflow Artifacts
```

---

## 🗺️ Ecosystem Architecture & Public API Layer

AutoPilot-ML is structured with a strict decoupling between the high-performance proprietary engine backend and the user-facing execution wrapper. This allows stakeholders to inspect the workflow, configure parameters, and review predictions via standard Jupyter interfaces while maintaining a clean abstraction.

### Interactive Notebook Showcase

The primary entry points for exploring the capabilities of the system are the interactive notebooks:

> [!TIP]
> **Rendering Note**: Due to saved execution states and rich HTML dashboards, some notebooks are large and may experience rendering timeouts (infinite loading spinners) on GitHub. Use the **Direct Render** links to view them instantly on nbviewer with all dashboard styling preserved, or download the .ipynb files to open them locally.

| Interactive Notebook | Direct Render | Showcase Domain | Target Operations |
|---|---|---|---|
| [`data_scraper.ipynb`](data_scraper.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/data_scraper.ipynb) | Data Ingestion | Stealth async web scraping and subprocess isolation. |
| [`data_profiler.ipynb`](data_profiler.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/data_profiler.ipynb) | Statistical Profiling | Semantic type detection, quality score calculations, and ERD generation. |
| [`data_cleaner.ipynb`](data_cleaner.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/data_cleaner.ipynb) | Deterministic Cleaning | 12-step sequential data repair, outlier treatment, and imputation. |
| [`ml_tabular.ipynb`](ml_tabular.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/ml_tabular.ipynb) | Tabular AutoML | Supervised classification, regression, multi-label models, and SHAP explainability. |
| [`ml_timeseries.ipynb`](ml_timeseries.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/ml_timeseries.ipynb) | Time Series Forecasting | Multi-item forecasting, quantile uncertainty bounds, and automated covariate enrichment. |
| [`ml_clustering.ipynb`](ml_clustering.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/ml_clustering.ipynb) | Unsupervised Discovery | MiniBatch K-Means, HDBSCAN, UMAP/PCA dimensionality reductions, and archetype profiling. |
| [`ml_nlp.ipynb`](ml_nlp.ipynb) | [⚡nbviewer](https://nbviewer.org/github/Rakishu02/AutoPilot-ML/blob/main/ml_nlp.ipynb) | NLP Engines | Supervised intent classification, zero-shot routing, and unsupervised topic discovery. |

### Output Artifact Structure

When the pipeline runs, it generates structured artifact directories within the local workspace:

```
📦 Workspace Output/
├── cleaned_dataset/          ← Cleaned CSV datasets from the Data Cleaning Engine
├── Exports/                  ← Extracted data files from the Data Scraper
└── automl_run/               ← Outputs from the AutoML Engine
    ├── models/               ← Trained model artifacts (serialized models, weights)
    ├── models_nlp/           ← NLP models (Transformers, BERTopic, BGE-M3)
    ├── models_multilabel/    ← Multilabel classifier outputs
    ├── models_ts/            ← TimeSeries predictor models
    ├── plots/                ← Metric charts and visual dashboards
    ├── predictions/          ← Inference outputs and cluster profiles
    └── mlruns/               ← MLflow tracking repositories
```

---

## 🕷️ The Data Scraper — Async & Stealth Ingestion

The web scraping system manages async, isolated data ingestion pipelines using a **Dual-Mode Engine Architecture**:

### 🤖 Google Play Reviews Scraper
- **Robust Integration**: Utilizes the specialized `google-play-scraper` library, incorporating intelligent retry logic if the store limits requests to guarantee consistent and reliable data collection.
- **Human-like Scraping Patterns**: Dynamically injects randomized delays (jitter) between requests to emulate human browsing and naturally bypass bot detection.
- **Fault-Tolerant Checkpointing**: Collects user reviews page-by-page and writes incremental checkpoints to disk, protecting the pipeline against network drops or mid-run interruptions.
- **Automated Text Normalization**: Automatically normalizes messy timestamps and text encodings into structured tables, preparing clean datasets for immediate analysis.

### 🕷️ General HTML Website Scraper
- **Background Subprocess Isolation**: Runs scraping jobs in dedicated background processes to completely prevent event loop conflicts and keep interactive environments like Jupyter notebooks highly responsive.
- **Stealth Bypass Capabilities**: Integrates `scrapling`'s stealth session engine to seamlessly handle security challenges (like Cloudflare/Turnstile) and adapt to dynamic layout modifications.
- **Customizable Targeted Extraction**: Uses precision CSS selectors to automatically route, parse, and map single text fields, custom lists, or structured arrays based on configuration.

### Shared Pipeline Safety
- **Memory-Safe Local Archival**: Continuously dumps extracted records directly to disk to prevent memory footprint bloat.
- **Structured Data Reconstruction**: Automatically parses and restores complex nested list structures (via list evaluation) during data reload, maintaining schema consistency.
- **Interactive Execution Dashboard**: Visualizes execution logs, scrape speeds, and dataset previews in a premium dark-themed HTML interface.

---

## 🔍 The Data Profiler — Schema & Relationship Discovery

The statistical profiling module analyzes data schemas beyond simple summaries:
- **Intelligent Semantic Detection**: Auto-detects **18 distinct semantic types** (such as emails, IP addresses, coordinates, phone numbers, and keys) to classify fields correctly and shield them from invalid mathematical transformations.
- **Comprehensive Quality Scorecard**: Computes a single weighted quality score (0–100) combining data completeness, uniqueness, and format consistency.
- **Placeholder Extraction**: Automatically flags hidden missing-value placeholders (like `"n/a"`, `"?"`, or `"unknown"`).
- **Multicollinearity Checks**: Evaluates high-correlation feature pairs using memory-safe bounded sampling.
- **Relational Map Generation (ERD)**: Spans multiple datasets to automatically identify primary/foreign key connections (using smart name normalization and value-overlap verification), handles multi-language dates (English, Indonesian, Italian, German, Dutch), and outputs a dynamic Mermaid Entity-Relationship diagram.

---

## 🧹 The Data Cleaner — 14-Step Deterministic Pipeline

The data cleaning pipeline executes a rigid, sequential set of transformations to prepare raw data for downstream modeling:

```
┌───────────────────────────────────────────────────────────────────────┐
│ Step  1: Drop Columns ──→ Remove high-missingness/redundant           │
│ Step  2: Deduplicate ──→ Enforce row uniqueness (first/last)          │
│ Step 2b: Leakage Handling ──→ Prune temporal look-ahead cols          │
│ Step  3: Datetime Conversions ──→ Parse strings to datetime64         │
│ Step  4: Coercion Cleansing ──→ Force mixed-type to numeric           │
│ Step 4b: Value Mapping ──→ Replace dirty tokens / null aliases        │
│ Step  5: Text Cleaning ──→ Unicode normalize, strip, lowercase        │
│ Step  6: Imputation ──→ Median/Mode, KNN, or MICE repair              │
│ Step  7: Cardinality Grouping ──→ Entropy-based rare-label            │
│ Step  8: Transforms ──→ Log1p, Box-Cox, Yeo-Johnson                   │
│ Step  9: Outlier Treatment ──→ IQR / MAD / Winsorization              │
│ Step 10: Resolve Categorical Association ──→ Prune redundant classes  │
│ Step 11: Resolve Multicollinearity ──→ Spearman ρ pairwise pruning    │
│ Step 12: Memory Optimization ──→ Downcast dtypes to save RAM          │
└───────────────────────────────────────────────────────────────────────┘
```

### Class Imbalance & Smart Imputation
- **Target Imbalance Controls**: Automatically identifies skewed target distributions, flagging imbalance risks and enabling post-train decision threshold calibration to balance precision and recall.
- **Advanced Multivariate Imputation**: Combines KNN (K-Nearest Neighbors) and MICE (Multiple Imputation by Chained Equations) algorithms to handle complex missing-value patterns.
- **O(1) Memory Safeguards**: Automatically degrades advanced imputers to simple baselines if the dataset size risks triggering Out-of-Memory (OOM) errors, logging the event for debugging. Target variables and relational foreign keys are strictly shielded from modification.

### Adaptive Imputation Strategy

The cleaning engine dynamically chooses or falls back between three imputation tiers based on data shape and system memory:

| Imputation Level | Algorithm / Method | Best Use Case |
|---|---|---|
| **Simple Imputation** | Mean, Median, Mode, or Constant values | Fast, low-overhead baseline correction |
| **KNN Imputation** | K-Nearest Neighbors regression | Locally correlated numerical features |
| **MICE Imputation** | Multiple Imputation by Chained Equations | Complex, highly correlated multi-variable missingness |

---

## 🤖 The ML Engine — Multi-Domain Modeling Suite

The proprietary ML Engine is accessed via the high-level `AutoMLFactory` interface. It routes execution to one of four ML domains based on the configuration:

### 📋 Tabular Domain (Classification / Regression / Multi-Label)
*Powered by the **AutoGluon v1.5 infrastructure**, with model presets ranging from `medium` to `extreme`.*
- **Ensembled Prototyping**: Automates multi-model training, stacked ensembling, and foundation models (e.g., TabPFN, TabICL) on the highest presets.
- **Class Imbalance Handling**: Integrates cost-sensitive objective functions and weighted training parameters to optimize classification on highly imbalanced targets.
- **SHAP Explainability**: Generates SHAP explainability matrices and feature importance rankings with automated sampling controls.
- **Threshold Calibration**: Calibrates decision thresholds on binary targets to optimize for specific MLOps targets (F1, precision, or recall).

### 📈 Time Series Domain (Probabilistic Forecasting)
- **Multi-Item Optimization**: Handles parallel forecasting for thousands of time-series items with static features.
- **Quantile Forecasting**: Generates uncertainty-aware predictions (e.g., quantiles `[0.05, 0.5, 0.95]`).
- **Automated Covariates**: Enriches inputs with localized country holiday calendars and temporal indicators (e.g., `is_weekend`).
- **Temporal Alignment**: Automatic frequency inference and backtesting walk-forward validation splits.

### 🔮 Clustering Domain (Unsupervised Discovery)
- **Algorithm Swapping**: Trains and benchmarks MiniBatch K-Means, HDBSCAN, Agglomerative, DBSCAN, spectral, and KMeans clustering models simultaneously.
- **Bayesian Optimization & Custom Objective**: Integrates **Optuna** (via the `clustering_tune_trials` configuration) to sweep UMAP and clustering hyperparameters, maximizing a composite geometric objective: $\text{Score} = \text{Silhouette} + \frac{1}{1 + \text{Davies-Bouldin}} + 0.05 \times \ln(1 + \text{Calinski-Harabasz})$ to find mathematically robust cohort boundaries.
- **Automated Algorithm & K Sweeping**: Benchmarks multiple cluster counts (from K=2 up to `clustering_max_k`) using Silhouette, Davies-Bouldin, and Calinski-Harabasz validation metrics to automatically identify the optimal cohort configuration when tuning is disabled.
- **Dimensionality Reduction**: Performs **UMAP/PCA dimensionality reductions** to compress features while retaining topological structure.
- **Inference Proxies**: Saves a trained K-Nearest-Neighbors model alongside the clustering outputs, allowing real-time cluster assignments for new streaming data points.

### 💬 NLP Domain (Supervised, Zero-Shot, & Unsupervised Modes)
- **Supervised Classification**: Powered by **AutoGluon Tabular** text-feature processing to train classification models on labeled text datasets (e.g. sentiment, intent).
- **Zero-Shot Routing**: Uses DeBERTa models to route text records to dynamic candidate classes without labeled training data, auto-accepting high-confidence labels and flagging low-confidence rows.
- **Unsupervised Topic Discovery**: Integrates **BERTopic NLP architectures** using dense BGE-M3 text embeddings.
- **Semantic Labeling**: Utilizes LLMs (such as Google Gemini) to generate readable topic names, with c-TF-IDF keyword summaries as a deterministic local fallback.


---

## 🧪 Engine Verification & Integrity Matrix

To ensure production-grade stability, the core engines are validated by a rigorous test suite of **256 automated test cases** (spanning 4,000+ lines in `engine_test.py`). This validation layer secures API contracts and guarantees pipeline reliability.

The integrity verification covers the following test modules:

| Verification Suite | Target Engine Class / Test Scope | Validated Pipeline Functionality |
|---|---|---|
| **Web Scraper Suite** | `TestDataScraperEngine` | Process-isolated async crawling, sequential Play Store scraping, bot bypass, and format consistency. |
| **Data Profiler Suite** | `TestDataProfilerEngine` | 18 semantic type inferences, multi-language date translations, key naming normalization, and Mermaid ERD rendering. |
| **Deterministic Cleaner Suite** | `TestDataCleanerEngine` | 14-step sequential cleaning order, target shielding, KNN/MICE imputation fallbacks, and memory footprint scaling. |
| **Tabular AutoML Suite** | `TestMLTabularEngine` | Supervised regression & classification, autoregressive multilabel target chaining, and threshold optimization. |
| **Time Series Suite** | `TestMLTimeSeriesEngine` | Quantile forecast intervals, walk-forward validation splits, known covariates, and static metadata features. |
| **Clustering Discovery Suite** | `TestMLClusteringEngine` | Auto-K sweeps, silhouette/Davies-Bouldin metrics, Optuna hyperparameter tuning, and KNN batch inference proxies. |
| **NLP Engine Suite** | `TestMLNLPEngine` | Supervised text classification, Zero-Shot routing arrays, unsupervised BERTopic modeling, and Gemini fallback API routines. |

---

## 📂 Repository Showcase Structure

The public repository exposes the interactive tutorial notebooks that consume the AutoPilot-ML engine:

```
📦 AutoPilot-ML
│
│── Interactive Notebook Showcase ──────────────────────────────────
├── data_scraper.ipynb            📓 Async stealth web scraping & pipeline wrappers
├── data_profiler.ipynb           📓 Statistical data profiling, ERD output, & LLM context
├── data_cleaner.ipynb            📓 Deterministic 12-step cleaning pipeline and imputer options
├── ml_tabular.ipynb              📓 Tabular classification, regression, and threshold optimization
├── ml_timeseries.ipynb           📓 Probabilistic time-series forecasting & covariates
├── ml_clustering.ipynb           📓 Unsupervised clustering, UMAP/PCA, and archetype profiling
├── ml_nlp.ipynb                  📓 Supervised NLP, zero-shot routing, and unsupervised BERTopic
│
│── Project Documentation ──────────────────────────────────────────
├── README.md                     📄 Showcase documentation & system reference
│
│── Workspace Artifacts (Gitignored) ────────────────────────────────
├── Dataset/                      📁 Local source datasets
├── cleaned_dataset/              📁 Cleaned output datasets
├── Exports/                      📁 Raw web scraped outputs
└── automl_run/                   📁 Saved models, SHAP charts, MLflow trackers
```

---

## 🔧 High-Level Interface Configuration Schema

The system behavior is managed via runtime config dictionaries parsed by the wrapper classes:

### AutoMLFactory Schema

| Key | Type | Description | Available Options | Example |
|:---|:---|:---|:---|:---|
| **Core / Shared Parameters** | | | | |
| `experiment_name` | `str` | MLflow experiment identifier. | Any string | `"Customer_Segmentation"` |
| `task_type` | `str` | ML task routing. | `"tabular"`, `"nlp"`, `"time_series"`, `"clustering"` | `"tabular"` |
| `dataset_path` | `str` | Path to training/source CSV dataset. | Any valid path | `"Dataset/train.csv"` |
| `target_column` | `List[str]` or `str` | Target column name(s). Always a list for Tabular/Time Series; string for NLP (omit/empty for Unsupervised). | Column name(s) in dataset | `["target"]` |
| `presets` | `str` | Model quality training preset. | **Tabular/NLP:** `"extreme"`, `"best"`, `"high"`, `"medium"` <br> **Time Series:** `"best"`, `"high"`, `"medium"` | `"medium"` |
| `time_limit_seconds` | `int` | Maximum training wall-clock time limit allowed in seconds. | Any positive integer | `300` |
| `auto_stack` | `bool` | Auto-stack ensemble models for boosted performance. | `True`, `False` | `False` |
| `calibrate_decision_threshold` | `bool` | Calibrate decision threshold (binary classification only). | `True`, `False` | `False` |
| `base_output_dir` | `str` | Centralized artifact output root directory. | Any valid directory path | `"automl_run"` |
| `prediction_data_path` | `str` | Path to unseen prediction data for batch inference. | Any valid path, `None` | `"Dataset/unseen.csv"` |
| `fast_dev_run` | `bool` | Quick prototyping mode (subsamples data). | `True`, `False` | `False` |
| `ai_context` | `str` | Business context string to guide the AI natural language report summary. | Any string, `None` | `"Predicting customer churn based on historical features."` |
| **Tabular Specific** | | | | |
| `problem_types` | `List[str]` | Problem type(s) per target. Leave `[]` for auto-inference. | `"binary"`, `"multiclass"`, `"regression"` | `[]` |
| `eval_metrics` | `List[str]` | Optimization metric(s). One per target column. | **Binary/Multiclass:** `"f1_macro"`, `"f1_weighted"`, `"precision_macro"`, `"precision_weighted"`, `"recall_macro"`, `"recall_weighted"`, `"accuracy"` <br> **Regression:** `"mae"`, `"mape"`, `"rmse"`, `"mse"`, `"r2"` | `["f1"]` |
| `multimodal_mode` | `bool` | Enable image/text routing. | `True`, `False` | `False` |
| `image_column` | `str` | Column name for image paths. | Any column name in dataset | `"image_path"` |
| **NLP Specific** | | | | |
| `text_column` | `str` | Column containing raw text. | Column name in dataset | `"review_body"` |
| `candidate_labels` | `List[str]` | Candidate labels for Zero-Shot classification. Only used when `target_column` is empty/omitted. | List of label strings, `None` | `["positive", "negative", "neutral"]` |
| `nlp_embedding_batch_size` | `int` | Batch size for BGE-M3 embedding extraction (Unsupervised). | Any positive integer | `16` |
| `nlp_zero_shot_batch_size` | `int` | Batch size for Zero-Shot inference pipeline. | Any positive integer | `8` |
| **Time Series Specific** | | | | |
| `item_id_column` | `str` | Column identifying each individual time series. | Column name in dataset | `"store_id"` |
| `timestamp_column` | `str` | Column containing date/time values. | Column name in dataset | `"date"` |
| `prediction_length` | `int` | Forecast horizon (number of steps into the future). | Any positive integer | `14` |
| `freq` | `str` | Pandas frequency string. Auto-detected if `None`. | `"D"`, `"H"`, `"W"`, etc. | `"D"` |
| `generate_covariates` | `bool` | Auto-generate `is_weekend` and `is_holiday` covariates. | `True`, `False` | `True` |
| `quantile_levels` | `List[float]` | Quantile levels for probabilistic forecasting. | `[0.05, 0.5, 0.95]`, etc. | `[0.05, 0.5, 0.95]` |
| `static_features_path` | `str` | Path to CSV with item-level metadata. | Any valid path, `None` | `"Dataset/static.csv"` |
| `eval_metric` | `str` | Time Series evaluation metric. | `"MSE"`, `"RMSE"`, `"MAPE"`, `"MAE"`, `"WQL"` | `"RMSE"` |
| **Clustering Specific** | | | | |
| `features` | `List[str]` | Explicit columns for clustering; empty list uses all numeric columns. | List of column names, `[]` | `[]` |
| `exclude_features` | `List[str]` | Columns to explicitly ignore or exclude from clustering. | List of column names, `[]` | `["customer_id"]` |
| `n_clusters` | `int` | Fixed number of clusters (K). `None` enables Auto-K sweep. | Any positive integer, `None` | `None` |
| `clustering_max_k` | `int` | Upper bound for Auto-K optimization sweeps. | Any positive integer | `10` |
| `clustering_algorithms` | `List[str]` | List of candidate clustering algorithms to evaluate. | `"kmeans"`, `"mbkmeans"`, `"dbscan"`, `"hdbscan"`, `"agglomerative"`, `"spectral"` | `["mbkmeans", "hdbscan", "agglomerative"]` |
| `clustering_reduction_method` | `str` | Dimension reduction method prior to clustering. | `"pca"`, `"umap"`, `"auto"` | `"auto"` |
| `clustering_tune_trials` | `int` | Number of Optuna trials to run. `None` disables tuning. | Any positive integer, `None` | `None` |

---

## 📜 Proprietary Distribution & Licensing

This showcase repository contains the public tutorial layer for demonstrating pipeline execution, visualization, and validation. The underlying core execution engines and styling libraries are proprietary intellectual property.

For commercial inquiries or system customization requests, please contact the repository administrator.

---

<p align="center">
  <strong>Engineered to deliver enterprise-grade automation for high-impact machine learning workflows.</strong>
</p>
