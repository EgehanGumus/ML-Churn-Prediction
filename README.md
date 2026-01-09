# 📊 Müşteri Kaybı (Churn) Analizi

## 📌 Proje Hakkında
Bu projede, telekomünikasyon sektöründe müşteri kaybını (churn) tahmin etmek için makine öğrenmesi modelleri kullanılmıştır.  
Proje, önce **Spyder** ortamında hazırlanmış, ardından **Jupyter Notebook** ile rapor haline getirilmiştir.  

## 📊 Veri Seti
Veri seti; müşteri süresi (tenure), kontrat tipi, internet hizmeti, ödeme yöntemi, toplam fatura tutarı gibi özellikleri içermektedir.  
Hedef değişken, müşterinin hizmeti bırakıp bırakmadığını gösteren `churn` değişkenidir.  

Veri hazırlığı kapsamında:
- **Eksik değer analizi** yapılmıştır
- **EDA (Exploratory Data Analysis)** ile veri seti görselleştirilmiş ve aykırı değerler analiz edilmiştir.  
- **Korelasyon analizi** ile değişkenler arası ilişkiler incelenmiştir.  
- **Özellik mühendisliği** ile kategorik değişkenler dummy encoding yöntemiyle dönüştürülmüştür.  

## 🤖 Kullanılan Modeller
- Logistic Regression  
- KNN (K-Nearest Neighbors)  
- SVM (Support Vector Machine)  
- Random Forest  
- XGBoost  
- LightGBM

## ⚙️ Kullanılan Python Kütüphaneleri
- NumPy  
- Pandas  
- Seaborn  
- Matplotlib
- SciPy
- Scikit-learn
- XGBoost
- LightGBM 

## 📈 Sonuç
- **ROC-AUC ≈ 0.84** ile en iyi performansı Logistic Regression vermiştir.  
- **Threshold analizi** sonucunda 0.35 eşik değeri seçilmiştir. Bu değer, churn problemlerinde kritik olan **Recall**’ı yükseltirken Precision ve F1-score açısından kabul edilebilir bir denge sağlamaktadır.  
- **Odds Ratio analizi** ile müşteri kaybını artıran ve azaltan faktörler belirlenmiştir:  
  - Uzun kontratlar ve ek hizmetler (telefon, güvenlik, teknik destek) churn riskini azaltmaktadır.  
  - Fiber internet, yüksek fatura tutarı ve bazı ödeme yöntemleri (e-fatura, elektronik çek) churn riskini artırmaktadır.  

## 📁 Dosyalar
- `Churn.csv` : Veri seti  
- `Müşteri_ Kayıp_Tahmini.ipynb` : Veri analizi, modelleme ve sonuçlar  
- `README.md` : Proje özeti ve kullanım rehberi  

> Not: Bu notebook rapor formatında hazırlanmış olup tüm analizler, çıktılar ve görseller çalıştırılmış şekilde sunulmaktadır. Projeyi incelemek için yeniden çalıştırılması zorunlu değildir.  
> Dileyen kullanıcılar projeyi kendi ortamlarında çalıştırmak isterse:  
> - **Lokal ortamda:** Bilgisayarında Python (Anaconda önerilir) kurulu olmalıdır. Repo indirildikten sonra Anaconda Navigator üzerinden Jupyter Notebook açılarak `Müşteri_ Kayıp_Tahmini.ipynb` dosyası `Restart & Run All` ile çalıştırılabilir.  
> - **Web üzerinden:** Proje, Google Colab veya benzeri çevrim içi Jupyter ortamlarına yüklenerek de çalıştırılabilir. Bu durumda veri dosyasının `data/` klasörü altında bulunmasına dikkat edilmelidir.  
