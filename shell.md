# Cek ukuran folder
du -sh *

# Cek port terbuka
netstat -tulpn

# Ganti permission semua file jadi 644
find . -type f -exec chmod 644 {} \;

# Hapus semua file .log
find . -name "*.log" -type f -delete
