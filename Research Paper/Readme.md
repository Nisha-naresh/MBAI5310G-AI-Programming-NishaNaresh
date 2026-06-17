
# Explainable Multimodal AI for Clinical Prediction and Patient-Specific Medical Decision Support

Final project for **MBAI 5310G, AI Programming**.

## Student Information
- **Name:** Nisha Naresh
- **Course:** MBAI 5310G, AI Programming
- **Term:** Spring 2026
- **Instructor:** Zahra Atf

## Project Overview
This project develops and evaluates an **explainable multimodal AI system** for patient-specific clinical prediction. In plain terms, the system looks at several kinds of patient data at once (structured records, clinical notes, and medical images or signals), predicts a clinical outcome such as deterioration, and then explains *why* it made that prediction for the individual patient. The study measures the prediction quality, the reliability of the explanations, and whether those explanations actually help clinicians trust and use the result.

The work is framed as an empirical, mixed-methods data-science study. It combines a computational strand (model building and technical evaluation) with a human-centered strand (a structured study of clinician trust and usefulness).

## Title
Explainable Multimodal AI for Clinical Prediction and Patient-Specific Medical Decision Support.

## Clinical Background
Multimodal models that fuse electronic health records, clinical text, imaging, and physiological signals predict outcomes such as ICU admission, deterioration, and mortality with strong performance [2], [13], [15], [16]. Real clinical reasoning is itself multimodal, so fusion mirrors how clinicians work. The problem is that these models are usually opaque, so a clinician is asked to trust a number without seeing the reasoning. Explainable AI is the proposed remedy, but recent evidence shows that explanation does not automatically produce trust [1], [11].

## Problem Statement
Multimodal models predict well and many explanation methods exist, yet the link between them is weak. Prediction studies treat explanation as an add-on, explanation studies evaluate technical proxies rather than clinician needs, and the assumption that good explanations produce appropriate trust is the very assumption recent work undermines [1], [11]. The problem this project addresses is the absence of an integrated approach that builds a multimodal model, generates patient-specific explanations, and evaluates those explanations for both technical quality and clinician trust on the same system.

## Research Gap
No study in the reference set develops a multimodal model, attaches a patient-specific explanation layer reporting both feature-level and modality-level contributions, and evaluates that layer jointly on (a) predictive performance, (b) explanation faithfulness and stability, and (c) clinician trust and usefulness, all on one model and one task. Prior contributions are real but partitioned across these three concerns. This project addresses the partition itself.

## Aim and Objectives
**Aim:** to design, build, and evaluate an explainable multimodal AI system for patient-specific clinical prediction, and to determine when its patient-level explanations improve clinician trust rather than merely accompanying the prediction.

**Objectives:**
1. Build a multimodal model fusing structured data, clinical text, and at least one further modality, benchmarked against single-modality baselines.
2. Design a patient-specific explanation layer reporting feature-level and modality-level contributions.
3. Quantify explanation faithfulness and stability, testing the reliability concern of [11].
4. Evaluate clinician trust and perceived usefulness through a structured human-centered study, informed by [4] and [7].
5. Analyse when explanation quality corresponds to appropriate trust, revisiting [1].
6. Release a reproducible pipeline and evaluation protocol.

## Research Questions and Hypotheses
**Research questions:**
1. Does multimodal fusion improve patient-specific prediction over the best single-modality baseline, and at what cost to interpretability?
2. How faithful and stable are the patient-level explanations, and do these properties differ across modalities?
3. Do explanations increase appropriate clinician trust and usefulness compared with the prediction alone?
4. Under what conditions does explanation quality correspond to appropriate trust?

**Hypotheses:**
- **H1:** Fusion gives significant gains in discrimination and calibration over the best single modality.
- **H2:** Explanation faithfulness and stability vary by modality, with structured features more stable than imaging.
- **H3:** A faithful, stable, patient-specific explanation increases appropriate trust over the prediction alone, but the effect is moderated by explanation stability [1].

