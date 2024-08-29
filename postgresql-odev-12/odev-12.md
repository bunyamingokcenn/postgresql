Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

    ```sql
        SELECT COUNT(length) FROM film 
        WHERE length > ANY 
        (
	        SELECT ROUND(AVG(length)) FROM film 
        );	

    ```

2. film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

    ```sql 
        SELECT COUNT(rental_rate) FROM film
        WHERE rental_rate = ANY 
        (
	        SELECT MAX(rental_rate) FROM film	        
        );


        
    ```

3. film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

    ```sql 
        SELECT * FROM film
        WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) 
        AND replacement_cost = (SELECT MIN(replacement_cost) FROM film);


    ```

4. payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

    ```sql 
        SELECT payment.customer_id, customer.first_name, customer.last_name,  COUNT(payment.amount) AS total_amount
        FROM payment
        INNER JOIN customer ON customer.customer_id = payment.customer_id
        GROUP BY payment.customer_id, customer.first_name, customer.last_name
        ORDER BY total_amount DESC
        LIMIT 1;

    ```
