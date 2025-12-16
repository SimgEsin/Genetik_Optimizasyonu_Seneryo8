
#  Sunucu Performans Optimizasyonu - Genetik Algoritma

Bu proje, bir sunucunun CPU ve RAM kaynaklarını optimize ederek maksimum performans skoruna ulaşmayı hedefler. Genetik Algoritma (GA) kullanılarak, belirlenen kısıtlar altında en iyi donanım konfigürasyonu bulunur.

##  Problem Tanımı
Bir yazılım şirketi için aşağıdaki amaç fonksiyonuna göre sunucu ayarları optimize edilmektedir:

**Amaç Fonksiyonu:** `y = 5x₁ + 7x₂ - 0.1x₁² - 0.2x₂²`

**Değişkenler:**
- `x₁` (CPU Çekirdeği): [2, 12] aralığında.
- `x₂` (RAM Miktarı): [4, 64] aralığında.

**Kısıtlar:**
1. `x₁ * x₂ ≤ 512` (Kaynak çarpımı sınırı)
2. `x₁ ≥ 4` (Minimum 4 çekirdek gerekli)

##  Algoritma Yapısı
Proje Python kullanılarak geliştirilmiş ve aşağıdaki genetik operatörleri içerir:

1. **Başlangıç:** Belirlenen aralıklarda rastgele `[CPU, RAM]` popülasyonu oluşturulur.
2. **Uygunluk (Fitness):** Amaç fonksiyonundan elde edilen skor hesaplanır. Kısıtları ihlal eden bireylere ceza puanı uygulanarak skor düşürülür.
3. **Seçim (Selection):** Rulet tekerleği yöntemi ile performansı yüksek bireylerin seçilme şansı artırılır.
4. **Çaprazlama (Crossover):** Seçilen ebeveynlerin genleri karıştırılarak yeni bireyler üretilir.
5. **Mutasyon:** Rastgele oranlarda gen değerleri değiştirilerek çeşitlilik sağlanır ve yerel minimumdan kaçınılır.

##  Sonuçlar
Algoritma çalıştırıldığında, nesiller ilerledikçe performans skorunun arttığı ve optimum CPU/RAM değerlerine yakınsadığı gözlemlenmiştir.
<img width="1125" height="673" alt="image" src="https://github.com/user-attachments/assets/403a32fe-1b10-4ae8-93e9-450be32f0089" />


## 🚀 Kurulum ve Çalıştırma
1. `.ipynb` dosyasını Google Colab veya Jupyter Notebook ile açın.
2. Tüm hücreleri sırasıyla çalıştırın.
3. Sonuç grafiği en altta görüntülenecektir.
