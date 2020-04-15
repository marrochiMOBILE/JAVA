# Wrapper Classes / kelas pembungkus

## Java Wrapper Classes

Kelas wrapper menyediakan cara untuk menggunakan tipe data primitif (int, boolean, dll.) Sebagai objek.
| Primitive Data Type  |  Wrapper Class |
|---|---|
|  byte |  Byte |  
|  short | Short  |  
| int  | 	Integer  | 
|  long | Long | 
| float  |  	Float | 
|   double| Double  | 
| boolean  |  	Boolean | 
| char  | 	Character  | 

Terkadang Anda harus menggunakan kelas wrapper, misalnya saat bekerja dengan objek Koleksi, seperti ArrayList, di mana tipe primitif tidak dapat digunakan (daftar hanya dapat menyimpan objek):

```java
ArrayList<int> myNumbers = new ArrayList<int>(); // Invalid
```
```java
ArrayList<Integer> myNumbers = new ArrayList<Integer>(); // Valid
```

## Creating Wrapper Objects
Untuk membuat objek wrapper, gunakan kelas wrapper alih-alih tipe primitif. Untuk mendapatkan nilai, Anda cukup mencetak objek:
```java
public class MyClass { 
  public static void main(String[] args) { 
    Integer myInt = 5; 
    Double myDouble = 5.99; 
    Character myChar = 'A'; 
    System.out.println(myInt);
    System.out.println(myDouble);
    System.out.println(myChar);
  }
}
```

output:
```java
5
5.99
A
```

Karena Anda sekarang bekerja dengan objek, Anda dapat menggunakan metode tertentu untuk mendapatkan informasi tentang objek tertentu.
```java
public class MyClass { 
  public static void main(String[] args) { 
    Integer myInt = 5; 
    Double myDouble = 5.99; 
    Character myChar = 'A'; 
    System.out.println(myInt.intValue());
    System.out.println(myDouble.doubleValue());
    System.out.println(myChar.charValue());
  }
}
```

output:
```
5
5.99
A
```
Metode lain yang bermanfaat adalah metode `toString ()`, yang digunakan untuk mengubah objek pembungkus menjadi string.

Dalam contoh berikut, kami mengonversi bilangan bulat ke sebuah String, dan menggunakan metode length () dari kelas String untuk menampilkan panjang "string":

```java

public class MyClass { 
  public static void main(String[] args) { 
    Integer myInt = 100; 
    String myString = myInt.toString();
    System.out.println(myString.length());
  }
}
```
output:
```
3
```


