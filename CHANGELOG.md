# Changelog

TABİP İlaç Veritabanı için tüm önemli değişiklikler bu dosyada belgelenir.

Format: [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/)  
Sürümleme: [Semantic Versioning](https://semver.org/lang/tr/)

## [2.0.0] - 2026

### Eklenen
- SQLite (`ilac.db`) format desteği
- Parquet (`ilac.parquet`) format desteği
- Satıcı Bilgisi (firma adı, reçete türü, durum)
- SGK Bilgisi (kamu no, eşdeğer grup, iskonto oranları, SUT kaynağı)
- İlaç ve SGK bilgi ekleniş tarihleri
- `Kullanım_Yolu` alanı
- Nested (iç içe) JSON veri yapısı
- `data/{csv,json,db,parquet}/` standart klasör yapısı

### Değişen
- README modernize edildi
- Alan adları standartlaştırıldı
- Veri yapısı nested (iç içe) formata geçirildi

### Kaldırılan
- (Yok)

## [1.0.0]

### Eklenen
- İlk sürüm: CSV ve JSON formatları
- Temel ilaç bilgileri (barkod, ATC, etken madde, ürün adı)
- 5 seviyeli kategori bilgisi
- Açıklama alanı
