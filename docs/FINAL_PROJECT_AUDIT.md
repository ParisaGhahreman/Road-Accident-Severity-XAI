# Final Project Audit

## Critical findings

1. `README.md`, `requirements.txt`, and `.gitignore` were empty in the supplied archive. They have been rebuilt for GitHub use.
2. `LICENSE` and `CITATION.cff` were also empty. They were **not fabricated**; complete these before public release.
3. Jupyter checkpoint files and `catboost_info/` training artifacts were removed from the GitHub-ready copy.
4. Notebook execution outputs and execution counters were cleared to avoid stale-output conflicts and reduce repository size. Saved analytical CSV/PNG outputs were retained.
5. Empty trailing cells were removed from all notebooks.
6. Notebook 01 contained a duplicated UK diagnostic block accidentally stored as Markdown; the duplicate was removed.
7. Notebook 02 contained an unrelated New Zealand CAS exploration and redundant file-existence/save checks; these were removed. Summary metadata tables were redirected to `outputs/tables/` for consistency.
8. Notebook 02 was patched so the France accident-level `surface_common` feature is merged into `fr_final` before final common-feature validation.
9. Notebook 03 contained an exploratory junction-feature expansion section that was not part of the retained final model and duplicated later model-development work. It was removed from the cleaned workflow. An accidental prose-in-code cell was converted to Markdown.
10. The later notebooks (04–08) contain the final validation, Ethiopia analysis, cross-country transfer, SHAP, and intervention framework. Their analytical cells were retained because they document model selection, negative/robustness tests, or final outputs.

## Curated manuscript outputs

Main figures are copied to `outputs/article/figures/`; secondary robustness/diagnostic figures to `outputs/article/supplementary_figures/`. Main and supplementary tables are similarly separated. The original complete `outputs/figures/` and `outputs/tables/` directories remain available for reproducibility.

## Release blockers

Before making the repository public:
- complete `CITATION.cff` with the final article/repository title, author metadata, version, and repository URL;
- choose and populate `LICENSE`;
- complete the exact source URLs/DOIs and reuse terms in `DATA_SOURCES.md`;
- the project owner reported successful end-to-end execution of all notebooks with the local datasets after the final France surface merge fix; this packaged audit still cannot independently rerun the pipeline because datasets are intentionally excluded.

## Interpretation guardrail

The intervention framework is based on predictive associations, SHAP attribution, stability, actionability scoring, and cross-country distribution shift. It does not estimate causal intervention effects. Manuscript wording should preserve this distinction.
