<div align="center">

# Smart Embedded Systems Lab

**OTH Regensburg** · Ostbayerische Technische Hochschule Regensburg

Trustworthy AI: detecting AI-generated content and explaining why.

[Website](https://elektro-informationstechnik.oth-regensburg.de/labore/smart-embedded-systems) · [Publications](#publications) · [Featured project](#featured-project) · [Datasets](#datasets) · [People](#people)

</div>

---

## About

The Smart Embedded Systems Lab (SES Lab) at OTH Regensburg works on AI systems that hold up outside the lab. Our current focus is the detection of AI-generated content in text and images: detectors that generalise across datasets, generators and domains, that survive adversarial manipulation of their input, and whose decisions can be explained to the people who rely on them.

All code, model weights and demos released here are free to use for research. Each repository states its own licence.

## Featured project

### [DeBERTa-ConPara](https://github.com/SES-Lab-OTH/deberta-conpara): attack-aware detection of AI-generated text

[![Paper](https://img.shields.io/badge/AACL--IJCNLP-2026-1f6feb)](https://arxiv.org/abs/2610.00883)
[![arXiv](https://img.shields.io/badge/arXiv-2610.00883-b31b1b)](https://arxiv.org/abs/2610.00883)
[![Model](https://img.shields.io/badge/%F0%9F%A4%97%20Model-deberta--conpara-ffcc4d)](https://huggingface.co/mohamedmady/deberta-conpara)
[![Demo](https://img.shields.io/badge/%F0%9F%A4%97%20Demo-live-ff9d00)](https://huggingface.co/spaces/mohamedmady/deberta-conpara)

A detector of AI-generated text built for deployment conditions: unknown domains, unknown generators, adversarially perturbed input and no labels for threshold calibration. The central finding is that Unicode normalisation acts in opposite directions depending on where it is applied. Normalising the training corpus deletes the adversarial supervision, while normalising at inference is an effective defence.

| RAID hidden test (official leaderboard) | |
|---|---|
| AUROC | **99.61 %** |
| TPR at 5 % FPR | **99.01 %** |
| TPR at 1 % FPR | **96.57 %** |
| Homoglyph and zero-width-space attacks (TPR at 1 % FPR) | 11.05 % and 1.12 % → **96.98 %** |

Code, the released checkpoint and a live demo are public; see the [repository](https://github.com/SES-Lab-OTH/deberta-conpara) to reproduce every number in the paper.

## Publications

**AI-Generated Content Detection: A Cross-Modal Survey of Methods, Challenges, and Future Directions.**
Mohamed Mady, Yupei Li, Björn W. Schuller, Berrak Sisman, Johannes Reschke.
*Preprint, Research Square, 2026.*
[Preprint](https://www.researchsquare.com/article/rs-10864156/v1) · [DOI](https://doi.org/10.21203/rs.3.rs-10864156/v1)

**DeBERTa-ConPara: Attack-Aware and Deployment-Realistic Detection of AI-Generated Text.**
Mohamed Mady, Yupei Li, Johannes Reschke, Björn W. Schuller.
*AACL-IJCNLP 2026, main conference.*
[Paper](https://arxiv.org/abs/2610.00883) · [Code](https://github.com/SES-Lab-OTH/deberta-conpara) · [Model](https://huggingface.co/mohamedmady/deberta-conpara) · [Demo](https://huggingface.co/spaces/mohamedmady/deberta-conpara)

**Feature-Augmented Transformers for Robust AI-Text Detection Across Domains and Generators.**
Mohamed Mady, Johannes Reschke, Björn W. Schuller.
*arXiv preprint, 2026.*
[Paper](https://arxiv.org/abs/2605.03969)

## Datasets

| Dataset | Size | Content |
|---|---|---|
| [Academic-Text-arxiv-gpt-gemini](https://huggingface.co/datasets/mohamedmady/Academic-Text-arxiv-gpt-gemini) | 669,008 paragraphs | Human academic paragraphs from arXiv (papers before 2022) and AI-generated counterparts from GPT-3.5-Turbo and Gemini 2.0 Flash |
| [HC3-Gemini-Flash-Responses](https://huggingface.co/datasets/mohamedmady/HC3-Gemini-Flash-Responses) | 23,463 responses | Gemini 2.0 Flash answers to the HC3 questions, for measuring generator shift against HC3 |

## People

- **Prof. Dr. Johannes Reschke**, professor at OTH Regensburg
- **Mohamed Mady**, doctoral researcher (cooperative doctorate with the Technical University of Munich)
- **Gerald Schickhuber**, lab engineer

## Contact

For questions about our code or models, please open an issue in the respective repository. For research collaboration, contact details are on the [lab website](https://elektro-informationstechnik.oth-regensburg.de/labore/smart-embedded-systems).
