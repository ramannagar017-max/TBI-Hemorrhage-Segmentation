# TBI-Hemorrhage-Segmentation
I have built a preprocessing pipeline and used a Swin-Unet model with weighted sampling and combined loss functions to improve segmentation accuracy, helping in faster and more reliable detection of brain hemorrhages.
## 📌 Features
- Preprocessing pipeline:
  - Normalization  
  - CLAHE + Gamma Correction for contrast enhancement  
  - Sharpening to highlight lesion boundaries  
  - Bilateral Denoising to preserve edges while removing noise  
- Weighted sampling to address class imbalance  
- Data augmentation (rotations, flips, intensity variations)  
- Two-phase training:
  - Phase 1: Frozen encoder, training decoder + segmentation head  
  - Phase 2: Full fine-tuning of encoder + decoder  
- Loss functions explored:
  - Dice Loss  
  - Dice + BCE  
  - Dice + BCE + Focal Tversky (best performance)  
- Evaluation with per-class Dice, mean Dice, and qualitative results  
- Foundation for 3D volume estimation from stacked slices  

---

## 🛠️ Tech Stack
- Python 3.x  
- PyTorch / MONAI  
- NumPy, OpenCV  
- Matplotlib, Seaborn  
- scikit-learn  
