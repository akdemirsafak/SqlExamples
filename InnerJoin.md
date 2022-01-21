## Sql Examples



####  Inner Join Examples



##### dvdrental Database







```
 city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```



> Select city,country from city Inner Join country ON city.country_id=country.country_id;



```
customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```



> Select customer.first_name ||' '|| customer.last_name As FullName from customer Inner Join payment On customer.customer_id=payment.customer_id;



```
customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
```



> Select customer.first_name ||' '|| customer.last_name As FullName from customer Inner Join rental On customer.customer_id=rental.customer_id;