# Early Screening of Student Mental-Health Risks Using Multimodal AI Frameworks

## Project Overview
This repository contains the code, data architecture, and documentation for a multimodal AI framework designed to support the early screening of mental health risk indicators in university students. The project investigates how integrating text, voice, and image data can improve the detection of mental health risks compared to single-modality systems. 

This repository serves as the well-documented technical implementation required for the Gisma University of Applied Sciences Computer and Data Sciences (CDS) dissertation.

## Research Questions
This project is driven by the following core research question:
* How can a multimodal AI framework integrating text, voice, and image data support early screening of mental health risk indicators in university students?

## Sub-questions explored in this repository include:
* To what extent does multimodal fusion improve screening performance compared with single-modality models?
* Which modalities or features contribute most strongly to prediction performance?
* How can the system's output be designed to provide interpretable screening support?

## Hypotheses
* **H1 (Feature Optimization):** A model that uses a selected set of high-relevance variables will achieve better classification performance than a model that includes all available variables without selection.
* **H2 (Demographic/User-Driven Variance):** There will be a meaningful difference between international and German students in how they perceive the relevance of selected screening variables.
* **H3 (Interpretability & Fusion):** A fusion-based multimodal architecture will outperform a single-source baseline model on the target classification task.

## Methodology
This project utilizes a "Human-in-the-Loop" (HITL) approach via a two-part Mixed-Methods study to strictly mitigate GDPR risks.
1. **Phase 1 (Human Fieldwork):** Quantitative Likert-scale data is collected via a survey to test statistical variance between German and International students. 
2. **Phase 2 (AI Modeling):** Descriptive statistics representing the modalities students trust most are converted into a numerical Feature Weighting Matrix. This matrix acts as a human-in-the-loop attention mask, instructing the AI model on which data streams to prioritize.

## Data Architecture
Because we cannot collect actual biometric data from students, the data pipeline is strictly split into two parts

* Survey Dataset (User-Perception):** An anonymized dataset gathering core screening indicators such as Academic Stress, Sleep Quality, Fatigue, Concentration, and Social Withdrawal.
* **Multimodal AI Benchmarks:** The technical architecture is trained and evaluated using pre-existing, validated academic datasets. Candidate datasets include:
  * **DAIC-WOZ:** Clinical interviews supporting the diagnosis of psychological distress.
  * **CMU-MOSEI:** A large dataset for sentence-level sentiment analysis and emotion recognition.
  * **IEMOCAP:** Interactive emotional dyadic motion capture data.

## Ethics and Data Privacy
* This research operates under the ethical approval of the GISMA Business School University Ethics Sub-Committee.
* All collected survey data is processed in compliance with the General Data Protection Regulation (GDPR).
* Participant identities are strictly confidential and will not be revealed in any publications, reports, or repository files.

## Repository Structure
* `data/`: Contains the fully anonymized CSV files from the student survey.
* `src/`: Source code for the multimodal ML pipeline, including single-modality baselines and the fusion-based architecture.
* `notebooks/`: Jupyter notebooks detailing the exploratory data analysis (EDA), statistical variance testing (e.g., ANOVA/T-tests) for H2, and the generation of the Feature Weighting Matrix[cite: 2].
* `docs/`: Supporting documentation, presentations, and methodology flowcharts.

## Getting Started

These instructions will help you set up the environment, process the anonymized survey data, and run the multimodal AI framework for early mental health risk screening[cite: 5].

### 1. Prerequisites
Ensure you have Python 3.8+ installed. It is highly recommended to use a virtual environment to manage dependencies.

### 2. Installation
Clone this repository and install the necessary dependencies:
```bash
git clone [https://github.com/Harsh-GISMA/The_Thesis.git](https://github.com/Harsh-GISMA/The_Thesis.git)
cd The_Thesis
pip install -r requirements.txt
