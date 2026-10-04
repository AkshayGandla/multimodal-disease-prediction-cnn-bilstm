# Multimodal Disease Prediction: Chest X-ray CNN + Radiology-Report BiLSTM

A staged applied-ML project proposing and analysing a **multimodal deep-learning model** that fuses chest X-ray images with radiology text reports to predict thoracic disease.

**Final report:** [`report/Final_Report.pdf`](report/Final_Report.pdf)

## Design
- **Image branch**: CNN feature extractor on chest X-rays.
- **Text branch**: tokenised radiology reports into a **BiLSTM**.
- **Fusion**: concatenated features feeding a multi-label classifier for five findings: cardiomegaly, atelectasis, pleural effusion, pneumonia, infiltration.
- **Datasets (public)**: MIMIC-CXR and the Indiana University Chest X-ray collection (not redistributed here).
- **Training set-up**: Adam (lr 0.001), batch size 32, up to 20 epochs with early stopping.
- **Evaluation metrics**: accuracy, precision, recall, F1 and AUC.

## Reported results (from the final report)
Overall accuracy **82.8%**, macro-F1 **0.87** across the five conditions, with the fused model reported as better than image-only or text-only baselines.

## Honest scope note
This repository holds the **final written report only** (slide decks are not published); the training code is not part of this submission, so the numbers above are as reported in the document and are **not reproducible from this repo**. The report itself lists GPU constraints that limited batch size and epochs as a limitation. Treat this as a documented design and analysis, not a clinical tool.

## Skills demonstrated
Multimodal learning, CNNs, BiLSTM / NLP for clinical text, medical-imaging datasets, evaluation metrics for multi-label classification, project planning and technical presentation.

## Context
Completed as part of the MSc in Artificial Intelligence & Machine Learning at the University of Adelaide (Applied Machine Learning, COMP SCI 7416, 2025). Individual work.

## Licence
MIT. See [LICENSE](LICENSE). Third-party datasets and course materials are not redistributed.
