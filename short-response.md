# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

A database is an organized system for storing, managing and retrieving data. Databases are used instead of a JavaScript array because databases are designed to handle large amount of data. JavaScript arrays only exist in memory and are lost when the server stops running. However, in databases the data persists even when the server restarts. Databases can also be used to filter, sort and index data which are difficult to manage manually in code. 

---

## Question 2

What is a primary key? Why does every table need one?

A primary key is a unique identifier for each row in a table. It ensures that every record can be distinguished from others. Every table needs a primary key so that the data can be reliably accessed, updated or deleted. Without primary key, it would be difficult to target a specific row, especially if multiple rows have similar data. 

---

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

It returns the five most published books in the fiction genre.

---

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

Running `DELETE FROM books` without a `WHERE` clause is dangerous because it removes every row in the table. It does not filter or limit the deletion but deletes all records in `books`. This can result in permanent data loss if there is not backup. Developers typically use a `WHERE` clause to specify which rows should be deleted.

---

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

`ORDER BY` is used to sort the results of a query based on one or more columns, while `LIMIT` is used to restrict the number of rows returned. It is possible to use one without the other. For example, `ORDER BY year DESC` can be used to sort all books from newest to oldest without limiting the number of results. On the other hand, `LIMIT 10` can be used to return the first 10 rows. However, they are used together in order to get a specific subset of stored data.
