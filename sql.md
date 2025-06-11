# 🗃️ SQL Query Cheatsheet

Kumpulan SQL query yang sering digunakan untuk manipulasi data, analisis, dan administrasi database. Cocok untuk MySQL, PostgreSQL, dan SQL Server dasar.

---

## 📄 Basic Queries

```sql
-- Ambil semua data
SELECT * FROM users;

-- Ambil 10 data pertama
SELECT * FROM users LIMIT 10;

-- Urutkan berdasarkan kolom
SELECT * FROM users ORDER BY created_at DESC;

-- Ambil data unik
SELECT DISTINCT country FROM users;

-- Rename alias kolom
SELECT name AS username FROM users;
```


### 🔍 WHERE & Filter
```sql
-- Filter berdasarkan kondisi
SELECT * FROM users WHERE age > 18;

-- Kombinasi AND / OR
SELECT * FROM users WHERE age > 18 AND country = 'Thailand';

-- IN & NOT IN
SELECT * FROM users WHERE role IN ('admin', 'editor');

-- BETWEEN
SELECT * FROM orders WHERE total BETWEEN 100 AND 500;

-- LIKE (pattern matching)
SELECT * FROM users WHERE name LIKE '%john%';
```

### 🧮 Aggregate Functions
```sql
-- Total data
SELECT COUNT(*) FROM users;

-- Rata-rata umur
SELECT AVG(age) FROM users;

-- Total pendapatan
SELECT SUM(amount) FROM orders;

-- Max/Min
SELECT MAX(price), MIN(price) FROM products;
```

### 🧠 GROUP BY & HAVING
```sql
-- Jumlah user per negara
SELECT country, COUNT(*) FROM users GROUP BY country;

-- Hanya ambil yang total user-nya > 10
SELECT country, COUNT(*) AS total 
FROM users 
GROUP BY country 
HAVING total > 10;
```

### 🔗 JOIN
```sql
-- INNER JOIN
SELECT u.name, o.total
FROM users u
JOIN orders o ON u.id = o.user_id;

-- LEFT JOIN
SELECT u.name, o.total
FROM users u
LEFT JOIN orders o ON u.id = o.user_id;

-- RIGHT JOIN
SELECT u.name, o.total
FROM users u
RIGHT JOIN orders o ON u.id = o.user_id;
```

### ✍️ Insert, Update, Delete
```sql
-- Insert data
INSERT INTO users (name, email) VALUES ('Cuy', 'cuy@mail.com');

-- Update data
UPDATE users SET name = 'Jinwoo' WHERE id = 1;

-- Hapus data
DELETE FROM users WHERE id = 2;
```

### 🛠️ Tabel & Index

```sql
-- Buat tabel baru
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tambah kolom
ALTER TABLE users ADD COLUMN age INT;

-- Buat index
CREATE INDEX idx_email ON users(email);
```

### 📌 Snippet ini diuji di MySQL 5.7+, PostgreSQL 12+, dan kompatibel untuk kebanyakan RDBMS.
### ⭐ Star repo ini kalau kamu suka!
