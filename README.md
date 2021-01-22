# Bahasa Pemrograman Rust

![Build Status](https://github.com/rust-lang/book/workflows/CI/badge.svg)

Repositori ini berisi sumber dari buku "The Rust Programming Language".

[Buku tersebut tersedia dalam format dead-tree dari No Starch Press][nostarch].

[nostarch]: https://nostarch.com/rust

Kamu juga bisa mendapatkannya secara daring dengan gratis. Silakan lihat buku tersebut 
yang tersedia dengan rilis Rust terbaru versi [stable], [beta], atau [nightly]. Mohon diperhatikan 
bahwa isu-isu yang terdapat pada versi-versi di atas kemungkinan sudah diperbaiki di repositori ini, 
karena versi di atas lebih jarang mendapatkan pembaruan.

[stable]: https://doc.rust-lang.org/stable/book/
[beta]: https://doc.rust-lang.org/beta/book/
[nightly]: https://doc.rust-lang.org/nightly/book/

Lihat [releases] untuk mengunduh kode sumber saja dari semua kode sumber yang ada di buku tersebut.

[releases]: https://github.com/rust-lang/book/releases

## Persyaratan

Kamu membutuhkan [mdBook] untuk membentuk buku ini, idealnya menggunakan versi yang sama dengan 
rust-lang/rust yang digunakan di [berkas ini][rust-mdbook]. Untuk mendapatkannya:

[mdBook]: https://github.com/rust-lang-nursery/mdBook
[rust-mdbook]: https://github.com/rust-lang/rust/blob/master/src/tools/rustbook/Cargo.toml

```bash
$ cargo install mdbook --vers [version-num]
```

## Building

To build the book, type:

```bash
$ mdbook build
```

Hasilnya akan berada di subdirektori `book`. Gunakan perambanmu untuk memeriksanya.

_Firefox:_
```bash
$ firefox book/index.html                       # Linux
$ open -a "Firefox" book/index.html             # OS X
$ Start-Process "firefox.exe" .\book\index.html # Windows (PowerShell)
$ start firefox.exe .\book\index.html           # Windows (Cmd)
```

_Chrome:_
```bash
$ google-chrome book/index.html                 # Linux
$ open -a "Google Chrome" book/index.html       # OS X
$ Start-Process "chrome.exe" .\book\index.html  # Windows (PowerShell)
$ start chrome.exe .\book\index.html            # Windows (Cmd)
```

Untuk menjalankan test:

```bash
$ mdbook test
```

## Kontribusi

Kami senang akan bantuanmu! Silakan lihat [CONTRIBUTING.md][contrib] untuk mempelajari macam kontribusi apa yang sekiranya kamu cari.

[contrib]: https://github.com/rust-lang/book/blob/master/CONTRIBUTING.md

### Penerjemahan

Kami akan sangat senang membantu menerjemahkan buku! Silakan lihat label [Translations] untuk bergabung dengan upaya penerjemahan yang sedang berlangsug. Buka sebuah isu baru untuk memulai penerjemahan ke dalam bahasa baru! Kami  menunggu [mdbook support] di berbagai bahasa sebelum menggabungkannya, for multiple languages before we merge any in, namun silakan saja untuk memulai!

[Translations]: https://github.com/rust-lang/book/issues?q=is%3Aopen+is%3Aissue+label%3ATranslations
[mdbook support]: https://github.com/rust-lang-nursery/mdBook/issues/5

## Pemeriksaan Ejaan

Untuk memindai kesalahan ejaan di berkas sumber, kamu dapat menggunakan skrip `spellcheck.sh`
. Diperlukan kamus kata-kata yang valid, yang disediakan di
`dictionary.txt`. Jika hasil skrip adalah _false positive_ (katakanlah, kamu menggunakan kata
`BTreeMap` yang dianggap skrip tidak valid), kamu perlu menambahkan kata tersebut ke
`dictionary.txt` (pastikan urutannya tetap konsisten).