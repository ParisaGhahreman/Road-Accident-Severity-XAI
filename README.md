# Explainable Machine Learning for Road Accident Severity Prediction

Cross-country road-accident severity modeling and explainable AI framework using harmonized crash data from the **UK, France, and Ethiopia**. The workflow covers data audit, harmonization, cost-sensitive multiclass modeling, external/cross-country validation, domain-shift analysis, SHAP interpretation, driver-factor analysis, and an XAI-guided intervention-priority framework.

## Repository structure

- `notebooks/01_Data_Audit.ipynb` — source-data audit and target/feature compatibility checks.
- `notebooks/02_Data_Preparation.ipynb` — three-country harmonization and processed-data generation.
- `notebooks/03_Modeling_and_XAI.ipynb` — baseline UK model comparison.
- `notebooks/04_External_Validation_France.ipynb` — cost-sensitive model selection and UK→France external validation.
- `notebooks/05_Ethiopia_Driver_Factors.ipynb` — driver-factor ablation and repeated CV in Ethiopia.
- `notebooks/06_Cross_Country_Comparative_Analysis.ipynb` — three-country domain shift and six-direction transfer.
- `notebooks/07_SHAP_Explainability.ipynb` — UK/Ethiopia SHAP interpretation and stability analysis.
- `notebooks/08_Intervention_Framework.ipynb` — evidence-to-action prioritization, transferability, and sensitivity analysis.
- `outputs/article/` — curated manuscript-ready figures and tables.
- `outputs/tables/` and `outputs/figures/` — full reproducibility outputs.

## Data

Raw and processed datasets are intentionally excluded from this repository. The notebooks expect source files under `data/raw/` and generate harmonized files under `data/processed/`. See `data/README.md` for the expected local layout and `DATA_SOURCES.md` for the exact download pages, citations, and reuse terms.

Datasets used in the analysis:
- UK STATS19 road-safety data
- France BAAC road-accident data
- Ethiopia road-accident dataset used in the project

## Main analytical design

The target is harmonized to three severity classes: **Slight, Serious, Fatal**. Eleven common predictors are used for the principal cross-country transfer analysis. Because of class imbalance, model assessment emphasizes macro-averaged metrics and class-specific recall rather than accuracy alone. CatBoost is used for the final cost-sensitive modeling workflow, with SHAP for model interpretation.

The intervention framework is **predictive and evidence-prioritizing, not causal**. SHAP importance and the resulting intervention-priority scores must not be interpreted as causal treatment effects.

## Reproducibility

Create an environment and install dependencies:

```bash
pip install -r requirements.txt
```

Download the three source datasets into the locations documented in `data/README.md`, then run the notebooks in numerical order. Notebook cell outputs are cleared in this GitHub-ready copy to avoid stale-result conflicts; saved CSV/PNG analytical outputs are retained under `outputs/`.

## Manuscript-ready outputs

The curated set is under:

- `outputs/article/figures/`
- `outputs/article/tables/`
- `outputs/article/supplementary_figures/`
- `outputs/article/supplementary_tables/`

## Citation and license

Please cite the repository using `CITATION.cff`. The source code is released under the [MIT License](LICENSE). Dataset licenses are independent of the code license; do not redistribute datasets unless their terms allow it.
