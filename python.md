# Baca file CSV
import csv
with open('file.csv') as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)

# Cek URL aktif
import requests
r = requests.get('https://google.com')
print(r.status_code)
