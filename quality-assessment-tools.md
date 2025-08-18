
## Image Quality Assessment — Papers & Code

### Full-reference
| Metric | Paper (link) | Code (reliable impls) |
|---|---|---|
| **PSNR** | — | [scikit-image](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.peak_signal_noise_ratio) · [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/peak_signal_noise_ratio.html) · [MONAI](https://docs.monai.io/en/stable/metrics.html#monai.metrics.image.psnr.PSNRMetric) |
| **SSIM** | [Wang et al., 2004](https://ieeexplore.ieee.org/document/1284395) | [scikit-image](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.structural_similarity) · [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/structural_similarity.html) · [PIQ](https://github.com/photosynthesis-team/piq) · [MONAI](https://docs.monai.io/en/stable/metrics.html#monai.metrics.image.ssim.SSIMMetric) |
| **MS-SSIM** | [Wang et al., 2003](https://ieeexplore.ieee.org/document/1292216) | [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/multiscale_structural_similarity.html) · [PIQ](https://github.com/photosynthesis-team/piq) |
| **VIF** | [Sheikh & Bovik, 2006](https://ieeexplore.ieee.org/document/1576816) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **LPIPS** | [Zhang et al., 2018](https://arxiv.org/abs/1801.03924) | [Official (PerceptualSimilarity)](https://github.com/richzhang/PerceptualSimilarity) · [PIQ](https://github.com/photosynthesis-team/piq) |

### No-reference Metrics
| Metric | Paper (link) | Code |
|---|---|---|
| **NIQE** | [Mittal et al., 2013](https://ieeexplore.ieee.org/document/6353522) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **BRISQUE** | [Mittal et al., 2012](https://ieeexplore.ieee.org/document/6272356) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **NIMA** | [Talebi & Milanfar, 2018 (CVPR)](https://arxiv.org/abs/1709.05424) | [idealo/image-quality-assessment (PyTorch)](https://github.com/idealo/image-quality-assessment) · [Keras ref impl](https://github.com/kentsyx/Neural-IMage-Assessment) |

## MONAI — Downstream Task Metrics (Paper & Code)

| Metric | Task | Paper | Code |
|---|---|---|---|
| Dice (DSC) | Segmentation | [Taha & Hanbury (2015)][taha15] | [MONAI][monai-metrics] |
| Jaccard / IoU | Segmentation | [Taha & Hanbury (2015)][taha15] | [MONAI][monai-metrics] |
| Hausdorff (HD95) | Segmentation | [Huttenlocher et al. (1993)][hutten93] | [MONAI][monai-metrics] |
| ASSD | Segmentation | [Taha & Hanbury (2015)][taha15] | [MONAI][monai-metrics] |
| ROC AUC | Classification | [Fawcett (2006)][fawcett06] | [MONAI][monai-metrics] |
| Conf. Matrix / ACC / F1 | Classification | [Sokolova & Lapalme (2009)][sokolova09] | [MONAI][monai-metrics] |

[taha15]: https://bmcmedimaging.biomedcentral.com/articles/10.1186/s12880-015-0068-x
[hutten93]: https://people.eecs.berkeley.edu/~malik/cs294/Huttenlocher93.pdf
[fawcett06]: https://www.sciencedirect.com/science/article/pii/S016786550500303X
[sokolova09]: https://www.sciencedirect.com/science/article/abs/pii/S0306457309000259
[monai-metrics]: https://docs.monai.io/en/stable/metrics.html

