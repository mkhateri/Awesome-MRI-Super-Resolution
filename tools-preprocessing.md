## Preprocessing

Preprocessing is a foundational step in MRI super‑resolution. Raw MR images often contain motion artifacts, intensity inhomogeneities, geometric distortions, noise and other nuisances that may confound downstream processing. Appropriate preprocessing can address some of these issues. However, the desired combination of preprocessing steps will depend heavily on the details of the acquisition and the specific super‑resolution objective. The table below summarises a few common operations and links to some representative tools. In general, it is recommend to use a tool like `dcm2bids` to organize your data into something close to the BIDs file structure standard prior to preprocessing steps for compatiblity with most modern tools/pipelines. 

<!-- ### Common steps and representative tools

| Preprocessing Step                       | Purpose                                                                       | Tools (code/docs)                                                                                                                                                                                                                                                          |
| ---------------------------------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Motion correction**                    | Reduce intra-scan motion artifacts (common in fetal, neonatal, elderly).      | [MCFLIRT (FSL)](https://web.mit.edu/fsl_v5.0.10/fsl/doc/wiki/MCFLIRT.html) · [SVRTK](https://github.com/SVRTK/SVRTK) · [NiftyMIC](https://github.com/gift-surg/NiftyMIC)                                                                                                   |
| **Image registration**                   | Align scans across timepoints, modalities, or subjects.                       | [ANTs](https://github.com/ANTsX/ANTs) · [elastix](https://elastix.dev/) · [SimpleElastix](https://github.com/SuperElastix/SimpleElastix)                                                                                                                                   |
| **Bias field correction**                | Correct low-frequency intensity non-uniformities (B0/B1).                     | [N4ITK (SimpleITK)](https://simpleitk.readthedocs.io/en/master/link_N4BiasFieldCorrection_docs.html) · [ANTs](https://github.com/ANTsX/ANTs) · [SimpleITK](https://github.com/SimpleITK/SimpleITK)                                                                         |
| **Skull stripping / brain extraction**   | Remove non-brain tissue to isolate relevant anatomy.                          | [BET (FSL)](https://web.mit.edu/fsl_v5.0.10/fsl/doc/wiki/BET%282f%29UserGuide.html) · [HD-BET](https://github.com/MIC-DKFZ/HD-BET) · [SynthStrip (docs)](https://surfer.nmr.mgh.harvard.edu/docs/synthstrip/) · [SynthStrip (code)](https://github.com/nipreps/synthstrip) |
| **Resampling & intensity normalization** | Standardize voxel geometry and scale intensities for comparability/stability. | [ANTs](https://github.com/ANTsX/ANTs) · [SimpleITK](https://github.com/SimpleITK/SimpleITK)                                                                                                                                                                                | -->

<!-- ### Pipelines & utilities

| Name         | What it does                                                     | Link                                                                             |
| ------------ | ---------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **fMRIPrep** | Robust, reproducible fMRI preprocessing pipeline (BIDS).         | [https://github.com/nipreps/fmriprep](https://github.com/nipreps/fmriprep)       |
| **QSIPrep**  | Diffusion MRI preprocessing, denoising, reconstruction (BIDS).   | [https://github.com/PennLINC/qsiprep](https://github.com/PennLINC/qsiprep)       |
| **SynthSeg** | Contrast-agnostic brain segmentation (useful for QC/downstream). | [https://github.com/BBillot/SynthSeg](https://github.com/BBillot/SynthSeg)       |
| **ITK-SNAP** | Interactive 3D segmentation/inspection utility.                  | [https://www.itksnap.org/download/snap/](https://www.itksnap.org/download/snap/) | -->



## Preprocessing

Preprocessing is a foundational step in MRI super-resolution. It improves anatomical consistency, harmonizes intensity distributions, and increases robustness across subjects, scanners, and protocols.

### Common steps and some representative tools

| Preprocessing Step | Purpose | Tools (code/docs) |
|---|---|---|
| **Image registration/Motion Correction** | Align scans across timepoints, modalities, or subjects. | [antsRegistration](https://github.com/ANTsX/ANTs/wiki/Anatomy-of-an-antsRegistration-call)[/antsRegistrationSyN (ANTs)](https://github.com/ANTsX/ANTs/blob/master/Scripts/antsRegistrationSyN.sh) · [FLIRT](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/registration/flirt/index)/[FNIRT](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/registration/fnirt/index)/[MMORF](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/registration/mmorf) · [elastix](https://github.com/SuperElastix/elastix/wiki/Documentation)/[ITK-Elastix](https://github.com/InsightSoftwareConsortium/ITKElastix?tab=readme-ov-file)/[SimpleElastix](https://simpleelastix.github.io/) · [mni_autoreg (MINC)](https://github.com/BIC-MNI/mni_autoreg) |
| **Slice-wise motion correction** | Reduce intra-scan motion (useful for fetal, neonatal, or elderly data). | [EDDY S2V (FSL)](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/EDDY/Faq#How_does_slice-to-volume_motion_correction_work.3F) · [SVRTK](https://github.com/SVRTK/SVRTK) |
| **Bias field correction** | Correct low-frequency intensity non-uniformities (B0/B1 effects). | [N4ITK (SimpleITK)](https://simpleitk.readthedocs.io/en/master/link_N4BiasFieldCorrection_docs.html) · [FAST (FSL)](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FAST) · [nu_correct (MINC)](https://freesurfer.net/fswiki/nu_correct) · [dwibiascorrect (MRtrix3)](https://mrtrix.readthedocs.io/en/latest/reference/commands/dwibiascorrect.html) |
| **Intensity normalization** | Standardize image intensity statistics across datasets. | [inormalize (MINC)](https://bic-mni.github.io/man-pages/man1/inormalize.html) · [dwiintensitynorm (MRtrix3)](https://mrtrix.readthedocs.io/en/latest/reference/commands/dwiintensitynorm.html) · [nilearn](https://nilearn.github.io/stable/index.html) |
| **Skull stripping / brain extraction** | Remove non-brain tissue to isolate relevant anatomy. | [BET (FSL)](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/BET) · [HD-BET](https://github.com/MIC-DKFZ/HD-BET) · [SynthStrip (docs)](https://surfer.nmr.mgh.harvard.edu/docs/synthstrip/) · [SynthStrip (code)](https://github.com/nipreps/synthstrip) |
| **Susceptibility distortion correction** | Correct geometric distortions in EPI (fMRI, DWI). | [TOPUP (FSL)](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/TOPUP) · [DR-BUDDI (TORTOISE)](https://github.com/QMICodeBase/TORTOISEV4) · [3dQwarp (AFNI)](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dQwarp.html) · [SynB0-DISCO](https://github.com/MASILab/Synb0-DISCO) |
| **Denoising** | Reduce thermal noise while preserving edges. | [DenoiseImage (ANTs)](https://github.com/ANTsX/ANTs/wiki/DenoiseImage) · [dwidenoise (MRtrix3)](https://mrtrix.readthedocs.io/en/latest/reference/commands/dwidenoise.html) · [patch2self (DIPY)](https://dipy.org/documentation/1.5.0./reference/dipy.denoise.patch2self/) · [nlmeans (DIPY)](https://dipy.org/documentation/1.5.0./reference/dipy.denoise.nlmeans/) · [localpca (DIPY)](https://dipy.org/documentation/1.5.0./reference/dipy.denoise.localpca/) · [SANLM (CAT12)](https://neuro-jena.github.io/cat12-help/#denoising) |
| **Gibbs unringing** | Reduce discrete Fourier ringing artifacts. | [mrdegibbs (MRtrix3)](https://mrtrix.readthedocs.io/en/latest/reference/commands/mrdegibbs.html) · [gibbs_removal (DIPY)](https://dipy.org/documentation/1.5.0./reference/dipy.denoise.gibbs.html) |


### Existing Pipelines 

The existing pipeline can be used to accelerate the selection or application of various pre-processing steps. 

| Name | What it does | Link |
|---|---|---|
| **fMRIPrep** | Robust, reproducible BIDS fMRI preprocessing using FSL, ANTs, FreeSurfer, AFNI. | [https://fmriprep.org/en/stable/](https://fmriprep.org/en/stable/) |
| **sMRIPrep** | Structural MRI preprocessing (T1w, T2w, FLAIR) with B1 correction, segmentation, normalization, and skull stripping. | [https://www.nipreps.org/smriprep/](https://www.nipreps.org/smriprep/) |
| **QSIPrep** | Diffusion MRI preprocessing, denoising, and reconstruction. | [https://qsiprep.readthedocs.io/en/latest/](https://qsiprep.readthedocs.io/en/latest/) |
| **TORTOISE** | Diffusion MRI processing suite with DIFFPREP, DR-BUDDI, DIFFCALC, DRTAMAS modules. | [https://tortoise.nibib.nih.gov/](https://tortoise.nibib.nih.gov/) |
| **DeepPrep** | Deep-learning MRI preprocessing pipeline using FastSurfer, FastCSR, SUGAR, and SynthMorph (Nextflow-based). | [https://deepprep.readthedocs.io/en/latest/](https://deepprep.readthedocs.io/en/latest/) |
| **FreeSurfer recon-all** | Full cortical reconstruction, segmentation, and surface generation pipeline. | [https://surfer.nmr.mgh.harvard.edu/fswiki/recon-all](https://surfer.nmr.mgh.harvard.edu/fswiki/recon-all) |
| **FSL_anat** | Anatomical preprocessing: reorientation, cropping, bias correction, registration, brain extraction, segmentation. | [https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/fsl_anat](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/fsl_anat) |
| **MRtrix3 dwipreproc** | DWI preprocessing script for motion, eddy-current, and susceptibility correction (FSL integration). | [https://mrtrix.readthedocs.io/en/latest/reference/scripts/dwipreproc.html](https://mrtrix.readthedocs.io/en/latest/reference/scripts/dwipreproc.html) |
| **AFNI afni_proc.py** | fMRI processing script generator for single-subject analyses (task/rest). | [https://afni.nimh.nih.gov/pub/dist/doc/program_help/afni_proc.py.html](https://afni.nimh.nih.gov/pub/dist/doc/program_help/afni_proc.py.html) |
| **SynthSeg** | Contrast-agnostic brain segmentation for QC or downstream use. | [https://github.com/BBillot/SynthSeg](https://github.com/BBillot/SynthSeg) |
| **ITK-SNAP** | Interactive 3D segmentation and inspection utility. | [https://www.itksnap.org/download/snap/](https://www.itksnap.org/download/snap/) |
