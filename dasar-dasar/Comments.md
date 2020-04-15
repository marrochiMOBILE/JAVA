# Comments


Komentar dapat digunakan untuk menjelaskan kode Java, dan membuatnya lebih mudah dibaca. Itu juga dapat digunakan untuk mencegah eksekusi ketika menguji kode alternatif.

Komentar baris tunggal dimulai dengan dua garis miring (//).

Teks apa pun antara // dan akhir baris diabaikan oleh Java (tidak akan dieksekusi).

Contoh ini menggunakan komentar satu baris sebelum satu baris kode

```java
// komentar disini bebas -> tujuanya untuk menjelaskan program tersebut
System.out.println("Hello World");
```

Contoh ini menggunakan komentar satu baris di akhir baris kode:

```java
System.out.println("Hello World"); // komentar disini bebas -> tujuanya untuk menjelaskan program tersebut
```

## Java Multi-line Comments

Komentar multi-baris dimulai dengan / * dan diakhiri dengan * /.

Teks apa pun antara / * dan * / akan diabaikan oleh Java.

Contoh ini menggunakan komentar multi-baris (blok komentar) untuk menjelaskan kode:

```java
/* 
Kode di bawah ini akan mencetak kata Hello World
ke layar, dan itu luar biasa
*/
System.out.println("Hello World");
```
