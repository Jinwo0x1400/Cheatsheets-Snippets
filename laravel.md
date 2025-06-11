# 🚀 Laravel Artisan Cheatsheet

Kumpulan perintah Laravel Artisan yang sering digunakan dalam pengembangan proyek Laravel. Cocok untuk pemula maupun expert yang butuh shortcut cepat.

---

## 🔧 Artisan Commands

```bash
php artisan list
# Lihat semua perintah artisan

php artisan route:list
# Tampilkan semua route terdaftar

php artisan make:model Post -mcr
# Buat model 'Post' + migration + controller + resource

php artisan make:controller MyController
# Buat controller biasa

php artisan make:seeder UserSeeder
# Buat seeder untuk isi data

php artisan migrate
# Jalankan semua migration

php artisan migrate:fresh --seed
# Reset database dan jalankan seeder

php artisan config:cache
# Cache semua konfigurasi

php artisan view:clear
# Hapus cache view blade

php artisan storage:link
# Buat symbolic link ke folder public/storage

php artisan tinker
# Console interaktif (REPL)

php artisan schedule:run
# Jalankan semua jadwal (cron)

php artisan make:model Post -a
# Buat model dengan semua resource: controller, factory, seeder, migration, dan policy

php artisan migrate:rollback
# Batalkan migrasi terakhir

php artisan migrate:status
# Lihat status semua migration

php artisan db:seed --class=UserSeeder
# Jalankan seeder tertentu
```
