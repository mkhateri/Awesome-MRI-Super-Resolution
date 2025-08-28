## Preprocessing

Preprocessing is a foundational step in MRI super-resolution (SR). It improves anatomical consistency, harmonizes intensity distributions, and increases robustness across subjects, scanners, and protocols.

### Essential steps and representative tools

| Preprocessing Step | Purpose | Tools (code/docs) |
|---|---|---|
| **Motion correction** | Reduce intra-scan motion artifacts (common in fetal, neonatal, elderly). | [MCFLIRT (FSL)](https://web.mit.edu/fsl_v5.0.10/fsl/doc/wiki/MCFLIRT.html) · [SVRTK](https://github.com/SVRTK/SVRTK) · [NiftyMIC](https://github.com/gift-surg/NiftyMIC) |
| **Image registration** | Align scans across timepoints, modalities, or subjects. | [ANTs](https://github.com/ANTsX/ANTs) · [elastix](https://elastix.dev/) · [SimpleElastix](https://github.com/SuperElastix/SimpleElastix) |
| **Bias field correction** | Correct low-frequency intensity non-uniformities (B0/B1). | [N4ITK (SimpleITK)](https://simpleitk.readthedocs.io/en/master/link_N4BiasFieldCorrection_docs.html) · [ANTs](https://github.com/ANTsX/ANTs) · [SimpleITK](https://github.com/SimpleITK/SimpleITK) |
| **Skull stripping / brain extraction** | Remove non-brain tissue to isolate relevant anatomy. | [BET (FSL)](https://web.mit.edu/fsl_v5.0.10/fsl/doc/wiki/BET%282f%29UserGuide.html) · [HD-BET](https://github.com/MIC-DKFZ/HD-BET) · [SynthStrip (docs)](https://surfer.nmr.mgh.harvard.edu/docs/synthstrip/) · [SynthStrip (code)](https://github.com/nipreps/synthstrip) |
| **Resampling & intensity normalization** | Standardize voxel geometry and scale intensities for comparability/stability. | [ANTs](https://github.com/ANTsX/ANTs) · [SimpleITK](https://github.com/SimpleITK/SimpleITK) |


### Pipelines & utilities

| Name | What it does | Link |
|---|---|---|
| **fMRIPrep** | Robust, reproducible fMRI preprocessing pipeline (BIDS). | [https://github.com/nipreps/fmriprep](https://github.com/nipreps/fmriprep) |
| **QSIPrep** | Diffusion MRI preprocessing, denoising, reconstruction (BIDS). | [https://github.com/PennLINC/qsiprep](https://github.com/PennLINC/qsiprep) |
| **SynthSeg** | Contrast-agnostic brain segmentation (useful for QC/downstream). | [https://github.com/BBillot/SynthSeg](https://github.com/BBillot/SynthSeg) |
| **ITK-SNAP** | Interactive 3D segmentation/inspection utility. | [https://www.itksnap.org/download/snap/](https://www.itksnap.org/download/snap/) |
