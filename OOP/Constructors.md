# Constructors


Konstruktor di java adalah metode khusus yang digunakan untuk menginisialisasi objek. Konstruktor dipanggil ketika objek kelas dibuat. Ini dapat digunakan untuk mengatur nilai awal untuk atribut objek:

```java
// Membuat Class
public class MyClass {
  int x;

  // Membuat Constructor
  public MyClass() {
    x = 5;
  }

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}
```

output : 
```
5
```
Perhatikan bahwa nama konstruktor harus cocok dengan nama kelas, dan tidak boleh memiliki tipe kembali (seperti batal).

Perhatikan juga bahwa konstruktor dipanggil saat objek dibuat.

Semua kelas memiliki konstruktor secara default: jika Anda tidak membuat konstruktor kelas sendiri, Java membuat satu untuk Anda. Namun, maka Anda tidak dapat menetapkan nilai awal untuk atribut objek.
<hr>

## Constructor Parameters
Konstruktor juga dapat mengambil parameter, yang digunakan untuk menginisialisasi atribut.

Contoh berikut menambahkan parameter int ke konstruktor. Di dalam konstruktor kita atur x ke y (x = y). Ketika kita memanggil konstruktor, kita meneruskan parameter ke konstruktor (5), yang akan menetapkan nilai x ke 5:

```java
public class MyClass {
  int x;

  public MyClass(int y) {
    x = y;
  }

  public static void main(String[] args) {
    MyClass myObj = new MyClass(5);
    System.out.println(myObj.x);
  }
}
```
output :
```
5
```

Anda dapat memiliki banyak parameter yang Anda inginkan:
```java
public class Car {
  int modelYear;
  String modelName;

  public Car(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Car myCar = new Car(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}
```
output :
```
1969 Mustang
```
