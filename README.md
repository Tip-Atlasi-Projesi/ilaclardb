<div align="center">

# 💊 TABİP İlaç Veritabanı
### *Bilgi İyileştirir!*

<p align="center">
  <b>Türkiye'de Kullanılan İlaçlara Ait Açık Veri Kümesi</b>
</p>

<p align="center">
  <a href="http://tabip.rf.gd" target="_blank"><img src="https://img.shields.io/badge/Web%20Sitesi-tabip.rf.gd-0D9488?style=for-the-badge&logo=internet-explorer&logoColor=white" alt="Website"></a>
  <a href="https://www.linkedin.com/company/tabip1/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-Company-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:tipatlasiprojesi@gmail.com"><img src="https://img.shields.io/badge/İletişim-E--posta-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Konum-Türkiye-C8102E?style=for-the-badge&logo=turkey&logoColor=white" alt="Location">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Sürüm-v2.0.0-0D9488?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Lisans-CC0%201.0-lightgrey?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/UTF--8-Destekli-success?style=for-the-badge" alt="UTF-8">
  <img src="https://img.shields.io/badge/Format-JSON%20%7C%20CSV%20%7C%20SQLite%20%7C%20Parquet-blue?style=for-the-badge" alt="Formats">
</p>

</div>

---

## 🌟 TABİP İlaç Veritabanı Nedir?

**TABİP İlaç Veritabanı**; Türkiye'de kullanılan ilaçlara ait barkod, ATC kodu, etken madde, ürün, firma, kategori ve SGK bilgilerini içeren yapılandırılmış açık veri kümesidir.

TABİP ekosisteminin bir parçası olarak; geliştiriciler, araştırmacılar, öğrenciler ve sağlık profesyonelleri için **çevrimdışı erişilebilir**, **makine tarafından okunabilir** ve **standartlaştırılmış** ilaç verisi sunmayı amaçlar.

Amacımız; Türkçe ilaç bilgisini akademik çerçevede standartlaştırmak, doğrulanabilir ve sürekli güncellenen açık bir dijital altyapı olarak sunmaktır.

---

## ✨ Özellikler

<table>
<tr>
<td width="50%">

**📊 Kapsamlı Veri**
- Barkod, ATC kodu, etken madde
- Firma ve reçete bilgileri
- 5 seviyeli ATC kategorileri
- SGK geri ödeme ve iskonto bilgileri

**🌍 UTF-8 Desteği**
- Türkçe karakterler tam uyumlu
- Standart alan adlandırması

</td>
<td width="50%">

**📦 Çoklu Format**
- CSV, JSON, SQLite, Parquet
- Her senaryo için optimize edilmiş

**⚡ Çevrimdışı Erişim**
- İnternet bağlantısı gerektirmez
- Yerel projelere kolay entegrasyon

**🔄 Düzenli Güncelleme**
- Sağlık Bakanlığı ve SGK verileriyle senkronize

</td>
</tr>
</table>

---

## 📦 Desteklenen Formatlar

Bu depo, aynı veriyi farklı kullanım senaryoları için birden fazla formatta sunmaktadır.

| Format | Dosya | Açıklama |
| :--- | :--- | :--- |
| 📄 **CSV** | `ilac.csv` | Microsoft Excel, LibreOffice Calc, Google Sheets, Pandas ve veri analizi uygulamaları için uygundur. |
| 🔷 **JSON** | `ilac.json` | Web uygulamaları, API geliştirme ve JavaScript projeleri için önerilir. |
| 🗄️ **SQLite** | `ilac.db` | Sunucu gerektirmeyen, taşınabilir, doğrudan kullanılabilir veritabanı dosyasıdır. |
| 🚀 **Parquet** | `ilac.parquet` | Büyük veri, Apache Spark, Pandas ve sütun bazlı analizler için optimize edilmiştir. |

---

## 📁 Klasör Yapısı

```text
ilaclardb/
│
├── data/
│   ├── csv/
│   │   └── ilac.csv
│   ├── json/
│   │   └── ilac.json
│   ├── db/
│   │   └── ilac.db
│   └── parquet/
│       └── ilac.parquet
│
├── CHANGELOG.md
├── LICENSE
└── README.md
```

---

## 🧬 Veri Yapısı

Her kayıt; **İlaç**, **Satıcı**, **Kategori** ve **SGK** bilgilerini içeren iç içe (nested) bir yapıya sahiptir.

### Örnek Kayıt (JSON)

