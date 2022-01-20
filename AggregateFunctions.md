## Sql Examples



#### Aggregate Functions Examples



##### dvdrental Database





```
film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
```



> Select AVG(rental_rate) from film;



```
film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
```



> Select Count(*) from film Where title Like 'C%';



```
film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
```



> Select Max(film.length) from film Where rental_rate=0.99;



```
film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
```



> Select Count(replacement_cost) from film Where film.length>150