# Tıp Atlası Projesi  | İlaçlar Veri Seti

Bu veri seti, Türkiye Sağlık Bakanlığı tarafından onaylanmış tüm ilaçların detaylı bilgilerini içermektedir. Araştırmacılar, sağlık uzmanları ve geliştiriciler için ilaç verilerinin kolayca erişilebileceği bir kaynaktır.

## Veri Seti İçeriği
Veri seti aşağıdaki alanları içermektedir:

| Alan Adı            | Açıklama                                                   |
|---------------------|-----------------------------------------------------------|
| **ID**             | Her bir ilaca özgü benzersiz bir tanımlayıcı.             |
| **barcode**        | İlacın barkod numarası.                                   |
| **ATC_code**       | İlacın ATC (Anatomik Tedavi Kimyasal) sınıflandırma kodu. |
| **Active_Ingredient** | İlacın aktif bileşeni.                                    |
| **Product_Name**   | İlacın ticari adı.                                         |
| **Category_1**     | Ana kategori (ör. Kas İskelet Sistemi).                   |
| **Category_2**     | Alt kategori (ör. Antienflamatuar ve Antiromatikler).     |
| **Category_3**     | Daha spesifik alt kategori (ör. Non-steroid).             |
| **Category_4**     | Daha detaylı alt kategori (ör. Asetik Asit Türevi İlaçlar).|
| **Category_5**     | Ek detay kategorisi.                                       |
| **Description**    | İlacın tam kullanım talimatları veya açıklamaları.         |

## Örnek Kayıt
Aşağıda veri setindeki bir örnek kayıt verilmiştir:

```
ID: 1
barcode: 8699580090635
ATC_code: M01AB08
Active_Ingredient: Etodolak
Product_Name: DOLARIT 300 MG 10 FILM TABLET
Category_1: Kas İskelet Sistemi
Category_2: Antienflamatuar ve Antiromatikler
Category_3: Non-steroid
Category_4: Asetik Asit Türevi İlaçlar
Category_5: Asetik Asit Türevi İlaçlar
Description: Dolarit 300 Mg Film Kaplı Tablet Kullanma Talimat...
```

## Kullanım Alanları
Bu veri seti, aşağıdaki kullanım alanları için uygundur:
- İlaç araştırmaları
- Sağlık teknolojisi uygulamaları geliştirme
- İlaç sınıflandırmaları üzerinde analiz
- Eğitim ve akademik çalışmalar

# TIP ATLASI PROJESİ WE SİTESİ
Bu wep sayfası sayesenide verileri indirmeden direk olarak araya bilirsiniz.
http://tipatlasi.rf.gd/?i=1
## Lisans
Bu veri seti, Creative Commons Attribution 4.0 International altında lisanslanmıştır. Lütfen kullanım sırasında bu lisansa uygun hareket ediniz.

## Katkıda Bulunma
Eğer bu veri setine katkıda bulunmak isterseniz, lütfen bir pull request gönderin veya issue oluşturun.

## İletişim
Herhangi bir sorunuz veya öneriniz için lütfen tipatlasiprojesi@gmail.com üzerinden iletişime geçin.

---

**Not:** Bu veri seti yalnızca bilgilendirme ve araştırma amaçlıdır. Sağlıkla ilgili kararlar için bir uzmana danışmanız önemlidir.
