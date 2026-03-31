# Spectral-X: Latent Prior Enhanced Spectral CT Restoration with Mamba-assisted X-Net
Yikun Zhang, Jiashun Wang, Xi Wang, et al.


## Abstract
> Compared with conventional computed tomography (CT), spectral CT can simultaneously visualize internal structures and characterize the material composition of scanned objects by acquiring data at different energy spectra. Photon-counting CT (PCCT) and multi-source CT (MSCT) are two promising implementations of spectral CT. Besides, radiation exposure remains a long-standing concern in CT imaging, as excessive X-ray exposure may lead to genetic and cellular damage. For PCCT and MSCT, the radiation dose can be reduced by lowering the tube current and adopting complementary limited-view scanning, respectively. To mitigate the noise and artifacts induced by low-dose acquisition protocols, this paper proposes a Mamba-assisted X-Net leveraging latent priors for spectral CT, termed Spectral-X. First, considering the intrinsic characteristics of spectral CT, Spectral-X exploits the latent representation of the enhanced full-spectrum prior image to facilitate the restoration of multi-energy CT (MECT). Second, Spectral-X employs an X-shaped network with feature fusion blocks to adaptively capture and leverage multi-scale prior information in the latent space. Third, Spectral-X integrates a novel all-around Mamba mechanism that can efficiently model long-range dependencies, thereby enhancing the performance of the image restoration backbone network. Spectral-X is evaluated on both PCCT denoising and limited-view MSCT restoration tasks, and the experimental results demonstrate that Spectral-X achieves state-of-the-art performance in noise suppression, artifact removal, and structural restoration.

## Motivation Diagram
>As illustrated in (c5) and (d5), although the raw PCCT prior reconstructed using the full-spectrum projection data and the raw MSCT prior reconstructed using the merged projection data exhibit significantly better quality compared to the corresponding degraded MECT images, the raw prior images still suffer from slight artifacts and noise. Using such images as priors might lead to suboptimal results. In fact, the slight artifacts and noise can be easily eliminated to produce the enhanced prior images, as shown in (c6) and (d6). Taking the latent representation of the enhanced prior as guidance facilitates the restoration of the degradedMECT images.
<figure align="center">
  <img src="./assets/Motivation.jpg" width="100%">
  <figcaption>
    (a) Diagram of the complementary limited-view scanning protocol for multi-source CT.
    (b) Diagram of the scanning principle for photon-counting CT.
    (c1)–(c4) Degraded multi-energy CT images obtained through (a).
    (c5) Raw prior image from merged projections.
    (c6) Enhanced prior image in MSCT.
    (d1)–(d4) Degraded images from (b).
    (d5) Raw prior image from full-spectrum projections.
    (d6) Enhanced prior image in PCCT.
  </figcaption>
</figure>

## Architecture Diagram
<p align="center"> <img src="./assets/Network.jpg" width="100%"> </p>

## Visual Result @ PCCT Denoising
<p align="center"> <img src="./assets/Comparison@PCCT.jpg" width="100%"> </p>

## Visual Result @ Sparse-View MSCT Restoration
<p align="center"> <img src="./assets/Comparison@MSCT.jpg" width="100%"> </p>

## Usage
### 1.Environment Setup
```bash
pip install -r requirements.txt
```
