# Bahasa Pemrograman Rust

*oleh Steve Klabnik dan Carol Nichols, dengan kontribusi dari komunitas Rust*

Di versi ini kami mengasumsikan anda menggunakan Rust 1.41.0 atau versi terbaru dengan 
`edition="2018"` di *Cargo.toml* dari semua proyek untuk menggunakan idiom Edisi Rust 2018. Lihat [bagian “Instalasi” di Bab 1][install]<!-- ignore -->
untuk menginstal atau memperbarui Rust, dan lihat [Lampiran E][editions]<!-- ignore--> yang baru untuk informasi edisi-edisi yang ada.

Bahasa Rust Edisi 2018 mencakup sejumlah peningkatan yang membuat Rust lebih ergonomis dan lebih mudah dipelajari. Iterasi buku ini berisi sejumlah perubahan untuk mencerminkan peningkatan tersebut:

- Bab 7, Mengelola Proyek dengan _Package_, _Crate_, dan Modul,”
  sebagian besar telah ditulis ulang. Sistem modul dan cara kerja _path_ di Edisi 2018 
  telah dibuat ubntuk lebih konsisten.
- Bab 10 mempunyai bagian baru yang berjudul “_Traits_ sebagai Parameter” dan “Mengembalikan Tipe yang Mengimplementasikan _Traits_” yang menjelaskan tentang sintaks  `impl Trait` baru.
- Bab 11 mempunyai bagian baru yang berjudul “Menggunakan `Result<T, E>` di Tes” yang 
  menunjukkan cara menulis test yang menggunakan operator `?`.
- Bagian “_Lifetime_ Lanjutan” di Bab 19 telah dihilangkan karena perbaikan kompilator
  membuat _construct_ dibagian ini semakin jarang digunakan.
- Lampiran D sebelumnya, “Makro,” telah dikembangkan dengan memasukkan makro procedural
  dan dipindahkan ke bagian “Makro” di Bab 19.
- Lampiran A, “Keywords,” juga menjelaskan fitur _raw identifier_ yang
  memungkinkan kode yang ditulis menggunakan edisi 2015 bekerja edisi 2018 dan sebaliknya.
- Lampiran D sekarang berjudul Alat-alat Pengembangan yang Berguna” dan mencakup 
  alat-alat yang baru saa dirilis untuk membantu anda menulis kode-kode Rust.
- Kami memperbaiki sejumlah kesalahan kecil dan kata-kata yang tidak tepat di seluruh buku.
  Terima kasih kepada anda para pembaca yang telah melaporkannya ke kami!

Perlu dicatat bahwa kode di iterasi *Bahasa Pemrograman Rust* sebelumnya
yang telah terkompilasi akan tetap dikompilasi tanpa mendefinisikan `edition="2018"` di dalam
*Cargo.toml*, walaupun anda telah memperbarui versi kompilator Rust yang anda gunakan. Hal tersebut adalah _backward compatibility_ dari Rust!

Format HTML tersedia secara dasring di 
[https://doc.rust-lang.org/stable/book/](https://doc.rust-lang.org/stable/book/)
dan luring bersama instalasi Rust yang dibuat dengan `rustup`; jalankan `rustup docs
--book` untuk membukanya.

Teks ini tersedia dalam [format kertas dan ebook dari No Starch
Press][nsprust].

[install]: ch01-01-installation.html
[editions]: Lampiran-05-editions.html
[nsprust]: https://nostarch.com/rust
