# 💗 Segmentasi dan Klasifikasi Tumor Malignant pada Citra Ultrasound Payudara menggunakan Deep Learning

Dataset : https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset (malignant)

Proyek ini bertujuan mengembangkan sistem segmentasi otomatis berbasis Deep Learning untuk mendeteksi tumor ganas (malignant) pada citra ultrasound payudara. Dengan pendekatan ini, proses diagnosis dapat dilakukan lebih cepat, akurat, dan efisien.

---


## 🎯 Tujuan

1. Mengembangkan model segmentasi citra ultrasound payudara yang akurat menggunakan U-Net.
2. Mengevaluasi efektivitas segmentasi menggunakan Deep Learning vs metode konvensional.
3. Membangun sistem klasifikasi dan segmentasi otomatis untuk mendukung diagnosis kanker payudara.

---

## 🔧 Metodologi

### 🛠️ Metode Konvensional
- **Preprocessing:** Penyesuaian kontras, histogram equalization, normalisasi, resizing.
- **Segmentasi:** Thresholding, deteksi tepi (sobel, canny), morphological operation.
- **Post-processing:** Fill holes, dilasi/erosi.
- **Optimisasi:** Active contour, Chan-Vese, morphological refinement.
- **Evaluasi:** Jaccard Index, visualisasi overlay GT.

### 🤖 Metode Deep Learning
- **Preprocessing:** Resize gambar 256x256, augmentasi rotasi/zoom.
- **Model:** U-Net + Attention Gate.
- **Pelatihan:** Adam Optimizer, Binary Crossentropy Loss, 25 epoch, EarlyStopping.
- **Evaluasi:** Accuracy, Loss, IoU, visualisasi input-GT-prediksi.

---

## 🧪 Hasil Evaluasi

### 📉 Metode Konvensional

| Iterasi | Jaccard Index |
|--------|----------------|
| Iter-001 | 19.77% |
| Iter-002 | 18.62% |
| Iter-003 | 18.89% |
| Iter-004 | 18.88% |
| Iter-005 | 18.94% |
| Iter-006 | 18.89% |

**Final Jaccard Index (tanpa leak): 65.15%**  
> Setelah refinement dengan morphological + Chan-Vese, tanpa GT, dicapai peningkatan signifikan.

### 📈 Metode Deep Learning

- **Akurasi pelatihan meningkat**, loss menurun, dan **IoU stabil di sekitar 0.43**.
- Visualisasi hasil segmentasi menunjukkan **prediksi mendekati ground truth**, lebih baik dibanding metode konvensional.

---



