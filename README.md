# TABİP İlaç Veritabanı

Türkiye'de kullanılan ilaçlara ait barkod, ATC kodu, etken madde ve ürün bilgilerini içeren açık veri kümesi.

Bu depo, geliştiriciler, araştırmacılar, öğrenciler ve sağlık alanında çalışan kişiler için hazırlanmış olup, ilaç verilerine çevrimdışı erişim sağlamak amacıyla yayınlanmaktadır.

## İçerik

Bu veri kümesi ilaçlara ait temel ve açıklayıcı bilgileri içermektedir.

Her kayıt aşağıdaki bilgileri içerebilir:

* Barkod
* Ürün Adı
* Etken Madde
* ATC Kodu
* Kategori Bilgileri
* Açıklama

Veri kümesi UTF-8 karakter kodlaması kullanılarak hazırlanmıştır ve Türkçe karakterleri tam olarak desteklemektedir.

---

# Desteklenen Dosya Formatları

Bu depo aynı veriyi farklı kullanım senaryoları için birden fazla formatta sunmaktadır.

| Format | Açıklama                                                                                             |
| ------ | ---------------------------------------------------------------------------------------------------- |
| JSON   | Web uygulamaları, API geliştirme ve JavaScript projeleri için önerilir.                              |
| CSV    | Microsoft Excel, LibreOffice Calc, Google Sheets, Pandas ve veri analizi uygulamaları için uygundur. |
| SQL    | MySQL ve MariaDB veritabanlarına doğrudan aktarılabilecek SQL döküm dosyasıdır.                      |

---

# Klasör Yapısı

```text
data/
├── csv/
│   └── ilaclar.csv
│
├── json/
│   └── ilaclar.json
│
└── sql/
    └── ilaclar.sql
```

---

# JSON Veri Yapısı

Her kayıt aşağıdaki yapıya sahiptir.

```json
{
    "barcode": "869XXXXXXXXXX",
    "ATC_code": "M01AB08",
    "Active_Ingredient": "Etodolak",
    "Product_Name": "Örnek İlaç",
    "Category_1": "...",
    "Category_2": "...",
    "Category_3": "...",
    "Category_4": "...",
    "Category_5": "...",
    "Description": "..."
}
```

> Alanlar veri güncellemeleriyle genişletilebilir. Yeni alanlar eklendiğinde mevcut alan adları mümkün olduğunca korunmaya çalışılır.

---

# TABİP API

Bu veri kümesi, **TABİP API** tarafından kullanılan ilaç verilerinin çevrimdışı sürümüdür.

API kullanarak ilaç verilerine internet üzerinden erişebilir, bu depodaki dosyaları indirerek aynı verileri kendi projelerinizde çevrimdışı olarak kullanabilirsiniz.

TABİP API aşağıdaki sorguları desteklemektedir:

* Barkoda göre ilaç arama
* ATC koduna göre ilaç arama
* Etken maddeye göre ilaç arama
* JSON formatında çıktı
* HTTP GET istekleri
* UTF-8 desteği
* Hafif ve hızlı REST benzeri yapı

API dokümantasyonu için ilgili TABİP API deposunu inceleyebilirsiniz.

---

# Kullanım Alanları

Bu veri kümesi aşağıdaki projelerde kullanılabilir:

* İlaç bilgi sistemleri
* Hastane bilgi sistemleri
* Eczane yazılımları
* Klinik karar destek sistemleri
* Mobil sağlık uygulamaları
* Web uygulamaları
* Masaüstü uygulamaları
* Üniversite araştırmaları
* Veri analizi çalışmaları
* Makine öğrenmesi projeleri

---

# Veri Kaynağı

Bu veri kümesi, **T.C. Sağlık Bakanlığı** tarafından yayımlanan ilaç kayıtları ve ilaç sınıflandırmaları esas alınarak hazırlanmıştır.

İlaçların terapötik sınıflandırılmasında **Dünya Sağlık Örgütü (WHO) Anatomical Therapeutic Chemical (ATC) Classification System** esas alınmıştır.

Bu depoda yer alan veriler, TABİP projesi kapsamında geliştiricilerin daha kolay kullanabilmesi amacıyla düzenlenmiş, standartlaştırılmış ve makine tarafından okunabilir veri formatlarına (JSON, CSV ve SQL) dönüştürülmüştür.

TABİP tarafından gerçekleştirilen çalışmalar arasında şunlar yer almaktadır:

* Verilerin standart veri yapısına dönüştürülmesi
* UTF-8 karakter kodlaması ile uyumlu hale getirilmesi
* JSON, CSV ve SQL formatlarında yayımlanması
* Alan adlarının standartlaştırılması
* Barkod ve ATC bilgilerinin düzenlenmesi
* Etken madde bilgilerinin standartlaştırılması
* Geliştiriciler için kullanılabilir veri kümelerinin oluşturulması

Bu proje, resmî ilaç bilgi sistemlerinin yerine geçmeyi amaçlamaz. Eğitim, araştırma, yazılım geliştirme ve veri analizi çalışmalarında kullanılmak üzere hazırlanmış açık bir veri kümesidir.

En güncel ve resmî ilaç bilgileri için ilgili kurumların yayımladığı kaynaklar takip edilmelidir.

---

# Sürümleme

Her sürüm GitHub Releases üzerinden yayımlanmaktadır.

Sürüm geçmişi için `CHANGELOG.md` dosyasını inceleyebilirsiniz.

---

# Lisans

Bu depodaki verileri kullanmadan önce `LICENSE` dosyasındaki lisans koşullarını incelemeniz önerilir.

---

# Katkıda Bulunma

Hatalı kayıtlar, eksik bilgiler veya geliştirme önerileri için GitHub Issues ve Pull Request kullanılabilir.

Topluluk katkıları veri kalitesinin artırılmasına yardımcı olmaktadır.

---

# TABİP Projesi

Bu veri kümesi, sağlık verilerini geliştiriciler için daha erişilebilir hale getirmeyi amaçlayan **TABİP** açık veri projesinin bir parçasıdır.

TABİP kapsamında hastalık veritabanı, ilaç veritabanı, anatomi atlası ve diğer sağlık odaklı açık veri projeleri geliştirilmekte ve yayımlanmaktadır.

Teşekkür ederiz.
