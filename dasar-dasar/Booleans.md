# Booleans
Sangat sering, dalam pemrograman, Anda akan memerlukan tipe data yang hanya dapat memiliki satu dari dua nilai, seperti:
 
 <ul>
       <li>YA TIDAK</li>
       <li>ON / OFF</li>
       <li>BENAR SALAH</li>
   </ul>



Untuk ini, Java memiliki tipe data boolean, yang dapat mengambil nilai benar atau salah.

## Boolean Values
Jenis boolean dideklarasikan dengan kata kunci boolean dan hanya bisa mengambil nilai benar atau salah:

```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```

Namun, lebih umum untuk mengembalikan nilai boolean dari ekspresi boolean, untuk pengujian bersyarat (lihat di bawah).

## Boolean Expression

Ekspresi Boolean adalah ekspresi Java yang mengembalikan nilai Boolean: true atau false.

Anda dapat menggunakan operator pembanding, seperti operator yang lebih besar dari (>) untuk mengetahui apakah ekspresi (atau variabel) benar:
```java
int x = 10;
int y = 9;
System.out.println(x > y); // returns true, because 10 is higher than 9
```
Or even easier:
```java
System.out.println(10 > 9); // returns true, because 10 is higher than 9
```


Dalam contoh di bawah, kami menggunakan operator sama dengan (==) untuk mengevaluasi ekspresi:

```java
int x = 10;
System.out.println(x == 10); 
// returns true, because the value of x is equal to 10 / mengembalikan nilai benar karena nilai dari x sama dengan 10
```

```java
System.out.println(10 == 15); // returns false, because 10 is not equal to 15
```

