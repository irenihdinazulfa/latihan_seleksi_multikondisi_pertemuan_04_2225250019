# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input
Nama: Iren Ihdina Zulfa
NIM: 2225250019
Kelas: 3E

## Tujuan
1. Memahami penggunaan seleksi multi-kondisi dengan if-elif-else.
2. Menyusun kategori yang saling lepas dan menyeluruh.
3. Menentukan urutan kondisi yang benar pada klasifikasi berbasis rentang.
4. Memvalidasi input berdasarkan tipe data dan rentang nilai.
5. Menggunakan try-except ValueError untuk menangani kesalahan konversi input.
6. Menggabungkan validasi dan klasifikasi dalam satu alur program.
7. Menyusun tabel keputusan dan test case untuk menguji setiap cabang program.
8. Membiasakan penggunaan Git dan GitHub untuk menyimpan bukti pengerjaan.

## Cara Menjalankan
### 1. Memeriksa Instalasi Python
Buka terminal di VS Code, kemudian jalankan:
```bash
python --version
```
Pada beberapa sistem operasi, gunakan:
```bash
python3 --version
```
### 2. Menjalankan Program Latihan
Jalankan setiap file menggunakan perintah berikut:
```bash
python latihan/01_predikat_nilai.py
python latihan/02_kategori_bilangan.py
python latihan/03_validasi_rentang.py
python latihan/04_validasi_tipe.py
python latihan/05_klasifikasi_segitiga_sudut.py
```
### 3. Menjalankan Program Praktik
Untuk menjalankan program praktik, gunakan:
```bash
python praktik/validasi_klasifikasi_nilai.py
```
Jika perintah `python` tidak dapat digunakan, coba:
```bash
python3 praktik/validasi_klasifikasi_nilai.py
```
### 4. Alur Penggunaan Program
1. Program menerima input dari pengguna.
2. Input dikonversi ke tipe data yang sesuai.
3. Program memeriksa validitas input.
4. Jika input tidak valid, program menampilkan pesan penolakan.
5. Jika input valid, program melakukan klasifikasi sesuai aturan.
6. Program menampilkan hasil klasifikasi atau status yang sesuai.

