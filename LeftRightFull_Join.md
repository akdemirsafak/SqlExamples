## Sql Examples



#### Left Join - Right Join - Full Join Examples



##### dvdrental Database





```
city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
```



> Select city,country from city Left JOIN country ON city.country_id=country.country_id



```
customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
```



> Select first_name,last_name from customer Right Join payment On customer.customer_id=payment.customer_id



```
customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
```



> Select first_name,last_name from customer Full Join rental On customer.customer_id=rental.customer_id

