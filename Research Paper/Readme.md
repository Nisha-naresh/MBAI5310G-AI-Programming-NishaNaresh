# Explainable Multimodel AI for Clinical Prediction and Patient-Specific Medical Decision Support

**Final Paper, MBAI 5310G AI Programming**

## Student Information
- **Name:** Nisha Naresh
- **Student ID:** 101008896
- **University:** Ontario Tech University
- **Course:** AI Programming (MBAI 5310G)
- **Instructor:** Zahra Atf

## Summary
This paper proposes an explainable multimodal AI framework that fuses medical imaging with structured electronic health record (EHR) data to predict patient outcomes, and that generates patient-specific, clinician-readable explanations to support decision-making at the bedside. It is an observational, retrospective, data-science study using de-identified public data.

## Paper Outline
1. **Introduction:** AI and ML in healthcare, the accuracy versus interpretability barrier, and why explainable multimodal AI matters [1], [2], [3], [10], [11].
2. **Clinical Background:** clinical reasoning is multimodal; deep fusion models are accurate but behave as black boxes, and population-level importance is not patient-specific [12], [13], [14], [17].
3. **Problem Statement:** the gap between predictive performance and clinical usability; multimodal models rarely produce patient-specific, clinician-readable explanations [4], [6], [7], [9], [11].
4. **Literature Review:** four themes, multimodal prediction, XAI methods, trust and human-AI interaction, and critical or ethical perspectives [1] to [17].
5. **Research Gap:** unimodal focus, little testing of clinical utility, scarce patient-specific explanation, and no standard way to evaluate XAI quality [2], [4], [7], [8], [10], [12], [13].
6. **Aim and Objectives:** build and evaluate an explainable multimodal framework with patient-specific explanations, set out as four objectives from literature synthesis to evaluation.
7. **Research Questions and Hypotheses:** four questions on fusion design, the best XAI techniques, the effect on clinician trust, and the right evaluation criteria.
8. **Related Work in XAI and Healthcare:** fusion reliably improves prediction and explanation links to trust, but the two lines of work rarely meet [1], [4], [7], [8], [11], [12], [13] to [17].
9. **Clinical Decision Support System:** a planned single-patient view showing the predicted outcome with the features and image regions that drove it.
10. **Multimodal Data Sources:** at least two modalities, imaging (chest X-ray or CT) and structured EHR data (vital signs, laboratory values, demographics) [13], [15], [17].
11. **XAI Methodology:** SHAP for the tabular stream, Grad-CAM or attention maps for the imaging stream, and LIME as a consistency check, combined into one patient-specific cross-modal explanation [11], [12].
12. **Model Architecture:** a CNN image encoder and a feed-forward tabular encoder joined by intermediate fusion, with early and late fusion as baselines [13], [14], [17].
13. **Model Training and Optimization:** train, validation, and test split, regularization (dropout, early stopping), class-imbalance handling, and recorded settings for reproducibility.
14. **Evaluation Metrics:** prediction (accuracy, AUROC, F1, sensitivity, specificity) and explanation (faithfulness, stability, cross-modal agreement), plus clinician-style review [4], [8], [10].
15. **Conceptual Framework:** six linked constructs from multimodal inputs through fusion, prediction, the XAI layer, explanation, and clinician interpretation, to trust and decision quality, with explainability acting as a moderator [1], [7].
16. **Clinical Methodology:** observational, retrospective, secondary anonymized data; five steps from data preparation to reporting; a public multimodal dataset such as COVID imaging with clinical variables or a MIMIC-derived cohort [13], [14], [16], [17].
17. **Expected Contributions:** theoretical (extends the explainability and trust link to the multimodal clinical setting), methodological (one cross-modal patient-specific explanation plus a two-part evaluation), and practical (a usable point-of-care decision-support view) [1], [4], [7], [11].
18. **Limitations:** dataset generalizability, the difficulty of a formal clinician evaluation in a short project, and the over-confidence risk of plausible explanations [11].
19. **Future Work:** extend beyond two modalities, validate prospectively with clinicians, test subgroup fairness, and study longer-term effects on clinician behaviour.
20. **Ethical Considerations:** anonymized public data under existing consent and governance, no re-identification, subgroup fairness checks, and awareness of automation bias [10].
21. **Timeline:** a June 2026 schedule running from literature review and dataset selection through model building, evaluation, and submission.
22. **References:** 17 sources in IEEE format.

## Folder Structure
```
Research Paper/
├── README.md                     # this outline
├── Final_Naresh_Nisha.docx       # the full final paper
└── Final_Naresh_Nisha.pdf        # PDF version for submission
```

## Responsible AI Note
All work is for educational purposes. No confidential, private, sensitive, copyrighted, or restricted data is used; the study relies on de-identified public datasets under their original consent and governance. AI tools were used for drafting and structuring support, and the final content was reviewed and verified by the author.

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
