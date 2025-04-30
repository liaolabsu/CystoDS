# CystoDS, a multi-class image dataset for computer-assisted cystoscopy
**CystoDS** is a curated image dataset for bladder cancer research, designed for the development and validation of AI-based cystoscopic image classification models. It includes 68,944 high-quality annotated images across 160 patients, with ground truth labels linked to pathology results.

This repository provides:
- Dataset overview
- Model evaluation results
- Download links for trained models
- Optional scripts for inference demonstration

> 🔧 Code is not provided here since all models were implemented using [OpenMMLab's MMPRETRAIN](https://github.com/open-mmlab/mmpretrain).
>
> ---
>
> ## 📦 Dataset Summary

- **Total Images**: 68,944
- **Categories**:
  - Malignant tumor
  - Benign lesion
  - Normal mucosa
  - Ureteral orifice
  - Foreign body
  - Resection scar
  - Instrument
- **Source**: Cystoscopy videos with pathology-confirmed labeling
- **Annotations**: Region-level, expert-verified

---

## 🧠 Models Used for Evaluation

We validated CystoDS using four backbone architectures from MMPRETRAIN:
- ResNet-50
- EfficientNet-B0
- HRNet-W18
- Swin-Transformer-Tiny

See [MODEL_ZOO.md](./MODEL_ZOO.md) for details and performance.

---

## 🚀 Download Trained Models

| Model                | Download Link                                 |
|---------------------|-----------------------------------------------|
| ResNet-50           | [Google Drive](#) / [Baidu Pan](#)           |
| EfficientNet-B0     | [Google Drive](#) / [Baidu Pan](#)           |
| HRNet-W18           | [Google Drive](#) / [Baidu Pan](#)           |
| Swin-Tiny           | [Google Drive](#) / [Baidu Pan](#)           |

All checkpoints are fine-tuned on CystoDS.

---

## 🧪 Inference Example (Optional)

You can run inference using a trained model and sample config:

python sample_inference/inference.py \
    --img_path test.jpg \
    --checkpoint trained_models/resnet50_cystods.pth \
    --config configs/resnet50_cystods.py

---

## 📋 Evaluation Results

| Model              | Accuracy | Precision | Recall | F1-Score |
|-------------------|----------|-----------|--------|----------|
| ResNet-50         | XX.X%    | XX.X%     | XX.X%  | XX.X%    |
| EfficientNet-B0   | XX.X%    | XX.X%     | XX.X%  | XX.X%    |
| HRNet-W18         | XX.X%    | XX.X%     | XX.X%  | XX.X%    |
| Swin-Tiny         | XX.X%    | XX.X%     | XX.X%  | XX.X%    |

---

## 📌 Citation

@article{qiu2025cystods,
  title={CystoDS, a multi-class image dataset for computer-assisted cystoscopy},
  author={Tim and et al.},
  journal={Scientific Data},
  year={2025}
}

