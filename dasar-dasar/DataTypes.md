# Data Types

Seperti yang dijelaskan di bab sebelumnya, variabel di Java harus tipe data yang ditentukan:

```java
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99f;    // Floating point number
char myLetter = 'D';         // Character
boolean myBool = true;       // Boolean
String myText = "Hello";     // String
```


Jenis data dibagi menjadi dua kelompok:
1. Tipe data **primitif** - termasuk byte, short, int, long, float, dobel, boolean, dan char
1. Tipe data **non-primitif** - seperti String, Array, dan Kelas (Anda akan mempelajari lebih lanjut tentang ini di bab selanjutnya)

## Primitive Data Types

Tipe data primitif menentukan ukuran dan jenis nilai variabel, dan tidak memiliki metode tambahan.

Ada delapan tipe data primitif di Java:

|   Data Type|  	Size |  	Description | 
|---|---|---|
|  byte | 	1 byte  |  Menyimpan seluruh angka dari -128 hingga 127|
|  short |  	2 bytes | Menyimpan bilangan bulat dari -32.768 hingga 32.767  |
|  int | 4 bytes  | Menyimpan bilangan bulat dari -2.147.483.648 hingga 2.147.483.647  | 
| long  |  8 bytes | Menyimpan seluruh angka dari -9.223.372.036.854.775.808 hingga 9.223.372.036.854.775.807  | 
| float  | 	4 bytes  | Menyimpan angka pecahan. Cukup untuk menyimpan 6 hingga 7 angka desimal  | 
|  double |  8 bytes | Menyimpan angka pecahan. Cukup untuk menyimpan 15 angka desimal  | 
|  boolean | 	1 bit  | Menyimpan nilai benar **(true)** atau salah **(false)**  | 
|  char |  2 bytes | Menyimpan satu karakter / huruf atau nilai ASCII | 

## Numbers

Jenis bilangan primitif dibagi menjadi dua kelompok:

1. Tipe integer menyimpan bilangan bulat, positif atau negatif (seperti 123 atau -456), tanpa desimal. Jenis yang valid adalah byte, pendek, int dan panjang. Jenis mana yang harus Anda gunakan, tergantung pada nilai numerik.

1. Tipe floating point mewakili angka dengan bagian fraksional, mengandung satu atau lebih desimal. Ada dua jenis: float dan double.

Meskipun ada banyak tipe numerik di Java, angka yang paling banyak digunakan adalah int (untuk bilangan bulat) dan double (untuk bilangan floating point). Namun, kami akan menjelaskan semuanya saat Anda terus membaca.

## Integer Types
### Byte
Tipe data byte dapat menyimpan bilangan bulat dari -128 hingga 127. Ini dapat digunakan sebagai ganti tipe integer atau lainnya untuk menghemat memori ketika Anda yakin bahwa nilainya akan berada di -128 dan 127:
```java
byte myNum = 100;
System.out.println(myNum); // 100
```
### Short
Tipe data pendek dapat menyimpan seluruh nomor dari -32768 hingga 32767:
```java
short myNum = 5000;
System.out.println(myNum); // 5000
```

### int
Tipe data int dapat menyimpan bilangan bulat dari -2147483648 hingga 2147483647. Secara umum, dan dalam tutorial kami, tipe data int adalah tipe data yang disukai ketika kita membuat variabel dengan nilai numerik.
```java
int myNum = 100000;
System.out.println(myNum); // 100000
```

### Long
Tipe data yang panjang dapat menyimpan bilangan bulat dari -9223372036854775808 hingga 9223372036854775807. Ini digunakan ketika int tidak cukup besar untuk menyimpan nilai. Perhatikan bahwa Anda harus mengakhiri nilai dengan "L

```java
long myNum = 15000000000L;
System.out.println(myNum); // 15000000000
```

## Floating Point Types
### Float
Tipe data float dapat menyimpan bilangan pecahan dari 3.4e − 038 hingga 3.4e + 038. Perhatikan bahwa Anda harus mengakhiri nilai dengan "f":
```java
float myNum = 5.75f;
System.out.println(myNum); // 5.75
```
### Double
Tipe data ganda dapat menyimpan bilangan pecahan dari 1,7e − 308 hingga 1,7e + 308. Perhatikan bahwa Anda harus mengakhiri nilai dengan "d":

```java
double myNum = 19.99d;
System.out.println(myNum); // 19.99
```

Gunakan float atau double?

Ketepatan nilai floating point menunjukkan berapa digit nilai yang dapat dimiliki setelah titik desimal. Ketepatan float hanya enam atau tujuh digit desimal, sedangkan variabel ganda memiliki presisi sekitar 15 digit. Oleh karena itu lebih aman menggunakan ganda untuk sebagian besar perhitungan.

### Scientific Numbers

Angka floating point juga bisa menjadi angka ilmiah dengan "e" untuk menunjukkan kekuatan 10:
```java
float f1 = 35e3f;
double d1 = 12E4d;
System.out.println(f1); // 35000.0
System.out.println(d1); // 120000.0
```

## Booleans

Tipe data boolean dideklarasikan dengan kata kunci boolean dan hanya bisa mengambil nilai benar atau salah:
```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```
Nilai Boolean sebagian besar digunakan untuk pengujian bersyarat, yang akan Anda pelajari lebih lanjut di bab selanjutnya.

## Characters
Tipe data char digunakan untuk menyimpan satu karakter. Karakter harus dikelilingi oleh tanda kutip tunggal, seperti 'A' atau 'c':

```java
char myGrade = 'B';
System.out.println(myGrade); //B
```


Atau, Anda dapat menggunakan nilai ASCII untuk menampilkan karakter tertentu:

```java
char a = 65, b = 66, c = 67;
System.out.println(a); // A
System.out.println(b); // B
System.out.println(c); // C
```

## Strings
Tipe data String digunakan untuk menyimpan urutan karakter (teks). Nilai string harus dikelilingi oleh tanda kutip ganda:
```java
String greeting = "Hello World";
System.out.println(greeting); // Hello World
```
Tipe String sangat banyak digunakan dan terintegrasi di Java, yang beberapa menyebutnya "tipe kesembilan khusus".

String di Java sebenarnya adalah tipe data non-primitif, karena mengacu pada objek. Objek String memiliki metode yang digunakan untuk melakukan operasi tertentu pada string. Jangan khawatir jika Anda belum memahami istilah "objek" dulu. Kita akan belajar lebih banyak tentang string dan objek di bab selanjutnya

## Non-Primitive Data Types
Tipe data non-primitif disebut tipe referensi karena merujuk pada objek.

Perbedaan utama antara tipe data primitif dan non-primitif adalah:

1. Tipe primitif sudah ditentukan sebelumnya (sudah ditentukan) di Jawa. Tipe non-primitif dibuat oleh programmer dan tidak didefinisikan oleh Java (kecuali untuk String).
1. Tipe non-primitif dapat digunakan untuk memanggil metode untuk melakukan operasi tertentu, sedangkan tipe primitif tidak bisa.
1. Tipe primitif selalu memiliki nilai, sedangkan tipe non-primitif bisa menjadi nol.
1. Tipe primitif dimulai dengan huruf kecil, sedangkan tipe non-primitif dimulai dengan huruf besar.
1. Ukuran tipe primitif tergantung pada tipe data, sedangkan tipe non-primitif memiliki semua ukuran yang sama.

Contoh tipe non-primitif adalah String, Array, Kelas, Antarmuka, dll. Anda akan belajar lebih banyak tentang ini di bab selanjutnya.
