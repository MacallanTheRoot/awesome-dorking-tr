# Eski ve Kaldırılmış Google Operatörleri

**Son doğrulama:** 25 Ağustos 2026

Bu belge güncel operatör listesinden ayrı tutulur. Buradaki sözdizimlerinin bir kısmı tarihsel, bir kısmı güvenilmez, bir kısmı da başka ürünlerden yanlış aktarılmıştır.

<a id="eski-guvenilmez-sozdizimleri"></a>
## Eski, güvenilmez veya yanlış aktarılan sözdizimleri

| Sözdizimi | Kategori | Durum | Açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `AND` | Mantıksal ifade | ⚠️ GÜVENİLMEZ / LEGACY | Google sorgu terimlerini zaten birlikte değerlendirir; açık `AND` gerekli veya güvenilir bir gruplama komutu değildir. | `osint verification` | [D1](kaynaklar.md#d1), [G4](kaynaklar.md#g4) | 2026-08-25 |
| `()` | Gruplama | ⚠️ GÜVENİLMEZ / LEGACY | Parantezler Boolean öncelik veya gruplama sağlamaz; karmaşık alternatifler ayrı sorgulara bölünmelidir. | `A B OR C D` | [D1](kaynaklar.md#d1) | 2026-08-25 |
| `define:` | Eski tanım biçimi | ⚠️ GÜVENİLMEZ / LEGACY | Kolonlu eski biçim yerine güncel kolonsuz `define <terim>` kalıbı kullanılmalıdır. | `define osint` | [D1](kaynaklar.md#d1), [T1](kaynaklar.md#t1) | 2026-08-25 |
| `location:` | Eski Google News | ⚠️ GÜVENİLMEZ / LEGACY | Haberleri konuma göre daraltan eski dikey sözdizimidir; Web Search çekirdeğinde güvenilir değildir. | `teknoloji location:Turkey` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `loc:` | Bölgesel daraltma | ⚠️ GÜVENİLMEZ / LEGACY | Eski listelerde bölge daraltması olarak geçer; güncel davranışı tutarsızdır. | `teknoloji loc:Ankara` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `daterange:` | Eski tarih filtresi | ⚠️ GÜVENİLMEZ / LEGACY | Julian gün sayılarını kullanan eski yöntemdir; `before:` ve `after:` tercih edilmelidir. | `rapor daterange:2459000-2459100` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `@` | Eski sosyal arama | ⚠️ GÜVENİLMEZ / LEGACY | Güncel Web Search'te normal sorgudan ayrı bir sosyal profil filtresi olduğu doğrulanmaz. | `@example` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `#` | Aranabilir karakter | ⚠️ GÜVENİLMEZ / LEGACY | Hashtag metni aranabilir; ancak güncel, bağımsız bir filtre operatörü değildir. | `#açıkveri` | [D1](kaynaklar.md#d1), [T1](kaynaklar.md#t1) | 2026-08-25 |
| `safesearch:` | Eski ayar komutu | ⚠️ GÜVENİLMEZ / LEGACY | Güncel SafeSearch ayarı veya URL mekanizması tercih edilmelidir. | `safesearch:örnek` | [G1](kaynaklar.md#g1), [T2](kaynaklar.md#t2) | 2026-08-25 |
| `stock:` | Finans diğer adı | ⚠️ GÜVENİLMEZ / LEGACY | Güncel resmî bir Web Search operatörü olarak belgelenmez. | `stock:GOOG` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `numrange:` | Eski sayısal aralık | ⚠️ GÜVENİLMEZ / LEGACY | Eski listelerde `..` için uzun biçim olarak geçer; güncel Google arayüzü `..` biçimini gösterir. | `ürün 100..500` | [G4](kaynaklar.md#g4), [T2](kaynaklar.md#t2) | 2026-08-25 |
| `contains:` | Yanlış ürün aktarımı | ⚠️ GÜVENİLMEZ / LEGACY | Güncel Google Web Search operatörü değildir; başka arama sistemleriyle karıştırılır. | `"contains:" example` | [G1](kaynaklar.md#g1), [D1](kaynaklar.md#d1) | 2026-08-25 |
| `date:` | Yanlış diğer ad | ⚠️ GÜVENİLMEZ / LEGACY | Güncel Google Web tarih operatörü değildir; `before:` ve `after:` kullanılmalıdır. | `rapor after:2025-01-01` | [G1](kaynaklar.md#g1) | 2026-08-25 |
| `relate:` | Yazım hatası | ⚠️ GÜVENİLMEZ / LEGACY | Kaldırılmış `related:` ile karıştırılan doğrulanmamış bir biçimdir. | `"relate:" example.com` | [G3](kaynaklar.md#g3) | 2026-08-25 |
| `author:` | Ürün kapsamı dışında | ⚠️ GÜVENİLMEZ / LEGACY | Scholar veya Groups bağlamında görülebilir; genel Web Search çekirdek operatörü değildir. | `"Ada Lovelace"` | [D1](kaynaklar.md#d1) | 2026-08-25 |
| `index of` | Sıradan ifade | ⚠️ GÜVENİLMEZ / LEGACY | Özel Google operatörü değildir; normal bir metin ifadesidir. | `"index of" "public documents"` | [G1](kaynaklar.md#g1), [D1](kaynaklar.md#d1) | 2026-08-25 |

## Kaldırılmış operatörler

| Sözdizimi | Kategori | Durum | Eski işlev veya kaldırılma notu | Güvenli tarihsel örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `related:` | Benzer siteler | ❌ KALDIRILDI | Google, artık desteklenmediği için 18 Temmuz 2023'te operatör belgesinden kaldırdı. | `related:example.com` | [G3](kaynaklar.md#g3) | 2026-08-25 |
| `cache:` | Önbellek | ❌ KALDIRILDI | Google, artık çalışmadığı için 24 Eylül 2024'te operatör belgesini kaldırdı. | `cache:example.com` | [G3](kaynaklar.md#g3) | 2026-08-25 |
| `link:` | Gelen bağlantılar | ❌ KALDIRILDI | Belirli URL'ye bağlantı veren sayfaları arardı; 2016 ortasında kullanımdan kaldırıldı. | `link:example.com` | [D1](kaynaklar.md#d1) | 2026-08-25 |
| `info:` | URL bilgisi | ❌ KALDIRILDI | Bir URL hakkında bilgi ve yardımcı bağlantılar gösterirdi; 2017 ortasında kaldırıldı. | `info:example.com` | [D1](kaynaklar.md#d1) | 2026-08-25 |
| `id:` | `info:` diğer adı | ❌ KALDIRILDI | `info:` için kullanılan eski, belgelenmemiş diğer addı; ana işlevle birlikte geçersizleşti. | `id:example.com` | [D1](kaynaklar.md#d1), [T2](kaynaklar.md#t2) | 2026-08-25 |
| `phonebook:` | Telefon rehberi | ❌ KALDIRILDI | Telefon listesi aramasıydı; Kasım 2010'da kaldırıldı. | `phonebook:"Örnek Kişi"` | [H2](kaynaklar.md#h2) | 2026-08-25 |
| `+` | Zorunlu tam kelime | ❌ KALDIRILDI | Google eski tam kelime operatörünü 2011'de kaldırdı ve çift tırnağı önerdi. | `"tamkelime"` | [H1](kaynaklar.md#h1) | 2026-08-25 |
| `~` | Eşanlamlı genişletme | ❌ KALDIRILDI | Eşanlamlıları dahil ederdi; 2013'te kaldırıldı. | `örnek eşanlamlı` | [H3](kaynaklar.md#h3) | 2026-08-25 |
| `blogurl:` | Google Blog Search | ❌ KALDIRILDI | Eski Blog Search'te blog URL'si bulurdu; ilgili arama dikeyi sona erdi. | `blogurl:example.com` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `inpostauthor:` | Google Blog Search | ❌ KALDIRILDI | Eski Blog Search'te yazara göre gönderi arardı. | `inpostauthor:"Örnek Yazar"` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `allinpostauthor:` | Google Blog Search | ❌ KALDIRILDI | Eski Blog Search'te birden çok yazar terimini eşleştirirdi. | `allinpostauthor:Örnek Yazar` | [T2](kaynaklar.md#t2) | 2026-08-25 |
| `inposttitle:` | Google Blog Search | ❌ KALDIRILDI | Eski Blog Search'te gönderi başlığı arardı. | `inposttitle:araştırma` | [T2](kaynaklar.md#t2) | 2026-08-25 |

## Envantere alınmayan biçimler

- `links:`: `link:` için doğrulanmış bir Google diğer adı olduğuna dair yeterli kanıt yoktur.
- Google Scholar, Google Books ve Google Groups'e özgü `inauthor:`, `inpublisher:`, `isbn:`, `group:` ve `insubject:` gibi sözdizimleri genel Web Search envanterine dahil edilmez.

Başka bir Google ürününde aynı adın kullanılması, onu Google Web Search operatörü yapmaz.
