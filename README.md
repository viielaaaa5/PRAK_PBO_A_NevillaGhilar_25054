# Laporan Praktikum Sebelum dan Sesudah Perbaikan — PBO A (Nevilla Ghilar Apryanti, 4525210054)

## 1. Susunan Folder Repository

```text
PRAK_PBO_A_NevillaGhilar_25054/
├── Materi&Code Sebelumnya/
│   └── Kumpulan materi dan source code awal
│
├── PRAK PBO/
│   └── Kumpulan file hasil pengerjaan praktikum
│
├── SS Sebelum/
│   └── Dokumentasi kode dan output sebelum perbaikan
│
└── SS Setelah/
    └── Dokumentasi kode dan output setelah perbaikan
```

Folder-folder tersebut memiliki fungsi yang berbeda untuk memudahkan penyimpanan dan pemeriksaan hasil praktikum.

1. `Materi&Code Sebelumnya/` berisi materi serta source code awal yang dijadikan acuan dalam mengerjakan praktikum.

2. `PRAK PBO/` menjadi tempat penyimpanan file program hasil pengerjaan dan perbaikan selama praktikum berlangsung.

3. `SS Sebelum/` menyimpan bukti visual berupa screenshot kode dan hasil program pada kondisi awal.

4. `SS Setelah/` menyimpan screenshot setelah kode mengalami perbaikan, sehingga perubahan program dapat dibandingkan dengan kondisi sebelumnya.

## 2. Menjalankan Program Sebelum Perbaikan

Source code awal tersimpan di folder `Materi&Code Sebelumnya/`. Sebelum menjalankan program, buka terminal pada direktori tempat file program berada.

### A. Program Java

Pastikan Java Development Kit (JDK) sudah terinstal. Setelah masuk ke folder yang berisi file Java, jalankan perintah berikut:

```bash
javac *.java
java Main
```

Perintah pertama berfungsi untuk menerjemahkan source code Java menjadi file yang dapat dijalankan. Setelah proses kompilasi berhasil, perintah kedua digunakan untuk menjalankan program melalui class `Main`.

### B. Program PHP

Untuk menjalankan program PHP, pastikan PHP sudah terpasang dan dapat digunakan melalui terminal. Masuk ke direktori yang berisi file utama, kemudian jalankan:

```bash
php main.php
```

Perintah tersebut akan mengeksekusi program yang terdapat di dalam `main.php`. Jika nama file utama berbeda, gunakan nama file yang sesuai dengan isi folder.

## 3. Menjalankan Program Setelah Perbaikan

File hasil pengerjaan praktikum disimpan di dalam folder `PRAK PBO/`. Proses menjalankan program dilakukan kembali setelah perubahan kode selesai dibuat.

### A. Program Java

Apabila source code menggunakan direktori `src/java/` dan hasil kompilasi disimpan di folder `bin/`, gunakan perintah berikut:

```bash
javac -d bin src/java/*.java
java -cp bin Main
```

Penjelasan perintah:

1. `javac -d bin src/java/*.java` digunakan untuk mengompilasi seluruh file Java pada direktori `src/java/` dan menempatkan hasilnya di folder `bin/`.

2. `java -cp bin Main` digunakan untuk menjalankan class utama dengan mengambil file hasil kompilasi dari folder `bin/`.

Pastikan perintah dijalankan dari direktori praktikum yang benar agar lokasi file dapat ditemukan.

### B. Program PHP

Jika file PHP berada di direktori `src/php/`, program dapat dijalankan menggunakan perintah:

```bash
php src/php/main.php
```

Perintah tersebut digunakan untuk mengeksekusi file utama PHP setelah kode selesai diperbaiki. Lokasi file perlu disesuaikan apabila susunan direktori yang digunakan berbeda.

## 4. Dokumentasi Pengujian Program

Screenshot digunakan sebagai bukti pengerjaan sekaligus untuk memperlihatkan perbedaan kondisi program sebelum dan setelah perbaikan.

| Kondisi | Screenshot yang Dikumpulkan | Kegunaan |
|---|---|---|
| Sebelum perbaikan | Source code awal | Memperlihatkan kode yang pertama kali dikerjakan |
| Sebelum perbaikan | Output atau pesan error | Menunjukkan hasil pengujian awal |
| Setelah perbaikan | Source code yang telah diperbarui | Memperlihatkan perubahan pada kode |
| Setelah perbaikan | Output terbaru | Membuktikan hasil pengujian setelah perbaikan |

Screenshot harus memperlihatkan bagian kode atau keluaran terminal yang relevan. Apabila terjadi error, pesan yang muncul sebaiknya ikut didokumentasikan agar masalah yang ditemukan dapat dijelaskan.

Hal-hal yang perlu diperhatikan ketika mengambil screenshot:

