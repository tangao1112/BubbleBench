# BubbleBench: Bubble Image Datasets
This repository contains three distinct datasets related to bubble images: **Annotated Bubble Dataset**, **Defocused Bubble Dataset**, and **Simulated Bubble Dataset**. The dataset can be viewed from the branch (master). Below is a detailed description of each dataset.

---

## Annotated Bubble Dataset
- **Description**: 100 bubble images were randomly selected from 7 experimental conditions (details in Appendix I) and semi-automatically annotated using the open-source tool [Labelme](https://doi.org/10.1007/s11263-007-0090-8). A total of 12,159 discrete bubbles and 907 overlapping bubbles were annotated. The equivalent circular diameter of the annotated bubbles is mostly less than 1000 μm, with a concentration in the range of 200 to 600 μm.
- **Usage**: Primarily used for training and validating various deep learning models.
- **Dataset Structure**:
  - Total images: 100
  - Training set: 80 images
  - Test set: 20 images
  - Formats: COCO dataset format and Stardist/Splinedist-compatible formats.

---

## Defocused Bubble Dataset
- **Description**: 1,000 defocused bubble samples were selected from the annotated bubble dataset to create this dataset. It is mainly used to compare the ability of different models in edge detection of defocused bubbles.
- **Dataset Construction**: Randomly extracted 1000 discrete bubbles from the annotated dataset using the provided code (path: `Experimental Dataset\defocused bubbles`).

---

## Simulated Bubble Dataset
- **Description**: The [BubGAN model](https://doi.org/10.1016/j.ces.2019.04.004) was used to generate simulated bubble images at different porosities (ε). Gaussian blur was applied to simulate defocus effects, and overlapping bubbles with varying degrees of defocus were generated to ensure similarity to experimental images.
- **Dataset Structure**:
  - Total images: 180 (60 images for each porosity: ε = 0.1, 0.15, 0.2)
  - Formats: COCO dataset format and Stardist/Splinedist-compatible formats.
- **Validation**: The distribution characteristics of bubble area fraction (φ) in both experimental and simulated images are compared in Figure A4.

---

## Publication
For more details, please refer to our publication:  
**Cai T, Tang A, Xu R, et al.** *Balanced Deep Learning-Based Bubble Segmentation: Model Comparison, Optimization, and Application in Microbubble Detection.*  
[Read the paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5142422)  

If this work inspires you, please cite our paper!

---

## References
1. **LabelMe**: Russell, B. C., Torralba, A., Murphy, K. P., et al. *LabelMe: a database and web-based tool for image annotation.* International Journal of Computer Vision, 2008. [DOI](https://doi.org/10.1007/s11263-007-0090-8)  
2. **Stardist**: Schmidt, U., Weigert, M., Broaddus, C., et al. *Cell detection with star-convex polygons.* MICCAI, 2018.  
3. **SplineDist**: Mandal, S., Uhlmann, V. *SplineDist: Automated Cell Segmentation with Spline Curves.* IEEE ISBI, 2021.  
4. **BubGAN**: Fu, Y., Liu, Y. *BubGAN: Bubble generative adversarial networks for synthesizing realistic bubbly flow images.* Chemical Engineering Science, 2019. [DOI](https://doi.org/10.1016/j.ces.2019.04.004)  
5. **Depth from Defocus**: Xu, R., Huang, Z., Gong, W., et al. *Depth from Defocus technique for irregular particle images.* Measurement, 2024. [DOI](https://doi.org/10.1016/j.measurement.2024.115156)  

---

