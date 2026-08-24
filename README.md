# Awesome Google Dorking TR [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Google arama operatörleri, gelişmiş arama sözdizimi ve doğrudan ilgili Google Search özellikleri için Türkçe referans.

**Son doğrulama:** 25 Ağustos 2026

Google güncel ve eksiksiz tek bir operatör listesi yayımlamaz. Bu proje, operatörleri resmî belgeler, değişiklik kayıtları ve güvenilir teknik kaynaklarla karşılaştırarak mümkün olduğunca kapsamlı ve kaynaklı bir envanter sunar.

## Contents

- [Durum Etiketleri](#durum-etiketleri)
- [Temel Arama Sözdizimi](#temel-arama-sözdizimi)
- [Arama Operatörleri](#arama-operatörleri)
- [Başlık, URL ve Metin Operatörleri](#başlık-url-ve-metin-operatörleri)
- [Dosya ve İçerik Türleri](#dosya-ve-icerik-turleri)
- [Tarih ve Sayısal Filtreler](#tarih-ve-sayısal-filtreler)
- [Google Görseller Operatörleri](#google-görseller-operatörleri)
- [Google Search Dikeyleri ve Özellikleri](#google-search-dikeyleri-ve-özellikleri)
- [Değişken Operatörler](#değişken-operatörler)
- [Gelişmiş Kombinasyonlar](#gelişmiş-kombinasyonlar)
- [URL Parametreleri](#url-parametreleri)
- [Eski ve Kaldırılmış Operatörler](#eski-ve-kaldırılmış-operatörler)
- [Kaynaklar](#kaynaklar)
- [Katkı ve Lisans](#katkı-ve-lisans)

## Durum Etiketleri

| Etiket | Anlamı |
|---|---|
| ✅ RESMİ | Güncel bir Google kaynağında açıkça belgelenir. |
| 🟢 YAYGIN | Güncel kullanımda ve güvenilir teknik kaynaklarda yaygındır; resmî destek garantisi yoktur. |
| 🟡 DENEYSEL / DEĞİŞKEN | Davranışı sorguya, bölgeye veya arayüze göre değişebilir. |
| ⚠️ GÜVENİLMEZ / LEGACY | Eski kaynaklarda bulunur; desteği belirsiz veya davranışı tutarsızdır. |
| ❌ KALDIRILDI | Artık desteklenmediği doğrulanmıştır. |
| 🔗 URL PARAMETRESİ | Sorgu operatörü değildir; arama URL'sini veya arayüz davranışını değiştirir. |

## Temel Arama Sözdizimi

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `"..."` | Kelimeyi veya ifadeyi yazıldığı sırayla arar. | ✅ RESMİ | `"açık kaynak istihbaratı"` | Web | [G1](docs/kaynaklar.md#g1), [G4](docs/kaynaklar.md#g4) | 2026-08-25 |
| `-` | Önüne geldiği kelimeyi, ifadeyi veya desteklenen operatörü hariç tutar. | ✅ RESMİ | `jaguar -araba` | Web | [G1](docs/kaynaklar.md#g1) | 2026-08-25 |
| `OR` | Büyük harfle yazıldığında iki alternatiften en az birini ister. | ✅ RESMİ | `python OR rust` | Web | [G4](docs/kaynaklar.md#g4) | 2026-08-25 |
| <code>&#124;</code> | `OR` için yaygın kısa yazımdır; `OR` daha güvenilir tercihtir. | 🟢 YAYGIN | <code>python &#124; rust</code> | Web | [T1](docs/kaynaklar.md#t1), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `*` | Özellikle tırnaklı ifadelerde bir veya birkaç tam kelime için yer tutar; kelime parçası eşleştirmez. | 🟢 YAYGIN | `"en iyi * araçları"` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |

> Google Web Search'te `AND` gerekli değildir ve parantezler Boolean gruplama sağlamaz. Bu biçimler [eski ve güvenilmez sözdizimleri](docs/eski-ve-kaldirilan-operatorler.md#eski-guvenilmez-sozdizimleri) arasında açıklanır.

## Arama Operatörleri

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `site:` | Sonuçları bir alan adı, site, URL veya URL önekiyle sınırlar. | ✅ RESMİ | `site:example.com rapor` | Web | [G1](docs/kaynaklar.md#g1), [G2](docs/kaynaklar.md#g2) | 2026-08-25 |
| `-site:` | Belirtilen site veya alan adındaki sonuçları hariç tutar. | ✅ RESMİ | `araştırma -site:example.com` | Web | [G5](docs/kaynaklar.md#g5) | 2026-08-25 |

Yaygın kapsam biçimleri:

```text
site:example.com
site:example.com/docs/
site:.gov.tr
site:*.example.com
site:example.com -site:www.example.com
```

Wildcard kullanılan alan adı biçimleri Google'ın güncel kısa yardımında belgelenmez. `site:` sonuçları da eksiksiz bir indeks veya güvenlik envanteri değildir.

## Başlık, URL ve Metin Operatörleri

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `intitle:` | Hemen sonraki kelimeyi veya tırnaklı ifadeyi sayfa başlığında arar. | 🟢 YAYGIN | `intitle:"yıllık rapor"` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `allintitle:` | Ardındaki bütün sorgu terimlerini sayfa başlığıyla sınırlar. | 🟢 YAYGIN | `allintitle:açık kaynak istihbarat` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `inurl:` | Hemen sonraki kelimeyi veya tırnaklı ifadeyi URL içinde arar. | 🟢 YAYGIN | `inurl:profile` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `allinurl:` | Ardındaki bütün sorgu terimlerini URL ile sınırlar. | 🟢 YAYGIN | `allinurl:research profile` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `intext:` | Hemen sonraki kelimeyi veya tırnaklı ifadeyi sayfa gövdesinde arar. | 🟢 YAYGIN | `intext:"açık kaynak"` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `allintext:` | Ardındaki bütün sorgu terimlerini sayfa gövdesiyle sınırlar. | 🟢 YAYGIN | `allintext:açık kaynak istihbarat` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |

`allin...` biçimleri kendilerinden sonraki bütün terimleri kapsar. Karmaşık sorgularda tekil `intitle:`, `inurl:` ve `intext:` biçimleri daha öngörülebilirdir.

<a id="dosya-ve-icerik-turleri"></a>
## Dosya ve İçerik Türleri

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `filetype:` | HTTP `Content-Type` değeri veya dosya uzantısına göre sonuçları sınırlar. | ✅ RESMİ | `faaliyet raporu filetype:pdf` | Web | [G1](docs/kaynaklar.md#g1), [G2](docs/kaynaklar.md#g2), [G8](docs/kaynaklar.md#g8) | 2026-08-25 |
| `ext:` | `filetype:` için yaygın fakat resmî kısa listede bulunmayan diğer addır. | 🟢 YAYGIN | `rapor ext:pdf` | Web | [T1](docs/kaynaklar.md#t1), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |

`filetype:` yalnızca Google'ın indeksleyebildiği içerik kadar sonuç verir. Güncel resmî liste CSV'yi destekler; MP3 ise desteklenen medya türleri arasında listelenmez.

## Tarih ve Sayısal Filtreler

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `before:` | Belirtilen tarihten önce güncellenen belgeleri arar; yıl veya tam tarih kabul eder. | ✅ RESMİ | `rapor before:2025-01-01` | Web | [G1](docs/kaynaklar.md#g1) | 2026-08-25 |
| `after:` | Belirtilen tarihten sonra güncellenen belgeleri arar; yıl veya tam tarih kabul eder. | ✅ RESMİ | `rapor after:2025-01-01` | Web | [G1](docs/kaynaklar.md#g1) | 2026-08-25 |
| `..` | İki sayı arasındaki değerleri, gerekirse para veya ölçü birimiyle birlikte arar. | ✅ RESMİ | `fotoğraf makinesi 3000..5000 TL` | Web | [G4](docs/kaynaklar.md#g4) | 2026-08-25 |

`before:` ve `after:` kesin ilk yayın tarihini değil, Google'ın belge için yorumladığı güncelleme tarihini filtreler.

## Google Görseller Operatörleri

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `imagesize:` | Tam piksel ölçüsündeki görselleri içeren sayfaları bulur. | ✅ RESMİ | `imagesize:1200x800` | Yalnızca Google Görseller | [G2](docs/kaynaklar.md#g2) | 2026-08-25 |
| `src:` | Belirli görsel URL'sini `src` niteliğinde kullanan sayfaları bulur. | ✅ RESMİ | `src:https://example.com/images/logo.png` | Yalnızca Google Görseller | [G2](docs/kaynaklar.md#g2) | 2026-08-25 |

## Google Search Dikeyleri ve Özellikleri

Bu sorgular Google'ın güncel çekirdek operatör tablosunda yer almaz. Bazıları doğal dil niyetiyle aynı bilgi kutusunu tetikleyebilir; kolonun tek başına özel bir operatör olarak işlendiği varsayılmamalıdır.

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `define <terim>` | Terim tanımını tetikleyen kolonsuz sorgu kalıbıdır. | 🟢 YAYGIN | `define osint` | Web / bilgi kutusu | [D1](docs/kaynaklar.md#d1) | 2026-08-25 |
| `source:` | Haber sonuçlarını belirli bir yayın kaynağına daraltmayı amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `iklim source:reuters` | Google News | [T1](docs/kaynaklar.md#t1), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `weather:` | Hava durumu sonuçlarını tetiklemeyi amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `weather:Ankara` | Web / bilgi kutusu | [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `stocks:` | Şirket veya sembol için finans sonuçlarını tetiklemeyi amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `stocks:GOOG` | Web / finans | [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `map:` | Harita sonuçlarını öne çıkarmayı amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `map:Ankara` | Web / Maps | [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `movie:` | Film bilgi sonuçlarını tetiklemeyi amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `movie:Arrival` | Web / bilgi kutusu | [T2](docs/kaynaklar.md#t2) | 2026-08-25 |

Operatör olmayan fakat yararlı sorgu kalıpları:

| Kalıp | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `<değer> in <birim>` | Google'ın resmî birim veya para dönüştürücüsünü tetikleyen doğal dil kalıbıdır. | 🟢 YAYGIN | `10 km in miles` | Web / dönüştürücü | [G6](docs/kaynaklar.md#g6), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| Para ve ölçü işaretleri | `$`, `€` ve `%` gibi işaretler aranabilir ve sayısal aralığa bağlam sağlar. | 🟢 YAYGIN | `kitap €30..€50` | Web | [G4](docs/kaynaklar.md#g4), [D1](docs/kaynaklar.md#d1) | 2026-08-25 |

## Değişken Operatörler

| Sözdizimi | Açıklama | Durum | Örnek | Kapsam | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `terim1 AROUND(n) terim2` / `terim1 AROUND n terim2` | İki terimi yaklaşık `n` kelime yakınlığında aramayı amaçlar; kesin mesafe garantisi vermez. | 🟡 DENEYSEL / DEĞİŞKEN | `Alice AROUND(5) research` | Web | [D1](docs/kaynaklar.md#d1), [T1](docs/kaynaklar.md#t1) | 2026-08-25 |
| `inanchor:` | Hemen sonraki terimi sayfaya gelen bağlantıların metninde aramayı amaçlar. | 🟡 DENEYSEL / DEĞİŞKEN | `inanchor:research` | Web | [D1](docs/kaynaklar.md#d1), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |
| `allinanchor:` | Ardındaki bütün terimleri gelen bağlantıların metniyle sınırlar; sonuçlar tutarsız olabilir. | 🟡 DENEYSEL / DEĞİŞKEN | `allinanchor:security research` | Web | [D1](docs/kaynaklar.md#d1), [T2](docs/kaynaklar.md#t2) | 2026-08-25 |

## Gelişmiş Kombinasyonlar

```text
site:example.com "yıllık rapor"
site:example.com filetype:pdf "faaliyet raporu"
"açık kaynak" after:2025-01-01 before:2026-01-01
site:example.com intitle:"faaliyet raporu" filetype:pdf
```

Araştırma, alan adı inceleme, doküman arama, akademik arama, OSINT ve tarih filtreleme örnekleri için [Örnek Kombinasyonlar](docs/ornek-kombinasyonlar.md) belgesine bakın.

## URL Parametreleri

`pws=`, `tbs=`, `udm=` ve `tbm=` gibi değerler operatör değildir. Google Search sonuç URL'sini veya arayüz modunu değiştirir ve yalnızca [Google Search URL Parametreleri](docs/google-url-parametreleri.md) belgesinde listelenir.

## Eski ve Kaldırılmış Operatörler

`cache:`, `related:`, `link:`, `info:`, `+`, `~` ve diğer tarihsel sözdizimleri aktif listeye karıştırılmaz. Durumları, kaldırılma tarihleri ve yaygın yanlış aktarımlar [Eski ve Kaldırılmış Operatörler](docs/eski-ve-kaldirilan-operatorler.md) belgesinde bulunur.

## Kaynaklar

Kaynak önceliği şöyledir:

1. Güncel Google Search Help ve Search Central belgeleri
2. Google Search Central değişiklik kayıtları
3. Güncel ve tekrarlanabilir davranış
4. Güvenilir teknik kaynaklar
5. Tarihsel listeler ve topluluk referansları

Kullanılan kaynakların tamamı ve doğrulama notları [Kaynaklar](docs/kaynaklar.md) belgesindedir. Eski bir kaynak güncel resmî Google belgesiyle çelişirse güncel resmî belge esas alınır.

## Katkı ve Lisans

Yeni bir operatör veya durum değişikliği önermeden önce [katkı rehberini](CONTRIBUTING.md) inceleyin. Hazır parola, gizli anahtar, açık cihaz veya yetkisiz erişim sorguları bu projenin kapsamı dışındadır.

Dokümantasyon [Creative Commons Attribution 4.0 International](LICENSE) lisansı altındadır.
