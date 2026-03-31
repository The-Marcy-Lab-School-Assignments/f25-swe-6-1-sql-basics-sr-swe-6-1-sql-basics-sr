# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

--- A database is a structured system used to store, organize, and manage data efficiently. We use a database instead of a JavaScript array because databases can handle large amounts of data, persist data even after the server restarts, and allow multiple users or processes to access the data safely at the same time. Databases also provide powerful query tools (like SQL) to search, filter, and manipulate data more efficiently than in-memory arrays. In contrast, arrays stored on a server are temporary and not suitable for long-term or scalable data storage.

## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

---A primary key is a unique identifier for each row in a table, usually a column like id. It ensures that every record can be uniquely identified and accessed without confusion. Every table needs a primary key so that each row can be reliably referenced, updated, or deleted. Without a primary key, it would be difficult to distinguish between duplicate or similar records. It also helps establish relationships between tables using foreign keys

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

**Your answer:**

---This query retrieves up to five fiction books from the database, ordered by the most recent publication year first.

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

---Running DELETE FROM books without a WHERE clause is dangerous because it removes all rows from the table. Without a condition, the database has no way to filter which records to delete, so every book entry will be permanently erased. This can lead to complete data loss if used unintentionally. It is important to always include a WHERE clause to specify exactly which records should be deleted. Otherwise, the operation affects the entire table.

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
ORDER BY is used to sort the results based on a column, while LIMIT is used to restrict the number of rows returned. You can use ORDER BY without LIMIT if you just want sorted results without limiting how many are returned. For example, SELECT * FROM books ORDER BY year DESC; will sort all books by year. You can also use LIMIT without ORDER BY, but the results will not be in any specific order, such as SELECT * FROM books LIMIT 5;, which returns any 5 rows from the table.