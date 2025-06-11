-- Ambil 10 data terakhir
SELECT * FROM users ORDER BY id DESC LIMIT 10;

-- Total user per negara
SELECT country, COUNT(*) FROM users GROUP BY country;

-- Cari user tanpa email
SELECT * FROM users WHERE email IS NULL;

-- Join 2 tabel
SELECT u.name, o.total 
FROM users u
JOIN orders o ON u.id = o.user_id;
