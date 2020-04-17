# If ... Else

## Java Conditions and If Statements
Java mendukung kondisi logis yang biasa dari matematika:

  <ul>
       <li>Kurang dari: a <b</li>
       <li>Kurang dari atau sama dengan: a <= b</li>
       <li>Lebih besar dari: a> b</li>
       <li>Lebih besar atau sama dengan: a> = b</li>
       <li>Sama dengan a == b</li>
       <li>Tidak Setara dengan: a! = B</li>
       <li>Anda dapat menggunakan kondisi ini untuk melakukan tindakan berbeda untuk keputusan yang berbeda.</li>
   </ul>


Java memiliki pernyataan kondisional berikut:
  <ul>
       <li>Gunakan jika/if untuk menentukan blok kode yang akan dieksekusi, jika kondisi yang ditentukan benar</li>
       <li>Gunakan yang lain/else untuk menentukan blok kode yang akan dieksekusi, jika kondisi yang sama salah</li>
       <li>Gunakan lagi jika/else if untuk menentukan kondisi baru untuk diuji, jika kondisi pertama salah</li>
       <li>Gunakan sakelar/switch untuk menentukan banyak blok kode alternatif yang akan dieksekusi</li>
   </ul>

## The if Statement

Gunakan pernyataan if untuk menentukan blok kode Java yang akan dieksekusi jika kondisinya benar.

```java
if (condition) {
  // block of code to be executed if the condition is true
}
```

> Perhatikan bahwa jika dalam huruf kecil. Huruf besar (Jika atau IF) akan menghasilkan kesalahan.

Dalam contoh di bawah ini, kami menguji dua nilai untuk mengetahui apakah 20 lebih besar dari 18. Jika kondisinya benar, cetak beberapa teks:
```java
if (20 > 18) {
  System.out.println("20 is greater than 18"); // 20 is greater than 18
}
```

Kami juga dapat menguji variabel:
```java
int x = 20;
int y = 18;
if (x > y) {
  System.out.println("x is greater than y"); // x is greater than y / x lebih besar dari y
}
```
#### Contoh dijelaskan
Pada contoh di atas kita menggunakan dua variabel, x dan y, untuk menguji apakah x lebih besar dari y (menggunakan operator `>` ). Karena x adalah 20, dan y adalah 18, dan kita tahu bahwa 20 lebih besar dari 18, kita mencetak ke layar bahwa "x lebih besar dari y".

## The else Statement

Gunakan pernyataan else untuk menentukan blok kode yang akan dieksekusi jika kondisinya false.
```java
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```

```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening.
```
#### Contoh dijelaskan
Pada contoh di atas, waktu (20) lebih besar dari 18, sehingga kondisinya salah. Karena itu, kami beralih ke kondisi lain dan mencetak ke layar "Selamat malam". Jika waktunya kurang dari 18, program akan mencetak "Selamat siang".

## The else if Statement
Gunakan pernyataan else if untuk menentukan kondisi baru jika kondisi pertama salah.
```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

```java
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 20) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```

## Short Hand If...Else (Ternary Operator)


Ada juga short-hand if else, yang dikenal sebagai operator ternary karena terdiri dari tiga operan. Itu dapat digunakan untuk mengganti beberapa baris kode dengan satu baris. Ini sering digunakan untuk menggantikan pernyataan sederhana jika lain:


Alih-alih menulis:
```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
```


Anda cukup menulis:
```java
int time = 20;
String result = (time < 18) ? "Good day." : "Good evening.";
System.out.println(result); // Good evening.
```


