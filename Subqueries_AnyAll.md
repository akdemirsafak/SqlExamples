## Sql Examples

#### SubQueries - Any and All Operators Examples

##### dvdrental Database



` film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?`

> Select Count(*) from film Where (
> 	(
> 		Select AVG(film.length) from film 
> 	)
> )>film.length

` film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?`

> Select Count(*) from film 
> Where rental_rate=(Select MAX(rental_rate) from film);

` film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.`

> Select title,replacement_cost,rental_rate from film 
> Where rental_rate=(Select MIN(rental_rate) from film )
> AND replacement_cost=(Select MIN(replacement_cost) from film );



` payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.`

> Select * from customer INNER JOIN payment ON customer.customer_id=payment.customer_id
> Where amount=(Select MAX(amount) from payment)
