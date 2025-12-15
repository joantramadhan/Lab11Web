# Praktikum 11: Web Programming - PHP OOP Lanjutan

## Deskripsi
Praktikum ini bertujuan untuk menerapkan konsep **Framework Modular** dan **Routing** pada aplikasi web berbasis PHP. [cite_start]Kode program dipisahkan berdasarkan fungsinya (Konfigurasi, Library, Modul, dan Template) agar lebih terstruktur dan mudah dikelola [cite: 4, 11-34].

---

## Langkah-langkah Praktikum

### 1. Persiapan Struktur Folder
Membuat folder baru `lab11_php_oop` dan menyusun struktur direktori untuk memisahkan komponen aplikasi (Model-View-Controller sederhana).

- [cite_start]**class/**: Menyimpan library (`Database.php`, `Form.php`)[cite: 19].
- [cite_start]**module/**: Menyimpan logika halaman website[cite: 23].
- [cite_start]**template/**: Menyimpan layout (`header`, `footer`)[cite: 30].

<img width="217" height="283" alt="image" src="https://github.com/user-attachments/assets/4edbf136-eb16-4e70-b509-b19a4c3391eb" />


### 2. Konfigurasi dan Library
Saya memindahkan file `Database.php` dan `Form.php` ke folder `class/` dan membuat file `config.php` untuk menyimpan konfigurasi database secara terpusat.



### 3. Implementasi Routing (URL Rewrite)
Routing digunakan untuk membuat URL yang bersih (*Clean URL*) dan mengarahkan semua request ke satu pintu masuk.

- [cite_start]**.htaccess**: Mengarahkan semua request URL ke `index.php` [cite: 300-313].
- [cite_start]**index.php**: Berfungsi sebagai *Entry Point* yang memanggil modul berdasarkan request URL [cite: 314-347].

---

## Hasil Implementasi Modular

### 1. Tampilan Halaman Utama (Home)
Ketika mengakses `localhost/lab11_php_oop/`, sistem routing akan mengarahkan ke modul default (`home`) dan memuat template header/footer secara otomatis.

**Tampilan Browser:**
<img width="888" height="529" alt="image" src="https://github.com/user-attachments/assets/171eeb2c-2e8a-45d2-bced-6c4015b20a70" />


### 2. Menambah Data (Create)
Saya membuat form input untuk:
1.judul
2.kategori
3.isi
4.tanggal

Data kemudian disimpan menggunakan method $db->insert().

**Tampilan Form Tambah Data:**
<img width="1656" height="897" alt="image" src="https://github.com/user-attachments/assets/17681f92-68ca-4250-b185-c23b744c73c9" />


### 3. Struktur Modul Artikel
Logika program untuk fitur artikel disimpan terpisah di dalam folder `module/artikel/` yang berisi file `index.php`, `tambah.php`, dan `ubah.php`.

<img width="1510" height="144" alt="image" src="https://github.com/user-attachments/assets/dbd11327-1880-44ee-9bbd-bc682eebde3c" />


---

## Kesimpulan
Dengan menerapkan konsep Modular dan Routing, struktur aplikasi menjadi lebih rapi. URL menjadi lebih *user-friendly* dan kode program lebih mudah dikembangkan karena pemisahan yang jelas antara logika, tampilan, dan konfigurasi.

## Update 
### menambah home + Login 
<img width="1656" height="897" alt="image" src="https://github.com/user-attachments/assets/37777f50-875a-4ac9-ac78-0801e3d714fa" />
### User name : operator Password : password
<img width="1656" height="897" alt="image" src="https://github.com/user-attachments/assets/f0aaa5d5-3b13-41b0-a6a8-2871b84717d2" />
### Menambah opsi log out + home
<img width="1656" height="897" alt="image" src="https://github.com/user-attachments/assets/4ba90028-e498-40b1-80b8-46b846256d0a" />