```json
[
  {
    "İlaç Bilgisi": {
      "İlaç Adı": "NAXODER %1 KREM",
      "Barkod": 8680131752362,
      "ATC Kodu": "D01AE22",
      "Active_Ingredient": "Naftifin Hidroklorür",
      "Kullanım_Yolu": "Topikal (Deri üzerine)"
    },
    "Satıcı Bilgisi": {
      "Firma Adı": "VEFA İLAÇ SANAYİ VE TİCARET ANONİM ŞİRKETİ",
      "Reçete Türü": "Normal",
      "Durumu": "Aktif"
    },
    "Kategori Bilgisi": {
      "Category_1": "Dermatolojik İlaçlar",
      "Category_2": "Dermatolojik Antifungaller",
      "Category_3": "Topikal Antifungaller",
      "Category_4": "Topikal kullanım için diğer antifungal",
      "Category_5": "Topikal kullanım için diğer antifungal"
    },
    "İlaç_Ekleniş_Tarihi": "06/10/2026",
    "SGK_Bilgi_Ekleniş_Tarihi": "08/04/2026",
    "SGK_Bilgi_Kaynak": "08/04/2026 Tarihli ve 33218 Sayılı Resmî Gazete'de Yayımlanan \"Sosyal Güvenlik Kurumu Sağlık Uygulama Tebliğinde Değişiklik Yapılmasına Dair Tebliğ\"",
    "SGK_Bilgisi": {
      "Kamu No": "A17994",
      "Eşdeğer İlaç Grubu": "E712B",
      "Terapötik Referans Grubu": null,
      "Listeye Giriş Tarihi": "01/10/2020",
      "Aktiflenme Tarihi": null,
      "Pasiflenme Tarihi": null,
      "Uygulanan İndirim Oranlarına Esas Durumu": "FIYAT KORUMALI",
      "Depocuya Satış Fiyatı (Firma Satış Fiyatı) 151,25 TL ve üzeri ise": 0.28,
      "Depocuya Satış Fiyatı (Firma Satış Fiyatı) 100,38 TL - 151,24 TL arasında ise": 0.28,
      "Depocuya Satış Fiyatı (Firma Satış Fiyatı) 52,44 TL - 100,37 TL arasında ise": 0.28,
      "Depocuya Satış Fiyatı (Firma Satış Fiyatı) 52,43 TL ve altında ise": 0.28,
      "Özel İskonto": null,
      "Eczacı İskonto Oranı": "0-2,5%"
    }
  }
]
```

### Alan Açıklamaları

<details>
<summary><b>💊 İlaç Bilgisi</b></summary>

| Alan | Tip | Açıklama |
| :--- | :--- | :--- |
| `İlaç Adı` | `string` | Ürünün ticari adı |
| `Barkod` | `number` | EAN-13 barkod numarası |
| `ATC Kodu` | `string` | WHO ATC sınıflandırma kodu |
| `Active_Ingredient` | `string` | Etken madde |
| `Kullanım_Yolu` | `string` | Uygulama yolu (oral, topikal, vb.) |

</details>

<details>
<summary><b>🏢 Satıcı Bilgisi</b></summary>

| Alan | Tip | Açıklama |
| :--- | :--- | :--- |
| `Firma Adı` | `string` | Ruhsat sahibi firma |
| `Reçete Türü` | `string` | Normal, Kırmızı, Yeşil, Mor, vb. |
| `Durumu` | `string` | Aktif / Pasif |

</details>

<details>
<summary><b>📂 Kategori Bilgisi</b></summary>

ATC tabanlı 5 seviyeli terapötik sınıflandırma (`Category_1` → `Category_5`).

</details>

<details>
<summary><b>🏛️ SGK Bilgisi</b></summary>

| Alan | Tip | Açıklama |
| :--- | :--- | :--- |
| `Kamu No` | `string` | SGK kamu numarası |
| `Eşdeğer İlaç Grubu` | `string` | Eşdeğer ilaç grubu kodu |
| `Terapötik Referans Grubu` | `string` | Terapötik referans grubu |
| `Listeye Giriş Tarihi` | `string` | SGK listesine giriş tarihi |
| `Aktiflenme / Pasiflenme Tarihi` | `string` | Durum değişiklik tarihleri |
| `Uygulanan İndirim Oranlarına Esas Durumu` | `string` | Fiyat korumalı / korumasız |
| `Depocuya Satış Fiyatı ...` | `number` | Fiyat dilimlerine göre iskonto oranları |
| `Özel İskonto` | `number` | Varsa özel iskonto oranı |
| `Eczacı İskonto Oranı` | `string` | Eczacıya uygulanan iskonto aralığı |

</details>

> ℹ️ Alanlar veri güncellemeleriyle genişletilebilir. Yeni alanlar eklendiğinde mevcut alan adları mümkün olduğunca korunmaya çalışılır.

