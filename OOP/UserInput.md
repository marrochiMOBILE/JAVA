# User Input
Kelas Scanner digunakan untuk mendapatkan input pengguna, dan ditemukan dalam paket java.util.

Untuk menggunakan kelas Pemindai, buat objek kelas dan gunakan salah satu metode yang tersedia yang ditemukan dalam dokumentasi kelas Pemindai. Dalam contoh kita, kita akan menggunakan metode nextLine (), yang digunakan untuk membaca Strings:

```java
import java.util.Scanner;  // Import class Sacnner

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);  // membuat Scanner object
    System.out.println("Enter username");

    String userName = myObj.nextLine();  // membaca input user // misalnya masukan kata ochi
    System.out.println("Username is: " + userName);  // Output user input
  }
}
```
output:
```
Enter username
ochi

Username is: ochi
```


Jika Anda tidak tahu apa itu paket, baca Tutorial Paket/packages Java kami.
## Input Types
| type  | penjelasn |
| ----- | --- |
| nextBoolean()  | Membaca nilai boolean dari pengguna |
|nextByte()| Membaca nilai byte dari pengguna  |
|nextDouble()	| Membaca nilai ganda dari pengguna |
|nextFloat()| Membaca nilai float dari pengguna |
|nextInt()| Membaca nilai integer dari pengguna|
|nextLine() | Membaca nilai string dari pengguna|
|nextLong()| Membaca nilai panjang dari pengguna |
|nextShort()| Membaca nilai pendek dari pengguna|


Dalam contoh di bawah ini, kami menggunakan metode berbeda untuk membaca data dari berbagai jenis:

```java

import java.util.Scanner;

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);

    System.out.println("Enter name, age and salary:");

    // String input
    String name = myObj.nextLine(); // misal marrochi (enter)

    // Numerical input
    int age = myObj.nextInt(); // misal 20 (enter)
    double salary = myObj.nextDouble(); // misal 20000000 (enter)

    // Output input by user
    System.out.println("Name: " + name); 
    System.out.println("Age: " + age); 
    System.out.println("Salary: " + salary); 
  }
}
```

output:
```
Enter name, age and salary:
ochi

20

20000000

Name: ochi
Age: 20
Salary: 20000000
```


Catatan: Jika Anda memasukkan input yang salah (mis. Teks dalam input numerik), Anda akan mendapatkan pesan pengecualian / kesalahan (seperti "InputMismatchException").
