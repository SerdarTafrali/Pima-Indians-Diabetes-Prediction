# Pima Indians Diabetes Prediction

## Proje Açıklaması

Bu proje, Pima Indians Diabetes veri seti kullanılarak diyabet hastalığının beş yıl içinde gelişip gelişmeyeceğini tahmin etmeyi amaçlamaktadır. Proje kapsamında dört farklı makine öğrenimi algoritması kullanılmıştır: Naive Bayes, K-En Yakın Komşuluk (KNN), Multi-Layer Perceptron (MLP) ve Support Vector Machines (SVM).

## Veri Seti

- **Veri Seti:** Pima Indians Diabetes Dataset
- **Açıklama:** Pima Indians veri seti, belirli tıbbi detaylar verilerek beş yıl içinde diyabet hastalığının gelişip gelişmeyeceğini tahmin etmeyi içeren ikili (2 sınıflı) bir sınıflandırma problemidir.
- **Özellikler:**
  1. Gebelik sayısı
  2. Plazma glikoz konsantrasyonu (2 saatlik oral glikoz tolerans testi)
  3. Diyastolik kan basıncı (mm Hg)
  4. Triseps cilt kıvrımı kalınlığı (mm)
  5. 2 Saatlik serum insülini (mu U/ml)
  6. Vücut kitle indeksi (kg/m²)
  7. Diyabet soyağacı fonksiyonu
  8. Yaş (yıl)
  9. Sınıf değişkeni (0 veya 1)

## Algoritmalar ve Sonuçlar

### Naive Bayes Sonuçları

**Eğitim Seti:**

- Accuracy: 0.767
- F1 Score: 0.638
- ROC AUC: 0.725

**Test Seti:**

- Accuracy: 0.745
- F1 Score: 0.642
- ROC AUC: 0.725
- Ortalama Karesel Hata: 0.255

### KNN Sonuçları

**Eğitim Seti:**

- Accuracy: 0.767
- F1 Score: 0.622
- ROC AUC: 0.717

**Test Seti:**

- Accuracy: 0.727
- F1 Score: 0.553
- ROC AUC: 0.671
- Ortalama Karesel Hata: 0.273

### MLP Sonuçları

**Eğitim Seti:**

- Accuracy: 0.791
- F1 Score: 0.699
- ROC AUC: 0.768

**Test Seti:**

- Accuracy: 0.723
- F1 Score: 0.579
- ROC AUC: 0.682
- Ortalama Karesel Hata: 0.277

### SVM Sonuçları

**Eğitim Seti:**

- Accuracy: 0.780
- F1 Score: 0.612
- ROC AUC: 0.714

**Test Seti:**

- Accuracy: 0.736
- F1 Score: 0.561
- ROC AUC: 0.678
- Ortalama Karesel Hata: 0.264

## İçgörüler ve Yorumlar

### Model Karşılaştırması

- **Accuracy ve F1 Score:** Eğitim setinde en yüksek doğruluk ve F1 skorlarına sahip olan model MLP olmuştur. Test setinde ise Naive Bayes, en iyi doğruluğu sağlamış ancak F1 skoru MLP kadar yüksek olmamıştır.
- **ROC AUC:** ROC AUC skorlarına bakıldığında, MLP modeli eğitim setinde en yüksek değeri sağlamıştır. Test setinde ise Naive Bayes ve MLP modelleri benzer sonuçlar vermiştir.
- **Ortalama Karesel Hata (MSE):** En düşük MSE değerini Naive Bayes modeli sağlamıştır, bu da Naive Bayes modelinin test setindeki hata oranının diğer modellere göre daha düşük olduğunu göstermektedir.

### Model Seçimi

Bu sonuçlara göre, en iyi performansı gösteren model MLP olarak değerlendirilmiştir. Ancak, Naive Bayes modeli de oldukça başarılı sonuçlar vermiştir ve test setinde en düşük hata oranını sağlamıştır. SVM ve KNN modelleri de makul performans göstermiştir, ancak diğer iki model kadar güçlü değildir.

## Öneriler

- **Veri Ön İşleme:** Eksik değerlerin daha dikkatli bir şekilde işlenmesi ve veri setinin dengesizliğine karşı stratejiler uygulanması (örneğin, SMOTE gibi veri artırma teknikleri) model performansını iyileştirebilir.
- **Model Tuning:** Modellerin hiperparametre optimizasyonu yapılarak daha iyi performans elde edilebilir. Özellikle MLP ve SVM gibi karmaşık modellerde bu optimizasyonlar önemlidir.
- **Ek Metrikler:** Model performansını değerlendirirken precision, recall ve AUC gibi ek metrikler de dikkate alınabilir. Bu metrikler, özellikle dengesiz veri setlerinde daha anlamlı olabilir.
