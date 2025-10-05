# FC26 Player Analysis Project

Bu proje, **FIFA 26 (FC26) veri seti** kullanılarak oyuncu analizi ve öneri sistemi geliştirmeyi amaçlamaktadır. Özellikle MacBook Air kullanıcıları için optimize edilmiştir ve veri görselleştirme, kümeleme, radar chart ve benzer oyuncu önerisi içerir.

---


## Kullanılan Teknolojiler

* Python 3.13
* Pandas, Numpy → Veri işleme
* Matplotlib, Seaborn → Görselleştirme
* Scikit-learn → Standartlaştırma, Kümeleme
* Jupyter Notebook → Analiz ve sunum

---

## Proje Adımları

### 1️⃣ Veri Yükleme ve Temizlik

* CSV dosyası yüklenir (`low_memory=False` ile).
* Sayısal sütunlarda eksik veriler temizlenir.

### 2️⃣ Temel Analiz

* Oyuncu sayısı, yaş, overall, potential gibi temel istatistikler.
* Top 10 overall oyuncu grafikleri.

### 3️⃣ Pozisyon Bazlı Analiz

* Oyuncuların birincil pozisyonları alınır.
* Pozisyon bazında ortalama overall analizi.
* Pozisyon bazlı radar chart ile skill profili görselleştirilir.

### 4️⃣ İleri Görselleştirmeler

* Yaş vs Overall vs Potential scatter plot.
* Kulüp bazlı ortalama overall bar plot.

### 5️⃣ Kümeleme Analizi

* KMeans kullanılarak oyuncular 5 kümeye ayrılır.
* Küme bazlı scatter plot ve radar chart ile profil analizi yapılır.

### 6️⃣ Benzer Oyuncu Önerisi

* Öklid mesafesi kullanılarak belirli bir oyuncuya benzer oyuncular önerilir.
* Pozisyon bazlı filtreleme ile daha isabetli öneri.

---

## Görselleştirme Örnekleri

* **Radar Chart:** Oyuncunun skill profili
* **Bar Plot:** Top 10 oyuncu, kulüp veya pozisyon analizi
* **Scatter Plot:** Age vs Overall vs Potential
* **Kümeleme Scatter Plot:** Skill bazlı kümelenmiş oyuncular

---

## Özellikler

* Otomatik radar chart üretimi
* Pozisyon bazlı ve genel benzer oyuncu önerisi
* Küme profil analizi ile oyuncu tiplerini görselleştirme
* Büyük veri seti için örneklemleme (`sample()`) ile performans optimizasyonu

---

## Nasıl Kullanılır

1. `FC26_20250921.csv` dosyasını proje klasörüne ekleyin.
2. Jupyter Notebook’u açın:

   ```bash
   jupyter notebook untitled.ipynb
   ```
3. Hücreleri sırayla çalıştırarak analizi görüntüleyin.
4. `recommend_similar('Oyuncu Adı', 5)` veya `recommend_similar_pos('Oyuncu Adı', 5)` ile benzer oyuncuları bulun.
5. `player_radar('Oyuncu Adı')` ile radar chart görünümünü alın.
6. `cluster_radar(0)` veya `position_radar('CAM')` ile küme ve pozisyon analizlerini görselleştirin.

---

## İleri Geliştirme Önerileri

* 3D scatter plot ile overall/potential/age görselleştirme
* DBSCAN veya hiyerarşik kümeleme kullanımı
* Top oyuncuların radar chart’larını otomatik panelde gösterme
* Player development prediction (yaş + overall + potential)

---

## Notlar

* MacBook Air için örneklem (`sample(5000)`) kullanılmıştır, büyük veri setlerinde performans için önemlidir.
* `physical` sütunu veri setinde `physic` olarak geçmektedir.
