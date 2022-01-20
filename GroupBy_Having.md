## Sql Examples



#### Group By - Having Examples



##### dvdrental Database





```
film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
```



> Select rating from film Group By rating;



```
film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
```



> Select replacement_cost,Count(*) from film Group By replacement_cost
> Having Count(*)>50



```
customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
```



> Select store_id,Count(*) from customer Group By store_id



```
city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
```



> Select country_id, Count(*) from city Group By country_id Order By Count(*) Desc Limit 1 



