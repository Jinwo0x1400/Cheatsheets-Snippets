# 🚀 Laravel Cheatsheet

Kumpulan perintah Artisan, Composer, dan trik Laravel yang sering digunakan untuk pengembangan aplikasi Laravel sehari-hari.

---

## 🛠️ Artisan Command

```bash
php artisan list
# Lihat semua perintah artisan

php artisan make:model Post -mcr
# Buat model dengan migration, controller, dan resource

php artisan make:controller Admin/PostController --resource
# Controller dengan resource

php artisan route:list
# Lihat semua route

php artisan tinker
# Console interaktif

php artisan migrate:fresh --seed
# Reset semua migration dan jalankan seeder

php artisan config:clear
php artisan route:clear
php artisan view:clear
php artisan cache:clear
# Bersihkan semua cache
```

### 📦 Composer Commands
```bash
composer install
# Install semua dependency dari composer.lock

composer update
# Update dependency ke versi terbaru

composer dump-autoload
# Regenerasi autoload class

composer require barryvdh/laravel-debugbar --dev
# Install package
```

### 🧪 Testing & Seeder
```
php artisan db:seed
# Jalankan seeder

php artisan db:seed --class=UserSeeder
# Jalankan seeder tertentu

php artisan make:test UserTest
# Buat test

php artisan test
# Jalankan semua test
```

### 🔐 Auth & User

```
php artisan make:auth
# (Laravel < 6) Buat autentikasi default

composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
# Laravel Breeze (Login/Register simple)

php artisan make:middleware AdminOnly
# Buat middleware

php artisan make:policy PostPolicy --model=Post
# Buat policy untuk model
```


### 📁 File & Storage
``` 
php artisan storage:link
# Link folder public/storage ke storage/app/public

// Upload file (di controller)
$request->file('avatar')->store('avatars');

// Ambil URL file
Storage::url('avatars/file.jpg');
```


### ⚙️ Tips Tambahan

```
// Gunakan mutator (model)
public function getTitleAttribute($value)
{
    return strtoupper($value);
}

// Global scope (model)
protected static function booted()
{
    static::addGlobalScope('active', function ($query) {
        $query->where('status', 1);
    });
}
```

### 📌 Tambahkan juga package populer:
 ```
composer require spatie/laravel-permission
composer require barryvdh/laravel-debugbar --dev
composer require maatwebsite/excel
```

#### ⭐ Jangan lupa star repo ini kalau bermanfaat ya!
