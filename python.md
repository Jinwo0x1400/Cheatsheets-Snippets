# 🐍 Python Snippets Cheatsheet

Kumpulan snippet Python singkat yang sering digunakan dalam scripting, automasi, manipulasi file, data, dan web request.

---

## 📦 Dasar

```python
# Cetak ke layar
print("Halo Dunia")

# Variabel dan tipe data
nama = "Cuy"
umur = 25
aktif = True

# List dan dict
buah = ["apel", "pisang", "mangga"]
user = {"nama": "Jinwoo", "umur": 25}
```

### 🔁 Struktur Kontrol
```python
# If else
if umur >= 18:
    print("Dewasa")
else:
    print("Anak-anak")

# For loop
for i in range(5):
    print(i)

# While loop
count = 0
while count < 5:
    print(count)
    count += 1
```

### 📂 File & Directory
```python
# Baca isi file
with open("data.txt", "r") as f:
    isi = f.read()

# Tulis ke file
with open("data.txt", "w") as f:
    f.write("Isi baru")

# Cek apakah file/dir ada
import os
os.path.exists("data.txt")
os.path.isdir("folder")
```

### 🧰 List & String
```python
# Loop list
for buah in buah:
    print(buah)

# Join & split
text = "-".join(buah)
arr = text.split("-")

# Replace string
"Hello World".replace("World", "Python")

# Cek substring
"python" in "belajar python"
```

### 🌐 HTTP Request
```python
import requests

# GET
r = requests.get("https://httpbin.org/get")
print(r.status_code, r.text)

# POST
data = {"nama": "Cuy"}
r = requests.post("https://httpbin.org/post", data=data)
print(r.json())
```

### 📊 JSON & CSV
```python
import json
import csv

# JSON
json_str = json.dumps(user)
parsed = json.loads(json_str)

# CSV
with open("file.csv", newline='') as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

### 🕒 Waktu & Acak
```python
import time
import random

# Delay 2 detik
time.sleep(2)

# Angka random 1-100
n = random.randint(1, 100)
```

### 🛠️ Fungsi & Exception
```python
def halo(nama="Cuy"):
    return f"Halo {nama}!"

try:
    hasil = 10 / 0
except ZeroDivisionError:
    print("Tidak bisa bagi nol!")
```

