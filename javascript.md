# ⚡ JavaScript Snippets

Kumpulan snippet JavaScript berguna untuk DOM manipulation, array, string, clipboard, dan lainnya. Cocok buat front-end dan fullstack developer!

---

## 🧩 DOM Manipulation

```js
// Cek apakah elemen ada
if (document.querySelector('#myid')) {
  // ada
}

// Ubah isi elemen
document.getElementById('myid').innerText = 'Halo Dunia';

// Tambah class
document.querySelector('.kotak').classList.add('aktif');

// Hapus elemen
document.querySelector('#hapus').remove();
```

### ✂️ String Helpers

```js
// Ubah huruf besar/kecil
let text = "hello";
text.toUpperCase(); // "HELLO"
text.toLowerCase(); // "hello"

// Replace
let kalimat = "aku suka PHP";
kalimat.replace("PHP", "JavaScript");

// Cek apakah mengandung
"Hello World".includes("World"); // true
```

### 📚 Array & Object

```js
// Looping array
const arr = [1, 2, 3];
arr.forEach(x => console.log(x));

// Filter & Map
let genap = arr.filter(n => n % 2 === 0);
let kelipatan2 = arr.map(n => n * 2);

// Cek key dalam object
const obj = { nama: "cuy" };
"nama" in obj; // true
```
### 📋 Clipboard & Copy

```js
// Copy teks ke clipboard
navigator.clipboard.writeText("Halo Dunia");
```

### 🖱️ Event Listener
```js
// Event click
document.getElementById("tombol").addEventListener("click", function() {
  alert("Tombol diklik!");
});

// Event input
document.querySelector("#inputku").addEventListener("input", function(e) {
  console.log("Isi:", e.target.value);
});
```

### ⏱️ Delay & Timer

```js
// Delay 1 detik
setTimeout(() => {
  console.log("1 detik berlalu");
}, 1000);

// Interval
let count = 0;
let timer = setInterval(() => {
  count++;
  console.log(count);
  if (count >= 5) clearInterval(timer);
}, 1000);
```

### 🚀 Utilities

```js
// Debounce
function debounce(fn, delay) {
  let timeout;
  return function () {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn.apply(this, arguments), delay);
  };
}

// Generate angka random
let random = Math.floor(Math.random() * 100);
```

### 📌 Snippet ini bisa dipakai langsung di browser console atau file JS kamu.
### ⭐ Jangan lupa kasih bintang repo kalau bermanfaat ya!



