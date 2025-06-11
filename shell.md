### 🐚 Shell Command Cheatsheet

Kumpulan perintah Linux Shell (Bash) yang sering digunakan untuk administrasi server, maintenance, dan scripting harian.

---

## 📦 File & Folder

```bash
# Cek ukuran semua folder/file
du -sh *

# Cari semua file .log dan hapus
find . -name "*.log" -type f -delete

# Ganti permission semua file jadi 644
find . -type f -exec chmod 644 {} \;

# Ganti permission semua folder jadi 755
find . -type d -exec chmod 755 {} \;

# Cari semua file yang bisa ditulis
find / -type f -writable 2>/dev/null
```


### 🌐 Jaringan & Port
```bash
# Cek port terbuka
netstat -tulpn

# Cek IP publik
curl ifconfig.me

# Cek IP lokal
ip a | grep inet

# Ping domain
ping google.com

# Lihat koneksi aktif
ss -tulwn
```

###🧪 System Info & Monitoring
```bash
# Cek informasi CPU
lscpu

# Cek penggunaan RAM
free -h

# Cek disk usage
df -h

# Top process
top

# Cek system uptime
uptime

# Cek kernel & OS
uname -a
```

### 🔧 Miscellaneous

```
# Jalankan skrip setiap 1 menit (cron)
* * * * * /path/to/script.sh

# Cek waktu server
date

# Ekstrak ZIP
unzip file.zip

# Kompres ke ZIP
zip -r archive.zip folder/

# Ganti nama semua .txt ke .bak
rename 's/\.txt$/.bak/' *.txt
```

### 💡 Tips: Tambahkan sudo di depan perintah jika butuh akses root.
### 📌 Jangan lupa star repo ini jika bermanfaat ⭐
