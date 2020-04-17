# For Loop
Ketika Anda tahu persis berapa kali Anda ingin mengulang melalui blok kode, gunakan loop untuk bukan loop sementara:

```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
 }
```

Pernyataan/statement 1 dieksekusi (satu kali) sebelum eksekusi blok kode.

Pernyataan/statement 2 mendefinisikan kondisi untuk mengeksekusi blok kode.

Pernyataan/statement 3 dieksekusi (setiap kali) setelah blok kode dieksekusi.

Contoh di bawah ini akan mencetak angka 0 hingga 4:

```java
  for (int i = 0; i < 5; i++) {
      System.out.println(i);
    } 
/*
output :
0
1
2
3
4
*/    
```

#### Contoh dijelaskan
Pernyataan/statement 1 menetapkan variabel sebelum loop dimulai (int i = 0).

Pernyataan/statement 2 mendefinisikan kondisi untuk menjalankan loop (saya harus kurang dari 5). Jika kondisinya benar, loop akan memulai lagi, jika itu salah, loop akan berakhir.

Pernyataan/statement 3 meningkatkan nilai (i ++) setiap kali blok kode dalam loop telah dieksekusi

## Another Example

Contoh ini hanya akan mencetak nilai genap antara 0 dan 10:
```java
  for (int i = 0; i <= 10; i = i + 2) {
      System.out.println(i);
    }  
 
 /*
 output:
 0
2
4
6
8
10
 */   
 
```

## For-Each Loop

Ada juga loop "untuk masing-masing", yang digunakan secara eksklusif untuk mengulang elemen-elemen dalam array:

```java
for (type variableName : arrayName) {
  // code block to be executed
}
```
Contoh berikut menampilkan semua elemen dalam array mobil/car, menggunakan loop "untuk masing-masing":
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    for (String i : cars) {
      System.out.println(i);
    }   
  /*
output :
Volvo
BMW
Ford
Mazda
*/ 
  
```
> Catatan: Jangan khawatir jika Anda tidak mengerti contoh di atas. Anda akan mempelajari lebih lanjut tentang Array di bab Java Array.
