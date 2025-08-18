
## Image Quality Assessment — Papers & Code

### Full-reference & Perceptual Metrics

## Image Quality Assessment — Papers & Code

### Full-reference / Perceptual Metrics
| Metric | Paper (link) | Code (reliable impls) |
|---|---|---|
| **PSNR** | — | [scikit-image](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.peak_signal_noise_ratio) · [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/peak_signal_noise_ratio.html) |
| **SSIM** | [Wang et al., 2004](https://ieeexplore.ieee.org/document/1284395) | [scikit-image](https://scikit-image.org/docs/stable/api/skimage.metrics.html#skimage.metrics.structural_similarity) · [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/structural_similarity.html) · [PIQ](https://github.com/photosynthesis-team/piq) |
| **MS-SSIM** | [Wang et al., 2003](https://ieeexplore.ieee.org/document/1292216) | [TorchMetrics](https://lightning.ai/docs/torchmetrics/stable/image/multiscale_structural_similarity.html) · [PIQ](https://github.com/photosynthesis-team/piq) |
| **VIF** | [Sheikh & Bovik, 2006](https://ieeexplore.ieee.org/document/1576816) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **FSIM** | [Zhang et al., 2011](https://ieeexplore.ieee.org/document/5705575) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **GMSD** | [Xue et al., 2014](https://ieeexplore.ieee.org/document/6873260) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **LPIPS** | [Zhang et al., 2018](https://arxiv.org/abs/1801.03924) | [Official (PerceptualSimilarity)](https://github.com/richzhang/PerceptualSimilarity) · [PIQ](https://github.com/photosynthesis-team/piq) |
| **DISTS** | [Ding et al., 2020](https://arxiv.org/abs/2004.07728) | [Official](https://github.com/dingkeyan93/DISTS) · [PIQ](https://github.com/photosynthesis-team/piq) |

### No-reference Metrics
| Metric | Paper (link) | Code |
|---|---|---|
| **NIQE** | [Mittal et al., 2013](https://ieeexplore.ieee.org/document/6353522) | [PIQ](https://github.com/photosynthesis-team/piq) |
| **BRISQUE** | [Mittal et al., 2012](https://ieeexplore.ieee.org/document/6272356) | [PIQ](https://github.com/photosynthesis-team/piq) |