## Brief Literature Review
The cited work falls into four streams. Multimodal prediction studies show fusion works: Kizilisik, Terzi, and Candemir [2], Mehta and colleagues [3], Wu and colleagues [13], Chieregato and colleagues [14], Choi and colleagues [15], Shamout and colleagues [16], and Wu and colleagues [17], with the common limitation that explanation is secondary and untested on users. Explanation surveys map the method space: Mesinovic, Watkinson, and Zhu [6], Loh and colleagues [9], Rasheed and colleagues [10], and the XAI 2.0 manifesto of Longo and colleagues [8], which by their nature describe rather than test methods on a task. Trust and human-centered work centres the user: the meta-analysis of Atf and Lewis [1], the clinician-preference study of Xian and colleagues [4], the interaction study of Kim and colleagues [7], and the patient-specific monitoring of Sree Vani and colleagues [12]. Foundational arguments set the stakes: Caruana and colleagues [5] make the case for intelligible models, while Ghassemi, Oakden-Rayner, and Beam [11] caution that post-hoc explanations can be unstable and misleading. This project sits in the space these streams leave open: a single controlled system that measures explanation reliability and clinician response together.

## Conceptual Framework
The framework links five concepts in a chain: **multimodal input → predictive model → explanation layer → explanation quality → human-decision outcome.** Explanation quality (faithfulness and stability) acts as a mediator, so the model affects clinician trust only through explanations that are faithful and stable. Explanation stability is treated as a moderator on the link between explanation quality and appropriate trust. This mediation structure is what the study tests, and it distinguishes the framework from the common assumption that any explanation yields trust.

## Clinical Methodology
- **Design:** retrospective, observational computational strand plus a within-subject human-centered strand (prediction alone vs prediction with explanation).
- **Data:** a public, de-identified critical-care dataset accessed under a credentialed data-use agreement, containing structured measurements, clinical notes, and linked imaging.
- **Target:** short-horizon clinical deterioration (for example ICU transfer within a fixed window), mirroring [2], [15], [16].
- **Preprocessing:** per-modality cleaning and encoding, explicit missingness indicators, full version control of every step.
- **Model:** single-modality baselines, then intermediate and late fusion compared; a partly transparent additive component over structured features in the spirit of [5].
- **Explanation layer:** patient-specific feature-level and modality-level attributions, with methods matched to modality using [6].
- **Technical evaluation:** discrimination (AUROC, AUPRC), calibration, and operating points; explanation faithfulness via perturbation tests and stability under input and seed perturbations, addressing [11].
- **Human-centered evaluation:** clinicians review de-identified cases under both conditions, rating trust, confidence, and usefulness, with appropriate trust computed against whether the model was correct.
- **Analysis:** mixed-effects models for the trust data and thematic analysis for the interviews.

## Expected Contribution
- **Theoretical:** sharper evidence on when explanation supports appropriate trust, refining [1] and addressing [11] with direct measurement.
- **Practical:** a reproducible pipeline for patient-specific multimodal decision support whose explanations are vetted for stability and assessed by clinicians.
- **Methodological:** an evaluation protocol coupling technical explanation metrics with a clinician trust study on the same model and task, answering the call in [8].

## Ethical Considerations
- **Privacy and consent:** only de-identified public data under a data-use agreement; no re-identification. Clinician participation is voluntary and informed, with anonymised responses.
- **Fairness:** performance and explanation quality checked across demographic subgroups and reported transparently.
- **Responsible use:** the system is decision support, not an autonomous decision-maker; the clinician retains responsibility, guarding against the over-reliance risk in [11].
- **Approvals:** the clinician strand proceeds only after research ethics board approval, under a documented data governance plan.

## Timeline
| Phase | Main activities | Duration |
|-------|-----------------|----------|
| 1. Scoping and pre-registration | Confirm dataset, define cohort and outcome, pre-register | Weeks 1 to 4 |
| 2. Data access and preprocessing | Credentialed access, encode modalities, build pipeline | Weeks 4 to 9 |
| 3. Model development | Baselines and fusion models, select strategy | Weeks 9 to 15 |
| 4. Explanation layer | Feature and modality attributions, stability tests | Weeks 14 to 19 |
| 5. Technical evaluation | Prediction and explanation quality, fairness analysis | Weeks 18 to 22 |
| 6. Ethics and clinician study | Approval, recruitment, trust study | Weeks 16 to 26 |
| 7. Analysis and synthesis | Mixed-effects and thematic analysis | Weeks 26 to 30 |
| 8. Writing and dissemination | Paper, code release, presentation | Weeks 28 to 34 |

