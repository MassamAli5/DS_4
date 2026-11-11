# DS-A4: Model Comparison and Calibration Lab

## 1. Project Overview

This project compares three classification models using a frozen evaluation protocol. The objective is to evaluate predictive performance, probability calibration, classification errors, and threshold-based decision-making under limited human review capacity.

Course: Data Science
Assignment: DS-A4 — Model Comparison and Calibration Lab

## 2. Dataset and Provenance

The data used in this analysis are from Table S2 of the published supplementary workbook Supplementray_Files.xlsx associated with:

Ali et al., Journal of Asian Earth Sciences (2025).

DOI: https://doi.org/10.1016/j.jseaes.2025.106927

The supplementary workbook is not included in this repository.

To reproduce the analysis:

Obtain the original supplementary workbook from the article's supplementary material.

Save it locally at:

data/raw/Supplementray_Files.xlsx

Execute the analysis using the provided Jupyter Notebook.

The original workbook is never edited. All data cleaning, preprocessing, and transformations are performed programmatically within the analysis code, preserving the original source measurements and data provenance.
## 2. Dataset

The original supplementary Excel dataset contains 103 observations and 77 columns.

The classification task involves four mineral phases:

- Oolite Rim
- Oolite core
- Pellet Core
- Pellet Rim

The original measurements are retained as the source data.

## 3. Models Compared

Three classification models are evaluated:

1. Logistic Regression — simple baseline.
2. Random Forest — ensemble model.
3. Support Vector Machine (SVM) — alternative classification model.

## 4. Evaluation Protocol

The analysis uses five frozen evaluation folds with group separation to prevent observations from the same group appearing in both training and test sets.

The models are compared using identical evaluation folds and the same performance metrics.

Evaluation includes:

- Accuracy and macro F1-score.
- Precision–Recall and ROC-AUC.
- Probability calibration.
- Brier score and Expected Calibration Error (ECE).
- Bootstrap uncertainty intervals.
- Paired model comparisons.
- Critical error slices and failure analysis.
- Cost-based threshold selection and sensitivity analysis.

## 5. Project Structure

```text
DS_4/
├── data/
│   └── raw/
│       └── Supplementray_Files.xlsx
├── notebooks/
├── results/
├── figures/
├── reports/
├── scripts/
├── logs/
├── requirements.txt
├── README.md
└── .gitignore
```

## 6. Reproducibility

### Environment

Python 3.13.9 was used for the current analysis.

Install the recorded dependencies using:

```bash
python -m pip install -r requirements.txt
```

### Execution

1. Open `notebooks/01_data_inspection.ipynb` in VS Code.
2. Select the project's `.venv` Python kernel.
3. Execute the notebook from beginning to end.
4. Verify the frozen evaluation assignments.
5. Check the generated results and figures.

The notebook currently uses the local project directory. Update its project paths if reproducing the analysis on another computer.

## 7. Results and Outputs

Numerical results and evaluation records are stored in `results/`.

Generated figures are stored separately in `figures/`.

The threshold analysis uses explicitly stated illustrative error costs and human review capacity. These assumptions should not be interpreted as measured operational costs.

## 8. Data and AI-use Integrity

Original measurements and evaluation assignments are retained. Failed runs, negative results, and relevant limitations should be documented.

AI assistance and independent verification are documented separately in the project logs.

## 9. Assignment Deliverables

The repository is intended to contain:

- Executable Jupyter notebook.
- Original supplementary dataset.
- Frozen evaluation protocol.
- Paired predictions and statistical results.
- Calibration and cost curves.
- Error analysis and counterexamples.
- Final PDF report.
- Python dependency record.
- AI-use and verification log.

**Assignment:** DS-A4 — Model Comparison and Calibration Lab.