# Awesome MRI Super-Resolution 
A curated list of deep learning methods, datasets, papers, and tools for MRI Super-Resolution.

---

<summary><strong>📚 Survey Paper</strong></summary>

This repository accompanies our survey paper:  
**MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions**  
🔗 [Link to paper](#) (arXiv or journal link)


---

<details open>
<summary><strong> Contents</strong></summary>

- [Papers](#papers)  
- [Methods and Architectures](#methods-and-architectures)  
- [Datasets](#datasets)  
- [Clinical and Pre-clinical Applications](#applications)  
- [Code and Tools](#code-and-tools)  
  - [Preprocessing Tools](#preprocessing-tools)  
- [Related Talks](#related-talks)  
- [Famous Groups & Labs](#famous-groups--labs)  
- [Useful Links](#useful-links)  
- [Citation](#citation)

</details>

---

<details>
<summary><strong> Papers</strong></summary>

- [CycleINR (Fang et al., 2024)](https://arxiv.org/abs/2402.12345)  
- [NESVoR (Xu et al., 2023)](https://arxiv.org/abs/2303.23456)

</details>


<details>
<summary><strong> Methods and Architectures</strong></summary>

**Generative AI**
- Diffusion Models  
- GAN-based Super-Resolution

**Implicit Methods**
- Implicit Neural Representations (INR)  
- Plug-and-Play Optimization Models

</details>


<details>
<summary><strong> Datasets</strong></summary>

We highlight major public MRI datasets used in super-resolution research.

| Dataset | Description | Modality | Link |
|--------|-------------|----------|------|
| **fastMRI** | Knee and brain MRI with LR-HR scans | T1, T2, PD, FLAIR | [Link](https://fastmri.med.nyu.edu/) |
| **IXI** | 600 subject clinical dataset | T1, T2, PD, DWI, MRA | [Link](https://brain-development.org/ixi-dataset/) |
| **HCP** | Connectome mapping | T1, T2, fMRI, DWI | [Link](https://www.humanconnectome.org/study/hcp-young-adult/data-releases) |
| **dHCP** | Neonatal brain MRI | T1, T2, fMRI | [Link](https://www.developingconnectome.org/) |
| **NAMIC** | Multi-modal MR data | T1, T2, DWI, fMRI, PD, MRA | [Link](https://www.na-mic.org/wiki/Downloads) |
| **FeTA** | Fetal brain segmentation | T1 | [Link](http://neuroimaging.ch/feta) |
| **BraTS** | Brain tumor segmentation | T1, T1c, T2, FLAIR | [Link](https://www.med.upenn.edu/cbica/brats2020/data.html) |
| **UK Biobank** | Whole-body imaging | T1, T2, fMRI, DTI | [Link](https://biobank.ctsu.ox.ac.uk/crystal/) |

</details>


<details>
<summary><strong> Applications</strong></summary>

### Clinical Applications
- Fetal and Pediatric MRI  
- Neurodegenerative Disease  
- Cardiac Imaging  
- Brain Tumor Visualization  
- Spine and Interventional MRI

### Pre-Clinical Applications
- Small Animal Imaging  
- Ultra-High Field MRI  
- Morphometric and Tractography Validation

</details>


<details>
<summary><strong> Code and Tools</strong></summary>

- [MONAI](https://github.com/Project-MONAI/MONAI) – Deep learning in medical imaging  
- [deepinv Toolbox](https://deepinv.github.io/deepinv/quickstart.html) – Plug-and-play, diffusion-based inverse problems

<details>
<summary><strong> Preprocessing Tools</strong></summary>

| Task | Tool | Description | Link |
|------|------|-------------|------|
| Diffusion MRI | DIPY | dMRI reconstruction and processing | [Link](https://dipy.org) |
| Motion Correction | MCFLIRT | Motion correction (FSL) | [Link](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/MCFLIRT) |
|  | SPM Realign | Realignment of fMRI | [Link](https://www.fil.ion.ucl.ac.uk/spm/) |
| Image Registration | ANTs | Rigid/nonlinear registration | [Link](https://stnava.github.io/ANTs/) |
|  | Elastix | Rigid/nonrigid registration | [Link](https://elastix.lumc.nl) |
| Bias Correction | N4ITK | Bias field inhomogeneity correction | [Link](https://simpleitk.readthedocs.io) |
| Artifact Correction | TOPUP | Distortion correction (FSL) | [Link](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/TOPUP) |
|  | EDDY | Eddy-current correction (FSL) | [Link](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/EDDY) |

</details>

</details>



<details>
<summary><strong> Resources & Learning</strong></summary>

###  Tutorials
- [INR4MICCAI Tutorial](https://github.com/INR4MICCAI/INRTutorial)

###  Toolkits
- [MONAI](https://github.com/Project-MONAI/MONAI)
- [deepinv Toolbox](https://deepinv.github.io/deepinv/quickstart.html)

###  Talks
- [Generative AI & Diffusion Models – Michael Elad](https://www.youtube.com/playlist?list=PL0H3pMD88m8XPBlWoWGyal45MtnwKLSkQ)
- [MICCAI Tutorials – MRI SR](#)
- [ECCV/MIDL Talks – Deep Learning for Imaging](#)

</details>



<details>
<summary><strong> Famous Groups & Labs</strong></summary>

- MIT CSAIL - Medical Vision Group  
- Facebook AI Research (fastMRI)  
- NYU Grossman School of Medicine  
- King's College London  
- University of Eastern Finland  
- Stanford AIMI

</details>



<details>
<summary><strong> Useful Links</strong></summary>

- [Papers With Code – MRI SR](https://paperswithcode.com/task/mri-super-resolution)  
- [Awesome-Medical-Imaging](https://github.com/HzFu/Awesome-Medical-Imaging)  
- [ArXiv Medical Imaging](https://arxiv.org/list/eess.IV/recent)  
- [NeurIPS/ICLR Papers](https://openreview.net/)  

</details>



> 🧩 **Contribute**: Found something we missed? Open an issue or pull request!  
> ⭐ Star this repo if you find it helpful.  
> 📬 Contact [@mkhateri](https://github.com/mkhateri) or email: mohammad.khateri@uef.fi

---

<details open>
<summary><strong> Citation</strong></summary>

If you use this repository, please cite:

> Mohammad Khateri, *MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions*, arXiv:XXXX.XXXXX, 2025  
> 🔗 [View on arXiv](https://arxiv.org/abs/XXXX.XXXXX)

```bibtex
@article{khateri2025mrisr,
  title = {MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions},
  author = {Khateri, Mohammad and Vasylechko, Serge and Ghahremani, Morteza and Timms, Liam and Kocanaogullari, Deniz and Warfield, Simon K. and Karimi, Davood and Sierra, Alejandra and Tohka, Jussi and Kurugol, Sila and Afacan, Onur},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year = {2025}
}
```

</details>

