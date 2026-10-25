# FA-DeepMSM

Research code accompanying the publication:

**FA-DeepMSM: a few-shot adapted interpretable multimodal survival model for improved prognostic prediction in glioblastoma**

Minyoung Hwang, Junhyeok Lee, Sihyeon Kim, Minchul Kim, Seung Hong Choi, Sung Soo Ahn, Changhee Lee*, and Kyu Sung Choi*.

*These authors contributed equally to this work.*

**Scientific Reports**. 2026;16:4037. Published January 14, 2026.  
**DOI:** [10.1038/s41598-025-34134-9](https://doi.org/10.1038/s41598-025-34134-9)  
**PMID:** [41535701](https://pubmed.ncbi.nlm.nih.gov/41535701/)  
**Corresponding authors:** Changhee Lee (Korea University) and Kyu Sung Choi (Seoul National University Hospital).

## Research Overview

FA-DeepMSM (Few-shot Adapted Deep Multimodal Survival Model) combines self-supervised MRI representations with clinical and molecular variables to estimate individualized survival probabilities. It adapts a model developed in adult-type diffuse glioma to an external glioblastoma cohort using limited labeled data.

- **MRI representation learning:** A 3D vision transformer trained with DINOv2-based self-supervised learning extracts features from T1, T1CE, T2, and FLAIR MRI.
- **Multimodal survival prediction:** Imaging embeddings and structured variables are integrated to estimate time-dependent hazards and survival curves while accounting for right censoring.
- **Few-shot adaptation:** The final projection layer is fine-tuned using 5, 10, 20, or 40 external cases, with preceding layers frozen.
- **Interpretability:** Permutation-based analysis evaluates changing feature contributions across survival time points.

## Model Framework

<img width="1651" height="536" alt="image" src="https://github.com/user-attachments/assets/1c20cbf6-9970-42cb-88ab-3e062a3a4357" />

**Figure 1.** Self-supervised MRI feature learning and the multimodal survival prediction framework. Cropped from Figure 1 on page 3 of the published article; scientific content unchanged. Source: Hwang et al., *Scientific Reports* (2026), [doi:10.1038/s41598-025-34134-9](https://doi.org/10.1038/s41598-025-34134-9).

© The Author(s) 2026. Figure reproduced under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/). This figure attribution does not specify the software license.
