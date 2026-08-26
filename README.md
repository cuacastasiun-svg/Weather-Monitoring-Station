# ⚡ Neon Weather Monitoring Dashboard (5 Parameters)

Sebuah antarmuka web (Dashboard) bertema **Dark Neon (Hitam & Biru Laut)** berkonsep *Single Page Application* (SPA) untuk memonitor data stasiun cuaca, khusus disiapkan untuk integrasi dengan Firebase.

## ✨ Fitur Terbaru

1. **🎨 Tema Dark Neon:** Desain futuristik dengan latar belakang gelap dan aksen *glowing* neon.
2. **📡 5 Parameter Utama:** 
   - Suhu Udara (°C) - Merah Muda
   - Kelembapan Udara (%) - Biru
   - Intensitas Cahaya (Lux) - Kuning
   - Curah Hujan (mm) - Ungu
   - Kecepatan Angin (m/s) - Hijau
3. **📈 Grafik Terpisah & Kosong Default:** Tiap parameter memiliki grafik sendiri. Grafik dan tabel akan **tetap kosong** sebelum ada data asli yang masuk dari database.
4. **📥 Export to Excel (CSV):** Fitur untuk mengunduh log data dari tabel ke dalam format `.csv` dengan 5 parameter tersebut. Tombol akan memberikan peringatan jika belum ada data.

## 🚀 Cara Menjalankan

1. Ekstrak folder ini.
2. Buka file `index.html` menggunakan browser. Anda akan melihat UI siap pakai, dengan nilai `--` (kosong) dan grafik yang bersih.

## 🔄 Cara Menghubungkan ke Firebase

Di dalam file `index.html` (bagian paling bawah di dalam tag `<script>`), saya telah membuatkan **fungsi khusus bernama `updateDashboard()`** beserta **blok contoh kode Firebase** yang sudah di-komentar (comment out). 

Langkah yang perlu Anda lakukan:
1. Scroll ke bagian paling bawah file `index.html`.
2. Hapus komentar (`/*` dan `*/`) pada blok kode integrasi Firebase.
3. Masukkan `firebaseConfig` Anda (API Key, Database URL, dll dari konsol Firebase).
4. Sesuaikan nama *node* atau rute database pada `ref(db, 'SensorCuaca')`.
5. Sesuaikan properti data (`data.suhu`, `data.kelembapan`, dll) dengan nama variabel/struktur JSON yang dikirimkan oleh mikrokontroler IoT Anda.

Begitu perangkat IoT Anda mengirim data ke Firebase, fungsi `onValue()` akan mendeteksinya secara *real-time* dan otomatis memanggil `updateDashboard()`, yang kemudian akan menggambar grafik, mengisi kartu, dan mencatat riwayat dalam tabel!
