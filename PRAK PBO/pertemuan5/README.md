# Laporan Praktikum 05: Polimorphism

| Keterangan | Detail |
|---|---|
| Nama | Nevilla Ghilar Apryanti |
| NPM | 4525210054 |
| Kelas | PBO A 2025/2026 |
| Mata Kuliah | Pemrograman Berorientasi Objek |
| Dosen Pengampu | Adi Wahyu Pribadi, S.Si., M.Kom. |

## 1. Ringkasan Soal

Praktikum 5 membahas penerapan konsep polimorfisme dalam pemrograman berorientasi objek menggunakan Java dan PHP.

Program yang dibuat digunakan untuk menghitung luas dan keliling beberapa bangun datar, yaitu lingkaran, persegi, segitiga, dan trapesium. Class `BangunDatar` digunakan sebagai class induk, sedangkan setiap bangun datar memiliki perhitungan luas dan keliling sesuai bentuknya.

Praktikum ini juga membahas contoh *anti-pattern* dan proses refaktor untuk membuat struktur program menjadi lebih baik.

## 2. Implementasi Java

### A. Kode Sebelum Perbaikan

Pada kode Java sebelum perbaikan, program digunakan untuk menunjukkan contoh penerapan bangun datar dan permasalahan struktur kode (*anti-pattern*). Struktur kode tersebut kemudian diperiksa agar dapat diperbaiki sesuai konsep pemrograman berorientasi objek.

**Kode sebelum perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan5/java)

### B. Kode Setelah Perbaikan

Pada kode Java setelah perbaikan, class `BangunDatar` digunakan sebagai class induk, sedangkan `Lingkaran`, `Persegi`, `Segitiga`, dan `Trapesium` menjadi class turunannya.

Perbaikan yang dilakukan meliputi:

- Menggunakan pewarisan antara class induk dan class turunan.
- Menerapkan polimorfisme melalui method luas dan keliling.
- Menyesuaikan perhitungan berdasarkan bentuk bangun datar.
- Memperbaiki struktur kode melalui proses refaktor.
- Menampilkan hasil perhitungan luas dan keliling setiap bangun datar.

**Kode setelah perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan5/src))

## 3. Implementasi PHP

### A. Kode Sebelum Perbaikan

Pada kode PHP sebelum perbaikan, program digunakan sebagai contoh implementasi bangun datar dan struktur kode yang perlu diperbaiki. Program kemudian disesuaikan agar lebih terstruktur dan menerapkan konsep pemrograman berorientasi objek.

**Kode sebelum perbaikan PHP:**

[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan5/php)

### B. Kode Setelah Perbaikan

Pada kode PHP setelah perbaikan, konsep polimorfisme diterapkan agar setiap bangun datar dapat memiliki implementasi perhitungan luas dan keliling masing-masing.

Perbaikan yang dilakukan meliputi:

- Mengatur class induk dan class turunan.
- Membuat method perhitungan sesuai bentuk bangun datar.
- Menerapkan polimorfisme pada perhitungan luas dan keliling.
- Memperbaiki struktur kode agar lebih mudah dibaca dan dikelola.
- Menampilkan hasil perhitungan bangun datar melalui program utama.

**Kode setelah perbaikan PHP:**

[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan5/src)

## 4. Bukti Eksekusi

### A. Eksekusi Java

**Sebelum perbaikan**

<img width="359" height="148" alt="Pertemuan5" src="https://github.com/user-attachments/assets/dda5f48b-05ac-4bcc-ac82-8582af58fe53" />


**Sesudah perbaikan**

<img width="497" height="186" alt="Pertemuan5" src="https://github.com/user-attachments/assets/ba15a749-42e5-4bc3-a4d7-1c4338daca74" />


### B. Eksekusi PHP

**Sebelum perbaikan**

<img width="413" height="152" alt="Pertemuan5" src="https://github.com/user-attachments/assets/0aaa3271-023c-4e31-a1ba-f2957614e787" />

**Sesudah perbaikan**

<img width="456" height="205" alt="Pertemuan5" src="https://github.com/user-attachments/assets/c7e07642-2df2-4515-a7b9-133b5da80e61" />


## 5. Kesimpulan

Berdasarkan praktikum yang telah dilakukan, polimorfisme memungkinkan setiap class bangun datar memiliki implementasi method luas dan keliling yang berbeda. Dengan menggunakan class induk dan class turunan, program dapat dibuat lebih terstruktur dan mudah dikembangkan.

Melalui praktikum ini, saya memahami penerapan polimorfisme dalam Java dan PHP serta pentingnya melakukan refaktor untuk memperbaiki struktur kode agar lebih mudah dibaca dan dipelihara.
