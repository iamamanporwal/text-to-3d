![logo0](https://github.com/user-attachments/assets/5897092a-e745-4463-82c4-a21ca2a903c8) ![Views](https://komarev.com/ghpvc/?username=iamamanporwal&color=blue)


# VI3W ai: Text-to-3D Objects and Image-to-3D Objects.
A Text-to-3D & Image-to-3D model which is highly useful for Augmented Reality Pipeline in Ecom apps.

### Description: 
A system for generating high-resolution 3D objects from text prompts, using a combination of Stable Diffusion, Segment Anything Model 2 (SAM 2), and Instant NGP/NeRF. The purpose is to provide a scalable and efficient solution for text-to-3D content creation, metaverse and 3D printing.

## High-Level Architecture 🚀

### Overview:
The system consists of seven stages:
* Text-to-Image > Object Recognition > Character Sheet Generation > Character Sheet Segmentation > Image-to-3D > Discrimination > Rendering

### Key Components:
* Stable Diffusion (Text-to-Image)
* SAM 2 (Object Recognition)
* Control Net (Character Sheet Generation)
* Character Sheet Segmentation
* Instant NGP/NeRF (Image-to-3D)
* GAN's (Discrimination)

## Method Overview 🧊
![image](https://github.com/user-attachments/assets/70edaf6f-fdd9-4609-bc93-2c8440d5be06)<br>
In the Text-to-3D Object Generation project, the process begins with converting text prompts into 2D images using Stable Diffusion, which generates a visual representation of the described object or scene. These images are then analyzed by SAM 2, which segments individual objects within the image, isolating them for further processing. Control Net is employed to create a character sheet, offering multiple views of the segmented objects, essential for building a comprehensive 3D model.

Following this, the character sheet is segmented into individual object views, which are then transformed from 2D into 3D models using Instant NGP/NeRF, producing realistic three-dimensional representations. These 3D models undergo evaluation by GANs, which assess their quality, determining whether they meet the required standards. If the model is satisfactory, it is rendered as the final 3D object; if not, the model is re-generated to ensure high-quality output. This streamlined process efficiently converts text into high-resolution 3D objects through a series of advanced AI-driven stages.

## Components 🛠️

### Text-to-Image (Stable Diffusion)
* **Input:** Text prompt
* **Output:** 2D image

### Object Recognition (SAM 2)
* **Input:** 2D image
* **Output:** Segmented objects (e.g., chicken, surfboard)

### Character Sheet Generation (Control Net)
* **Input:** Segmented objects
* **Output:** Character sheet with multiple vi3ws

### Character Sheet Segmentation
* **Input:** Character sheet
* **Output:** Individual object vi3ws

### Image-to-3D (Instant NGP/NeRF)
* **Input:** Individual object vi3ws
* **Output:** 3D model

### Discrimination (GAN's)
* **Input:** 3D model
* **Output:** Discrimination result (good/bad)

### Rendering
* **Input:** Discrimination result
* **Output:** Final 3D model (if good) or re-generated model (if bad)

## Research Citations 📝 
[Magic3D: High-Resolution Text-to-3D Content Creation](https://research.nvidia.com/labs/dir/magic3d/)<br>
[SAM 2: Segment Anything](https://github.com/facebookresearch/segment-anything-2)<br>
[Stable Diffusion](https://github.com/Stability-AI/stablediffusion)<br>
[Stable Diffusion architecture](https://jalammar.github.io/illustrated-stable-diffusion/)