## Repository Structure
```
final_project/
│
├── README.md                       # this file
├── final_project_notebook.ipynb    # model building, explanation, evaluation
├── paper/
│   └── Research_Proposal_Explainable_Multimodal_AI.docx
├── outputs/
│   ├── model_comparison_results.csv
│   ├── explanation_stability_results.csv
│   └── clinician_study_summary.csv
├── figures/
│   ├── conceptual_framework.png
│   ├── model_performance.png
│   └── explanation_examples.png
└── data_description.md             # dataset, access terms, and feature dictionary
```

## Tools Used
- Python
- Jupyter Notebook / Google Colab
- GitHub
- scikit-learn
- TensorFlow / Keras
- Pandas and NumPy
- Explanation libraries (for example SHAP) and a clinical language model for text encoding
- Statistical analysis tools for mixed-effects modelling
- Other libraries as needed

## How to Reproduce
1. Clone the repository and open `final_project_notebook.ipynb`.
2. Review `data_description.md` and complete the dataset's credentialed access steps. Raw clinical data is not stored in this repository.
3. Install dependencies (a `requirements.txt` is provided in the project folder).
4. Run the notebook sections in order: preprocessing, baselines, fusion model, explanation layer, then evaluation.
5. Generated tables and figures are written to `outputs/` and `figures/`.

## Responsible AI Note
All work in this repository is for educational purposes. I will not upload confidential, private, sensitive, copyrighted, or restricted datasets; clinical data is accessed only under its data-use agreement and is not redistributed here. The system is intended as decision support and not as a replacement for clinical judgment. When using AI tools for support, I disclose how they were used and verify the final work. *(AI assistance was used to help structure and draft documentation and code scaffolding; the analysis, results, and final content were reviewed and verified by the author.)*

## References
[1] Z. Atf and P. R. Lewis, "Is trust correlated with explainability in AI? A meta-analysis," *IEEE Transactions on Technology and Society*, 2025, doi: 10.1109/TTS.2025.3558448.

[2] S. Kizilisik, A. Terzi, and S. Candemir, "Explainable multimodal machine learning model for predicting ICU admission at hospital arrival," *IEEE Access*, vol. 14, pp. 64412–64426, 2026, doi: 10.1109/ACCESS.2026.3687397.

[3] V. Mehta, B. Maram, J. Garg, N. Kumar, P. T. Raut, A. L. X. R. A. Selvarathinam, and P. Jindal, "A multimodal explainable artificial intelligence framework for interpretable Parkinson's disease prediction," *Scientific Reports*, vol. 16, p. 18143, 2026, doi: 10.1038/s41598-026-47769-z.

[4] T. Xian, N. Mehandjiev, P. Constantinides, Y.-W. Chen, Q. Quboa, and G. B. Kitchen, "Clinician preferences for explainable AI in critical care: a comparative study of interpretable models and visualizations for intubation decision support," *International Journal of Medical Informatics*, vol. 210, p. 106287, 2026, doi: 10.1016/j.ijmedinf.2026.106287.

