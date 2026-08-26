# 🌤️ Weather Monitoring Station Dashboard

Sebuah antarmuka web (Dashboard) berkonsep *Single Page Application* (SPA) untuk memonitor data stasiun cuaca. Proyek ini dirancang agar ringan dan dapat di-hosting secara gratis menggunakan **GitHub Pages**.

## ✨ Fitur Utama

Dashboard ini terdiri dari 3 halaman utama yang berjalan secara dinamis tanpa perlu memuat ulang halaman (*reload*):
1. **📡 Data Realtime:** Menampilkan nilai pembacaan sensor saat ini (Suhu, Kelembapan, dan Tekanan Udara) dalam bentuk kartu metrik.
2. **📈 Grafik Data:** Memvisualisasikan pergerakan data suhu dan kelembapan secara *real-time* menggunakan grafik garis (*line chart*).
3. **📜 Histori Data:** Mencatat setiap data yang masuk ke dalam tabel riwayat (log) beserta waktu perekamannya.

## 🛠️ Teknologi yang Digunakan

*   **HTML5 & CSS3:** Untuk struktur dan tampilan (*styling*) responsif.
*   **Vanilla JavaScript:** Untuk logika navigasi halaman dan manipulasi DOM.
*   **[Chart.js](https://www.chartjs.org/):** *Library* JavaScript untuk merender grafik data secara interaktif.

## 🚀 Cara Menjalankan di GitHub Pages

Karena proyek ini hanya menggunakan *front-end* statis, Anda bisa langsung menayangkannya melalui GitHub:
1. Buat repositori baru di GitHub.
2. Ekstrak folder ini dan unggah file `index.html` beserta `README.md` ke dalam repositori tersebut.
3. Buka tab **Settings** pada repositori Anda.
4. Pilih menu **Pages** di bilah sisi kiri.
5. Pada bagian *Build and deployment* -> *Branch*, ubah `None` menjadi `main` (atau `master`), lalu klik **Save**.
6. Tunggu beberapa menit, dan GitHub akan memberikan tautan (URL) untuk mengakses dashboard Anda.

## 🔄 Catatan Integrasi IoT (Firebase)

Secara bawaan (*default*), kode pada `index.html` menggunakan fungsi simulator `setInterval()` untuk menghasilkan data cuaca acak setiap 3 detik. Hal ini bertujuan agar UI dapat langsung diuji.

Untuk menghubungkannya dengan proyek IoT Anda (misalnya pengembangan Trainerkit Alat Monitoring Kualitas Udara), Anda perlu:
1. Menambahkan Firebase SDK ke dalam file HTML.
2. Mengganti blok kode simulasi dengan *listener* Firebase `onValue()` untuk mengambil data dari Firebase Realtime Database.
3. Mengarahkan mikrokontroler Anda untuk mengirimkan data pembacaan sensor ke *node* Firebase yang sesuai.

---
*Dibuat untuk keperluan monitoring IoT.*
