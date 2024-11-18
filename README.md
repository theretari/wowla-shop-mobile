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

## Readme Tugas 8
1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
    - Const digunakan untuk menandai nilai yang bersifat tetap dan tidak berubah saat waktu kompilasi dan runtime. Keuntungannya adalah efisiensi memori dan mempercepat waktu render dan membuat aplikasi lebih responsif. Sebaiknya digunakan untuk menetapkan pada ikon tetap atau dekorasi tidak dinamis, tidak digunakan jika widget bersifat interaktif (memerlukan input)

2.  Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
    - Column:  widget yang menyusun elemen anaknya secara vertikal, dari atas ke bawah. 
    - Row: widget yang menyusun elemen anaknya secara horizontal, dari kiri ke kanan.

3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
    - Elemen input yang digunakan
        - TextFormField: Digunakan untuk input teks seperti “mood” dan “feelings”.
        - ElevatedButton: Sebagai tombol untuk menyimpan atau mengirim data form.
    - Elemen input yang tidak digunakan 
        - Checkbox: Digunakan untuk pilihan dengan opsi true atau false.
        - Radio Button: Memungkinkan pengguna memilih satu opsi dari beberapa pilihan.
        - Switch: Berfungsi seperti Checkbox, tetapi lebih modern dalam tampilan on/off.
        - Slider: Untuk memilih nilai dari rentang tertentu, seperti skala intensitas.
        - Dropdown Button: Untuk pilihan yang menampilkan daftar pilihan tertentu

4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
    - Untuk menjaga konsistensi tema, kita dapat mendefinisikan ThemeData pada root widget MaterialApp.

5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
    - Salah satu cara yang dapat digunakan untuk berpindah-pindah halaman adalah dengan menggunakan widget navigator. Untuk menavigasu sebuah halaman baru, kita dapat mengakses navigator melalui BuildContext dan memanggil fungsi yang ada, yaitu:
        - push():  menambahkan suatu route ke dalam stack route yang dikelola oleh Navigator. Method ini menyebabkan route yang ditambahkan berada pada paling atas stack, sehingga route yang baru saja ditambahkan tersebut akan muncul dan ditampilkan kepada pengguna.
        - pop(): menghapus route yang sedang ditampilkan kepada pengguna (atau dalam kata lain, route yang berada pada paling atas stack) dari stack route yang dikelola oleh Navigator. Method ini menyebabkan aplikasi untuk berpindah dari route yang sedang ditampilkan kepada pengguna ke route yang berada di bawahnya pada stack yang dikelola Navigator.
        - pushReplacement(): Method pushReplacement() menghapus route yang sedang ditampilkan kepada pengguna dan menggantinya dengan suatu route. Method ini menyebabkan aplikasi untuk berpindah dari route yang sedang ditampilkan kepada pengguna ke suatu route yang diberikan. Pada stack route yang dikelola Navigator, route lama pada atas stack akan digantikan secara langsung oleh route baru yang diberikan tanpa mengubah kondisi elemen stack yang berada di bawahnya.


## Readme Tugas 9
1. Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?
    Model membantu menyusun data JSON ke dalam struktur yang terorganisir sehingga mudah dikelola dalam aplikasi. Selain itu, model memungkinkan validasi data untuk memastikan data JSON sesuai dengan format yang diharapkan serta mempermudah pengelolaan data. Jika tidak dibuat model mungkin saja tidak error namun kita harus decode data yang mentah.

2. Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini
    untuk melakukan komunikasi antara flutter dan django, seperti mengirim request HTTP, menambil data dari server, dan autentifikasi

3. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
    untuk mengelola cookie di aplikasi Flutter, terutama dalam autentikasi. Memungkinkan pengiriman dan penerimaan cookie dari backend, sehingga sesi pengguna dapat dikelola.Selain itu digunakan untuk mempertahankan status login pengguna di berbagai permintaan HTTP. Instance CookieRequest perlu dibagikan agar semua komponen aplikasi memiliki akses ke sesi pengguna yang sama.

4. Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.
    input data di fluter, kirim ke backend django, pemrosesan di backend django, kirim ke fluter dengan json, menampilkan data di flutter

5. Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
    memasukkan data yang dibutuhkan lalu flutter akan mengirimkan data tersebut dalam bentuk json ke django, lalu django memproses permintaan tersebut, setelah itu hasilnya dikirimkan dalam bentuk json dan ditampilkan ke flutter


6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
    pertama saya membuat django app authentication lalu membuat seluruh fitur atuhentication mulai dari regist, login, logout. setelah itu saya mengintegrasikan pada flutter berdasarkan request user yang sedang login. lalu saya membuat model kustom json yang terintegrasi dengan flutter. lalu mengintegrasikan model tsb dengan form. untuk mengambil seluruh data dari web saya menerapkan fetching dependensi http.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