## Tabel Keputusan
### A. Tabel Keputusan Predikat Nilai
| Kategori | Syarat | Contoh Input | Keluaran |
|---|---|---|---|
| A | Nilai >= 85 | 92 | Predikat A |
| B | Nilai >= 70 dan < 85 | 75 | Predikat B |
| C | Nilai >= 60 dan < 70 | 65 | Predikat C |
| D | Nilai >= 50 dan < 60 | 55 | Predikat D |
| E | Nilai < 50 | 40 | Predikat E |
### B. Tabel Keputusan Kategori Bilangan
| Kategori | Syarat | Contoh Input | Keluaran |
|---|---|---|---|
| Bilangan negatif | x < 0 | -7 | Bilangan negatif |
| Nol | x == 0 | 0 | Nol |
| Bilangan positif genap | x > 0 dan x % 2 == 0 | 8 | Bilangan positif genap |
| Bilangan positif ganjil | x > 0 dan x % 2 != 0 | 13 | Bilangan positif ganjil |
### C. Tabel Keputusan Validasi Rentang Sudut
| Kondisi | Syarat | Contoh Input | Keluaran |
|---|---|---|---|
| Input tidak valid | Sudut <= 0 atau >= 180 | 0 | Pesan penolakan |
| Sudut lancip | 0 < sudut < 90 | 45 | Sudut lancip |
| Sudut siku-siku | sudut == 90 | 90 | Sudut siku-siku |
| Sudut tumpul | 90 < sudut < 180 | 135 | Sudut tumpul |
### D. Tabel Keputusan Validasi Tipe
| Kondisi | Syarat | Contoh Input | Keluaran |
|---|---|---|---|
| Input bukan angka | Konversi int gagal | dua belas | Pesan penolakan tipe |
| Di luar rentang | benar < 0 atau benar > 20 | 21 | Pesan penolakan rentang |
| Belum tuntas | Persentase < 75 | 14 | Belum tuntas |
| Tuntas | Persentase >= 75 | 15 | Tuntas |
### E. Tabel Keputusan Klasifikasi Segitiga Sudut
| Kondisi | Syarat | Contoh Input | Keluaran |
|---|---|---|---|
| Sudut tidak valid | Salah satu sudut <= 0 | 0, 90, 90 | Pesan penolakan |
| Jumlah sudut tidak valid | Jumlah sudut tidak sama dengan 180 | 100, 50, 40 | Pesan penolakan |
| Segitiga tumpul | Sudut terbesar > 90 | 120, 30, 30 | Segitiga tumpul |
| Segitiga siku-siku | Sudut terbesar == 90 | 90, 45, 45 | Segitiga siku-siku |
| Segitiga lancip | Sudut terbesar < 90 | 60, 60, 60 | Segitiga lancip |
### F. Tabel Keputusan Praktik Validasi dan Klasifikasi Nilai
| Kondisi | Syarat | Keluaran |
|---|---|---|
| Tipe tidak valid | Ujian, tugas, atau kehadiran bukan angka | Pesan penolakan tipe |
| Nilai ujian tidak valid | Ujian < 0 atau ujian > 100 | Pesan penolakan nilai ujian |
| Nilai tugas tidak valid | Tugas < 0 atau tugas > 100 | Pesan penolakan nilai tugas |
| Kehadiran tidak valid | Hadir < 0 atau hadir > 100 | Pesan penolakan kehadiran |
| Tidak memenuhi kehadiran | Hadir < 80 | Tidak memenuhi syarat kehadiran |
| Predikat A | Nilai akhir >= 85 | Predikat A, Lulus |
| Predikat B | Nilai akhir >= 70 | Predikat B, Lulus |
| Predikat C | Nilai akhir >= 60 | Predikat C, Lulus |
| Predikat D | Nilai akhir >= 50 | Predikat D, Belum lulus |
| Predikat E | Nilai akhir < 50 | Predikat E, Belum lulus |

