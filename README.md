# Diabetes Risk Classification

> **Not:** Bu proje, Data Mining dersinin Yıl Sonu Bitirme Projesi ve Huawei Machine Learning Bootcamp sunumu olarak geliştirilmiştir.

Bu proje, klinik parametreler (örn. BMI, kan glukozu, HbA1c vb.) kullanarak diyabet riskini sınıflandırmak için ağaç tabanlı modeller (Random Forest, Gradient Boosting, XGBoost, LightGBM, vb.) ile kapsamlı bir EDA ve modelleme boru hattı sunar. Ana çalışma Jupyter Notebook içinde yer almaktadır.

## Proje yapısı

```
README.md                              - Proje özeti ve hızlı başlatma talimatları
requirements.txt                       - Projede kullanılan Python paketleri
diabet-prediction-gradientboost.ipynb  - Ana Jupyter Notebook: veri yükleme, EDA, ön işleme, modelleme, optimizasyon, görselleştirme
diabetes_prediction_dataset.csv        - Notebook tarafından kullanılan veri seti (repo kökünde)
```

## Teknolojiler ve Algoritmalar

- Python (Jupyter Notebook)
- pandas, numpy, matplotlib, seaborn
- scikit-learn (RandomForest, GradientBoosting, AdaBoost, RandomizedSearchCV, StratifiedKFold)
- xgboost, lightgbm
- imbalanced-learn (SMOTE)

## Veri seti

- Dosya: `diabetes_prediction_dataset.csv` (repo kökünde)
- Kolonlar (notebook'tan çıkarıldı): `gender`, `age`, `hypertension`, `heart_disease`, `smoking_history`, `bmi`, `HbA1c_level`, `blood_glucose_level`, `diabetes`
- Kaynak / lisans: README'ye eklenmedi. Lütfen veri setinin kaynağını, lisansını ve varsa atıf bilgisini buraya ekleyin.

## Kurulum ve Çalıştırma

Önerilen en kısa yol (yeni bir makinede):

```bash
git clone https://github.com/MuhamedEminKrd/diabetes-risk-classification.git
cd diabetes-risk-classification
python -m pip install -r requirements.txt
# Jupyter ile interaktif çalışmak için
jupyter notebook diabet-prediction-gradientboost.ipynb
```

Notlar:
- Python sürümü için öneri: Python 3.9–3.11 (kullandığınız ortamda uyumlu sürümü tercih edin).
- Tek komutla notebook'u baştan çalıştırmak isterseniz papermill veya nbconvert ekleyebilirsiniz; isterseniz ben örnek bir run script'i ekleyebilirim.

## Yeniden Üretilebilirlik

- Rastgelelik kontrolü için notbook'ta kullanılan seed ve sürüm bilgilerini README'ye veya ayrı bir `environment.yml`/`requirements.txt` içine sabitlemeniz önerilir.
- `requirements.txt` mevcut; daha kesin bağımlılık yönetimi için `environment.yml` (conda) veya pip `constraints.txt` ekleyebilirsiniz.

## Sonuçlar

Model karşılaştırmaları, hiperparametre aramaları ve değerlendirme metrikleri tümüyle `diabet-prediction-gradientboost.ipynb` içinde yer almaktadır. Hızlı bir özet eklemek isterseniz (ör. en iyi model ve AUC/precision/recall), ben README'ye kısa bir sonuç bölümü ekleyebilirim — bu bilgi notebook'tan alınmalıdır.

## Model Kaydetme ve Kullanım

Notebook'ta en iyi modeli kaydetme adımı bulunmuyorsa, `joblib` veya `pickle` ile kaydetme örneği eklenmesi yararlı olur. İsterseniz `models/` klasörü oluşturup `models/best_model.pkl` şeklinde kaydetmeyi otomatikleştiren bir script ekleyebilirim.

## Lisans

Lütfen projeye bir LICENSE dosyası ekleyin (ör. MIT) veya mevcut lisans bilgisini README'ye ekleyin. Şu anda lisans belirtilmemiştir.

## Katkıda Bulunma

Katkılar için lütfen issue açın veya pull request gönderin. Küçük düzenlemeler için doğrudan PR kabul edilir.

## İletişim

Soru/suggestion için repository sahibi: @MuhamedEminKrd

---

*Not:* README'deki veri kaynağı, lisans ve varsa çalışma sonuçları (en iyi model, metrikler) gibi boşlukları doldurursanız README'yi daha da güçlendirip tekrar commitleyebilirim.
