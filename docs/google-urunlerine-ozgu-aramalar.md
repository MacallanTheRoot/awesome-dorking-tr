# Google Ürünlerine Özgü Aramalar

**Son doğrulama:** 25 Ağustos 2026

> Bu sözdizimleri genel Google Web Search operatörleri değildir. Yalnızca belirtilen Google ürününün arama yüzeyinde geçerlidir.

Ürünler aynı karakterleri veya operatör adlarını farklı kurallarla işleyebilir. Örneğin Google Patents'teki `AND`, parantez ve `before:` desteği, aynı davranışın genel Web Search'te bulunduğunu kanıtlamaz. Kaynak kodları [Kaynaklar](kaynaklar.md) belgesine gider.

## Google Scholar

Google Scholar Help aşağıdaki sorgu biçimlerini açıkça gösterir.

| Sözdizimi | Tür | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `author:<ad>` | Yazar kısıtı | ✅ RESMİ — SCHOLAR | Sonuçları belirtilen yazar adına göre arar; ad tırnak içine alınabilir. | `author:"donald e knuth"` | [G10](kaynaklar.md#g10) | 2026-08-25 |
| `"<tam başlık>"` | Başlık araması | ✅ RESMİ — SCHOLAR | Makale başlığını tam ifade olarak arar. | `"A History of the China Sea"` | [G10](kaynaklar.md#g10) | 2026-08-25 |
| `site:<alan-adı>` | Kaynak site kısıtı | ✅ RESMİ — SCHOLAR | Scholar'ın birincil sürüm olarak indekslediği kayıtları belirtilen siteyle sınırlar; beklenen bütün kopyaları listelemeyebilir. | `site:example.gov climate research` | [G10](kaynaklar.md#g10) | 2026-08-25 |

Scholar Advanced Search ayrıca yazar, başlık ve yayın alanlarında arama ile tarih sınırlaması sunar. Arayüz alanlarının varlığı, `publication:` gibi aynı adlı kolonlu bir sözdiziminin desteğini tek başına kanıtlamaz.

## Google Patents

Google Patents, genel Web Search'ten ayrı bir sorgu dili kullanır. Aşağıdaki Boolean ve yakınlık sözdizimlerinin bir kısmı yalnızca Patents Advanced Search'teki Search Term alanında kullanılabilir.

### Metadata Kısıtları

| Sözdizimi | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|
| `inventor:` | ✅ RESMİ — PATENTS | Buluş sahibinin adına göre sınırlar. | `inventor:"Alexander Graham Bell"` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `assignee:` | ✅ RESMİ — PATENTS | Patent sahibine veya devralana göre sınırlar. | `assignee:"Google Inc"` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `before:` | ✅ RESMİ — PATENTS | Varsayılan olarak başvuru tarihinden önceki kayıtları sınırlar; arayüzden tarih türü değiştirilebilir. | `before:2010` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `after:` | ✅ RESMİ — PATENTS | Varsayılan olarak başvuru tarihinden sonraki kayıtları sınırlar; arayüzden tarih türü değiştirilebilir. | `after:"Jan 2006"` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `country:` | ✅ RESMİ — PATENTS | Patent ülkesine göre sınırlar. | `country:US` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `status:` | ✅ RESMİ — PATENTS | Patent durumuna göre sınırlar. | `status:grant` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `language:` | ✅ RESMİ — PATENTS | Belge diline göre sınırlar. | `language:english` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `cpc:` | ✅ RESMİ — PATENTS | CPC kodunu ve alt sınıflarını arar. | `cpc:A01B` | [G11](kaynaklar.md#g11) | 2026-08-25 |

### Boolean Mantığı

| Sözdizimi | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|
| `AND` | ✅ RESMİ — PATENTS | Varsayılan Boolean işlemdir; soldan birleşir. | `safety AND belt` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `OR` | ✅ RESMİ — PATENTS | Alternatif terimleri birleştirir. | `camera OR sensor` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `()` | ✅ RESMİ — PATENTS | Patents sorgu dilinde Boolean gruplama sağlar. | `(camera OR sensor) vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `-` | ✅ RESMİ — PATENTS | Bir anahtar kelimeyi, CPC kodunu, buluş sahibini veya patent sahibini olumsuzlar. | `camera -thermal` | [G11](kaynaklar.md#g11) | 2026-08-25 |

Resmî yardım, olumsuzlamayı eksi işaretiyle belgeler. Ayrı bir `NOT` kelimesi açıkça gösterilmediği için burada listelenmez.

### Yakınlık

Yakınlık biçimleri belge getirme kümesini değiştirmez; yalnız yakın eşleşmeleri sıralamada yükseltir.

| Sözdizimi | Sıra | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `NEAR` | Serbest | ✅ RESMİ — PATENTS | İki ifadenin yakınlığını sıralamada güçlendirir. | `camera NEAR vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `NEARx` | Serbest | ✅ RESMİ — PATENTS | En çok `x` kelimelik mesafeyi bitişik sayı biçimiyle belirtir. | `camera NEAR5 vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `NEAR/x` | Serbest | ✅ RESMİ — PATENTS | En çok `x` kelimelik mesafeyi eğik çizgiyle belirtir. | `camera NEAR/5 vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `/xw` | Serbest | ✅ RESMİ — PATENTS | En çok `x` kelimelik mesafe için kısa biçimdir. | `camera /5w vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `WITH` | Serbest | ✅ RESMİ — PATENTS | En çok 20 kelimelik mesafe uygular. | `camera WITH vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `SAME` | Serbest | ✅ RESMİ — PATENTS | En çok 200 kelimelik mesafe uygular. | `camera SAME vehicle` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `AJD` | Sıralı | ✅ RESMİ — PATENTS | `NEAR` ailesine benzer, ancak eşleşme sırasını korur. | `safety AJD belt` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `AJDx` | Sıralı | ✅ RESMİ — PATENTS | Sıralı yakınlığı bitişik sayı biçimiyle belirtir. | `safety AJD5 belt` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `ADJ/x` | Sıralı | ✅ RESMİ — PATENTS | Sıralı yakınlığı eğik çizgiyle belirtir. | `safety ADJ/5 belt` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `+xw` | Sıralı | ✅ RESMİ — PATENTS | Sıralı yakınlık için kısa biçimdir. | `safety +5w belt` | [G11](kaynaklar.md#g11) | 2026-08-25 |

Resmî kaynak aile adlarını `AJD` ve `AJDx`, örnekteki eğik çizgili biçimi ise `ADJ/5` olarak yazar. Bu yazım farkı kaynakta bulunduğu biçimiyle korunmuştur.

### Alan Sözdizimi

| Sözdizimi | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|
| `TI=` | ✅ RESMİ — PATENTS | Yalnız patent başlığında arar. | `TI=(safety belt)` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `AB=` | ✅ RESMİ — PATENTS | Yalnız özette arar. | `AB=(vehicle camera)` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `CL=` | ✅ RESMİ — PATENTS | Yalnız istemlerde arar. | `CL=(image sensor)` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `CPC=` | ✅ RESMİ — PATENTS | CPC alanında tam sınıfı arar; `/low` eki alt sınıfları da kapsar. | `CPC=B60R22/low` | [G11](kaynaklar.md#g11) | 2026-08-25 |

### Wildcard ve Kesme

Bu işaretler yalnız tek kelime üzerinde ve İngilizce kelimelerde çalışır. Patents, en yaygın ilk 25 eşleşmeyi `OR` ile birleştirir; aynı kelimede birden çok wildcard kullanılabilir.

| Sözdizimi | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|
| `?` | ✅ RESMİ — PATENTS | Sıfır veya bir karakter eşleştirir. | `saccharide?` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `*` | ✅ RESMİ — PATENTS | Sıfır veya daha fazla karakter eşleştirir. | `hydroxy*phenyl*` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `$` | ✅ RESMİ — PATENTS | Sıfır veya daha fazla karakter eşleştirir. | `sensor$` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `$x` | ✅ RESMİ — PATENTS | Sıfır ile `x` arasında karakter eşleştirir. | `sensor$3` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `#` | ✅ RESMİ — PATENTS | Tam bir karakter eşleştirir. | `colo#r` | [G11](kaynaklar.md#g11) | 2026-08-25 |

### Kimya Araması

| Sözdizimi | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|
| `SSS=` | ✅ RESMİ — PATENTS | Molekül alt yapısını arar. | `SSS=atrazine` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `~` | ✅ RESMİ — PATENTS | Belirtilen moleküle benzer molekülleri arar. | `~atrazine` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `SMARTS=` | ✅ RESMİ — PATENTS | SMARTS desenini arar. | `SMARTS=CC[O,N]` | [G11](kaynaklar.md#g11) | 2026-08-25 |
| `CL=~...` | ✅ RESMİ — PATENTS | Benzer molekül aramasını patent istemleriyle sınırlar. | `CL=~atrazine` | [G11](kaynaklar.md#g11) | 2026-08-25 |

Patents ayrıca çıplak SMILES ve InChI anahtarı girdilerini kabul eder. Bunlar adlandırılmış kolon operatörleri olmadığı için ayrı operatör olarak listelenmez. Alt yapı ve benzerlik aramaları üst düzey `AND` koşulu başına bir kullanımla sınırlıdır.

## Google Books

Google Books Advanced Book Search aşağıdaki alanları resmî arayüzünde sunar.

| Arayüz alanı | Durum | Türkçe açıklama | Kaynak | Son doğrulama |
|---|---|---|---|---|
| Title | ✅ RESMİ ARAYÜZ ALANI | Kitap başlığına göre arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| Author | ✅ RESMİ ARAYÜZ ALANI | Yazar adına göre arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| Publisher | ✅ RESMİ ARAYÜZ ALANI | Yayıncıya göre arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| Subject | ✅ RESMİ ARAYÜZ ALANI | Konuya göre arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| Publication Date | ✅ RESMİ ARAYÜZ ALANI | Yayın tarihi aralığını sınırlar. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| ISBN | ✅ RESMİ ARAYÜZ ALANI | ISBN ile kitap arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |
| ISSN | ✅ RESMİ ARAYÜZ ALANI | ISSN ile süreli yayın arama alanıdır. | [G12](kaynaklar.md#g12) | 2026-08-25 |

Bu alanlar `intitle:`, `inauthor:`, `inpublisher:`, `subject:`, `isbn:` veya `issn:` biçimlerinin güncel resmî Google Books sorgu operatörü olduğunu kanıtlamaz. Resmî arayüz literal kolonlu sözdizimini göstermediği için bu biçimler eklenmemiştir.

## Google Groups

`author:`, `group:`, `insubject:` ve `msgid:` gibi sözdizimleri tarihsel Google Groups kaynaklarında bulunur; güncel resmî destek bu doğrulama turunda teyit edilememiştir. Güncel yardım yalnız arayüz üzerinden aramayı açıklar. Bu nedenle bu biçimler `✅ RESMİ` olarak işaretlenmez. [G13](kaynaklar.md#g13), [H4](kaynaklar.md#h4)
