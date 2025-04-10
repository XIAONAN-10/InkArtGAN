# InkArtGAN
official implementation and DataSet of ink art Gan, A Gan-based model for high-quality ink painting generation with cultural feature fusion.
# InkArtGAN: A Deep Learning-Based Approach for Digital Generation of Ink Painting

This repository contains the official implementation, datasets, and results for the paper:

**InkArtGAN: A Deep Learning-Based Approach for Digital Generation of Ink Painting**  
Submitted to *Journal of Intelligent Manufacturing*, 2025.

## 🔍 Overview

InkArtGAN is an end-to-end generative framework designed to improve digital ink painting through:
- HSV-based preprocessing for seal removal
- VGG-based perceptual loss for brushstroke refinement
- Real-ESRGAN for resolution enhancement
- Cultural feature fusion via seal and inscription module

## 📁 Repository Contents

- `datasets/` – Example training data and processed ink images  
- `models/` – Trained model checkpoints  
- `results/` – Generated sample outputs  
- `src/` – Core training and testing code  
- `utils/` – Preprocessing scripts, loss functions, etc.

## 📦 Data & Model Access

All datasets and models are publicly available in this repository. Please cite our work if you use them.

## 📝 License

This project is released under the MIT License.

## 📫 Contact

For questions, please contact the corresponding author: [wxn1014@gmail.com]
