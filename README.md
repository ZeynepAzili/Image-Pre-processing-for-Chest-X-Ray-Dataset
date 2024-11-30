# Image Pre-processing for Chest X-Ray Dataset
 Pre-processing methods in chest X-ray image classification
1000 gözlem, 16 öznitelikten oluşan göğüs röntgen görüntülerinden tanı sınıflandırma probleminin görüntü ön işleme yöntemleri kullanılmıştır. 

1. Veri Yükleme
1.	Kütüphanelerin İçe Aktarılması
o	Veri işleme için pandas, sayısal işlemler için numpy, görselleştirme için matplotlib ve seaborn kütüphanelerini içe aktarın.
o	Ayrıca os modülünü kullanarak dosya yolunu belirtin.
2.	Veri Setinin Yüklenmesi
o	train_df olarak adlandırılan veri çerçevesine CSV dosyasını yükleyin ve ilk birkaç satırı inceleyin.
o	Toplam satır ve sütun sayısını ekrana yazdırın.
3.	Veri Özelliklerinin İncelenmesi
o	Sütunlardaki veri türlerini ve eksik değerleri inceleyin.
o	PatientId sütunundaki benzersiz hasta sayısını analiz edin ve her bir hastanın birden fazla görüntüsü olup olmadığını belirleyin.
 
2. Görüntü Yükleme ve Görselleştirme
1.	Rastgele Görüntüler Seçme
o	train_df içindeki "Image" sütunundan rastgele 9 görüntü seçin.
o	Bu görüntüleri yan yana görselleştirerek veri setindeki örnek görüntüleri inceleyin.
2.	Rastgele Görüntülerin İstatistiksel Özelliklerini Hesaplama
o	Seçilen görüntülerin her biri için maksimum, minimum, ortalama ve standart sapma değerlerini hesaplayın.
3.	Histogram Çizimi
o	Seçilen 9 görüntünün her biri için piksel yoğunluk dağılımını gösteren histogramlar oluşturun.
 
3. Görüntü İşleme ve İyileştirme
1.	Kontrast Germe (Stretching)
o	Minimum ve maksimum piksel değerlerini kullanarak kontrast germe işlemi yapın.
2.	Histogram Eşitleme (Equalization)
o	Kontrast germe işlemi sonrası histogram eşitleme uygulayarak kontrastı artırın.
3.	Gamma Düzeltme
o	Gamma düzeltme yöntemi ile görüntünün parlaklığını ayarlayın.
 
4. Gürültü Azaltma
1.	Median ve Gaussian Blur Uygulama
o	Gamma düzeltilmiş görüntüye median ve gaussian blur uygulayın ve sonuçları karşılaştırın.
 
5. Döndürme ve Ayna Çevirme (Flipping)
1.	Rastgele Açılarla Döndürme
o	Görüntüyü 0 ile 10 derece arasında rastgele bir açıda döndürün.
2.	Ayna Çevirme
o	Görüntüyü yatay olarak çevirin ve sonucu görselleştirin.
 
6. Frekans Alanında Filtreleme
1.	Fourier Dönüşümü ve Filtreleme
o	Fourier dönüşümü ile görüntüyü frekans alanına çevirin, düşük frekansları geçiren bir maske uygulayın, ardından ters Fourier dönüşümü ile frekans alanında filtreleme yapın.
 
7. Keskinleştirme ve Enterpolasyon
1.	Keskinleştirme
o	Unsharp masking tekniği kullanarak görüntüyü keskinleştirin.
2.	Bicubic Enterpolasyon
Keskinleştirilmiş görüntüyü iki kat büyüterek enterpolasyon uygulayın.

