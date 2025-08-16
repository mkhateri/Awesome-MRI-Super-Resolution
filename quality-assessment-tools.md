
## Image Quality Assessment — Papers & Code

### Full-reference & Perceptual Metrics

| Metric | Paper (link) | Code (reliable impls) | Notes |
|---|---|---|---|
| **PSNR** | — (classical SNR definition) | [scikit-image: `peak_signal_noise_ratio`](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.peak_signal_noise_ratio) · [TorchMetrics: PeakSignalNoiseRatio](https://lightning.ai/docs/torchmetrics/stable/image/peak_signal_noise_ratio.html) | Baseline fidelity metric; not perceptual. |
| **SSIM** | [Wang et al., 2004](https://ieeexplore.ieee.org/document/1284395) | [scikit-image: `structural_similarity`](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.structural_similarity) · [TorchMetrics: StructuralSimilarityIndexMeasure](https://lightning.ai/docs/torchmetrics/stable/image/structural_similarity.html) · [PIQ: SSIM](https://github.com/photosynthesis-team/piq) | Windowed, structure-aware; use Y-channel for RGB SR. |
| **MS-SSIM** | [Wang et al., 2003](https://ieeexplore.ieee.org/document/1292216) | [TorchMetrics: MultiScaleSSIM](https://lightning.ai/docs/torchmetrics/stable/image/multiscale_structural_similarity.html) · [PIQ: MS-SSIM](https://github.com/photosynthesis-team/piq) | Multi-scale variant; more robust to scale changes. |
| **VIF** | [Sheikh & Bovik, 2006](https://ieeexplore.ieee.org/document/1576816) | [PIQ: VIF](https://github.com/photosynthesis-team/piq) | Info-theoretic, strong correlation to human ratings. |
| **FSIM** | [Zhang et al., 2011](https://ieeexplore.ieee.org/document/5705575) | [PIQ: FSIM](https://github.com/photosynthesis-team/piq) | Phase congruency & gradient magnitude based. |
| **GMSD** | [Xue et al., 2014](https://ieeexplore.ieee.org/document/6873260) | [PIQ: GMSD](https://github.com/photosynthesis-team/piq) | Fast, gradient-magnitude similarity deviation. |
| **LPIPS** | [Zhang et al., 2018](https://arxiv.org/abs/1801.03924) | [Official PyTorch (PerceptualSimilarity)](https://github.com/richzhang/PerceptualSimilarity) · [PIQ: LPIPS](https://github.com/photosynthesis-team/piq) | Learned perceptual distance using deep features. |
| **DISTS** | [Ding et al., 2020](https://arxiv.org/abs/2004.07728) | [Official PyTorch](https://github.com/dingkeyan93/DISTS) · [PIQ: DISTS](https://github.com/photosynthesis-team/piq) | Deep structure & texture similarity. |

### No-reference (Opinion-Unaware) Metrics

| Metric | Paper (link) | Code | Notes |
|---|---|---|---|
| **NIQE** | [Mittal et al., 2013](https://ieeexplore.ieee.org/document/6353522) | [PIQ: NIQE](https://github.com/photosynthesis-team/piq) | No-ref naturalness; may not reflect clinical relevance. |
| **PIQE / BRISQUE** | [Saad et al., 2012](https://ieeexplore.ieee.org/document/6272356) / [Mittal et al., 2012](https://ieeexplore.ieee.org/document/6272356) | Popular Python impls exist; for PyTorch prefer the aggregated library below | Use with caution for MRI; consider task-aware eval. |

> ✅ For **medical downstream** evaluation (segmentation/classification), use **MONAI metrics** (e.g., Dice, Hausdorff, AUC) alongside IQA.

### Downstream Clinical / Task-based Metrics (for SR impact)

| Task | Code | Typical Metrics |
|---|---|---|
| **Segmentation** | [MONAI: `DiceMetric`, `HausdorffDistanceMetric`](https://docs.monai.io/en/stable/metrics.html) | Dice, HD95, ASSD |
| **Classification** | [MONAI / TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/classification.html) | AUC, ACC, F1 |
| **Detection** | [TorchMetrics: detection](https://lightning.ai/docs/torchmetrics/stable/detection/mean_ap.html) | mAP, sensitivity/specificity |

### Handy Aggregator Libraries

| Library | What you get | Link |
|---|---|---|
| **PIQ (PyTorch Image Quality)** | Many FR/NR metrics (SSIM, MS-SSIM, VIF, FSIM, GMSD, NIQE, LPIPS, DISTS, …) | https://github.com/photosynthesis-team/piq |
| **TorchMetrics (Lightning)** | Clean PyTorch metric modules (PSNR, SSIM/MS-SSIM, image/classif/detection) | https://lightning.ai/docs/torchmetrics/stable/ |
| **scikit-image** | Reference PSNR/SSIM implementations (NumPy) | https://scikit-image.org/docs/stable/api/skimage.metrics.html |
