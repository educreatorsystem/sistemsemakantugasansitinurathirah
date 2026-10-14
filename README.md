# Sistem Semakan Penghantaran Tugasan Murid

Aplikasi web ringkas untuk guru merekod penghantaran buku kerja atau tugasan murid, mengira mata terkumpul, dan memaparkan dashboard rekod untuk analisis serta cetakan.

## Fungsi Utama

- Dropdown kelas dan nama murid diambil daripada Google Sheet.
- Dropdown subjek diambil daripada Google Sheet.
- Rekod penghantaran murid:
  - Hantar + Lengkap: 3 mata
  - Hantar + Tidak Lengkap: 1 mata
  - Tidak Hantar + Tidak Hadir: 0 mata
  - Tidak Hantar + Tiada Sebab: -2 mata
- Dashboard rekod dengan tapisan kelas, subjek, julat tarikh dan nama tugasan.
- Kolum tarikh dinamik berdasarkan rekod.
- Fungsi cetak laporan dashboard.
- Simpan dan baca semula rekod melalui Google Apps Script.

## Struktur Fail

```text
.
├── index.html
├── README.md
└── apps-script
    └── Code.gs
```

## Konfigurasi Semasa

Sheet ID:

```text
1LZkkSoeZOEBz8d9nJ3IHGeSt6VNczdOMDwjJ7VsccxM
```

URL Apps Script:

```text
https://script.google.com/macros/s/AKfycbwcbfXE6GkhE15wYE-gZZibZCar0ThhhJcmvjBoRGsCI38IqWdnb2l12K5TBm_VtHZc/exec
```

CSV Kelas & Nama Murid:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQVycVKyGNhbVgloWoGSXqa6eB8CqZWmKeM4VqEybH8vWcOi5ZC9gPv6WSTbosXMOYqaYUH_J6rshG_/pub?gid=0&single=true&output=csv
```

CSV Subjek:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQVycVKyGNhbVgloWoGSXqa6eB8CqZWmKeM4VqEybH8vWcOi5ZC9gPv6WSTbosXMOYqaYUH_J6rshG_/pub?gid=1262893420&single=true&output=csv
```

## Cara Publish Di GitHub Pages

1. Upload/replace fail `index.html`, `README.md`, dan folder `apps-script/Code.gs` ke repository GitHub.
2. Pergi ke `Settings > Pages`.
3. Pada bahagian `Build and deployment`, pilih:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
4. Klik `Save`.
5. Tunggu GitHub Pages update dan refresh laman web.

## Cara Setup Google Apps Script

1. Buka Google Sheet utama.
2. Pergi ke `Extensions > Apps Script`.
3. Padam kod sedia ada dan tampal kandungan daripada `apps-script/Code.gs`.
4. Klik `Save`.
5. Pergi ke `Deploy > Manage deployments`.
6. Klik `Edit`, pilih `New version`, kemudian `Deploy`.
7. Tetapan Web App:
   - Execute as: `Me`
   - Who has access: `Anyone`
8. Pastikan URL Web App yang digunakan ialah:

```text
https://script.google.com/macros/s/AKfycbwcbfXE6GkhE15wYE-gZZibZCar0ThhhJcmvjBoRGsCI38IqWdnb2l12K5TBm_VtHZc/exec
```

## Google Sheet Sumber Dropdown

Data kelas dan nama murid perlu berada dalam format:

```text
KELAS, NAMA MURID
```

Data subjek perlu berada dalam format:

```text
BIL, SUBJEK
```

## Nota Penting

- Selepas mengubah `Code.gs`, deploy Apps Script sebagai versi baharu.
- Jika dashboard tidak memaparkan data terkini, refresh laman web.
- Pastikan Google Sheet sumber dropdown telah dipublish sebagai CSV.

## Konfigurasi Terkini

Sheet ID:

```text
1LZkkSoeZOEBz8d9nJ3IHGeSt6VNczdOMDwjJ7VsccxM
```

URL Apps Script:

```text
https://script.google.com/macros/s/AKfycbwcbfXE6GkhE15wYE-gZZibZCar0ThhhJcmvjBoRGsCI38IqWdnb2l12K5TBm_VtHZc/exec
```

CSV Kelas & Nama Murid:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQVycVKyGNhbVgloWoGSXqa6eB8CqZWmKeM4VqEybH8vWcOi5ZC9gPv6WSTbosXMOYqaYUH_J6rshG_/pub?gid=0&single=true&output=csv
```

CSV Subjek:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQVycVKyGNhbVgloWoGSXqa6eB8CqZWmKeM4VqEybH8vWcOi5ZC9gPv6WSTbosXMOYqaYUH_J6rshG_/pub?gid=1262893420&single=true&output=csv
```
