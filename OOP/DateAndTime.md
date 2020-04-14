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
2020-04-14
```

## Display Current Time
