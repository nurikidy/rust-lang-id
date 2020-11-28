# Introduction

> Catatan: Buku edisi ini sama dengan [The Rust Programming
> Language][nsprust] yang tersedia dalam bentuk cetak dan ebook dari [No Starch
> Press][nsp].

[nsprust]: https://nostarch.com/rust
[nsp]: https://nostarch.com/

Selamat datang di *Bahasa Pemrograman Rust*, sebuah pengenalan akan Rust.
Bahasa Pemrograman Rust membantu anda menulis perangkat lunak dengan lebih cepat dan lebih andal.
Ergonomi tingkat tinggi dan kontrol tingkat rendah sering kali bertentangan dalam desain sebuah bahasa pemrograman; Rust challenges that conflict. Through balancing powerful
technical capacity and a great developer experience, Rust gives you the option
to control low-level details (such as memory usage) without all the hassle
traditionally associated with such control.

## Who Rust Is For

Rust is ideal for many people for a variety of reasons. Let’s look at a few of
the most important groups.

### Teams of Developers

Rust is proving to be a productive tool for collaborating among large teams of
developers with varying levels of systems programming knowledge. Low-level code
is prone to a variety of subtle bugs, which in most other languages can be
caught only through extensive testing and careful code review by experienced
developers. In Rust, the compiler plays a gatekeeper role by refusing to
compile code with these elusive bugs, including concurrency bugs. By working
alongside the compiler, the team can spend their time focusing on the program’s
logic rather than chasing down bugs.

Rust also brings contemporary developer tools to the systems programming world:

* Cargo, the included dependency manager and build tool, makes adding,
  compiling, and managing dependencies painless and consistent across the Rust
  ecosystem.
* Rustfmt ensures a consistent coding style across developers.
* The Rust Language Server powers Integrated Development Environment (IDE)
  integration for code completion and inline error messages.

By using these and other tools in the Rust ecosystem, developers can be
productive while writing systems-level code.

### Students

Rust is for students and those who are interested in learning about systems
concepts. Using Rust, many people have learned about topics like operating
systems development. The community is very welcoming and happy to answer
student questions. Through efforts such as this book, the Rust teams want to
make systems concepts more accessible to more people, especially those new to
programming.

### Companies

Hundreds of companies, large and small, use Rust in production for a variety of
tasks. Those tasks include command line tools, web services, DevOps tooling,
embedded devices, audio and video analysis and transcoding, cryptocurrencies,
bioinformatics, search engines, Internet of Things applications, machine
learning, and even major parts of the Firefox web browser.

### Open Source Developers

Rust is for people who want to build the Rust programming language, community,
developer tools, and libraries. We’d love to have you contribute to the Rust
language.

### People Who Value Speed and Stability

Rust is for people who crave speed and stability in a language. By speed, we
mean the speed of the programs that you can create with Rust and the speed at
which Rust lets you write them. The Rust compiler’s checks ensure stability
through feature additions and refactoring. This is in contrast to the brittle
legacy code in languages without these checks, which developers are often
afraid to modify. By striving for zero-cost abstractions, higher-level features
that compile to lower-level code as fast as code written manually, Rust
endeavors to make safe code be fast code as well.

The Rust language hopes to support many other users as well; those mentioned
here are merely some of the biggest stakeholders. Overall, Rust’s greatest
ambition is to eliminate the trade-offs that programmers have accepted for
decades by providing safety *and* productivity, speed *and* ergonomics. Give
Rust a try and see if its choices work for you.

## Who This Book Is For

This book assumes that you’ve written code in another programming language but
doesn’t make any assumptions about which one. We’ve tried to make the material
broadly accessible to those from a wide variety of programming backgrounds. We
don’t spend a lot of time talking about what programming *is* or how to think
about it. If you’re entirely new to programming, you would be better served by
reading a book that specifically provides an introduction to programming.

## How to Use This Book

In general, this book assumes that you’re reading it in sequence from front to
back. Later chapters build on concepts in earlier chapters, and earlier
chapters might not delve into details on a topic; we typically revisit the
topic in a later chapter.

You’ll find two kinds of chapters in this book: concept chapters and project
chapters. In concept chapters, you’ll learn about an aspect of Rust. In project
chapters, we’ll build small programs together, applying what you’ve learned so
far. Chapters 2, 12, and 20 are project chapters; the rest are concept chapters.

Chapter 1 explains how to install Rust, how to write a “Hello, world!” program,
and how to use Cargo, Rust’s package manager and build tool. Chapter 2 is a
hands-on introduction to the Rust language. Here we cover concepts at a high
level, and later chapters will provide additional detail. If you want to get
your hands dirty right away, Chapter 2 is the place for that. At first, you
might even want to skip Chapter 3, which covers Rust features similar to those
of other programming languages, and head straight to Chapter 4 to learn about
Rust’s ownership system. However, if you’re a particularly meticulous learner
who prefers to learn every detail before moving on to the next, you might want
to skip Chapter 2 and go straight to Chapter 3, returning to Chapter 2 when
you’d like to work on a project applying the details you’ve learned.

