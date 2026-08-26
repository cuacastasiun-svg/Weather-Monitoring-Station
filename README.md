# 🌦️ Professional Weather Monitoring Dashboard

Dashboard pemantauan stasiun cuaca dengan antarmuka premium, interaktif, dan modern. Terinspirasi dari sistem monitoring industri dan SCADA.

## ✨ Fitur Tampilan Baru
1. **Aesthetic UI Design**: Menggunakan palet warna *Deep Dark Navy* dipadukan dengan aksen warna parameter yang tegas (Biru, Oranye, Hijau, Merah).
2. **Visual Widget Dinamis**:
   - **Termometer:** Animasi cairan yang naik-turun berdasarkan suhu.
   - **Circular Gauge:** Indikator cincin SVG untuk persentase kelembapan.
   - **Compass Dial:** Jarum kompas berputar untuk indikasi arah/kecepatan angin.
   - **Progress Bars:** Indikator batang vertikal & horizontal untuk cahaya, hujan, dan heat index.
3. **Responsive Grid Layout**: Menyerupai perangkat *hardware control panel* sungguhan.
4. **Data Ekspor Terintegrasi**: Mengunduh riwayat log ke dalam Microsoft Excel (CSV).

## 🚀 Penggunaan
- Cukup buka file `index.html` di browser Anda. Saat belum ada data, visualizer akan berada di posisi 0 (kosong).
- Sistem integrasi Firebase telah dipersiapkan di dalam tag `<script>`. Anda cukup menempelkan konfigurasi *Realtime Database* Anda untuk menghidupkan animasi datanya secara *real-time*.

*(Cocok digunakan sebagai antarmuka sistem Trainerkit Pendidikan atau proyek akhir IoT).*
