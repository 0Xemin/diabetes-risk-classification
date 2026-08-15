# Diabetes Risk Classification

> **Not:** Bu proje, Data Mining dersinin Yıl Sonu Bitirme Projesi ve Huawei Machine Learning Bootcamp sunumu olarak geliştirilmiştir.

Bu proje, klinik parametreler (örn. BMI, kan glukozu, HbA1c vb.) kullanarak diyabet riskini sınıflandırmak için ağaç tabanlı modeller (Random Forest, Gradient Boosting, XGBoost, LightGBM, vb.) ile kapsamlı bir EDA ve modelleme boru hattı sunar. Ana çalışma Jupyter Notebook içinde yer almaktadır.

## Proje yapısı

```
README.md                              - Proje özeti & hızlı başlatma talimatları
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
- Kaynak: Kaggle (lütfen repo dışı paylaşım ve lisans şartlarına dikkat edin). Eğer spesifik Kaggle sayfası URL'sini paylaşırsanız onu da buraya ekleyeyim.
- Kolonlar (notebook'tan çıkarıldı): `gender`, `age`, `hypertension`, `heart_disease`, `smoking_history`, `bmi`, `HbA1c_level`, `blood_glucose_level`, `diabetes`

## Kurulum ve Çalıştırma

Önerilen en kısa yol (yeni bir makinede):

```bash
git clone https://github.com/MuhamedEminKrd/diabetes-risk-classification.git
cd diabetes-risk-classification
python -m pip install -r requirements.txt
# Jupyter ile interaktif çalışmak için
jupyter notebook diabet-prediction-gradientboost.ipynb
```

Alternatif (headless) çalıştırma için:

```bash
# Conda ortamı oluşturduktan sonra
bash run_notebook.sh  # papermill ile notebook'u çalıştırır ve outputs/ içine kaydeder
bash run_train.sh     # basit eğitim script'ini çalıştırır ve models/best_model.pkl kaydeder
```

Notlar:
- Python sürümü için öneri: Python 3.9–3.11 (kullandığınız ortamda uyumlu sürümü tercih edin).

## Yeniden Üretilebilirlik

- Rastgelelik kontrolü için notebook'ta kullanılan seed ve sürüm bilgilerini README'ye veya ayrı bir `environment.yml`/`requirements.txt` içine sabitlemeniz önerilir.
- `requirements.txt` mevcut; daha kesin bağımlılık yönetimi için `environment.yml` (conda) veya pip `constraints.txt` eklenmiştir.

## Sonuçlar

Model karşılaştırmaları, hiperparametre aramaları ve değerlendirme metrikleri tümüyle `diabet-prediction-gradientboost.ipynb` içinde yer almaktadır. Hızlı bir özet eklemek isterseniz (ör. en iyi model ve AUC/precision/recall), notebook'u çalıştırıp çıktıdan bu değerleri README'ye ekleyebilirim.

## Model Kaydetme ve Kullanım

Notebook'ta en iyi modeli kaydetme adımı bulunmuyorsa, `joblib` veya `pickle` ile kaydetme örneği eklenmesi yararlı olur. `models/` klasörü repoya eklendi ve basit bir eğitim script'i (`train_and_save.py`) ile modeller/models/best_model.pkl kaydedilebilir.

## Lisans

Bu repository'nin kodu MIT lisansı altında yayımlanmıştır — detaylar LICENSE dosyasında.

## Katkıda Bulunma

Katkılar için lütfen issue açın veya pull request gönderin. Küçük düzenlemeler için doğrudan PR kabul edilir. Daha fazla bilgi için CONTRIBUTING.md dosyasına bakın.

## İletişim

Soru/suggestion için repository sahibi: @MuhamedEminKrd

---

*Not:* README'deki veri kaynağına "Kaggle" olarak eklendi. Eğer Kaggle sayfasının tam URL'sini paylaşırsanız onu da README'ye ekleyip tekrar commitleyeyim.
