# Median ve Gaussian Filtre Karşılaştırması

Bu proje, görüntü işleme alanında yaygın olarak kullanılan **Medyan (Median)** ve **Gauss (Gaussian)** filtrelerini karşılaştırmak amacıyla hazırlanmıştır. Amaç, her iki filtrenin gürültü giderme üzerindeki etkilerini gözlemlemek ve hangi durumlarda hangi filtrenin daha uygun olduğunu belirlemektir.

---

### Medyan Filtresi (Median Filter)

- **Lineer olmayan** bir tekniktir.
- Gürültü bastırmada özellikle tuz-biber (salt & pepper) gürültüsüne karşı etkilidir.
- Her pikselin çevresindeki komşu piksellerin **ortanca (medyan)** değeri alınır.
- Kenarları koruma konusunda başarılıdır.
- Hesaplama açısından **görece yavaştır** (sıralama işlemi içerdiğinden).

### Gauss Filtresi (Gaussian Filter)

- **Lineer ve düşük geçişli** bir filtredir.
- Her pikselin komşularıyla birlikte **ağırlıklı ortalaması** alınır.
- Gaussian çekirdeği (kernel) ile konvolüsyon işlemi yapılır.
- Daha **yumuşak geçişler** ve düzgün görüntü üretir.
- Hesaplama açısından **daha hızlıdır**.

---

## Kullanılan Kütüphaneler

- `OpenCV`
- `NumPy`
- `Matplotlib`
- `os`

## Karşılaştırma Tablosu

Özellik	Gaussian Filter	Median Filter

Gürültü Türü	Genelde etkili	Tuz-biber gürültüsüne karşı etkili

Kenar Koruma	Daha az	Daha iyi

Hesaplama Süresi	Daha hızlı	Daha yavaş (sıralama var)

Aykırı Değerlere Dayanıklılık	Düşük	Yüksek

Kullanım Alanı	Genel amaçlı	Özel durumlar

## Kaynakça

Digital Signal Processing (John G. Proakis, Dimitris K. Manolakis)

Median Filtering: A New Insight – Sebastián A. Villar, Sebastián Torcida

Comparison of Gaussian and Median Filters to Remove Noise in Dental Images

Two-Dimensional Digital Signal Processing II

## Örnek Çıktılar

Medyan filtre, kenar detaylarını koruyarak tuz-biber gürültüsünü başarılı şekilde azaltır.

Gaussian filtre, daha yumuşak ve pürüzsüz bir sonuç üretir, genel gürültü azaltmada uygundur.

## Not

Kodların çalışabilmesi için:

resimDosyasi/tesla.jpg ve resimDosyasi2/tesla2.jpg dosyalarının belirtilen klasörlerde yer alması gerekmektedir.

sigma değerini değiştirmek için Gaussian kodunda trackbar’ı kullanabilirsiniz. Çıkmak için 'q' tuşuna basmanız yeterlidir.


Kurmak için:

```bash
pip install opencv-python numpy matplotlib

