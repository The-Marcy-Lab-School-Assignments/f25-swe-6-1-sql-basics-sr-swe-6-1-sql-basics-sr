# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

A database is a persistant method of storing data, meaning they are unaffected by a server shut down, this is important because compared to this, an array lives on the RAM, which holds temporary data and when your computer shuts down that data is also disrupted and starts anew once you load the application up again.

## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

A primary key is a unique identifier for a key, for example in the example below, the primary key for this table could be book_id as each book should be uniquely idenitfiable.

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: _"It returns the 5 most recently published fiction books."_

**Your answer:**

This query selects fiction books and returns the the first 5 results based on the year in descending order, so the most recently published books.

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

Its dangerous to run without a `WHERE` because `DELETE FROM books` will just remove every row from the table if you dont specify what you want to remove with `WHERE`

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
The difference between `ORDER BY` and `LIMIT` is that `ORDER BY` is a clause that sorts the results meanwhile `LIMIT` caps the number of results. They are completely independent of eachother and can be used to return different results. For example if I wanted to see the top movies from a movie database I would use `SELECT * FROM movies ORDER BY rating DESC` but if i just wanted to see the first three results i could just do `SELECT * FROM movies LIMIT 3`
