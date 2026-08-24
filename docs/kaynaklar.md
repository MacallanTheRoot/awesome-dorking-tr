# Kaynaklar

**Son doğrulama:** 25 Ağustos 2026

## Kaynak politikası

Durum değerlendirmelerinde şu sıra kullanılır:

1. Güncel Google Search Help ve Search Central belgeleri
2. Google Search Central değişiklik kayıtları
3. Güncel ve tekrarlanabilir davranış
4. Güvenilir teknik kaynaklar
5. Tarihsel listeler ve topluluk referansları

Bir sorgunun sonuç üretmesi, içindeki noktalamanın veya kolonlu ifadenin özel bir operatör olarak işlendiğini tek başına kanıtlamaz. Eski veya üçüncü taraf bir kaynak güncel Google belgesiyle çelişirse Google kaynağı esas alınır.

## Resmî Google kaynakları

<a id="g1"></a>
### G1 — Google Search Help: Refine Google searches

<https://support.google.com/websearch/answer/2466433?hl=en>

`"..."`, `site:`, `-`, `before:`, `after:` ve `filetype:` sözdizimlerini açıkça gösterir.

<a id="g2"></a>
### G2 — Google Search Central: Debugging with Google Search operators

<https://developers.google.com/search/docs/monitor-debug/search-operators>

`filetype:`, `imagesize:`, `site:` ve `src:` için güncel resmî tablodur. Sayfa 10 Aralık 2025 tarihinde güncellenmiştir.

<a id="g3"></a>
### G3 — Google Search Central: Latest documentation updates

<https://developers.google.com/search/updates>

İlgili değişiklik kayıtları:

- 18 Temmuz 2023: `related:` artık desteklenmediği için operatör belgesinden kaldırıldı.
- 24 Eylül 2024: `cache:` artık Google Search'te çalışmadığı için operatör belgesi kaldırıldı.

<a id="g4"></a>
### G4 — Google Advanced Search

<https://www.google.com/advanced_search?hl=en>

Tam ifade, hariç tutma, `OR`, `..` sayısal aralığı, site veya alan adı, terimin konumu ve dosya türü seçeneklerini gösterir.

<a id="g5"></a>
### G5 — Google Search Help: Learn search tips and how results relate to your search

<https://support.google.com/websearch/answer/134479?hl=en>

`site:` ile site aramayı ve `-site:` ile site hariç tutmayı gösterir.

<a id="g6"></a>
### G6 — Google Search Help: Manage calculator, unit converter and color codes

<https://support.google.com/websearch/answer/3284611?hl=en>

Arama kutusunda birim ve para dönüşümü yapılabildiğini belgeler. `in` kelimesini bir alan filtresi olarak tanımlamaz; bu nedenle ilgili kullanım operatör değil sorgu kalıbı olarak sınıflandırılır.

<a id="g7"></a>
### G7 — Google Advanced Search formu

<https://www.google.com/advanced_search?hl=en>

Form alanlarında `as_q`, `as_epq`, `as_oq`, `as_eq`, `as_nlo`, `as_nhi`, `lr`, `cr`, `as_qdr`, `as_sitesearch`, `as_occt`, `as_filetype`, `as_rights` ve `tbs` adları bulunur. Bunlar sorgu operatörü değil URL veya form parametresidir.

<a id="g8"></a>
### G8 — Google Search Central: File types indexable by Google

<https://developers.google.com/search/docs/crawling-indexing/indexable-file-types>

3 Şubat 2026 güncellemeli resmî liste, `filetype:` davranışını ve indekslenebilen içerik türlerini açıklar. CSV desteklenen türler arasındadır; MP3 desteklenen medya listesinde bulunmaz.

## Teknik çapraz kontroller

<a id="d1"></a>
### D1 — Daniel M. Russell: Google Advanced Search Operators

<https://docs.google.com/document/d/1ydVaJJeL1EYbWtlfj9TPfBTE5IBADkQfZrQaBZxqXGs/edit>

8 Şubat 2024 tarihli kapsamlı referans; `allin...` ve `in...` aileleri, wildcard, yakınlık, sayı aralığı, `OR`, `define`, `site:` kapsam biçimleri ve parantezlerin gruplama yapmadığı notu için kullanılır. Belgedeki CSV notu daha güncel G8 kaynağıyla çeliştiği için benimsenmez.

<a id="t1"></a>
### T1 — Lawrence Hitches: Google Search Operators Cheatsheet

<https://www.lawrencehitches.com/google-search-operators-cheatsheet/>

25 Haziran 2026 güncellemeli teknik referans; `intitle:`, `allintitle:`, `inurl:`, `allinurl:`, `intext:`, `allintext:`, `ext:`, wildcard, `AROUND(X)` ve tarihsel operatörleri çapraz kontrol etmek için kullanılır. `related:` değerlendirmesi daha yeni G3 kaydıyla çeliştiği için benimsenmez.

<a id="t2"></a>
### T2 — Ahrefs: Google Search Operators — The Complete List

<https://ahrefs.com/blog/google-advanced-search-operators/>

25 Nisan 2023 tarihli geniş operatör matrisi; Web, News ve tarihsel operatör ailelerinin kapsam kontrolü için kullanılır. `cache:` ve `related:` değerlendirmeleri daha yeni G3 kayıtları karşısında yalnızca tarihsel değer taşır.

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

16 Kasım 2010 tarihli haber, Google çalışanı John Mueller'ın kaldırılma teyidini aktarır.

<a id="h3"></a>
### H3 — SearchReSearch: What happened to the tilde operator?

<https://searchresearch1.blogspot.com/2013/07/what-happened-to-tilde-operator.html>

Daniel M. Russell'ın 2 Temmuz 2013 tarihli açıklaması, `~` operatörünün kaldırıldığını ve bunun nedenlerini doğrudan açıklar.
