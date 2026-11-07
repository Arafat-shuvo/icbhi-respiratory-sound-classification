# ICBHI Respiratory Sound Classification

This repository contains a complete, reproducible pipeline for classifying
respiratory cycles from the ICBHI 2017 Challenge database into four classes:
Normal, Crackle, Wheeze, and Both.

The pipeline covers dataset exploration, audio preprocessing (resampling,
band-pass filtering, log-Mel spectrograms), patient-independent 5-fold
cross-validation, four model families (Baseline CNN, ResNet, CNN-BiLSTM and a
proposed CNN-Transformer), noise robustness experiments (white and pink noise,
SNR 20 to -5 dB), explainable AI (Grad-CAM, Integrated Gradients, attention
rollout and a deletion test), an ablation study, and statistical analysis
(patient-level bootstrap CIs, Wilcoxon, Friedman and McNemar tests with Holm
correction).

**Metrics:** Specificity (Sp), Sensitivity (Se), ICBHI Score = (Sp + Se) / 2,
Macro-F1 and Accuracy.

**Dataset:** ICBHI 2017 Respiratory Sound Database (Kaggle). Audio files are
not included in this repository.

**Note:** Results use 5-fold patient-wise cross-validation rather than the
official ICBHI train/test split, so numbers are not directly comparable with
papers that use the official split.