1. Pastikan kode atau output terlihat dengan jelas.
2. Tampilkan bagian program yang sedang diuji.
3. Simpan screenshot sesuai dengan kategorinya.
4. Bandingkan hasil awal dengan hasil setelah perubahan dilakukan.
5. Gunakan hasil pengujian yang benar-benar diperoleh ketika program dijalankan.

## 5. Analisis Perubahan Kode

Pemeriksaan dilakukan dengan membandingkan source code awal dan source code hasil perbaikan. Tujuannya adalah mengetahui perubahan yang dilakukan serta memastikan program dapat berjalan sesuai dengan fungsi yang diharapkan.

| Bagian yang Diperiksa | Sebelum Perbaikan | Setelah Perbaikan |
|---|---|---|
| Penulisan kode | Menggunakan source code awal | Disesuaikan berdasarkan hasil pemeriksaan |
| Struktur program | Diperiksa untuk menemukan bagian yang perlu diperbaiki | Ditinjau kembali setelah perubahan |
| Method dan constructor | Diperiksa kesesuaian fungsi dan parameter | Diuji kembali setelah penyesuaian |
| Validasi input | Diperiksa terhadap masukan yang tidak sesuai | Diuji untuk memastikan penanganannya |
| Output program | Dicatat dari hasil pengujian awal | Dibandingkan dengan hasil terbaru |
| Dokumentasi | Disimpan pada folder `SS Sebelum/` | Disimpan pada folder `SS Setelah/` |

Hasil analisis setiap pertemuan perlu disesuaikan dengan permasalahan yang benar-benar ditemukan. Jika terdapat kesalahan, jelaskan penyebabnya, bagian kode yang diubah, serta hasil yang diperoleh setelah program diuji kembali.

## 6. Evaluasi Source Code

Evaluasi dilakukan untuk memastikan bahwa kode yang telah dikerjakan sesuai dengan materi praktikum dan dapat dijalankan dengan benar.

Beberapa aspek yang menjadi bahan pemeriksaan adalah sebagai berikut:

1. **Class dan object**

   Memeriksa penggunaan class sebagai struktur program serta object sebagai hasil pembentukan dari class tersebut.

2. **Atribut dan constructor**

   Memastikan atribut dideklarasikan dengan tepat dan constructor digunakan untuk menginisialisasi object.

3. **Method**

   Memeriksa apakah setiap method telah menjalankan tugas sesuai dengan tujuan program.

4. **Validasi data**

   Menguji respons program terhadap data yang tidak sesuai dengan ketentuan, apabila validasi diperlukan.

5. **Kesesuaian hasil program**

   Membandingkan output dengan logika program untuk memastikan hasil yang ditampilkan sudah benar.

6. **Konsistensi penamaan**

   Memeriksa nama class, variabel, method, dan file agar sesuai dengan ketentuan bahasa pemrograman yang digunakan.

7. **Pengujian ulang**

   Menjalankan program kembali setelah perbaikan untuk memastikan perubahan yang dilakukan tidak menimbulkan kesalahan baru.

Catatan evaluasi sebaiknya ditulis berdasarkan hasil pemeriksaan masing-masing praktikum, bukan hanya berdasarkan perkiraan terhadap source code.

## 7. Penggunaan Git dan GitHub

Git digunakan untuk mencatat perubahan pada file, sedangkan GitHub berfungsi sebagai tempat penyimpanan repository secara daring. Keduanya membantu mengelola source code dan menyimpan hasil pengerjaan praktikum.

Repository: [PRAK_PBO_A_NevillaGhilar_25054](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054)

Perintah Git yang digunakan untuk memperbarui repository adalah:

```bash
git status
git add .
git commit -m "PrakPBO"
git push -u origin main
```

Fungsi dari setiap perintah:

1. `git status` menampilkan kondisi repository dan perubahan file yang belum disimpan ke dalam commit.

2. `git add .` memasukkan perubahan file ke staging area agar siap di-commit.

3. `git commit -m "PrakPBO"` mencatat perubahan ke dalam riwayat repository dengan pesan commit yang sesuai.

4. `git push -u origin main` mengirimkan commit dari branch `main` ke repository GitHub.

Sebelum melakukan push, periksa kembali perubahan yang akan dikirimkan dan pastikan repository lokal menggunakan branch yang benar.

## 8. Kesimpulan

Pengerjaan praktikum PBO A memberikan pemahaman mengenai penyusunan program berbasis objek, pemeriksaan kesalahan pada source code, dan proses pengujian setelah perbaikan. Perbandingan kode serta hasil eksekusi sebelum dan sesudah perbaikan dapat digunakan untuk melihat perubahan yang telah dilakukan.

Selain itu, penggunaan Git dan GitHub membantu proses penyimpanan, pencatatan perubahan, serta pengelolaan file praktikum agar lebih teratur. Dokumentasi yang disusun secara sistematis juga memudahkan proses pemeriksaan dan evaluasi hasil pengerjaan.
