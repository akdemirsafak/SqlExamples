## Sql Examples



#### Union - Intersect and Except Examples



##### dvdrental Database





```
actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
```



> (Select first_name from customer)
> UNION
> (Select first_name from actor)



```
actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
```



> (Select first_name from customer)
> Intersect
> (Select first_name from actor)



```
actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
```



> (Select first_name from customer)
> Except
> (Select first_name from actor)





```
İlk 3 sorguyu tekrar eden veriler için de yapalım.
```



> 1. Soru 
>
>    (Select first_name from customer)
>    UNION ALL
>    (Select first_name from actor)
>
> 2. Soru
>
>    ​	(Select first_name from customer)
>    ​	Intersect ALL
>    ​	(Select first_name from actor)
>
> 3. Soru
>
>    (Select first_name from customer)
>    Except
>    (Select first_name from actor)
>
>    

