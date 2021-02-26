# TEST SQL

```
SELECT u.id, u.first_name, u.last_name, b.author, COALESCE(b.name, '') FROM test_db.users as u
LEFT JOIN user_books ub on u.id = ub.user_id
LEFT JOIN books b on b.id = ub.book_id
WHERE u.age BETWEEN 7 AND 17
GROUP BY b.author
HAVING count(b.id) = 2

```
