# Kaynaklar

**Son doğrulama:** 25 Ağustos 2026

## Kaynak politikası

Durum değerlendirmelerinde şu sıra kullanılır:

1. Güncel Google Search Help ve Search Central belgeleri
2. Google Search Central değişiklik kayıtları
3. Güncel resmî Google arayüzleri
4. Güncel ve tekrarlanabilir davranış
5. Güvenilir teknik kaynaklar
6. Tarihsel listeler ve topluluk referansları

Bir sorgunun sonuç üretmesi, içindeki noktalamanın veya kolonlu ifadenin özel bir operatör olarak işlendiğini tek başına kanıtlamaz. Eski veya üçüncü taraf bir kaynak güncel Google belgesiyle çelişirse Google kaynağı esas alınır.

## Resmî Google kaynakları

<a id="g1"></a>
### G1 — Google Search Help: Refine Google searches

<https://support.google.com/websearch/answer/2466433?hl=en>

`"..."`, `site:`, `-`, `before:`, `after:` ve `filetype:` sözdizimlerini açıkça gösterir.

<a id="g2"></a>
### G2 — Google Search Central: Debugging with Google Search operators

<https://developers.google.com/search/docs/monitor-debug/search-operators>

`filetype:`, `imagesize:`, `site:` ve `src:` için güncel resmî genel bakış tablosudur. `site:` ve Google Görseller operatörlerinin ayrıntıları için G7 ve G9 birincil kaynak olarak kullanılır. Sayfa 10 Aralık 2025 tarihinde güncellenmiştir.

<a id="g3"></a>
### G3 — Google Search Central: Latest documentation updates

<https://developers.google.com/search/updates>

İlgili değişiklik kayıtları:

- 18 Temmuz 2023: `related:` artık desteklenmediği için operatör belgesinden kaldırıldı.
- 24 Eylül 2024: `cache:` artık Google Search'te çalışmadığı için operatör belgesi kaldırıldı.

<a id="g4"></a>
### G4 — Google Advanced Search

<https://www.google.com/advanced_search?hl=en>

Tam ifade ve hariç tutmanın yanında, arayüz yardım metninde literal `OR` ile `10..35` sözdizimlerini gösterir. Formda site veya alan adı, terimin konumu ve dosya türü seçenekleri bulunur. HTML alan adları arasında `as_q`, `as_epq`, `as_oq`, `as_eq`, `as_nlo`, `as_nhi`, `lr`, `cr`, `as_qdr`, `as_sitesearch`, `as_occt`, `as_filetype`, `as_rights` ve `tbs` yer alır; bunlar sorgu operatörü değil URL veya form parametresidir.

<a id="g5"></a>
### G5 — Google Search Help: Learn search tips and how results relate to your search

<https://support.google.com/websearch/answer/134479?hl=en>

`site:` ile site aramayı, `-site:` ile site hariç tutmayı, `define <terim>` tanım sorgusunu, `weather <yer>` hava durumu sorgusunu ve hesaplama/dönüşüm gibi doğal sorgu kalıplarını gösterir. Bunların bir kısmı kolonlu operatör değil Search özelliğini tetikleyen sorgu kalıbıdır.

<a id="g6"></a>
### G6 — Google Search Help: Manage calculator, unit converter and color codes

<https://support.google.com/websearch/answer/3284611?hl=en>

Arama kutusunda birim ve para dönüşümü yapılabildiğini belgeler. `in` kelimesini bir alan filtresi olarak tanımlamaz; bu nedenle ilgili kullanım operatör değil sorgu kalıbı olarak sınıflandırılır.

<a id="g7"></a>
### G7 — Google Search Central: `site:` operator documentation

<https://developers.google.com/search/docs/monitor-debug/search-operators/all-search-site>

`site:` kapsamının alan adı, URL ve URL öneki biçimlerini açıklar. `site:example.com` sorgusunun `www.example.com` ve `recipes.example.com` gibi alt alan adlarını kapsayabildiğini; sonuçların indekslenmiş URL'lerin eksiksiz listesi olmadığını belirtir.

<a id="g8"></a>
### G8 — Google Search Central: File types indexable by Google

<https://developers.google.com/search/docs/crawling-indexing/indexable-file-types>

3 Şubat 2026 güncellemeli resmî liste, `filetype:` davranışını ve indekslenebilen içerik türlerini açıklar. CSV desteklenen türler arasındadır; MP3 desteklenen medya listesinde bulunmaz.

<a id="g9"></a>
### G9 — Google Search Central: Google Images search operators

<https://developers.google.com/search/docs/monitor-debug/search-operators/image-search>

`imagesize:` ve `src:` sözdizimlerini yalnızca Google Görseller kapsamı için açıkça belgeler.

<a id="g10"></a>
### G10 — Google Scholar Search Help

<https://scholar.google.com/intl/us/scholar/help.html>

Google Scholar ürününe özgü `author:`, tam başlık tırnağı ve `site:` örneklerini gösterir. Advanced Search yüzeyindeki yazar, başlık, yayın ve tarih alanlarını da açıklar. Bu kanıtlar genel Google Web Search operatörleri için kullanılmaz.

<a id="g11"></a>
### G11 — Google Patents Search Help

<https://support.google.com/faqs/answer/7049475?hl=en>

Google Patents ürününe özgü metadata kısıtlarını, Boolean ve yakınlık sözdizimlerini, alan öneklerini, wildcard sınırlamalarını ve kimya aramasını belgeler. Patents desteği genel Google Web Search desteği anlamına gelmez.

<a id="g12"></a>
### G12 — Google Books Advanced Book Search

