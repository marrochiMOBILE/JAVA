# Arrays
Array digunakan untuk menyimpan beberapa nilai dalam satu variabel, alih-alih mendeklarasikan variabel terpisah untuk setiap nilai.

Untuk mendeklarasikan sebuah array, tentukan tipe variabel dengan tanda kurung:

```java
String[] cars
```
Kami sekarang telah mendeklarasikan variabel yang memiliki array string. Untuk memasukkan nilai ke dalamnya, kita bisa menggunakan array literal - tempatkan nilai dalam daftar yang dipisahkan koma, di dalam kurung kurawal:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```


Untuk membuat array bilangan bulat, Anda bisa menulis

```java
int[] myNum = {10, 20, 30, 40};
```

## Access the Elements of an Array

Anda mengakses elemen array dengan merujuk ke nomor indeks.

Pernyataan ini mengakses nilai elemen pertama dalam mobil/cars:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    System.out.println(cars[0]);
    // Outputs Volvo
```

> Catatan: Array indeks mulai dengan 0: [0] adalah elemen pertama. [1] adalah elemen kedua, dll.

## Change an Array Element

Untuk mengubah nilai elemen tertentu, lihat nomor indeks:
> cars[0] = "Opel";
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
System.out.println(cars[0]);
// Sekarang mengeluarkan Opel dan bukan Volvo
```

## Array Length
Untuk mengetahui berapa banyak elemen yang dimiliki array, gunakan properti length:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
// Outputs 4
```

## Loop Through an Array
Anda bisa mengulang-ulang elemen array dengan for loop, dan menggunakan properti length untuk menentukan berapa kali loop harus dijalankan.

Contoh berikut menampilkan semua elemen dalam array mobil:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    for (int i = 0; i < cars.length; i++) {
      System.out.println(cars[i]);
    }
 /*
 output:
 Volvo
BMW
Ford
Mazda
 */   
```
## Loop Through an Array with For-Each

Ada juga loop "untuk masing-masing", yang digunakan secara eksklusif untuk loop melalui elemen dalam array:
```java
for (type variable : arrayname) {
  ...
}
```

Contoh berikut menampilkan semua elemen dalam array mobil, menggunakan loop "untuk masing-masing":
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    for (String i : cars) {
      System.out.println(i);
    } 
     /*
 output:
 Volvo
BMW
Ford
Mazda
 */  
```
Contoh di atas dapat dibaca seperti ini: untuk setiap elemen String (disebut i - seperti dalam indeks) di mobil, cetak nilai i.

Jika Anda membandingkan loop untuk dan untuk-setiap loop, Anda akan melihat bahwa untuk-setiap metode lebih mudah untuk ditulis, itu tidak memerlukan penghitung (menggunakan properti panjang), dan itu lebih mudah dibaca.

## Multidimensional Arrays


Array multidimensi adalah array yang berisi satu atau lebih array.

Untuk membuat array dua dimensi, tambahkan setiap array dalam set kurungnya sendiri:

> int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };


myNumbers sekarang merupakan array dengan dua array sebagai elemen-elemennya.

Untuk mengakses elemen array myNumbers, tentukan dua indeks: satu untuk array, dan satu untuk elemen di dalam array itu. Contoh ini mengakses elemen ketiga (2) dalam array kedua (1) dari myNumbers:

```java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
int x = myNumbers[1][2];
System.out.println(x); // Outputs 7
```

Kita juga bisa menggunakan loop for di dalam loop lain untuk mendapatkan elemen array dua dimensi (kita masih harus menunjuk ke dua indeks):

```java
 int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
     for (int i = 0; i < myNumbers.length; ++i) {
        for(int j = 0; j < myNumbers[i].length; ++j) {
           System.out.println(myNumbers[i][j]);
        }
     }
     /*
     output :
     1
      2
      3
      4
      5
      6
      7
     */
```
