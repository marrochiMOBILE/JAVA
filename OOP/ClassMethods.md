# class methods
Anda belajar dari bab Metode Java bahwa metode dideklarasikan dalam kelas, dan bahwa mereka digunakan untuk melakukan tindakan tertentu:
```java
public class MyClass {
  static void myMethod() {
    System.out.println("Hello World!");
  }
}
```
myMethod () mencetak teks (aksi), ketika dipanggil. Untuk memanggil metode, tulis nama metode diikuti oleh dua tanda kurung () dan tanda titik koma;
> Di dalam main, panggil myMethod ():

```java
public class MyClass {
  static void myMethod() {
    System.out.println("Hello World!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}
```
output :
```java
Hello World!
```
<hr>

