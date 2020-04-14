# Packages & API

Paket/Packages di Java digunakan untuk mengelompokkan kelas terkait. Anggap saja sebagai folder dalam direktori file. Kami menggunakan paket/Packages untuk menghindari konflik nama, dan untuk menulis kode yang dapat dikelola dengan lebih baik. Paket/Packages dibagi menjadi dua kategori:
1. Paket Built-in / Built-in Packages (paket dari Java API)
1. Paket Buatan Pengguna/ User-defined Packages (buat paket Anda sendiri)

## Built-in Packages
Java API adalah pustaka kelas yang sudah ditulis sebelumnya, yang bebas digunakan, termasuk dalam Java Development Environment.

Perpustakaan berisi komponen untuk mengelola input, pemrograman basis data, dan banyak lagi lainnya. Daftar lengkapnya dapat ditemukan di situs web Oracles: https://docs.oracle.com/javase/8/docs/api/.

Perpustakaan dibagi menjadi beberapa paket dan kelas. Berarti Anda dapat mengimpor satu kelas (beserta metode dan atributnya), atau seluruh paket yang berisi semua kelas yang termasuk dalam paket yang ditentukan.

Untuk menggunakan kelas atau paket dari perpustakaan, Anda harus menggunakan kata kunci impor:

```java
import package.name.Class;   // Import satu class
import package.name.*;   // Import keseluruhan paket
```

### Import a Class

Jika Anda menemukan kelas yang ingin Anda gunakan, misalnya, kelas Pemindai, yang digunakan untuk mendapatkan input pengguna, tulis kode berikut:
```java
import java.util.Scanner;
```
Pada contoh di atas, java.util adalah sebuah paket, sementara Scanner adalah kelas dari paket java.util.

Untuk menggunakan kelas Pemindai, buat objek kelas dan gunakan salah satu metode yang tersedia yang ditemukan dalam dokumentasi kelas Pemindai. Dalam contoh kita, kita akan menggunakan metode nextLine (), yang digunakan untuk membaca baris lengkap:
```java
import java.util.Scanner; // import class Scanner 

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in); // untuk memanggil kelas Scanner yg sudah di import
    String userName;
    
    // masukan nama dan enter
    // misalkan saya masukan nama ochi terus enter
    System.out.println("Enter username"); 
    userName = myObj.nextLine();   
       
    System.out.println("Username is: " + userName);        
  }

```

output :
```java
Enter username
ochi

Username is: ochi
```

### Import a Package

Ada banyak paket untuk dipilih. Pada contoh sebelumnya, kami menggunakan kelas Scanner dari paket java.util. Paket ini juga berisi fasilitas tanggal dan waktu, generator nomor acak, dan kelas utilitas lainnya.

Untuk mengimpor seluruh paket, akhiri kalimat dengan tanda bintang (*). Contoh berikut akan mengimpor SEMUA kelas di paket java.util:
```java
import java.util.*; // import seleuruh paket yang ada di java.util 

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);  // untuk memanggil kelas Scanner yg sudah di import
    String userName;
    
     // masukan nama dan enter
    // misalkan saya masukan nama ochi terus enter
    System.out.println("Enter username"); 
    userName = myObj.nextLine();   
       
    System.out.println("Username is: " + userName);        
  }
}
```


output :
```java
Enter username
ochi

Username is: ochi
```

