## Sql Examples



#### OrderBy - Limit and Offset Examples



##### dvdrental Database





```
film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
```



> Select * from film Where title Like '%n' Order By length(title) DESC LIMIT 5;



```
film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
```



> Select * from film Where title Like '%n' Order By length(title) Offset 5 Limit 5;



```
customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
```



> Select * from customer Where store_id=1 Order By last_name ASC Limit 4;