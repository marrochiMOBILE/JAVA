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

## Static vs. Non-Static

Anda akan sering melihat program Java yang memiliki atribut dan metode statis atau publik.
Dalam contoh di atas, kami membuat metode statis, yang berarti dapat diakses tanpa membuat objek kelas, tidak seperti publik, yang hanya dapat diakses oleh objek:
```java
public class MyClass {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }

  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // memanggil method static

    MyClass myObj = new MyClass(); // membuat object untuk memanggil method public/ non static
    myObj.myPublicMethod(); // memanggil method public
  }
}
```
output :
```
Static methods can be called without creating objects
Public methods must be called by creating objects
```
> 
Catatan: Anda akan mempelajari lebih lanjut tentang kata kunci ini (disebut pengubah) di bab Java Modifiers.
<hr>

## Access Methods With an Object

```java
// membuat class bernama Car
public class Car {
 
  // membuat method dengan nama fullThrottle() 
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  // membuat method dengan nama speed() dengan 1 parameter maxSpeed dengan tipe integer
  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }

  // Di dalam main, panggil metode pada objek myCar
  public static void main(String[] args) {
    Car myCar = new Car();     // membuat object myCar
    myCar.fullThrottle();      // Panggil method fullThrottle() 
    myCar.speed(200);          // Panggil method   speed() 
  }
}

```
output :
```
The car is going as fast as it can!
Max speed is: 200
```
<hr>

## Using Multiple Classes
Seperti yang kami sebutkan di bab Kelas, itu adalah praktik yang baik untuk membuat objek kelas dan mengaksesnya di kelas lain.

Ingat bahwa nama file java harus sesuai dengan nama kelas. Dalam contoh ini, kami telah membuat dua file di direktori yang sama:

1. Car.java
1. OtherClass.java

#### Car.java
```java
public class Car {
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }
}
```
#### OtherClass.java
```java
class OtherClass {
  public static void main(String[] args) {
    Car myCar = new Car();     // membuat object
    myCar.fullThrottle();      // panggil method fullThrottle()
    myCar.speed(200);          // panggil method speed()
  }
}
```
output : 
```
The car is going as fast as it can!
Max speed is: 200
```