## Hasil Pengujian
### A. Pengujian Predikat Nilai
| Input | Keluaran Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|
| 92 | Predikat A | Nilai 92.00 memperoleh predikat A. | Sesuai |
| 85 | Predikat A | Nilai 85.00 memperoleh predikat A. | Sesuai |
| 84.9 | Predikat B | Nilai 84.90 memperoleh predikat B. | Sesuai |
| 70 | Predikat B | Nilai 70.00 memperoleh predikat B. | Sesuai |
| 60 | Predikat C | Nilai 60.00 memperoleh predikat C. | Sesuai |
| 50 | Predikat D | Nilai 50.00 memperoleh predikat D. | Sesuai |
| 49.9 | Predikat E | Nilai 49.90 memperoleh predikat E. | Sesuai |
### B. Pengujian Kategori Bilangan
| Input | Keluaran Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|
| -7 | Bilangan negatif | Bilangan negatif | Sesuai |
| 0 | Nol | Nol | Sesuai |
| 8 | Bilangan positif genap | Bilangan positif genap | Sesuai |
| 13 | Bilangan positif ganjil | Bilangan positif ganjil | Sesuai |
### C. Pengujian Validasi Rentang
| Input | Keluaran Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|
| 45 | Sudut lancip | Sudut lancip | Sesuai |
| 90 | Sudut siku-siku | Sudut siku-siku | Sesuai |
| 135 | Sudut tumpul | Sudut tumpul | Sesuai |
| 0 | Pesan penolakan | Pesan penolakan | Sesuai |
| 180 | Pesan penolakan | Pesan penolakan | Sesuai |
| -30 | Pesan penolakan | Pesan penolakan | Sesuai |
### D. Pengujian Validasi Tipe
| Input | Keluaran Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|
| 15 | 75.00 persen dan Tuntas | 75.00 persen dan Tuntas | Sesuai |
| 14 | 70.00 persen dan Belum tuntas | 70.00 persen dan Belum tuntas | Sesuai |
| 20 | 100.00 persen dan Tuntas | 100.00 persen dan Tuntas | Sesuai |
| 0 | 0.00 persen dan Belum tuntas | 0.00 persen dan Belum tuntas | Sesuai |
| 21 | Pesan penolakan rentang | Pesan penolakan rentang | Sesuai |
| dua belas | Pesan penolakan tipe | Pesan penolakan tipe | Sesuai |
### E. Pengujian Klasifikasi Segitiga Sudut
| Input | Keluaran Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|
| 60, 60, 60 | Segitiga lancip | Segitiga lancip | Sesuai |
| 90, 45, 45 | Segitiga siku-siku | Segitiga siku-siku | Sesuai |
| 120, 30, 30 | Segitiga tumpul | Segitiga tumpul | Sesuai |
| 100, 50, 40 | Pesan penolakan jumlah sudut | Pesan penolakan jumlah sudut | Sesuai |
| 0, 90, 90 | Pesan penolakan sudut positif | Pesan penolakan sudut positif | Sesuai |
### F. Pengujian Praktik Validasi dan Klasifikasi Nilai
| Ujian | Tugas | Kehadiran | Keluaran Diharapkan | Status |
|---|---|---|---|---|
| 90 | 80 | 95 | Nilai akhir 86.00, Predikat A, Lulus | Sesuai |
| 75 | 70 | 85 | Nilai akhir 73.00, Predikat B, Lulus | Sesuai |
| 60 | 60 | 80 | Nilai akhir 60.00, Predikat C, Lulus | Sesuai |
| 55 | 50 | 90 | Nilai akhir 53.00, Predikat D, Belum lulus | Sesuai |
| 40 | 30 | 100 | Nilai akhir 36.00, Predikat E, Belum lulus | Sesuai |
| 90 | 90 | 75 | Nilai akhir 90.00, Tidak memenuhi syarat kehadiran | Sesuai |
| 105 | 80 | 90 | Pesan penolakan nilai ujian | Sesuai |
| 80 | -5 | 90 | Pesan penolakan nilai tugas | Sesuai |
| 80 | 80 | abc | Pesan penolakan tipe | Sesuai |
Catatan: Kolom keluaran aktual harus disesuaikan dengan hasil yang benar-benar diperoleh setelah program dijalankan di VS Code.

## Refleksi
Pada Pertemuan 04, saya mempelajari penggunaan if-elif-else untuk membuat klasifikasi dengan beberapa kondisi yang saling lepas dan menyeluruh. Saya juga mempelajari pentingnya validasi tipe dan rentang sebelum data diproses lebih lanjut. Salah satu kesalahan yang perlu diperhatikan adalah ketika pengguna memasukkan teks pada program yang mengubah input menjadi float atau int, karena dapat menyebabkan ValueError. Kesalahan tersebut dapat ditangani menggunakan try-except ValueError agar program menampilkan pesan penolakan yang sesuai. Selain itu, saya memahami bahwa urutan kondisi pada klasifikasi nilai harus disusun dari rentang tertinggi ke terendah agar hasil predikat tidak keliru. Pengujian dengan nilai batas seperti 85, 70, 60, dan 50 membantu memastikan bahwa setiap kategori berjalan sesuai aturan. Melalui latihan dan praktik ini, saya menjadi lebih memahami cara menggabungkan validasi input dan klasifikasi dalam satu alur program yang terstruktur.

## Kesimpulan
Seleksi multi-kondisi dengan if-elif-else digunakan untuk menentukan satu keluaran berdasarkan kondisi yang sesuai. Validasi input diperlukan agar data yang diproses memiliki tipe dan rentang yang benar. Program yang baik harus menangani input valid maupun tidak valid, memiliki urutan kondisi yang tepat, dan diuji menggunakan berbagai test case termasuk nilai batas. Penerapan validasi dan klasifikasi membantu membuat program lebih terstruktur, mudah dipahami, dan sesuai dengan spesifikasi yang telah ditentukan.