## Sql Examples

#### Like(case sensitive) - ILike(not case sensitive) Examples

##### dvdrental Database



` country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.`

> Select * from country Where country LIKE 'A%a'

` country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.`

> Select * from country Where country LIKE '%_____n'

` film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.`

>  Select * from film Where title ILike '%T%T%T%T%'

` film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.`

> Select * from film Where  length(title)>90 AND rental_rate=2.99 AND title LIKE 'C%' 
> (Böyle bir data yok.)