<https://books.google.com/advanced_book_search>

Google Books arayüzündeki başlık, yazar, yayıncı, konu, yayın tarihi, ISBN ve ISSN alanlarını gösterir. Arayüz alanlarının varlığı aynı adlarla kolonlu sorgu operatörü desteğinin kanıtı değildir.

<a id="g13"></a>
### G13 — Google Groups Help: Find and join a group

<https://support.google.com/groups/answer/1067205?hl=en>

Güncel Google Groups'ta grup adı, e-posta adresi veya konu ile arama arayüzünü açıklar; `author:`, `group:`, `insubject:` veya `msgid:` için güncel resmî sözdizimi kanıtı sunmaz. Bu nedenle tarihsel Groups biçimleri aktif veya resmî olarak sınıflandırılmaz.

## Teknik çapraz kontroller

<a id="d1"></a>
### D1 — Daniel M. Russell: Google Advanced Search Operators

<https://docs.google.com/document/d/1ydVaJJeL1EYbWtlfj9TPfBTE5IBADkQfZrQaBZxqXGs/edit>

8 Şubat 2024 tarihli kapsamlı referans; `allin...` ve `in...` aileleri, wildcard, parantezsiz `AROUND n` yakınlık yazımı, sayı aralığı, `OR`, `define` ve `site:` kapsam biçimlerini karşılaştırmak için kullanılır. Parantez davranışı konusunda T3 ile çeliştiğinden kesin hüküm için kullanılmaz. Belgedeki CSV notu daha güncel G8 kaynağıyla çeliştiği için benimsenmez.

<a id="t1"></a>
### T1 — Lawrence Hitches: Google Search Operators Cheatsheet

<https://www.lawrencehitches.com/google-search-operators-cheatsheet/>

25 Haziran 2026 güncellemeli teknik referans; `intitle:`, `allintitle:`, `inurl:`, `allinurl:`, `intext:`, `allintext:`, `ext:`, wildcard, `AROUND(X)` ve tarihsel operatörleri çapraz kontrol etmek için kullanılır. `related:` değerlendirmesi daha yeni G3 kaydıyla çeliştiği için benimsenmez.

<a id="t2"></a>
### T2 — Ahrefs: Google Search Operators — The Complete List

<https://ahrefs.com/blog/google-advanced-search-operators/>

25 Nisan 2023 tarihli geniş operatör matrisi; Web, News ve tarihsel operatör ailelerinin kapsam kontrolü için kullanılır. `cache:` ve `related:` değerlendirmeleri daha yeni G3 kayıtları karşısında yalnızca tarihsel değer taşır.

<a id="t3"></a>
### T3 — Moz: Google Search Operators Cheat Sheet

<https://moz.com/learn/seo/search-operators>

Güncel teknik çapraz kontrol kaynağı; `AROUND(X)` yazımını ve parantezleri gruplama aracı olarak listeler. Parantez iddiası D1 ile çeliştiği ve Google'ın güncel resmî Web Search belgelerinde doğrulanmadığı için güvenilir Boolean öncelik kanıtı sayılmaz. Kaldırılmış operatörlerde resmî G3 değişiklik kayıtları üstündür.

## URL parametresi kaynakları

<a id="b1"></a>
### B1 — Bright Data: Google Search URL Parameters and Operators

<https://brightdata.com/blog/web-data/google-search-url-parameters>

2026 tarihli URL parametresi referansı; `q`, `hl`, `gl`, `lr`, `cr`, `start`, `safe`, `filter`, `pws`, `nfpr`, `tbs`, `tbm`, `udm`, `uule` ve `num` davranışlarını karşılaştırmak için kullanılır. Resmî veya sabit bir Google API sözleşmesi değildir.

<a id="b2"></a>
### B2 — SerpApi: Every Google `udm` in the world

<https://serpapi.com/blog/every-google-udm-in-the-world/>

13 Haziran 2024 tarihli tersine mühendislik referansı; yaygın `udm` değerlerini çapraz kontrol etmek için kullanılır. Değerler bölgeye ve arayüze göre değişebilir.

## Tarihsel kaldırılma kaynakları

<a id="h1"></a>
### H1 — Official Google Search Blog: Search using your terms, verbatim

<https://search.googleblog.com/2011/11/search-using-your-terms-verbatim.html>

Google'ın `+` operatörünü 2011'de kaldırdığını ve çift tırnak kullanımını önerdiğini belirtir.

<a id="h2"></a>
### H2 — Search Engine Land: Google Drops Phonebook Search Operator

<https://searchengineland.com/google-drops-phonebook-search-operator-56173>

16 Kasım 2010 tarihli haber, Google çalışanı John Mueller'ın `phonebook:` ve `rphonebook:` kaldırılmasına ilişkin teyidini aktarır.

<a id="h3"></a>
### H3 — SearchReSearch: What happened to the tilde operator?

<https://searchresearch1.blogspot.com/2013/07/what-happened-to-tilde-operator.html>

Daniel M. Russell'ın 2 Temmuz 2013 tarihli açıklaması, `~` operatörünün kaldırıldığını ve bunun nedenlerini doğrudan açıklar.

<a id="h4"></a>
### H4 — SANS: Google Hacking and Defense Cheat Sheet

<https://www.sans.org/posters/google-hacking-and-defense-cheat-sheet>

Eski Google arama yüzeylerindeki `bphonebook:` ve Google Groups biçimlerini tarihsel kapsam karşılaştırması için gösteren cheat sheet'tir. Güncel operatör desteği veya kaldırılma tarihi için tek başına otorite kabul edilmez.