[5] R. Caruana, Y. Lou, J. Gehrke, P. Koch, M. Sturm, and N. Elhadad, "Intelligible models for healthcare: predicting pneumonia risk and hospital 30-day readmission," in *Proc. 21st ACM SIGKDD Int. Conf. Knowledge Discovery and Data Mining (KDD '15)*, New York, NY, USA: ACM, 2015, pp. 1721–1730, doi: 10.1145/2783258.2788613.

[6] M. Mesinovic, P. Watkinson, and T. Zhu, "Explainable AI for clinical risk prediction: a survey of concepts, methods, and modalities," arXiv preprint arXiv:2308.08407, 2023.

[7] S. S. Y. Kim, E. A. Watkins, O. Russakovsky, R. Fong, and A. Monroy-Hernández, "'Help me help the AI': understanding how explainability can support human-AI interaction," in *Proc. 2023 CHI Conf. Human Factors in Computing Systems (CHI '23)*, 2023, pp. 1–17, doi: 10.1145/3544548.3581001.

[8] L. Longo, M. Brcic, F. Cabitza, J. Choi, R. Confalonieri, J. Del Ser, R. Guidotti, Y. Hayashi, F. Herrera, A. Holzinger, R. Jiang, H. Khosravi, F. Lecue, G. Malgieri, A. Páez, W. Samek, J. Schneider, T. Speith, and S. Stumpf, "Explainable Artificial Intelligence (XAI) 2.0: a manifesto of open challenges and interdisciplinary research directions," *Information Fusion*, vol. 106, p. 102301, 2024, doi: 10.1016/j.inffus.2024.102301.

[9] H. W. Loh, C. P. Ooi, S. Seoni, P. D. Barua, F. Molinari, and U. R. Acharya, "Application of explainable artificial intelligence for healthcare: a systematic review of the last decade (2011–2022)," *Computer Methods and Programs in Biomedicine*, vol. 226, p. 107161, 2022, doi: 10.1016/j.cmpb.2022.107161.

[10] K. Rasheed, A. Qayyum, M. Ghaly, A. Al-Fuqaha, A. Razi, and J. Qadir, "Explainable, trustworthy, and ethical machine learning for healthcare: a survey," *Computers in Biology and Medicine*, vol. 149, p. 106043, 2022, doi: 10.1016/j.compbiomed.2022.106043.

[11] M. Ghassemi, L. Oakden-Rayner, and A. L. Beam, "The false hope of current approaches to explainable artificial intelligence in health care," *The Lancet Digital Health*, vol. 3, no. 11, pp. e745–e750, 2021, doi: 10.1016/S2589-7500(21)00208-9.

[12] M. Sree Vani, R. V. Sudhakar, A. Mahendar, S. Ledalla, M. Radha, and M. Sunitha, "Personalized health monitoring using explainable AI: bridging trust in predictive healthcare," *Scientific Reports*, vol. 15, p. 31892, 2025, doi: 10.1038/s41598-025-15867-z.

[13] Y. Wu, A. Dravid, R. M. Wehbe, and A. K. Katsaggelos, "DeepCOVID-fuse: a multi-modality deep learning model fusing chest X-rays and clinical variables to predict COVID-19 risk levels," *Bioengineering*, vol. 10, no. 5, p. 556, May 2023.

[14] M. Chieregato, F. Frangiamore, M. Morassi, C. Baresi, S. Nici, C. Bassetti, C. Bnà, and M. Galelli, "A hybrid machine learning/deep learning COVID-19 severity predictive model from CT images and clinical data," *Scientific Reports*, vol. 12, no. 1, p. 4329, Mar. 2022.

[15] A. Choi, K. Lee, H. Hyun, K. J. Kim, B. Ahn, K. H. Lee, S. Hahn, S. Y. Choi, and J. H. Kim, "A novel deep learning algorithm for real-time prediction of clinical deterioration in the emergency department for a multimodal clinical decision support system," *Scientific Reports*, vol. 14, no. 1, p. 30116, Dec. 2024.

[16] F. E. Shamout, Y. Shen, N. Wu, A. Kaku, J. Park, T. Makino, S. Jastrzębski, J. Witowski, D. Wang, B. Zhang, S. Dogra, M. Cao, N. Razavian, D. Kudlowitz, L. Azour, W. Moore, Y. W. Lui, Y. Aphinyanaphongs, C. Fernandez-Granda, and K. J. Geras, "An artificial intelligence system for predicting the deterioration of COVID-19 patients in the emergency department," *npj Digital Medicine*, vol. 4, no. 1, p. 80, May 2021.

[17] Y. Wu, B. M. Rocha, E. Kaimakamis, G.-A. Cheimariotis, G. Petmezas, E. Chatzis, V. Kilintzis, L. Stefanopoulos, D. Pessoa, A. Marques, P. Carvalho, R. P. Paiva, S. Kotoulas, M. Bitzani, A. K. Katsaggelos, and N. Maglaveras, "A deep learning method for predicting the COVID-19 ICU patient outcome fusing X-rays, respiratory sounds, and ICU parameters," *Expert Systems with Applications*, vol. 235, p. 121089, Jan. 2024.
