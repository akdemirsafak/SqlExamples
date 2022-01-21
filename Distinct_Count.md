## Sql Examples

#### Distinct - Count Examples

##### dvdrental Database



` film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız..`

> Select DISTINCT replacement_cost from film

` film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?`

> Select DISTINCT replacement_cost,Count(*) from film Group By replacement_cost

`film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?`

> Select Count(*) from film Where title Like 'T%' AND rating='G'

`country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?`

> Select Count(*) from country Where Length(country)=5

`city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?`

> Select Count(*) from city Where city ILike '%r'