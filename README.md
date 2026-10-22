# 💻 UTS Machine Learning: Regresi Linier & Logistik

## 📌 Data Mahasiswa
* **Nama** : RAIHAN PUTRA FADILAH KUSUMA
* **NIM** : 241011401665
* **Kelas** : Reg C (05TPLE005)
* **Random State** : 65

---

## 📊 Rangkuman Perhitungan & Evaluasi Model

### 1. Model Linear Regression (`Ads_Data.csv`)
* **Persamaan Regresi (Normal Equation):**
  $$\hat{y} = 27.5256 + 9.2131 \times X$$

* **Metrik Kinerja Model:**
  | Dataset | MAE | MSE | RMSE | R² Score |
  |---|---|---|---|---|
  | **Training** | 3.8763 | 23.3664 | 4.8339 | 96.34% |
  | **Testing** | 7.1517 | 81.3320 | **9.0184** | **85.21%** |

* **Eksperimen Learning Rate:**
  - `Alpha = 0.001`: Lambat konvergen.
  - `Alpha = 0.02`: **Optimal**, hasil identik dengan Normal Equation.
  - `Alpha = 0.1`: Divergen / *overflow*.

---

### 2. Model Logistic Regression (`Email_Data.csv`)
* **Persamaan Probabilitas:**
  $$P(\text{Spam}) = \sigma(-9.2892 + 0.8569 \cdot \text{JumlahLink} + 0.8033 \cdot \text{KataPromo})$$

* **Perbandingan Ambang Batas (Threshold) Data Testing:**
  | Threshold | TN | FP | FN | TP | Akurasi | Presisi | Recall | F1-Score |
  |---|---|---|---|---|---|---|---|---|
  | `0.3` | 6 | 3 | 0 | 6 | 80.00% | 66.67% | 100.00% | 80.00% |
  | `0.5` | 8 | 1 | 1 | 5 | 86.67% | 83.33% | 83.33% | 83.33% |
  | **`0.7` (Dipilih)** | **9** | **0** | **1** | **5** | **93.33%** | **100.00%** | **83.33%** | **90.91%** |

* **Catatan Threshold:**
  Threshold **0.7** dipilih karena berhasil menekan **False Positive (FP) hingga 0%**, sehingga email penting tidak akan salah dikategorikan sebagai spam.

---

## 🛠️ Cara Menjalankan
Buka file `tugas_UTS.ipynb` menggunakan Jupyter Notebook / VS Code lalu pilih perintah **Run All**.
