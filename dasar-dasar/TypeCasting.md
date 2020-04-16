# Type Casting


Tipe casting adalah ketika Anda menetapkan nilai satu tipe data primitif ke tipe lain.

Di Java, ada dua jenis casting:


1. Widening Casting (otomatis) - mengonversi tipe yang lebih kecil ke ukuran tipe yang lebih besar <br>
**byte -> short -> char -> int -> long -> float -> double**

1. Penyempitan Sempit (secara manual) - mengonversi jenis yang lebih besar ke jenis yang lebih kecil <br>
**double -> float -> long -> int -> char -> short -> byte**

## Widening Casting
Pengecoran pelebaran dilakukan secara otomatis saat meneruskan tipe ukuran yang lebih kecil ke tipe ukuran yang lebih besar:

```java
public class MyClass {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double / kalo bahasa inggris ke gini g ngerti lu goblok

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```

## Narrowing Casting
Penyempitan yang sempit harus dilakukan secara manual dengan menempatkan jenis dalam tanda kurung di depan nilai:
```java
public class MyClass {
  public static void main(String[] args) {
    double myDouble = 9.78;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```

