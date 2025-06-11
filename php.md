# 🐘 PHP Snippets Cheatsheet

Kumpulan snippet PHP yang sering dipakai untuk web development, scripting, dan manipulasi data. Cocok untuk pemula sampai pro!

---

## 📋 Dasar

```php
// Tampilkan teks
echo "Halo Dunia";

// Komentar
// Ini komentar satu baris
/* Ini
   komentar
   multi-baris */

// Variabel
$nama = "Cuy";
$umur = 25;
```
### 🔁 Struktur Kontrol

```php
// If else
if ($umur >= 18) {
    echo "Dewasa";
} else {
    echo "Anak-anak";
}

// Looping for
for ($i = 0; $i < 5; $i++) {
    echo $i;
}

// Foreach
$arr = [1, 2, 3];
foreach ($arr as $val) {
    echo $val;
}
```

### 🧪 String & Array
```php
// String replace
str_replace("PHP", "Laravel", "Saya suka PHP");

// Pecah string jadi array
explode(",", "a,b,c");

// Gabung array jadi string
implode("-", ['a', 'b', 'c']);

// Cek apakah string mengandung substring
strpos("halo dunia", "dunia") !== false;
```

### 🧮 Fungsi & File
``` 
// Buat fungsi
function halo($nama) {
    return "Hai $nama!";
}

// Cek apakah file ada
if (file_exists("index.php")) {
    echo "File ditemukan";
}

// Baca isi file
$isi = file_get_contents("data.txt");

// Simpan ke file
file_put_contents("data.txt", "Isi baru");

// Include file
include "header.php";
```

### 📦 JSON & Superglobals

```
// Array ke JSON
$data = ["nama" => "Cuy"];
$json = json_encode($data);

// JSON ke array
$parsed = json_decode($json, true);

// Ambil data POST
$nama = $_POST['nama'] ?? 'Anonim';

// Ambil IP user
$ip = $_SERVER['REMOTE_ADDR'];
```

### 🔐 Security & Misc
```
// Escape output (prevent XSS)
htmlspecialchars($input, ENT_QUOTES, 'UTF-8');

// Hash password
$hash = password_hash("passwordku", PASSWORD_DEFAULT);

// Verifikasi hash
password_verify("passwordku", $hash);

// Generate random string
$token = bin2hex(random_bytes(16));
```

### ⭐ Jangan lupa star repo ini kalau bermanfaat!
### 📌 Tambahkan snippet favorit kamu lewat Pull Request 💪
