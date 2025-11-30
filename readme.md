# MSCViT: Multi-Scale Convolutional Vision Transformer for Pneumonia

**Hybrid CNN + ViT for Tiny Medical Datasets – Applied to Pneumonia Detection**

[![arXiv](https://img.shields.io/badge/arXiv-2501.06040-b31b1b.svg)](https://arxiv.org/abs/2501.06040)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Deep Learning in Medical Science](meta/Pneumonia.png)

MSCViT is a lightweight hybrid neural network combining the strengths of Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs). It integrates convolutions for local feature extraction with multi-scale self-attention for global context, making it exceptionally suited for data-scarce medical imaging tasks.

This repository includes an implementation inspired by the MSCViT architecture, applied to **pneumonia detection in chest X-rays**, where datasets are often limited, imbalanced, and privacy-constrained.

---

## 🚀 Why MSCViT for Medical Imaging?

| Medical Challenge                 | MSCViT Solution                                            |
| --------------------------------- | ---------------------------------------------------------- |
| Limited labeled data              | Convolutional priors reduce ViT's data needs               |
| Class imbalance                   | Multi-scale attention + support for weighted sampling/loss |
| Need both local & global features | Depth-wise convolutions + long-range attention             |
| Resource-constrained deployment   | Lightweight (3.8M–26M params, 0.5–4.8 GFLOPs)              |
| Interpretability                  | Sharper Grad-CAM heatmaps                                  |

MSCViT excels particularly in **tiny medical datasets**, outperforming CNNs and ViTs of similar size.

---

## 🧠 Architecture Overview

MSCViT integrates:

* **LFE** – Local Feature Extraction using 3×3 and 1×1 depth-wise convolutions
* **LMSSA** – Lightweight Multi-Scale Self-Attention with coarse-to-fine fusion
* **CFF** – Wavelet-based Convolutional Feature Fusion
* **FFN** – Standard feed-forward module

![MSCViT Architecture](meta/MSCViT.jpg)

---

## 👨‍⚕️ Clinical Workflow Example

![Doctor Workflow](meta/Pneumonia.gif)

---

## 📦 Repository Structure

```
MSCViT/
│
└── NoteBook/
   ├──  Chester MSCViT Training.ipynb      # Training-only notebook
   └──  Chester MSCViT Inference.ipynb     # Inference-only notebook
   
```

| Notebook                           | Colab Link                                                                                                                                                                                         |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Chester MSCViT Inference.ipynb** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MHM-Rajpoot/pneumonia/blob/main/NoteBook/Chester%20MSCViT%20Inference.ipynb) |
| **Chester MSCViT Training.ipynb**  | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MHM-Rajpoot/pneumonia/blob/main/NoteBook/Chester%20MSCViT%20Training.ipynb)  |


---

## 🧪 Features

* Train-from-scratch capability on tiny datasets
* Class-balanced loaders for medical imbalance issues
* Mixup, CutMix, and medical-specific augmentations
* Grad-CAM heatmaps for interpretability
* Modular architecture for easy customization

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgements

Special thanks to the researchers behind MSCViT and the creators of the Chest X-ray pneumonia dataset.

---

For questions or issues, feel free to open an **issue** or a **pull request**!








