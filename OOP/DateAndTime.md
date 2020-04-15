# Date and Time

Java tidak memiliki kelas Date bawaan, tetapi kami dapat mengimpor paket java.time untuk bekerja dengan API tanggal dan waktu. Paket termasuk banyak kelas tanggal dan waktu. Sebagai contoh:

| type  | penjelasn |
| ----- | --- |
| LocalDate  | Merupakan tanggal (tahun, bulan, hari (yyyy-MM-dd)) |
| LocalTime| Merupakan waktu (jam, menit, detik, dan milidetik (HH-mm-dt-zzz))  |
| LocalDateTime	| Merupakan tanggal dan waktu (yyyy-MM-dd-HH-mm-ss.zzz) |
| DateTimeFormatter|Formatter untuk menampilkan dan mem-parsing objek waktu-tanggal |


Jika Anda tidak tahu apa itu paket, baca Tutorial Paket/packages Java kami.

## Display Current Date

Untuk menampilkan tanggal saat ini, `impor kelas java.time.LocalDate`, dan gunakan metode `now ()`

```java
import java.time.LocalDate;  // import class LocalDate

public class MyClass {  
  public static void main(String[] args) {  
    LocalDate myObj = LocalDate.now();  // membuat object date
    System.out.println(myObj);  // tampilkan date
  }  
}  

```

output:
```
ini hanya sebuah contoh
2020-04-14
```

## Display Current Time
Untuk menampilkan waktu saat ini (jam, menit, detik, dan milidetik), impor kelas java.time.LocalTime, dan gunakan metode sekarang ():
```java

import java.time.LocalTime;  // import class localtime

public class MyClass {  
  public static void main(String[] args) {  
    LocalTime myObj = LocalTime.now();
    System.out.println(myObj);
  }  
}  

```
output:
```
ini hanya sebuah contoh
13:00:47.271838
```
## Display Current Date and Time

Untuk menampilkan tanggal dan waktu saat ini, impor kelas java.time.LocalDateTime, dan gunakan metode now ():
```java

import java.time.LocalDateTime;  // import class LocalDateTime

public class MyClass {  
  public static void main(String[] args) {  
    LocalDateTime myObj = LocalDateTime.now();
    System.out.println(myObj);
  }  
}  

```

output:
```
ini hanya sebuah contoh
2020-04-15T13:03:38.041906
```

## Formatting Date and Time
"T" pada contoh di atas digunakan untuk memisahkan tanggal dari waktu. Anda bisa menggunakan kelas DateTimeFormatter dengan metode `ofPattern ()` dalam paket yang sama untuk memformat atau mem-parsing objek tanggal-waktu. Contoh berikut akan menghapus "T" dan milidetik dari tanggal-waktu:
```java
import java.time.LocalDateTime;  // Import  LocalDateTime class
import java.time.format.DateTimeFormatter;  // Import  DateTimeFormatter class

public class MyClass {
  public static void main(String[] args) {  
    LocalDateTime myDateObj = LocalDateTime.now();  
    System.out.println("Before formatting: " + myDateObj);  
    DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");  
    
    String formattedDate = myDateObj.format(myFormatObj);  
    System.out.println("After formatting: " + formattedDate);  
  }  
}  

```

output:
```
ini hanya sebuah contoh
Before Formatting: 2020-04-15T13:07:03.219735
After Formatting: 15-04-2020 13:07:03
```

Metode ofPattern () menerima semua jenis nilai, jika Anda ingin menampilkan tanggal dan waktu dalam format yang berbeda. Sebagai contoh:
|  value | contoh  |  
|---|---|
|  yyyy-MM-dd | 	"1988-09-29"  | 
| dd/MM/yyyy  |  "29/09/1988" | 
|  dd-MMM-yyyy | 	"29-Sep-1988"  | 
|E, MMM dd yyyy|	"Thu, Sep 29 1988" |
