# Intel Image Classification --- ResNet18 (PyTorch)

------------------------------------------------------------------------

## 📌 Deskripsi Singkat

Klasifikasi gambar 6 kelas (buildings, forest, glacier, mountain, sea,
street) menggunakan ResNet18. Dataset: Intel Image Classification. Model
dilatih dengan PyTorch, mencapai akurasi **92.9%** di data test.
Mendukung inference langsung dari model tersimpan.

------------------------------------------------------------------------

## 📂 Dataset

Kaggle Dataset:\
https://www.kaggle.com/datasets/puneet6060/intel-image-classification

------------------------------------------------------------------------

## 📁 Project Structure

    📦 intel-resnet18-image-classification
    │
    ├── saved_model_TORCH/
    │   └── best_model.pth
    │
    ├── train.ipynb
    ├── predict.py
    ├── requirements.txt
    └── README.md

------------------------------------------------------------------------

## ⚙️ Environment

Project sudah menyertakan `requirements.txt`, sehingga instalasi cukup
dengan:

    pip install -r requirements.txt

------------------------------------------------------------------------

## 📊 Hasil Model

**=== Classification Report ===**

                  precision    recall  f1-score   support
    buildings       0.9500    0.9130    0.9312       437
    forest          0.9812    0.9895    0.9853       474
    glacier         0.8818    0.8770    0.8794       553
    mountain        0.8990    0.8648    0.8816       525
    sea             0.9471    0.9824    0.9644       510
    street          0.9247    0.9561    0.9401       501

    accuracy                         0.9290      3000
    macro avg       0.9306    0.9305    0.9303      3000
    weighted avg    0.9287    0.9290    0.9286      3000

**=== FINAL TEST METRICS ===**

    Precision : 0.9287
    Recall    : 0.9290
    F1 Score  : 0.9286
    Accuracy  : 0.9290

------------------------------------------------------------------------

## 🚀 Training

Semua proses training dilakukan dalam **1 notebook**:

    train.ipynb

Jika ingin menjalankan training via script (opsional):

    python train.py

------------------------------------------------------------------------

## 🔍 Inference

### 📌 Menggunakan fungsi Python

    from predict import predict_image

    img, pred = predict_image("test.jpg")
    print("Predicted:", pred)

### 📌 Melalui CLI

    python predict.py --img "test.jpg"

### 📌 Dalam Notebook (train.ipynb)

Model otomatis diload dari folder `saved_model_TORCH/` dan dapat
menjalankan prediksi langsung pada cell inference.

------------------------------------------------------------------------

## 📎 Model

Model tersimpan berada di:

    saved_model_TORCH/best_model.pth
