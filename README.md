# Rangkuman Tugas Analisis Algoritma (Strassen, No 3)

## Gambaran umum
Tugas individu mata kuliah Algoritma Komputasi (Magister Teknik Informatika). Kamu menganalisis satu algoritma secara formal, mengimplementasikan, menguji, lalu mempresentasikannya. Fokus penilaian adalah kaitan antara analisis teori dan hasil pengukuran, bukan sekadar kode yang berjalan.

## Tenggat dan jadwal
- **Kumpul:** Minggu, **11 Oktober 2026, 23.59 WITA**. Terlambat dipotong 10% per hari.
- **Presentasi:** sesi 1 (No 1–12), **12–16 Oktober 2026**. Strassen ada di No 3. Formatnya 15 menit presentasi dan 10 menit tanya jawab.
- **Yang dikumpulkan:** laporan PDF, kode, dan slide.

## Ketentuan format
| Aspek | Ketentuan |
|---|---|
| Laporan | PDF, **12–20 halaman**, format IEEE atau template prodi, Bahasa Indonesia baku |
| Kode | Repositori GitHub/GitLab atau Jupyter Notebook, dengan README |
| Bahasa pemrograman | Python (disarankan), C++, Java, atau Julia |
| Referensi | Minimal **8**, termasuk **3 artikel jurnal/konferensi 5 tahun terakhir** |
| Abstrak | 150–250 kata |

## Struktur laporan (5 bab)
1. **Pendahuluan:** latar belakang, definisi formal masalah, tujuan, batasan.
2. **Landasan teori:** paradigma desain, konsep matematis, minimal 3 penelitian terbaru.
3. **Analisis algoritma (inti):** contoh manual, pseudocode, bukti kebenaran, penurunan kompleksitas, perbandingan.
4. **Implementasi dan eksperimen:** studi kasus, lingkungan uji, kode inti, tabel dan grafik.
5. **Kesimpulan:** kelebihan, keterbatasan, peluang pengembangan.

Pelengkap: abstrak, lampiran, pustaka IEEE, tautan repositori.

## Aturan implementasi
- **Wajib:** inti algoritma buatan sendiri, terstruktur dalam fungsi/kelas dan diberi komentar, README (pustaka, cara menjalankan, contoh keluaran), minimal 3 kasus uji kecil yang bisa dicek manual.
- **Boleh:** pustaka untuk membaca data dan plotting, pustaka sebagai pembanding.
- **Tidak boleh:** memanggil fungsi pustaka sebagai inti, atau menyalin kode tanpa atribusi.

## Aturan eksperimen
- Minimal **5 ukuran input** berbeda.
- Minimal **5 kali pengulangan** per percobaan, lapor rata-rata dan simpangan baku.
- Minimal **1 pembanding** (algoritma alternatif atau pustaka).
- Grafik waktu terhadap ukuran harus **disandingkan dengan kurva kompleksitas teoretis**.
- Parameter sensitivitas (minimal 2) hanya untuk metaheuristik dan ML, jadi tidak wajib untuk Strassen.
- Algoritma stokastik memakai seed tetap.

## Bobot penilaian
| Komponen | Bobot |
|---|---|
| Analisis kompleksitas dan kebenaran | **25%** |
| Implementasi | 20% |
| Eksperimen dan pembahasan | 20% |
| Pemahaman dan landasan teori | 15% |
| Kualitas laporan | 10% |
| Presentasi dan tanya jawab | 10% |

Menyebut Big-O tanpa penurunan formal hanya masuk kategori "cukup".

## Integritas akademik
- Kemiripan maksimal 20% di luar daftar pustaka. Pelanggaran berat berarti nilai 0.
- Kode dari luar wajib diberi sumber di komentar dan README.
- Alat bantu AI boleh untuk memahami konsep, bahasa, dan debugging, tetapi **harus dilaporkan di lampiran** dan setiap referensi diverifikasi.
- Saat tanya jawab, kamu harus bisa menjelaskan **setiap baris kode inti dan setiap langkah penurunan kompleksitas**.

## Perbandingan dengan draf laporan yang sudah kita buat
Draf .odt tadi baru menutup sebagian ketentuan. Yang masih kurang:

1. **Panjang dan format:** draf 10 halaman, syaratnya 12–20 halaman, IEEE, dan **dikumpulkan sebagai PDF**.
2. **Struktur lima bab:** susunan draf berbeda dan belum ada Bab 3 yang berdiri sendiri.
3. **Bab 3 (bobot terbesar):** belum ada contoh perhitungan manual (misalnya 2×2), pseudocode, **bukti kebenaran formal** rumus M1–M7 (sekarang hanya dibuktikan lewat uji empiris), dan penurunan kompleksitas dengan Teorema Master untuk T(n) = 7T(n/2) + Θ(n²).
4. **Referensi:** belum ada sama sekali. Perlu minimal 8, termasuk 3 artikel 5 tahun terakhir. Verifikasi sendiri setiap referensi.
5. **Abstrak:** draf sudah ada tetapi perlu dicek apakah 150–250 kata.
6. **Pengulangan eksperimen:** n = 2048 hanya 3 kali dan n = 1024 hanya 5 kali, sedangkan aturan minimal 5 kali di semua ukuran, jadi perlu diulang.
7. **Grafik:** belum ada kurva teoretis n³ dan n^2,81 yang disandingkan dengan waktu hasil ukur.
8. **Kasus uji:** perlu minimal 3 kasus kecil yang bisa dicek manual, plus README dan repositori.
9. **Lampiran penggunaan AI:** karena draf dibuat dengan bantuan AI, ini wajib dilaporkan.
10. **Referensi pada Bab 2:** perlu minimal 3 penelitian terbaru.

Satu hal untuk dipertimbangkan: base case implementasimu memakai `A @ B` dari NumPy pada ukuran ≤ cutoff. Rekursi Strassen-nya buatanmu sendiri, tetapi aturan melarang pustaka sebagai "inti". Sebaiknya kamu konfirmasi ke dosen apakah base case seperti ini diterima, atau sediakan versi dengan base case perkalian tiga-loop buatan sendiri sebagai varian tambahan.

Waktu tersisa hanya dua hari, jadi prioritasnya Bab 3 (bobot 25%), referensi, dan pengulangan eksperimen. Saya bisa menyusun ulang laporan sesuai lima bab dan format IEEE mulai dari mana saja yang kamu butuhkan.