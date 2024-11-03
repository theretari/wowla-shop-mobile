# Tugas Pemograman Mobile Wowla Shop

## Data Diri
Theresia Tarianingsih
2306208810
PBP-C

## Readme Tugas 7
1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
    - ```Stateless Widget``` adalah widget yang tidak memiliki state yang dapat berubah. Widget ini digunakan untuk menampilkan data yang statis dan tidak membutuhkan perubahan dalam tampilan setelah di-render. Karena tidak memiliki state, StatelessWidget hanya memiliki satu kali proses build, sehingga cocok untuk tampilan statis.
    - ```Stateful Widget``` adalah widget yang memiliki state yang dapat berubah seiring waktu. Widget ini memungkinkan perubahan dalam tampilan atau data yang ditampilkan tanpa harus membuat ulang widget tersebut dari awal. Setiap perubahan state pada widget ini akan memanggil ```setState()``` dan menyebabkan widget tersebut di-render ulang dengan tampilan atau data yang diperbarui.

2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
    - Material app: mengatur tema aplikasi dan memulai dari halaman MyHomePage.
    - Scaffold: untuk membentuk layout utama halaman dengan bagian atas yang diisi oleh AppBar.
    - AppBar: menampilkan judul “Wowla Shop” dengan gaya teks yang khusus.
    - SnackBar: menampilkan pesan sementara di bagian bawah layar sebagai notifikasi singkat.
    - InfoCard: menampilkan informasi seperti NPM, Name, dan Class dengan tampilan kotak.

3. Apa fungsi dari ```setState()```? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
    ```setState()``` adalah metode yang digunakan pada StatefulWidget untuk memberitahukan bahwa ada perubahan pada state widget yang harus di-render ulang. Dengan setState(), Flutter mengetahui bahwa tampilan harus diperbarui sesuai dengan state yang baru. Seluruh variabel yang dideklarasikan dalam State dari statefulWidget terdampak oleh ```setState()```

4. Jelaskan perbedaan antara const dengan final.
    - ```const``` digunakan untuk mendeklarasikan nilai konstan yang diketahui pada saat kompilasi dan tidak akan berubah selama runtime. 
    - ```final``` digunakan untuk mendeklarasikan nilai yang tidak dapat diubah setelah diinisialisasi, namun nilai final ditentukan saat runtime sehingga lebih fleksibel dibandingkan const

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
    Pertama saya membuat proyek flutter baru bernama wowla shop. setelah itu saya membuat file baru bernama menu.dart dan memindahkan kode ```class MyHomePage``` dan ```class _MyHomePageState```. Pada file main.dart saya mengimport menu.dart sehingga dapat mengakses seluruh class yang telah dipindahkan. Setelah itu saya menentukan warna aplikasi, yakni biru pada main.dart dan mengubah sifat widget menjadi stateless. lalu saya membuat card yang berisi nama, npm, dan kelas. lalu membuat button card yang berisi nama dan icon. serta membuat list item home page yan berisi lihat produk, tambah produk, dan logout. Lalu saya mengintegrasikan infocard dan itemcard untuk ditampilkan dalam homepage.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
