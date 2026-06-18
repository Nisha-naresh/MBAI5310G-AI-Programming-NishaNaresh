# Explainable Multimodal AI for ICU Admission Prediction and Patient-Specific Clinical Decision Support

*A research proposal on making multimodal clinical AI explain its predictions for the individual patient, not just the population.*

This folder contains my final research proposal for **MBAI 5310G, AI Programming**. The study designs and evaluates an explainable multimodal AI framework that fuses chest X-ray images with structured electronic health record (EHR) data to predict ICU admission within 24 hours of hospital presentation, and that generates clinician-readable, patient-specific explanations to support decision-making at the bedside.

## At a Glance

| | |
|---|---|
| **Topic** | Explainable multimodal AI for ICU admission prediction |
| **Prediction task** | ICU admission within 24 hours of hospital presentation |
| **Data** | MIMIC-IV and MIMIC-CXR (de-identified, public) |
| **Modalities** | Chest X-ray imaging + structured EHR (vitals, labs, demographics) |
| **Model** | CNN (imaging) + feed-forward network (EHR), intermediate fusion, binary classification head |
| **Explainability** | SHAP (tabular), Grad-CAM / attention (imaging), LIME (consistency check) |
| **Evaluation** | Prediction: AUROC, F1, sensitivity, specificity. Explanation: faithfulness, stability, interpretability |
| **Study type** | Retrospective, observational, mixed-methods data-science proposal |

## Aim and Research Questions

**Aim.** To develop and evaluate an explainable multimodal AI framework that integrates chest X-ray images and structured EHR data to accurately predict ICU admission within 24 hours, while generating clinician-interpretable, patient-specific explanations.

1. How can multimodal AI integrate chest X-ray images and structured EHR data to accurately predict ICU admission risk?
2. Which XAI techniques produce the most clinically meaningful, patient-specific explanations?
3. How effectively do patient-specific explanations improve the transparency and interpretability of multimodal predictions?
4. What metrics best capture the quality and clinical utility of these explanations?

## Conceptual Framework

```
Multimodal inputs (chest X-ray + EHR)
        → Fusion model
        → ICU admission prediction
        → XAI layer (SHAP / Grad-CAM / attention)
        → Patient-specific explanation
        → Clinician interpretation
        → Trust and decision quality
```

Explainability acts as a moderator: an accurate prediction paired with a faithful, stable explanation is the combination most likely to be used well at the bedside.

## Proposal Outline

The full paper moves through: Introduction, Clinical Background, Problem Statement, Literature Review, Research Gap (four points), Aim and Objectives, Research Questions, Related Work, Clinical Decision Support System, Multimodal Data Sources, XAI Methodology, Model Architecture, Model Training, Evaluation Metrics, Conceptual Framework, Clinical Methodology, Expected Contributions, Limitations, Future Work, Ethical Considerations, Timeline, and References.

## Methodology in Brief

- **Design:** retrospective, observational data-science study, no new patient data collected.
- **Data:** linked MIMIC-IV (structured EHR) and MIMIC-CXR (chest radiographs), accessed under their credentialed data-use agreement.
- **Model:** modality-specific encoders (CNN for imaging, feed-forward for tabular) joined by intermediate fusion into a binary ICU-admission classifier.
- **Explainability:** patient-specific, cross-modal explanations combining feature-level and image-region attributions.
- **Evaluation:** predictive performance plus explanation faithfulness, stability, and interpretability, with a clinician-style review where possible.

## Expected Contribution

- **Theoretical:** extends the explainability and trust relationship to the multimodal clinical setting.
- **Methodological:** one cross-modal, patient-specific explanation plus a two-part evaluation of prediction and explanation.
- **Practical:** a point-of-care decision-support view a clinician could reasonably use.

## Folder Structure

```
Research Paper/
├── README.md                     # this file
├── Final_Naresh_Nisha.pdf        # the full proposal (with references)     
```

## Key References

The full reference list (17 sources, IEEE format) is included in the proposal. The anchor papers are:

- Z. Atf and P. R. Lewis, "Is trust correlated with explainability in AI? A meta-analysis," *IEEE Transactions on Technology and Society*, 2025.
- S. Kizilisik, A. Terzi, and S. Candemir, "Explainable multimodal machine learning model for predicting ICU admission at hospital arrival," *IEEE Access*, vol. 14, 2026.
- M. Ghassemi, L. Oakden-Rayner, and A. L. Beam, "The false hope of current approaches to explainable artificial intelligence in health care," *The Lancet Digital Health*, vol. 3, no. 11, 2021.
- Y. Wu et al., "DeepCOVID-fuse: a multi-modality deep learning model fusing chest X-rays and clinical variables to predict COVID-19 risk levels," *Bioengineering*, vol. 10, no. 5, 2023.
- F. E. Shamout et al., "An artificial intelligence system for predicting the deterioration of COVID-19 patients in the emergency department," *npj Digital Medicine*, vol. 4, no. 1, 2021.

## Author

**Nisha Naresh** · Student ID 101008896 · Ontario Tech University
MBAI 5310G, AI Programming · Instructor: Zahra Atf

## Responsible AI Note

This work is for educational purposes and relies only on de-identified, publicly available datasets under their original consent and governance. No re-identification is attempted, and the proposed system is positioned as clinical decision support, not an autonomous decision-maker. AI tools were used for drafting and structuring support, and the final content was reviewed and verified by the author.
