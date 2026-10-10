# Keputusan Desain - Praktikum 06
## Nevilla Ghilar Apryanti
## NPM: 4525210054

## Langkah 4: Penolakan Saat Kompilasi

Setelah membuat class `Sepeda`, saya mencoba memanggil method `isiPenuh(sepeda)` pada file `Main.java`. Namun, compiler menampilkan pesan kesalahan berikut:

```text
The method isiPenuh(Fuelable) in the type Main is not applicable for the arguments (Sepeda)
```

### Alasan Penolakan Saat Kompilasi Menguntungkan

Method `isiPenuh` menggunakan parameter bertipe `Fuelable`. Jadi, method tersebut hanya dapat menerima objek yang memiliki kemampuan untuk diisi bahan bakar, tanpa harus bergantung pada jenis class tertentu.

Sementara itu, class `Sepeda` hanya mengimplementasikan interface `Movable` dan tidak mengimplementasikan `Fuelable`, karena sepeda tidak memiliki tangki bahan bakar. Oleh sebab itu, Java menolak pemanggilan method tersebut sebelum program dijalankan.

Menurut saya, hal ini memberikan beberapa keuntungan:

1. **Kesalahan dapat diketahui lebih awal.** Compiler langsung menunjukkan kesalahan ketika kode ditulis sehingga bisa diperbaiki sebelum program dijalankan.
2. **Mencegah penggunaan method yang tidak sesuai.** Method pengisian bahan bakar tidak bisa digunakan pada objek yang memang tidak membutuhkan bahan bakar.
3. **Mengurangi pengecekan tambahan.** Programmer tidak perlu menambahkan pemeriksaan jenis objek secara manual di dalam method karena tipe parameter sudah membatasi objek yang bisa digunakan.
4. **Lebih mudah dikembangkan.** Class baru yang mengimplementasikan `Fuelable` dapat menggunakan method `isiPenuh` tanpa perlu mengubah isi method tersebut.

Setelah mencatat pesan kesalahan, saya menjadikan baris `isiPenuh(sepeda);` sebagai komentar agar program dapat dikompilasi dan dijalankan tanpa kesalahan tersebut.

## Perbandingan dengan PHP

Pada PHP, kesalahan serupa terjadi ketika program dijalankan dan menghasilkan `TypeError` karena objek `Sepeda` tidak sesuai dengan tipe parameter `Fuelable`.

Berbeda dengan Java yang memeriksa kesesuaian tipe melalui compiler sebelum program dijalankan, PHP menunjukkan kesalahan tersebut saat proses eksekusi. Dengan demikian, pemeriksaan tipe di Java membantu menemukan kesalahan lebih awal.
