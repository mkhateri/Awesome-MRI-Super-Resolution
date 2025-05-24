# Awesome MRI Super-Resolution 
A curated list of deep learning methods, datasets, papers, and tools for MRI Super-Resolution.

---

## 📚 Survey Paper  
This repository accompanies our survey paper:  
**MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions**  
🔗 [Link to paper](#) (arXiv or journal link)

---

## 📂 Contents  
-  [Papers](#papers)  
-  [Methods and Architectures](#methods-and-architectures)  
-  [Datasets](#datasets)  
-  [Clinical and Pre-clinical Applications](#applications)  
-  [Code and Tools](#code-and-tools)  
-  [Related Talks](#related-talks)  
-  [Famous Groups & Labs](#famous-groups--labs)  
-  [Useful Links](#useful-links)  

---

##  Papers  
- [CycleINR (Fang et al., 2024)](https://arxiv.org/abs/2402.12345)  
- [NESVoR (Xu et al., 2023)](https://arxiv.org/abs/2303.23456)  
- [Deep Plug-and-Play MRI SR (Wu et al., 2022)](https://arxiv.org/abs/2205.XXXX)  
- [SelfMRI (McGinnis et al., 2023)](https://arxiv.org/abs/2304.XXXX)  

---

##  Methods and Architectures  
- Implicit Neural Representations (INR)  
- Plug-and-Play Optimization Models  
- Diffusion Models  
- GAN-based Super-Resolution  
- Self-supervised and Contrastive Learning  
- Deep Unfolding & Physics-Informed SR  

---

## Datasets

We highlight major public MRI datasets used in super-resolution research, covering brain, fetal, neonatal, and whole-body imaging.

<details>
<summary>📂 Click to expand dataset list</summary>

<br>

| Dataset | Description | Modality | Link |
|--------|-------------|----------|------|
| **fastMRI** | Large-scale dataset for knee and brain MRI with paired and unpaired LR-HR scans | T1, T2, PD, FLAIR | [fastmri.med.nyu.edu](https://fastmri.med.nyu.edu/) |
| **IXI** | Clinical MRI scans from 600 healthy subjects across 3 hospitals | T1, T2, PD, DWI, MRA | [brain-development.org](https://brain-development.org/ixi-dataset/) |
| **HCP (Human Connectome Project)** | High-resolution data from 1,200 adults for connectome mapping | T1, T2, fMRI, DWI | [humanconnectome.org](https://www.humanconnectome.org/study/hcp-young-adult/data-releases) |
| **dHCP (Developing HCP)** | Neonatal MRI for studying early brain development | T1, T2, fMRI | [developingconnectome.org](https://www.developingconnectome.org/) |
| **NAMIC** | Multi-modal MRI data for segmentation and tractography | T1, T2, DWI, fMRI, PD, MRA | [na-mic.org](https://www.na-mic.org/wiki/Downloads) |
| **FeTA** | Fetal brain segmentation dataset with anatomical labels | T1-weighted fetal MRI | [neuroimaging.ch](http://neuroimaging.ch/feta) |
| **BraTS** | Brain tumor segmentation for high/low-grade gliomas | T1, T1c, T2, FLAIR | [BraTS Challenge](https://www.med.upenn.edu/cbica/brats2020/data.html) |
| **UK Biobank** | Population-scale dataset with brain and whole-body imaging | T1, T2, fMRI, DTI | [biobank.ctsu.ox.ac.uk](https://biobank.ctsu.ox.ac.uk/crystal/) |

</details>

---

##  Applications  

### Clinical Applications  
- Fetal and Pediatric MRI  
- Neurodegenerative Disease (e.g., Alzheimer's)  
- Cardiac Imaging  
- Brain Tumor Visualization  
- Spine and Interventional MRI  

### Pre-Clinical Applications  
- Small Animal Imaging (Mice, Rats, Primates)  
- Ultra-High Field MRI  
- Morphometric and Tractography Validation  

---

## 📚 Resources & Learning

### 🎓 Tutorials
- [INR4MICCAI Tutorial: Implicit Neural Representations](https://github.com/INR4MICCAI/INRTutorial)

### 💻 Code & Toolkits
- [MONAI (Medical Open Network for AI)](https://github.com/Project-MONAI/MONAI) – PyTorch framework for deep learning in medical imaging
- [deepinv Toolbox](https://deepinv.github.io/deepinv/quickstart.html) – Modular inverse problem solver with plug-and-play and diffusion support

### 🎙️ Talks & Courses
- [A Course on Generative AI & Diffusion Models (Michael Elad)](https://www.youtube.com/playlist?list=PL0H3pMD88m8XPBlWoWGyal45MtnwKLSkQ)
- [MICCAI Tutorials on MRI Super-Resolution (YouTube)](#)
- [Deep Learning for Imaging – ECCV/MIDL Invited Talks](#)


---

##  Famous Groups & Labs  
- MIT CSAIL - Medical Vision Group  

---

##  Useful Links  
- [Papers With Code – MRI SR](https://paperswithcode.com/task/mri-super-resolution)  
- [Awesome-Medical-Imaging](https://github.com/HzFu/Awesome-Medical-Imaging)  
- [ArXiv: Medical Imaging](https://arxiv.org/list/eess.IV/recent)  
- [NeurIPS/ICLR Papers on MRI](https://openreview.net/)  

---
> 🧩 **Contribute**: Found something we missed? Open an issue or pull request!  
> ⭐ Star this repo if you find it helpful.  
> 📬 For feedback or collaboration, contact [@mkhateri](https://github.com/mkhateri)  
> ✉️ If you have any questions or suggestions, feel free to email me directly.

---

## 📖 Citation

If you use this repository or its resources in your work, please cite the following paper:

> Mohammad Khateri, *MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions*, arXiv:XXXX.XXXXX, 2025  
> 🔗 [View on arXiv](https://arxiv.org/abs/XXXX.XXXXX)

**BibTeX:**

```bibtex
@article{khateri2025mrisr,
  title = {MRI Super-Resolution with Deep Learning: A Critical Review of Advances, Challenges, and Future Directions},
  author = {Khateri, Mohammad},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year = {2025}
}

