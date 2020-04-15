# Exceptions - Try...Catch

### Java Exceptions
Saat menjalankan kode Java, kesalahan yang berbeda dapat terjadi: kesalahan pengkodean yang dibuat oleh programmer, kesalahan karena input yang salah, atau hal-hal yang tidak terduga lainnya.

Ketika kesalahan terjadi, Java biasanya akan berhenti dan menghasilkan pesan kesalahan. Istilah teknis untuk ini adalah: Java akan melempar pengecualian (melempar kesalahan).

### Java try and catch

Pernyataan coba memungkinkan Anda untuk menentukan blok kode yang akan diuji untuk kesalahan saat sedang dieksekusi.

Pernyataan tangkap memungkinkan Anda untuk menentukan blok kode yang akan dieksekusi, jika kesalahan terjadi di blok coba.

Kata kunci coba dan tangkap berpasangan

```java
try {
  //  Blok kode untuk dicoba
}
catch(Exception e) {
  //  Blok kode untuk menangani kesalahan
}
```

kita coba :

```java

public class MyClass {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    }
  }
}

```

output:
```
Something went wrong.
```

### Finally
Pernyataan terakhir memungkinkan Anda mengeksekusi kode, setelah mencoba ... menangkap, terlepas dari hasilnya:
```java
public class MyClass {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    } finally {
      System.out.println("The 'try catch' is finished.");
    }
  }
}
```

output:
```
Something went wrong.
The 'try catch' is finished.
```

### The throw keyword
Pernyataan melempar memungkinkan Anda untuk membuat kesalahan khusus.

Pernyataan melempar digunakan bersama dengan tipe pengecualian. Ada banyak jenis pengecualian yang tersedia di Jawa: ArithmeticException, FileNotFoundException, ArrayIndexOutOfBoundsException, SecurityException, dll:

```java
public class MyClass {
  static void checkAge(int age) { 
    if (age < 18) {
      throw new ArithmeticException("Access denied - You must be at least 18 years old."); 
    } else {
      System.out.println("Access granted - You are old enough!"); 
    }
 } 
 
 public static void main(String[] args) { 
   checkAge(15); 
 } 
}

```

output:
```
Exception in thread "main" java.lang.ArithmeticException: Access denied - You must be at least 18 years old.
        at MyClass.checkAge(MyClass.java:4)
        at MyClass.main(MyClass.java:12)
```
