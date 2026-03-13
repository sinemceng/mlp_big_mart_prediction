# Big Mart Sales Prediction (Satış Tahminleme)

Bu proje, **Big Mart Sales Prediction** veri setini kullanarak farklı mağazalardaki ürünlerin toplam satış miktarlarını (Item_Outlet_Sales) tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır. Perakende sektöründe envanter yönetimi ve gelir tahmini için kritik olan bu süreç, derin öğrenme temelli regresyon modelleri ile analiz edilmiştir.

## Proje Özeti
Proje, Kaggle'da popüler olan perakende veri seti üzerinde gerçekleştirilmiş olup şu temel aşamalardan oluşmaktadır:
* **Keşifsel Veri Analizi (EDA):** Veri yapısının incelenmesi ve görselleştirilmesi.
* **Veri Temizleme:** Eksik değerlerin (Missing Values) ortalama ve mod yöntemleriyle doldurulması.
* **Aykırı Değer (Outlier) Yönetimi:** `Item_Outlet_Sales` sütunundaki aşırı değerlerin tespiti ve model performansını artırmak için **Logaritmik Dönüşüm** uygulanması.
* **Özellik Mühendisliği:** Kategorik verilerin standartlaştırılması (Örn: `Low Fat`, `LF`, `low fat` birleştirilmesi).
* **Modelleme:** Regresyon problemini çözmek için Çok Katmanlı Algılayıcı (**MLPRegressor**) mimarisinin kullanımı.

##  Veri Seti Özellikleri
Veri seti, ürünler ve mağazalar hakkında 12 farklı öznitelik içerir:
- **Item_Identifier:** Ürün kimlik numarası.
- **Item_Weight:** Ürün ağırlığı.
- **Item_Fat_Content:** Ürün yağ içeriği.
- **Item_MRP:** Ürünün maksimum perakende satış fiyatı.
- **Outlet_Size:** Mağazanın büyüklüğü.
- **Item_Outlet_Sales (Hedef):** Belirli bir üründen belirli bir mağazada yapılan toplam satış tutarı.

##  Kullanılan Teknolojiler
- **Python 3**
- **Pandas & NumPy:** Veri manipülasyonu.
- **Matplotlib & Seaborn:** Veri görselleştirme.
- **Scikit-learn:** Makine öğrenmesi ve veri ön işleme.

##  Analiz ve Sonuçlar
Proje kapsamında yapılan kutu grafiği (boxplot) ve histogram analizleri sonucunda, hedef değişkendeki sağa çarpık (skewed) dağılım tespit edilmiş ve bu durum **Logaritmik Dönüşüm (np.log1p)** yöntemiyle stabilize edilmiştir. Bu işlem, MLP modelinin aykırı değerlere karşı daha dirençli olmasını ve daha genel bir tahmin yeteneği kazanmasını sağlamıştır.

## Veri Seti
https://www.kaggle.com/datasets/shivan118/big-mart-sales-prediction-datasets?resource=download