Chapter 5 discusses structs and methods, and Chapter 6 covers enums, `match`
expressions, and the `if let` control flow construct. You’ll use structs and
enums to make custom types in Rust.

In Chapter 7, you’ll learn about Rust’s module system and about privacy rules
for organizing your code and its public Application Programming Interface
(API). Chapter 8 discusses some common collection data structures that the
standard library provides, such as vectors, strings, and hash maps. Chapter 9
explores Rust’s error-handling philosophy and techniques.

Chapter 10 digs into generics, traits, and lifetimes, which give you the power
to define code that applies to multiple types. Chapter 11 is all about testing,
which even with Rust’s safety guarantees is necessary to ensure your program’s
logic is correct. In Chapter 12, we’ll build our own implementation of a subset
of functionality from the `grep` command line tool that searches for text
within files. For this, we’ll use many of the concepts we discussed in the
previous chapters.

Chapter 13 explores closures and iterators: features of Rust that come from
functional programming languages. In Chapter 14, we’ll examine Cargo in more
depth and talk about best practices for sharing your libraries with others.
Chapter 15 discusses smart pointers that the standard library provides and the
traits that enable their functionality.

In Chapter 16, we’ll walk through different models of concurrent programming
and talk about how Rust helps you to program in multiple threads fearlessly.
Chapter 17 looks at how Rust idioms compare to object-oriented programming
principles you might be familiar with.

Bab 18 adalah referensi dari pola dan pencocokan pola, yang merupakan cara yang sangat ampuh
untuk mengekspresikan ide di pemrograman Rust. Bab 19 berisi sebuah 
kumpulan dari topik-topik lanjutan yang menarik, termasuk _unsafe_ Rust, makro, dan 
penjelasan lebih lanjut akan masa hidup, _trait_, tipe, fungsi dan _closure_.

Di Bab 20, kita akan menyelesaikan sebuah proyek yang berupa implementasi low-level
multithreaded pada sebuah web server!

Terakhir, beberapa lampiran berisi informasi berguna tentang Rust dalam format yang lebih
mirip referensi. Lampiran A mencakup kata kunci Rust, Lampiran B 
mencakup operator dan simbol Rust, Lampiran C mencakup sifat yang dapat diturunkan 
yang disediakan oleh perpustakaan standar, Lampiran D mencakup beberapa alat pengembangan yang berguna, dan Lampiran E menjelaskan edisi Rust.

Tidak ada cara yang salah untuk membaca buku ini: jika Anda ingin meliwati beberapa bagian, silakan!
Anda mungkin harus melompat kembali ke bab sebelumnya jika Anda mengalami
kebingungan. Lakukan apa yang menurut anda paling cocok.

<span id="ferris"></span>

Bagian penting dalam proses mempelajari Rust adalah belajar bagaimana membaca
pesan-pesan galat yang ditampilkan oleh kompilator: hal ini akan membantu anda kode yang bekerja dengan benar.

Maka dari itu, kami akan memberikan banyak contoh kode yang tidak dapat dikompulasi beserta 
pesan galat kompilator dalam berbagai situasi. 
As such, we’ll provide many examples that don’t compile along with the error
message the compiler will show you in each situation. Untuk diketahui jika anda 
secara asal 
memasukkan dan menjalankan contoh, kode tersebut mungkin tidak dapat dikompilasi!  Pastikan anda membaca 
teks disekelilingnya untuk melihat apakah contoh yang anda sedang coba untk jalankan
memang ditujukan untuk tidak dapat bekerja. 
Ferris juga dapat membantu anda membedakan kode mana yang memang tidak dimaksudkan untuk bekerja:

| Ferris                                                                 | Arti                                          |
|------------------------------------------------------------------------|--------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain"/>    | Kode ini tidak dapat dikompilasi!                      |
| <img src="img/ferris/panics.svg" class="ferris-explain"/>              | Kode ini _panics_!                                |
| <img src="img/ferris/unsafe.svg" class="ferris-explain"/>              | Blok ini mengandung kode yang tidak aman.            |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain"/>| Kode ini tidak menghasilkan kondisi yang diinginkan. |

Di kebanyakan situasi, kami akan memandu anda ke bagian yang benar dari kode yang tidak dapat dikompilaso.

## Kode Sumber

Berkas-berkas sumber buku ini dibuat dapat ditemukan di [GitHub][book].

[book]: https://github.com/rust-lang/book/tree/master/src
