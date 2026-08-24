# Google Search URL Parametreleri

**Son doğrulama:** 25 Ağustos 2026

> Bu değerler Google dork operatörü değildir. Google Search sonuç URL'sindeki sorgu, arayüz, filtre veya arama dikeyi davranışını değiştirir. `udm`, `tbm`, `tbs` ve bazı temel parametreler kamuya açık sabit bir Google API sözleşmesi değildir; arayüz değiştikçe farklılaşabilir.

Kaynak kodları [Kaynaklar](kaynaklar.md) belgesindeki aynı kodlara gider. Bu belgedeki bütün satırlar, istikrar düzeyinden bağımsız olarak `🔗 URL PARAMETRESİ` etiketiyle gösterilir; belirsizlik açıklama sütununda belirtilir.

## 1. Temel parametreler

| Parametre | Kategori | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `q=` | Sorgu | 🔗 URL PARAMETRESİ | Arama sorgusunu taşır; özel karakterler URL-encode edilmelidir. | `q=open+source` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `hl=` | Arayüz | 🔗 URL PARAMETRESİ | Google arayüz dilini seçer; sonuç dilini tek başına kesin olarak sınırlamaz. | `hl=tr` | [B1](kaynaklar.md#b1), [G7](kaynaklar.md#g7) | 2026-08-25 |
| `gl=` | Ülke bağlamı | 🔗 URL PARAMETRESİ | Aramanın ülke/market bağlamını etkiler. | `gl=tr` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `lr=` | İçerik dili | 🔗 URL PARAMETRESİ | Sonuçları belirtilen içerik dili veya dilleriyle sınırlar. | `lr=lang_tr` | [B1](kaynaklar.md#b1), [G7](kaynaklar.md#g7) | 2026-08-25 |
| `cr=` | Ülke kısıtı | 🔗 URL PARAMETRESİ | Sonuçları ülke bağlamına göre kısıtlar; `gl` ile aynı işlev değildir. | `cr=countryTR` | [B1](kaynaklar.md#b1), [G7](kaynaklar.md#g7) | 2026-08-25 |
| `start=` | Sayfalama | 🔗 URL PARAMETRESİ | Sonuç ofsetini belirtir; güncel arayüzde tipik adım 10'dur. | `start=10` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `safe=` | İçerik filtresi | 🔗 URL PARAMETRESİ | SafeSearch davranışını etkiler. Kullanıcı/hesap politikası URL değerinin önüne geçebilir. | `safe=active` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `filter=` | Sonuç kümesi | 🔗 URL PARAMETRESİ | Benzer veya tekrarlı sonuçların kümelenmesini etkiler. | `filter=0` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `pws=` | Kişiselleştirme | 🔗 URL PARAMETRESİ | `pws=0`, kişiselleştirme etkisini azaltmak için yaygın kullanılır; tam tarafsızlık garantisi değildir. | `pws=0` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `nfpr=` | Sorgu düzeltme | 🔗 URL PARAMETRESİ | `nfpr=1`, otomatik yazım düzeltmesini bastırmayı amaçlar. | `nfpr=1` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=` | Arama araçları | 🔗 URL PARAMETRESİ | Zaman, sıralama ve verbatim gibi filtreleri taşır; alt değerleri tersine mühendislikle belgelenir. | `tbs=qdr:d` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbm=` | Eski arama dikeyi seçimi | 🔗 URL PARAMETRESİ | Görsel, haber, video, alışveriş ve kitap gibi arama dikeylerini seçer; `udm` ile kısmen örtüşür. | `tbm=nws` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `udm=` | İçerik modu | 🔗 URL PARAMETRESİ | Yeni sonuç modlarını seçer. Google sabit bir resmî değer tablosu yayımlamaz; değerler gözlemseldir. | `udm=14` | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `uule=` | Hassas konum | 🔗 URL PARAMETRESİ | Şehir düzeyinde konum bağlamı için kodlanmış değer taşır; elle üretimi karmaşıktır. | `uule=<kodlanmış-konum>` | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `num=` | Eski sonuç sayısı | 🔗 URL PARAMETRESİ | Eskiden sayfa başına sonuç sayısını seçerdi. 2025 sonundan beri güncel testlerde yok sayıldığı raporlanır. | `num=100` | [B1](kaynaklar.md#b1) | 2026-08-25 |

## 2. Google Advanced Search form parametreleri

Bu adlar Google'ın güncel Advanced Search formunun HTML alanlarında doğrudan görülür. Arayüz girdileridir; sorgu kutusuna yazılan operatörler değildir.

| Parametre | Kategori | Durum | Türkçe açıklama | Güvenli örnek | Kaynak | Son doğrulama |
|---|---|---|---|---|---|---|
| `as_q=` | Gelişmiş sorgu | 🔗 URL PARAMETRESİ | Tüm kelimeler alanı. | `as_q=open+source` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_epq=` | Gelişmiş sorgu | 🔗 URL PARAMETRESİ | Tam ifade alanı. | `as_epq=annual+report` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_oq=` | Gelişmiş sorgu | 🔗 URL PARAMETRESİ | Kelimelerden herhangi biri alanı. | `as_oq=python+rust` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_eq=` | Gelişmiş sorgu | 🔗 URL PARAMETRESİ | Hariç tutulacak kelimeler alanı. | `as_eq=draft` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_nlo=` / `as_nhi=` | Sayısal aralık | 🔗 URL PARAMETRESİ | Alt ve üst sayısal sınır alanları. | `as_nlo=100&as_nhi=500` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_sitesearch=` | Site/domain | 🔗 URL PARAMETRESİ | Gelişmiş aramadaki site veya domain alanı. | `as_sitesearch=example.com` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_filetype=` | Dosya türü | 🔗 URL PARAMETRESİ | Gelişmiş aramadaki dosya türü alanı. | `as_filetype=pdf` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_occt=` | Terimin konumu | 🔗 URL PARAMETRESİ | Terimin sayfa, başlık, metin, URL veya bağlantı konumunu seçen alan. | `as_occt=title` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_qdr=` | Son güncelleme | 🔗 URL PARAMETRESİ | Advanced Search formundaki göreli zaman alanı. | `as_qdr=w` | [G7](kaynaklar.md#g7) | 2026-08-25 |
| `as_rights=` | Kullanım hakları | 🔗 URL PARAMETRESİ | Lisans/kullanım hakları filtresini taşır. Sonucun gerçek lisansını kaynak sitede ayrıca doğrulayın. | `as_rights=<form-değeri>` | [G7](kaynaklar.md#g7) | 2026-08-25 |

## 3. `tbs` alt değerleri

| Değer | Gözlemlenen işlev | Kaynak | Son doğrulama |
|---|---|---|---|
| `tbs=qdr:h` | Son saat | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=qdr:d` | Son 24 saat | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=qdr:w` | Son hafta | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=qdr:m` | Son ay | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=qdr:y` | Son yıl | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=cdr:1,cd_min:MM/DD/YYYY,cd_max:MM/DD/YYYY` | Özel tarih aralığı | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=sbd:1` | Tarihe göre sıralama | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbs=li:1` | Verbatim/literal sonuç modu | [B1](kaynaklar.md#b1) | 2026-08-25 |

## 4. `udm` modları

`udm` için Google tarafından yayımlanmış sabit ve eksiksiz bir kullanıcı dokümanı yoktur. Aşağıdaki değerler güncel üçüncü taraf canlı testlerinden gelir ve bölgeye göre değişebilir.

| Değer | Gözlemlenen mod | Güven notu | Kaynak | Son doğrulama |
|---|---|---|---|---|
| `udm=2` | Görseller | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=7` | Videolar | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=12` | Haberler | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=14` | Web / klasik bağlantılar | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=18` | Forumlar | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=28` | Alışveriş | Yaygın gözlem | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=36` | Kitaplar | Değişebilir | [B1](kaynaklar.md#b1), [B2](kaynaklar.md#b2) | 2026-08-25 |
| `udm=39` | Kısa videolar | Bölgeye göre değişebilir | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `udm=50` | AI Mode | Erişim/hesap/bölgeye göre değişebilir | [B1](kaynaklar.md#b1) | 2026-08-25 |

SerpApi ayrıca çok sayıda ülkeye özgü `udm` değeri raporlar; geniş ve tam doğrulanmamış listeyi burada sabit bir sözleşme gibi tekrar etmiyoruz.

## 5. `tbm` örnekleri

| Değer | Arama dikeyi | Kaynak | Son doğrulama |
|---|---|---|---|
| `tbm=isch` | Görseller | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbm=nws` | Haberler | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbm=vid` | Videolar | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbm=shop` | Alışveriş | [B1](kaynaklar.md#b1) | 2026-08-25 |
| `tbm=bks` | Kitaplar | [B1](kaynaklar.md#b1) | 2026-08-25 |

Google arayüzü `udm` tabanlı URL'ler de kullandığı için `tbm` değerleri uzun vadeli bir API sözleşmesi olarak görülmemelidir.

## 6. Operatör ile parametreyi birlikte kullanma

```text
https://www.google.com/search?q=site%3Aexample.com+filetype%3Apdf&pws=0&udm=14
```

Burada:

- `site:` ve `filetype:` sorgu operatörüdür.
- `q=`, `pws=` ve `udm=` URL parametresidir.

İç parametreler (`ei`, `ved`, `sxsrf`, `oq`, `gs_lp` gibi) oturum/telemetri amaçlı olabilir ve sonuçları denetlemek için kullanıcı parametresi olarak önerilmez.
