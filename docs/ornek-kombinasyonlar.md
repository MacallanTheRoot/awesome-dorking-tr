# Örnek Google Dorking Kombinasyonları

**Son doğrulama:** 25 Ağustos 2026

Bu örnekler [ana listedeki](../README.md) operatörlerin genel araştırma senaryolarında nasıl birleştirilebileceğini gösterir. Yer tutucuları kendi araştırma kapsamınıza göre değiştirin.

## Genel araştırma

```text
"araştırma konusu"
"araştırma konusu" OR "alternatif terim"
"araştırma konusu" -"ilgisiz bağlam"
"araştırma konusu" after:2025-01-01
```

## Alan adı araştırması ve site içi arama

```text
site:example.com "yıllık rapor"
site:example.com/docs/ "kullanım kılavuzu"
site:example.com inurl:blog "araştırma konusu"
"araştırma konusu" -site:example.com
```

`site:` sonuçları eksiksiz bir indeks veya varlık envanteri değildir.

## Doküman ve dosya arama

```text
site:example.com filetype:pdf "faaliyet raporu"
site:example.edu filetype:pptx "ders notları"
site:example.org filetype:csv "açık veri"
intitle:"yıllık rapor" filetype:pdf
```

Yalnızca kamuya açık ve kullanım yetkiniz bulunan içeriklerle çalışın.

## Akademik araştırma

```text
site:.edu "araştırma konusu" filetype:pdf
site:.edu.tr "araştırma konusu" filetype:pdf
"araştırma konusu" "literature review"
"araştırma konusu" after:2024-01-01
```

Google Scholar'a özgü operatörler genel Web Search envanterinin parçası değildir.

## Tarih filtreleme

```text
"araştırma konusu" before:2020-01-01
"araştırma konusu" after:2024-01-01
"araştırma konusu" after:2022-01-01 before:2024-01-01
```

Tarih operatörleri sayfanın kesin ilk yayın tarihini değil, Google'ın yorumladığı güncelleme tarihini kullanır.

## Başlık, URL ve metin daraltma

```text
intitle:"araştırma konusu"
inurl:research "araştırma konusu"
intext:"araştırma konusu" site:example.com
site:example.com intitle:"faaliyet raporu" filetype:pdf
```

## OSINT araştırması

```text
"kuruluş adı" "şehir"
"proje adı" "kuruluş adı" after:2024-01-01
site:example.org "kuruluş adı"
"kamuya açık kullanıcı adı" site:github.com
```

Kişi odaklı araştırmalarda yalnızca açık, meşru bir amaç için gerekli ve hukuka uygun verileri kullanın. Hassas bilgi, kimlik bilgisi veya yetkisiz erişim hedefleyen sorgular bu referansın kapsamı dışındadır.

## Google Görseller

```text
"kamusal alan eser" imagesize:1200x800
src:https://example.com/images/logo.png
```

`imagesize:` ve `src:` yalnızca Google Görseller bağlamında belgelenir.

## Sayısal aralık ve dönüşüm

```text
fotoğraf makinesi 3000..5000 TL
kitap €30..€50
10 km in miles
```

`in` bir alan operatörü değil, dönüştürücü özelliğini tetikleyen doğal dil kalıbıdır.
