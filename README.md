# car_price_prediction
Bu projede , ikinci el araçların özelliklerini kullanarak araç fiyat tahmini yapılmıştır.
## Proje Hakkında
Projede farklı algoritmalar kullanılarak araç fiyat tahmini yapılmıştır.
Proje Kapsamında;
-Veri analizi
-Veri temizleme
-Eksik değerlerin işlenmesi
-Aykırı değer analizi
-Feature engineering
-Kategorik değişkenlerin dönüştürülmesi
-Sayısal değerlerin standardizasyonu
-Model eğitimi
-Model değerlendirmesi
-Modellerin karşılaştırılması
İşlemleri gerçekleştirilmiştir.
## Kullanılan Özellikler 
Modelde araçların aşağıdaki özellikleri kullanılmıştır:

- Marka (brand)
- Model (model)
- Model yılı (model_year)
- Kilometre (mileage)
- Yakıt tipi (fuel_type)
- Beygir gücü (horsepower)
- Motor hacmi (engine_size)
- Silindir sayısı (cylinders)
- Vites tipi (transmission)
- Kaza durumu (accident)
- Temiz başlık (clean_title)

Tahmin edilmeye çalışılan hedef değişken:

- price
## Veri Ön İşleme

Veri üzerinde aşağıdaki işlemler uygulanmıştır:

- Eksik değerlerin doldurulması
- Kategorik değişkenlerin One-Hot Encoding ile dönüştürülmesi
- Sayısal değişkenlerin standardizasyonu
- IQR yöntemi ile fiyatlardaki aykırı değerlerin tespit edilmesi ve çıkarılması
- Verinin eğitim ve test olarak ayrılması

## Kullanılan Modeller

Projede üç farklı regresyon algoritması karşılaştırılmıştır:

1. Linear Regression
2. Random Forest Regressor
3. XGBoost Regressor

## Model Sonuçları

Modeller MAE, RMSE ve R² metrikleri kullanılarak değerlendirilmiştir.

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 6.321 | 9.521 | 0.80 |
| Random Forest | 5.777 | 8.488 | 0.84 |
| XGBoost | 5.236 | 7.789 | *0.86* |

## En İyi Model

Test edilen modeller arasında en iyi sonucu *XGBoost* vermiştir.

XGBoost sonuçları:

- *MAE:* ~5.236
- *RMSE:* ~7.789
- *R²:* 0.86

R² değerinin 0.86 olması, modelin test verisindeki fiyat değişkenliğinin yaklaşık %86'sını açıklayabildiğini göstermektedir.

## Görselleştirmeler

Projede aşağıdaki görselleştirmeler kullanılmıştır:

- Gerçek ve tahmin edilen fiyatların karşılaştırılması
- Tahmin hatalarının dağılımı
- Özellik önemleri (Feature Importance)

## Kullanılan Teknolojiler

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Jupyter Notebook / Google Colab

## Proje Yapısı

```text
car-price-prediction/
│
├── araba_fiyat_tahmini.ipynb
├── README.md
└── requirements.txt
## Not
Model performansı, IQR yöntemi kullanılarak fiyatlardaki aykırı değerler çıkarıldıktan sonra elde edilmiştir. Bu nedenle sonuçlar temizlenmiş veri setindeki araçları temsil etmektedir.
