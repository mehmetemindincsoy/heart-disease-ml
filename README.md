🫀 Kalp Hastalığı Risk Tahmin Modeli
> İki farklı coğrafyadan elde edilen verilerle makine öğrenmesi tabanlı kalp hastalığı erken teşhis sistemi

![Python](https://img.shields.io/badge/Python-3.14-blue)
![Status](https://img.shields.io/badge/Durum-Geliştiriliyor-yellow)
![License](https://img.shields.io/badge/Lisans-MIT-green)

---

## 📌 Projenin Amacı
Kalp hastalıkları dünya genelinde en büyük ölüm nedenidir. Bu proje, temel sağlık verileri kullanılarak kalp hastalığı riskini makine öğrenmesi ile tahmin etmeyi amaçlamaktadır. Pahalı testlere gerek kalmadan hızlı bir ön değerlendirme yapılabilmesi hedeflenmektedir.

---

## 📊 Kullanılan Veri Setleri
| Veri Seti | Yayıncı | Kaynak | Satır |
|---|---|---|---|
| Cardiovascular Disease Dataset | Svetlana Ulianova | [Kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset) | 70.000 |
| Heart Disease Health Indicators | Alex Teboul (CDC/BRFSS) | [Kaggle](https://www.kaggle.com/datasets/alexteboul/heart-disease-health-indicators-dataset) | 253.680 |

**Birleştirilmiş dataset:** 322.804 satır, 10 sütun

---

## 🔍 Veri Seti Özellikleri
| Sütun | Açıklama | Tür |
|---|---|---|
| `age` | Yaş | Sayısal |
| `gender` | Cinsiyet (1=Kadın, 2=Erkek) | Kategorik |
| `blood_pressure` | Yüksek tansiyon (0/1) | Binary |
| `cholesterol` | Yüksek kolesterol (0/1) | Binary |
| `smoking` | Sigara kullanımı (0/1) | Binary |
| `alcohol` | Alkol kullanımı (0/1) | Binary |
| `active` | Fiziksel aktivite (0/1) | Binary |
| `bmi` | Vücut kitle indeksi | Sayısal |
| `heart_disease` | Kalp hastalığı (0=Yok, 1=Var) | Hedef |
| `source` | Veri kaynağı | Kategorik |

---

## 📈 Önemli Bulgular
- 📍 Hastaların **%18.2**'sinde kalp hastalığı tespit edilmiştir
- 📍 En güçlü risk faktörleri: **yüksek tansiyon** ve **yaş**
- 📍 Obez bireylerde hastalık oranı zayıf bireylere kıyasla belirgin şekilde daha yüksek
- 📍 Fiziksel aktivite kalp hastalığı riskini **azaltıcı** etki göstermektedir
- 📍 876 aykırı BMI değeri tespit edilerek veri setinden çıkarılmıştır

---

## ⚠️ Veri Seti Sınırlılıkları
İki farklı coğrafyadan (Avrupa ve Amerika) veri birleştirilmiştir. Ölçek farklılıkları standartlaştırılmış olsa da bu durum model performansını etkileyebilir. Sonuçlar bu sınırlılık göz önünde bulundurularak yorumlanmalıdır.

---

## 🗂️ Proje Aşamaları
- [x] Veri seti seçimi
- [x] Veri birleştirme ve standartlaştırma
- [x] Keşifsel veri analizi (EDA)
- [x] Görselleştirme
- [ ] Model kurma (Random Forest, Karar Ağacı, Lojistik Regresyon)
- [ ] Model değerlendirme (Accuracy, F1, Precision, Recall)
- [ ] Tek kaynak vs çok kaynak karşılaştırması

---

## 🛠️ Kullanılan Teknolojiler
```python
pandas       # Veri işleme
numpy        # Matematiksel işlemler  
matplotlib   # Görselleştirme
seaborn      # Gelişmiş görselleştirme
scikit-learn # Model kurma (finale)
```

## ⚙️ Kurulum
```bash
# Gerekli kütüphaneleri yükle
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

```bash
# Projeyi çalıştır
jupyter notebook project.ipynb
```

---

## 📁 Dosya Yapısı
```
heart-disease-ml/
│
├── project.ipynb                 # Ana proje dosyası
├── combined_heart_disease.csv    # Birleştirilmiş temiz dataset
├── Svetlana-cardio_train.csv     # Ham veri (Svetlana)
├── Alex-heart_disease_...csv     # Ham veri (Alex)
├── analiz_grafikleri.png         # EDA görselleştirmeleri
├── bmi_analizi.png               # BMI analiz grafikleri
└── README.md                     # Bu dosya
```

---

## 👥 Ekip
| İsim | Öğrenci No | Rol |
|---|---|---|
| Mehmet Emin Dinçsoy | 33253304001 | Veri İşlemesi, model geliştirme |
| Ezgi Boztepe | 33253304003 | Veri İşlemesi, Dokümantasyon, analiz |

---

## 📚 Kaynaklar
- [Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset)
- [Heart Disease Health Indicators Dataset](https://www.kaggle.com/datasets/alexteboul/heart-disease-health-indicators-dataset)
- [Scikit-learn Dokümantasyonu](https://scikit-learn.org)
