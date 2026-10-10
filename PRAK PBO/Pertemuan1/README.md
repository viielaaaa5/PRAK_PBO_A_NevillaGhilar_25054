# Pertemuan 1 - Git dan GitHub

* Nama: Nevilla Ghilar Apryanti
* NPM: 4525210054

## 1. Instalasi Git

Langkah pertama adalah mengecek apakah Git sudah terpasang di komputer.

```bash
git --version
```

Jika Git sudah terpasang, terminal akan menampilkan versi Git yang digunakan.

## 2. Konfigurasi Git

Konfigurasi dilakukan untuk mengatur identitas pengguna Git.

### Mengatur Nama

```bash
git config --global user.name "Nevilla Ghilar Apryanti"
```

### Mengatur Email

```bash
git config --global user.email "nevillaghilar70@gmail.com"
```

### Mengatur Branch Utama

```bash
git config --global init.defaultBranch main
```

### Mengecek Konfigurasi

```bash
git config --global --list
```

Perintah tersebut digunakan untuk melihat konfigurasi Git yang sudah diatur.

## 3. Membuat SSH Key

SSH Key digunakan untuk menghubungkan komputer dengan akun GitHub.

### Membuat SSH Key

```bash
ssh-keygen -t ed25519 -C "nevillaghilar70@gmail.com"
```

Ikuti petunjuk yang muncul di terminal sampai proses selesai.

### Menjalankan SSH Agent

```bash
eval "$(ssh-agent -s)"
```

### Menambahkan SSH Key

```bash
ssh-add ~/.ssh/id_ed25519
```

### Melihat Public Key

```bash
cat ~/.ssh/id_ed25519.pub
```

Salin public key yang muncul, lalu buka GitHub dan masuk ke menu Settings → SSH and GPG keys → New SSH key. Tempelkan public key tersebut, kemudian simpan.

## 4. Pengujian Koneksi GitHub

Setelah SSH Key ditambahkan, lakukan pengujian koneksi dengan perintah berikut.

```bash
ssh -T git@github.com
```

Jika koneksi berhasil, terminal akan menampilkan pesan bahwa autentikasi berhasil dilakukan oleh GitHub.

## Kesimpulan

Dari praktikum ini, Git berhasil dikonfigurasi menggunakan nama dan email pengguna. SSH Key juga dibuat untuk menghubungkan komputer dengan GitHub, kemudian koneksi diuji melalui terminal.