---

## 🚀 Hızlı Başlangıç

### Python (Pandas ile CSV)

```python
import pandas as pd

df = pd.read_csv("data/csv/ilac.csv", encoding="utf-8")
print(df.head())
```

### Python (JSON)

```python
import json

with open("data/json/ilac.json", encoding="utf-8") as f:
    ilaclar = json.load(f)

for ilac in ilaclar:
    print(ilac["İlaç Bilgisi"]["İlaç Adı"], "-", ilac["İlaç Bilgisi"]["ATC Kodu"])
```

### Python (SQLite)

```python
import sqlite3
import pandas as pd

conn = sqlite3.connect("data/db/ilac.db")
df = pd.read_sql_query("SELECT * FROM ilaclar LIMIT 10", conn)
print(df)
```

### Python (Parquet)

```python
import pandas as pd

df = pd.read_parquet("data/parquet/ilac.parquet")
print(df.head())
```

### JavaScript / Node.js

```javascript
const ilaclar = require("./data/json/ilac.json");

const naftifin = ilaclar.find(
  i => i["İlaç Bilgisi"]["Active_Ingredient"].includes("Naftifin")
);
console.log(naftifin);
```

---

## 🌐 TABİP API

Bu veri kümesi, **TABİP API** tarafından kullanılan ilaç verilerinin çevrimdışı sürümüdür. İnternet üzerinden erişmek isterseniz API'yi kullanabilir, bu depodaki dosyalarla da aynı veriyi kendi projelerinize çevrimdışı olarak entegre edebilirsiniz.

**Desteklenen sorgular:**

- 🔍 Barkoda göre ilaç arama
- 🧪 ATC koduna göre ilaç arama
- ⚗️ Etken maddeye göre ilaç arama
- 📤 JSON formatında çıktı
- 🌐 HTTP GET istekleri
- 🔤 UTF-8 desteği
- 🪶 Hafif ve hızlı REST benzeri yapı

