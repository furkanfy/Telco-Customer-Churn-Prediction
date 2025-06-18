# Telco Customer Churn Prediction 🔍📊

Bu projede, Telco müşteri verisi kullanılarak müşterilerin hizmetten ayrılıp ayrılmayacağı (churn) tahmin edilmiştir. Amaç, özellikle "Yes" etiketli churn'ü doğru tahmin etmektir.

## 📌 Kullanılan Veri Seti
- Kaggle: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Toplam Gözlem: ~7000+
- Hedef Sütun: `Churn` (Yes/No)

## 🔧 Kullanılan Araçlar ve Kütüphaneler
- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (SMOTE, RandomForest, GridSearchCV, metrics)

## 🔍 Yapılan Adımlar

1. **Veri Keşfi (EDA)**  
   - Boş veriler, veri tipleri, dağılımlar incelendi.
   - Kategorik veriler `get_dummies` ile sayısal hale getirildi.

2. **Dengesizlikle Mücadele (SMOTE)**  
   - 'Churn = Yes' sınıfı azınlıktaydı.  
   - `SMOTE` ile dengeli dağılım sağlandı.

3. **Modelleme**  
   - `RandomForestClassifier` ile tahmin modeli oluşturuldu.
   - İlk modelin doğruluk ve recall skorları değerlendirildi.

4. **Model İyileştirme (GridSearchCV)**  
   - En iyi `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf` değerleri arandı.
   - En iyi model ile ROC AUC, f1-score ve recall gibi metrikler alındı.

5. **Değerlendirme**  
   - En iyi recall skoru: **%87.19**  
   - ROC AUC: **0.84+**  
   - True sınıfını tahmin etmede ciddi başarı elde edildi.

## 📈 Sonuç
- Bu model churn olan müşterilerin büyük bir kısmını yakalayabiliyor.
- SMOTE ve GridSearchCV, performans artışında etkili oldu.
- Telco gibi sektörlerde müşteri kaybını önlemek için uygulanabilir bir makine öğrenmesi çözümüdür.




