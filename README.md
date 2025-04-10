# 🖌️ InkArtGAN: An AI-based Ink Painting Generation System

InkArtGAN is a modular system designed to generate high-quality digital Chinese ink paintings from natural landscape photographs. It consists of data preprocessing, a GAN-based generation module, and post-processing modules including resolution enhancement and stylistic finishing like inscriptions and seals.

<p align="center">
  <img src="docs/Fig1_pipeline.png" alt="Pipeline" width="80%">
</p>

*Fig. 1. Pipeline of the Ink Painting System. The system includes (1) Data Processing Module (yellow, left), (2) GAN-Based Ink Painting Generation Module (blue, middle), and (3) Post-Processing and Enhancement Module (pink, right), producing the final ink painting with high resolution and cultural elements.*

---

### 🎨 Final Ink Painting Results

<p align="center">
  <img src="docs/result_01_mountain.png" width="24%">
  <img src="docs/result_02_mountain.png" width="24%">
  <img src="docs/result_03_mountain.png" width="24%">
  <img src="docs/result_04_mist.png" width="24%">
</p>

<p align="center">
  <img src="docs/result_05_temple.png" width="24%">
  <img src="docs/result_06_mountain.png" width="24%">
  <img src="docs/result_07_mist.png" width="24%">
  <img src="docs/result_08_mist.png" width="24%">
</p>

---

## 📁 Project Structure Overview

```
InkArtGAN/
├── DataProcessingModule_DataB/     # Red stamp removal and dataset cleaning
│   ├── dataB_raw/
│   ├── trainB_inpainted/
│   ├── batch_remove_redseal.py
│   ├── manual_inpaint_example.py
│   └── README.md

├── GAN_Generation_Module/          # GAN model training and testing
│   ├── datasets/
│   ├── pretrained_weights/
│   ├── saved_models/
│   ├── test_images/
│   ├── test_results/
│   ├── tools/
│   ├── utils/
│   ├── config.py
│   ├── train.py
│   ├── test.py
│   └── README.md

├── PostProcessing_Module/          # Super-resolution and artistic stamping
│   ├── real_esrgan/
│   │   ├── inference_realesrgan.py
│   │   ├── weights/
│   │   └── README.md
│   ├── stamp_text_module/
│   │   ├── fonts/
│   │   ├── output/
│   │   ├── references/
│   │   ├── results/
│   │   ├── seal.am/
│   │   ├── add_stamp_text.py
│   │   ├── utils.py
│   │   ├── requirements.txt
│   │   └── README.md
│   └── final_outputs/

├── experiment_data/                # Experiment results and comparisons
│   ├── generated_full_system/
│   ├── generated_with_loss/
│   ├── generated_with_resolution/
│   ├── generated_without_loss/
│   ├── input_images/
│   ├── reference_images/
│   ├── scripts/
│   ├── test_super_resolution.py
│   └── test_vgg_perceptual_loss.py

├── final_images/                   # Final output paintings
├── requirements.txt                # Global dependencies
└── README.md                       # Root documentation file
```

---

## 🔧 Environment Setup

Create and activate a virtual environment, then install dependencies:

```bash
pip install -r requirements.txt
```

Each module also contains its own `requirements.txt` file if run independently.

---

## 🚀 Pipeline Summary

1. **Data Preprocessing**:
   - Red seal removal using HSV masking and inpainting.
   - Cleaned dataset used to train the GAN model.

2. **GAN Generation Module**:
   - A CycleGAN-based model trained on real and generated ink data.
   - Outputs low-resolution ink-style images from real photos.

3. **Post-Processing**:
   - Apply Real-ESRGAN (`real_esrgan/`) to enhance image resolution.
   - Add digital Chinese seals and inscription text via `stamp_text_module/`.

4. **Evaluation**:
   - Result comparisons available in `experiment_data/`.

---

## 📌 Citation Reference

Reference layout and stamping design inspired by:
**“Arrangement Scheme of Inscriptions and Seals in Chinese Ink Landscape Painting”**

---

## License  
This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## 📬 Contact

For questions, reach out to the developer or open an issue.
