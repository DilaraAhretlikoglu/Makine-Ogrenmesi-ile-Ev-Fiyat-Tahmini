# **Ev Fiyatı Tahmin Modeli - Makine Öğrenmesi**
Bu proje, ev fiyatlarını tahmin etmek amacıyla bir makine öğrenmesi modeli oluşturulmasını hedefler. Ev alım-satımıyla ilgili yaşadığımız zorlukları göz önünde bulundurularak, bu model ile evlerin fiyatlarını tahmin etmeyi amaçlıyoruz. Proje, ev fiyatlarını tahmin edebilmek için çeşitli makine öğrenmesi algoritmalarını kullanır.

## 📜 **Proje Hakkında**
Bu model, ev fiyatı tahmin etmek için farklı özelliklere sahip veriler kullanarak bir regresyon problemi çözer. Veriseti, evlerin çeşitli özelliklerini ve satış fiyatlarını içermektedir. Model, bu veriler üzerinde eğitim alarak, verilen özelliklere dayalı olarak bir evin satış fiyatını tahmin eder.

## 🏠 **Veri Kümesi**
Veri kümesi şu 13 özelliği içermektedir:

* **Id**: Kayıtları saymak için kullanılan ID. 
* **MSSubClass**: Satışa konu olan evin türünü belirler. 
* **MSZoning**: Satışın gerçekleştiği genel bölge sınıflandırması. 
* **LotArea**: Ev arsasının büyüklüğü (m²). 
* **LotConfig**: Arsanın konfigürasyonu. 
* **BldgType**: Ev türü. 
* **OverallCond**: Evin genel durumu. 
* **YearBuilt**: İlk inşa yılı. 
* **YearRemodAdd**: Yenileme tarihi (yoksa ilk inşa tarihi). 
* **Exterior1st**: Evin dış kaplaması. 
* **BsmtFinSF2**: İkinci tip bitmiş alan (m²). 
* **TotalBsmtSF**: Toplam bodrum alanı (m²). 
* **SalePrice**: Tahmin edilmesi gereken satış fiyatı.
  
## 📚 **Kullanılan Kütüphaneler**
* **Pandas**: Veriyi yüklemek ve işlemek için kullanılır. 
* **Matplotlib**: Veriyi görselleştirmek için kullanılır. 
* **Seaborn**: Veriler arasındaki korelasyonu görmek için kullanılır. 
* **Scikit-Learn**: Makine öğrenmesi modellerini eğitmek ve değerlendirmek için kullanılır. 

## 🛠️ **Veri Yükleme ve Ön İşleme**
Veri, HousePricePrediction.xlsx dosyasından yüklenmiştir. İlk olarak veriler incelenir ve veri türlerine göre kategoriler oluşturulmuştur. Verideki eksik veya hatalı veriler temizlenmiş, kategorik değişkenler için One-Hot Encoding uygulanmıştır.

### Adımlar:
1. **Veri Yükleme**: Veriyi pandas ile yükleyip görüntüledik. 
2. **Eksik Veriler**: Eksik veriler, ortalama ile doldurulmuş ya da eksik kayıtlar çıkarılmıştır. 
3. **One-Hot Encoding**: Kategorik değişkenler ikili (binary) formata dönüştürülmüştür.
   
## 🧑‍💻 **Model Eğitimi**
Bu projede, üç farklı regresyon modeli kullanılmıştır:

* **SVM (Support Vector Machine)**: Regresyon için destek vektör makinesi modeli kullanılmıştır. 
* **Random Forest Regressor**: Karar ağaçlarının bir arada kullanıldığı bir modeldir. 
* **Linear Regression**: Basit doğrusal regresyon modeli.
  
Sonuçlar aşağıdaki gibidir:
* **SVM Modeli**: 0.187 MAE (Mean Absolute Error) 
* **Random Forest Regressor**: 0.191 MAE 
* **Linear Regression**: 0.187 MAE 

## 🎯 **Sonuçlar**
Projede, ev fiyatlarını tahmin etmek için kullanılan regresyon modelleri arasında en iyi sonucu SVM modelinin verdiği gözlemlenmiştir. Bu modelin doğruluk oranı, diğer modellere kıyasla daha yüksektir. 
