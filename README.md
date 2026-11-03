# MPCDehazeNet: Midget--Parasol Collaboration for Structure-Guided Remote Sensing Image Dehazing

MPCDehazeNet is an end-to-end remote-sensing image dehazing network inspired by complementary coarse- and fine-scale visual processing. It coordinates broad appearance correction and local detail recovery through two parallel pathways. The Parasol Structure Pathway (PSP) learns a bounded smooth coarse proposal and structural context without auxiliary coarse-image supervision, while the MSViM-based MPCDehaze-U backbone produces a detail-oriented estimate using decoder-guided skip fusion. The Cortical Texture Integrator (CTI) then spatially blends the two image proposals and uses structural context to condition feature-space refinement. Within CTI, two cascaded Retinal Dual Cells capture complementary spatial contexts, and a learned gate regulates the incremental update from the second cell. The resulting features predict a spatially controlled, amplitude-bounded correction to refine the blended image.

---

## 🧠 Network Architecture

![Network Architecture](images/1.png)

---

### 🚀 Getting Started

We train and test the code on **PyTorch 1.13.0 + CUDA 11.8**. The detailed configuration is mentioned in the paper.

#### Create a new conda environment
```bash
conda create -n MPCDehazeNet python=3.8 
conda activate MPCDehazeNet


