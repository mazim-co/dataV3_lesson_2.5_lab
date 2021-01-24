-- 1. Select all the actors with the first name ‘Scarlett’.
select first_name as 'First Name', last_name from sakila.actor
where first_name = 'Scarlett';

-- 2. How many films (movies) are available for rent and how many films have been rented?
select count(*) from sakila.rental;

-- 3. What are the shortest and longest movie duration? Name the values max_duration and min_duration.
select max(length) as 'maximum length', min(length) from sakila.film;
select floor(avg(length)) as 'avg duration' from sakila.film;

-- 4. What's the average movie duration expressed in format (hours, minutes)?
select floor(avg(length)) / 60 as 'avg duration', round(avg(length) % 60) as 'minutes' from sakila.film;

-- 5. How many distinct (different) actors' last names are there?
select sum(isnull(`last_name`)) from sakila.actor;

-- 6. Since how many days has the company been operating (check DATEDIFF() function)?

-- 7. Show rental info with additional columns month and weekday. Get 20 results.

-- 8. Add an additional column day_type with values 'weekend' and 'workday' depending on the rental day of the week.

-- 9. How many rentals were in the last month of activity?

