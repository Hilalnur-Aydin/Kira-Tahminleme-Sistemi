# 🏠 Kira Tahminleme Sistemi

Bu proje, gerçek dünyadan alınan konut verileri kullanılarak kira fiyatlarının tahmin edilmesini amaçlayan bir makine öğrenmesi uygulamasıdır. Veri ön işleme, öznitelik mühendisliği, görselleştirme ve regresyon modellerinin karşılaştırılması adımları içerir.

---

## 🎯 Projenin Amacı

Gerçek dünya konut verisiyle regresyon modelleri kurma ve performanslarını değerlendirme becerisini geliştirmek.

---

## 📊 Kullanılan Veri Seti

- **Veri Kaynağı:** Kamuya açık `House_Rent_Dataset.csv` (veri içeriği Kolkata, Mumbai, Delhi gibi Hint şehirlerine ait kira ve ev özellikleri)
- **Özellikler:**  
  - `BHK` (oda sayısı)  
  - `Rent` (kira fiyatı)  
  - `Size` (metrekare)  
  - `Bathroom` (banyo sayısı)  
  - `Floor` (kat bilgisi: “ground out of 2” gibi)  
  - `Area Type` (Super Area, Carpet Area vb.)  
  - `City` (şehir ismi)  
  - `Furnishing Status` (Eşyaların durumu)  
  - `Tenant Preferred` (kiracı tercihi)  

---

## ⚙️ Veri Ön İşleme ve Özellik Mühendisliği

- Eksik değerler temizlendi.
- `Floor` sütunundan iki ayrı sütun çıkarıldı:  
  - `Floor Level`: Bulunduğu kat (ground=0 olarak kodlandı)  
  - `Total Floors`: Binadaki toplam kat sayısı
- Kategorik değişkenler (City, Furnishing Status, Tenant Preferred, Area Type) One-Hot Encoding ile sayısallaştırıldı.

---

## 📈 Görselleştirme

- Kira fiyatı dağılımı ve özniteliklerle korelasyon grafiklerle analiz edildi.

---

## 🧮 Modelleme

İki farklı regresyon modeli uygulandı ve karşılaştırıldı:

| Model               | Açıklama                          |
|---------------------|----------------------------------|
| Linear Regression   | Basit doğrusal regresyon modeli  |
| XGBoost Regressor   | Gelişmiş, ağaç tabanlı ensemble  |

---

## 📉 Performans Değerlendirmesi

Model başarısı aşağıdaki metriklerle ölçüldü:

- RMSE (Root Mean Square Error)
- MAPE (Mean Absolute Percentage Error)

---

## 🛠️ Kullanılan Kütüphaneler

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

---

## 📁 Projenin Çalıştırılması

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
2. KiraTahminlemeSistemi.ipynb dosyasını Jupyter Notebook veya Google Colab üzerinde açın.

3. Veri dosyasını (House_Rent_Dataset.csv) yükleyin ve notebook’u çalıştırın.

📌 Notlar
Proje eğitim amaçlıdır.

Veri seti kamuya açık ve analiz için kullanılmıştır.
