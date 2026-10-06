CIVAP-Net Anonymous Reproducibility Package
Overview
This repository contains the code, configurations, documentation, validation checks, and execution records prepared for the CIVAP-Net reproducibility package. The source data files are not included.
Repository Contents
- configs/: YAML configuration files for datasets, model settings, training, baseline methods, robustness checks, and statistical analysis.
- data/: A data-placement guide describing the expected local structure for source and processed data files.
- docs/: Documentation covering data access, method-to-code traceability, the reproduction runbook, archive policy, and anonymity checks.
- logs/: Package-validation records and reference-target files organized by evaluation component.
- manifests/: JSON manifests defining foundation-model references, run contracts, and random seeds.
- outputs/: Reserved directory for generated checkpoints, predictions, metrics, figures, logs, and other run artifacts.
- scripts/: Numbered workflow scripts for package validation, data audit and harmonization, fold construction, CIVAP-Net training, baseline training, external evaluation, ablation, robustness analysis, statistical analysis, interpretability and efficiency analysis, figure generation, and archive construction.
- src/civap_net/: Python implementation modules for configuration loading, data harmonization, preprocessing, fold generation, model definition, losses, training, retrieval, calibration, metrics, baseline methods, robustness analysis, statistical utilities, interpretability, and input/output utilities.
- tests/: Automated checks for harmonization, fold separation and leakage prevention, model tensor shapes, and calibration metrics.
Workflow Components
The repository organizes the workflow into the following components:
1. Package validation and input auditing.
2. Cross-source data harmonization and fixed fold construction.
3. Cross-validation training and post-processing for CIVAP-Net.
4. Baseline-model training and external-cohort evaluation.
5. Ablation, robustness, statistical, interpretability, and efficiency analyses.
6. Generation of figures and archived execution materials.
Data and Outputs
The repository does not redistribute source datasets. Dataset access locations and required local file paths are documented in docs/DATA_ACCESS.md and configs/datasets.yaml. Generated files are written under outputs/, which is retained as an initially empty directory in the package.
Documentation and Validation
docs/RUNBOOK.md lists the intended execution sequence. docs/METHOD_TRACEABILITY.md maps manuscript components to their corresponding code modules and output artifacts. scripts/00_validate_package.py and the files in tests/ provide package-level validation checks.