> Detaylı API dokümantasyonu için [Tabip-api](https://github.com/Tip-Atlasi-Projesi/Tabip-api) deposunu inceleyebilirsiniz.

---

## 🎯 Kullanım Alanları

<table>
<tr>
<td width="50%">

**🏥 Sağlık BT**
- İlaç bilgi sistemleri
- Hastane bilgi sistemleri
- Eczane yazılımları
- Klinik karar destek sistemleri

</td>
<td width="50%">

**💻 Geliştirme**
- Mobil sağlık uygulamaları
- Web uygulamaları
- Masaüstü uygulamaları
- API servisleri

</td>
</tr>
<tr>
<td>

**🎓 Akademik**
- Üniversite araştırmaları
- Veri analizi çalışmaları
- Makine öğrenmesi projeleri

</td>
<td>

**📊 Finans / Politika**
- SGK geri ödeme analizleri
- Fiyat ve iskonto araştırmaları
- Sağlık politikası çalışmaları

</td>
</tr>
</table>

---

## 📚 Veri Kaynağı

Bu veri kümesi şu kaynaklar esas alınarak hazırlanmıştır:

- 🏛️ **T.C. Sağlık Bakanlığı** — İlaç kayıtları ve ruhsat bilgileri
- 🏦 **Sosyal Güvenlik Kurumu (SGK)** — Sağlık Uygulama Tebliği (SUT) bilgileri
- 🌍 **Dünya Sağlık Örgütü (WHO)** — Anatomical Therapeutic Chemical (ATC) sınıflandırma sistemi

### TABİP Tarafından Yapılan Çalışmalar

- ✅ Verilerin standart veri yapısına dönüştürülmesi
- ✅ UTF-8 karakter kodlaması ile uyumlu hale getirilmesi
- ✅ JSON, CSV, SQLite ve Parquet formatlarında yayımlanması
- ✅ Alan adlarının standartlaştırılması
- ✅ Barkod ve ATC bilgilerinin düzenlenmesi
- ✅ Etken madde bilgilerinin standartlaştırılması
- ✅ SGK geri ödeme ve iskonto bilgilerinin yapılandırılması
- ✅ Geliştiriciler için kullanılabilir veri kümelerinin oluşturulması

> ⚠️ **Yasal Uyarı:** Bu proje, resmî ilaç bilgi sistemlerinin yerine geçmeyi amaçlamaz. Eğitim, araştırma, yazılım geliştirme ve veri analizi çalışmalarında kullanılmak üzere hazırlanmış açık bir veri kümesidir. En güncel ve resmî ilaç bilgileri için ilgili kurumların yayımladığı kaynaklar takip edilmelidir.

---

## 🏗️ TABİP Ekosistemi

TABİP çatısı altında geliştirilen diğer açık kaynaklı modüller ve veritabanları:

| Proje | Açıklama | Teknoloji / Kapsam | Durum |
| :--- | :--- | :--- | :--- |
| **[tabip-sentetik](https://github.com/Tip-Atlasi-Projesi/tabip-sentetik)** | Türkiye'nin ilk ve en kapsamlı açık kaynak Türkçe sentetik hasta veri setidir. | Yapay Zeka, LLM & Sağlık Yazılımları | `Public` |
| **[Tabip-api](https://github.com/Tip-Atlasi-Projesi/Tabip-api)** | TABİP projesinin rest API uygulamaları ve servisleri. | Python, FastAPI/Flask, JS, REST API | `MIT License` |
| **[hastaliklar](https://github.com/Tip-Atlasi-Projesi/hastaliklar)** | WHO ICD listesinde yer alan 925 hastalığın detaylı verilerini içeren rehber. | JSON, SQL, Database, ICD | `MIT License` |
| **[ilaclardb](https://github.com/Tip-Atlasi-Projesi/ilaclardb)** | Sağlık Bakanlığı tarafından onaylanmış ilaçları içeren yapılandırılmış veri seti. | Python, JSON, SQL, ATC Kodları | `CC0 1.0 Universal` |

---

## 🧭 Web Tabanlı Modüller

Platformun arayüz üzerinden erişilebilen temel bileşenleri:

- 🧊 **Tabip Atlas:** Binlerce yapıyı Türkçe, İngilizce ve Latince destekleyen 3D interaktif anatomi atlası.
- 💊 **Tabip İlaç:** Etken madde, ATC kodları ve barkod bazlı yapılandırılmış ilaç veritabanı.
- 🩺 **Tabip Hastalık:** ICD kodlu, sistematik tanı ölçütleri ve klinik özetler içeren rehber.
- ⚡ **Tabip API:** Üçüncü taraf sistemler ve geliştiriciler için açık veri servisleri.

---

## 🔄 Sürüm Bilgisi

**Mevcut Sürüm:** `v2.0.0`

Bu sürümde öne çıkan yenilikler:

- ✨ **Yeni format desteği:** SQLite (`ilac.db`) ve Parquet (`ilac.parquet`)
- 🧬 **Genişletilmiş veri yapısı:** Satıcı, Kategori, SGK ve Tarih bilgileri eklendi
- 🏛️ **SGK entegrasyonu:** Kamu No, eşdeğer ilaç grubu, iskonto oranları
- 📂 **Standart klasör yapısı:** `data/{csv,json,db,parquet}/`
- 📝 **Yeniden yapılandırılmış README** ve alan sözlüğü

### Sürüm Geçmişi

| Sürüm | Tarih | Öne Çıkanlar |
| :--- | :--- | :--- |
| **v2.0.0** | 2026 | SQLite + Parquet desteği, SGK bilgileri, nested JSON yapısı |
| v1.0.0 | — | İlk sürüm: CSV, JSON, temel ilaç bilgileri |

> Detaylı sürüm notları için [`CHANGELOG.md`](CHANGELOG.md) dosyasını inceleyebilirsiniz.
> Tüm sürümler **GitHub Releases** üzerinden yayımlanmaktadır.

---

## 📜 Lisans

Bu depodaki veriler **CC0 1.0 Universal** lisansı altında yayımlanmaktadır. Detaylar için [`LICENSE`](LICENSE) dosyasını inceleyebilirsiniz.

---

## 🤝 Katkıda Bulunma

Katkılarınız projeyi güçlendirir! 🎉

- 🐛 **Hata bildirimi** için [Issues](../../issues) açın
- 💡 **Öneri ve geliştirmeler** için [Pull Request](../../pulls) gönderin
- 📝 **Hatalı / eksik kayıtlar** için veri düzeltme talebi oluşturun

Topluluk katkıları veri kalitesinin artırılmasına yardımcı olmaktadır.

---

## 👨‍💻 Geliştirici & İletişim

TABİP projesi, **Emin Neşat Gürses** tarafından açık kaynak topluluğunun katkılarıyla geliştirilmektedir.

- 🌐 **Web Sitesi:** [tabip.rf.gd](http://tabip.rf.gd)
- 💼 **LinkedIn:** [company/tabip1](https://www.linkedin.com/company/tabip1/)
- ✉️ **E-posta:** tipatlasiprojesi@gmail.com

---

<div align="center">

**⭐ Projeyi faydalı bulduysanız yıldız vermeyi unutmayın!**

<i>&copy; 2026 TABİP · Açık Kaynak Tıbbi Bilgi Platformu</i>

</div>
