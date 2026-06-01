# 📊 Uçtan Uca Müşteri Kaybı (Churn) Tahmini Pipeline Tasarımı

Bu proje, **BLM308 Veri Madenciliği** dersi kapsamında, abonelik tabanlı telekomünikasyon sistemlerinde müşteri kaybını (churn) önceden tahmin etmek amacıyla geliştirilmiştir. Süreç, **CRISP-DM** metodolojisi referans alınarak yürütülmüştür.

---

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler
- **Dil:** Python 3.x
- **Ortam:** Google Colab
- **Veri Manipülasyonu & Analiz:** `pandas 2.x`, `numpy`
- **Makine Öğrenmesi & Ön İşleme:** `scikit-learn 1.x`, `imblearn` (SMOTE)
- **Görselleştirme:** `matplotlib`, `seaborn`

---

## 🚀 Proje Yapısı ve Dosyalar
Projenin tüm kaynak dosyaları ana dizinde erişilebilir şekilde sunulmuştur:
- `rapor_churn_prediction.pdf`: Projenin \LaTeX\ ile yazılmış akademik final raporu.
- `rapor.tex`: Raporun \LaTeX\ kaynak kodları.
- `churn_pipeline.ipynb`: Tüm veri dönüştürme, ön işleme ve modelleme adımlarını içeren Jupyter Notebook dosyası.
- `Telco_customer_churn.xlsx`: IBM Telco Customer Churn ham Excel veri seti.
- `Telco_customer_churn.csv`: Excel'den Python ortamına aktarılarak dönüştürülen ana veri seti.
- `churn_dagilim.png` & `monthly_charges_kde.png`: Keşifsel Veri Analizi (EDA) grafikleri.
- `confusion_matrix.png`: En başarılı model olan Random Forest'a ait karmaşıklık matrisi.


---

## 📈 Model Performans Karşılaştırması
Eğitim kümesindeki sınıf dengesizliği problemi **SMOTE** algoritmasıyla $1:1$ oranına getirilerek çözülmüştür. Modellerin test kümesi üzerindeki sonuçları şu şekildedir:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Decision Tree** | 0.7316 | 0.4953 | 0.5704 | 0.5302 | 0.6807 |
| 🚀 **Random Forest (Tuned)** | **0.7761** | **0.5664** | 0.6684 | 0.6132 | 0.8299 |
| 🎯 **Logistic Regression** | 0.7576 | 0.5300 | **0.7700** | **0.6279** | **0.8475** |

### 🧠 Önemli Bulgular
- **En Yüksek Doğruluk (Accuracy):** %77.61 ile hiperparametre ayarı yapılmış (Tuned) Random Forest modeli en istikrarlı model olmuştur.
- **En Yüksek Yakalama Gücü (Recall):** %77.00 recall skoru ile Lojistik Regresyon, şirketi terk edecek riskli müşterileri en az hatayla yakalayan algoritmadır.

---

## 🎥 Proje Demo Videosu
Projenin kod yürütme, veri ön işleme adımları ve metrik analizini içeren ekran kaydı anlatım videosuna aşağıdaki bağlantıdan ulaşabilirsiniz:
👉 [BLM308 Veri Madenciliği Proje Demosu - Ekran Kaydı](https://drive.google.com/file/d/1dQ_uFwsxvuPhi0Xj0evMJKrySr6ApXeI/view?usp=sharing)

---

## 🧑‍💻 Geliştirici
- **Ad Soyad:** Evla Karagöz
- **Öğrenci Numarası:** 231041040
- **Bölüm:** Bilgisayar Mühendisliği Bölümü
