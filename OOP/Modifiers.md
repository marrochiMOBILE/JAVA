# Modifiers
Sekarang, Anda cukup akrab dengan kata kunci publik yang muncul di hampir semua contoh kami:

```java
public class MyClass
```
Kata kunci publik adalah pengubah akses, artinya digunakan untuk mengatur tingkat akses untuk kelas, atribut, metode, dan konstruktor.
Kami membagi pengubah menjadi dua kelompok:

1. Access Modifiers - mengontrol level akses
1. Non-Access Modifiers - tidak mengontrol level akses, tetapi menyediakan fungsionalitas lain

## Access Modifiers

Untuk kelas, Anda dapat menggunakan publik atau default:

#### public
```java
public class MyClass {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

#### default
```java
class MyClass {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}

```

> jadi sama aja mau nulis yg atas atau yg bawah karena itu default nya


Untuk atribut, metode, dan konstruktor, Anda dapat menggunakan salah satu dari yang berikut ini:
1. public - Kode ini dapat diakses untuk semua kelas
1. private - Kode hanya dapat diakses di dalam kelas yang dideklarasikan
1. default - Kode hanya dapat diakses dalam packet yang sama. Ini digunakan ketika Anda tidak menentukan pengubah. Anda akan mempelajari lebih lanjut tentang packet di bab packet
1. protected - Kode ini dapat diakses dalam paket dan subclass yang sama. Anda akan belajar lebih banyak tentang subclass dan superclasses di bab Inheritance

####  `public`
buat kelas dengan nama Person.java
```java
public class Person {
  public String fname = "John";
  public String lname = "Doe";
  public String email = "john@doe.com";
  public int age = 24;
}
```
dan buat kelas satu lagi denga nama MyClass.java
```java
class MyClass {
  public static void main(String[] args) {
    Person myObj = new Person(); 
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
  }
}
```

output : 
```
Name: John Doe
Email: john@doe.com
Age: 24
```

#### `private`
```java
public class Person {
  private String fname = "John";
  private String lname = "Doe";
  private String email = "john@doe.com";
  private int age = 24;
  
  public static void main(String[] args) {
    Person myObj = new Person();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
  }
}
```

output : 
```
Name: John Doe
Email: john@doe.com
Age: 24
```

#### `default`
```java
class Person {
  String fname = "John";
  String lname = "Doe";
  String email = "john@doe.com";
  int age = 24;
  
  public static void main(String[] args) {
    Person myObj = new Person();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
  }
}
```

output : 
```
Name: John Doe
Email: john@doe.com
Age: 24
```

#### `protected`
```java
class Person {
  protected String fname = "John";
  protected String lname = "Doe";
  protected String email = "john@doe.com";
  protected int age = 24;
}

class Student extends Person {
  private int graduationYear = 2018;
  public static void main(String[] args) {
    Student myObj = new Student();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
    System.out.println("Graduation Year: " + myObj.graduationYear);
  }
}
```

output :
```
Name: John Doe
Email: john@doe.com
Age: 24
Graduation Year: 2018
```

## Non-Access Modifiers
Untuk kelas, Anda dapat menggunakan final atau abstrak:

```java
final class Vehicle {
  protected String brand = "Ford";
  public void honk() {
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle { // disini akan terjadi error Kelas tidak dapat diwarisi oleh kelas lain (Anda akan belajar lebih banyak tentang warisan dalam bab Warisan/inheritance)
  private String modelName = "Mustang";
  public static void main(String[] args) {
    Car myFastCar = new Car();
    myFastCar.honk();
    System.out.println(myFastCar.brand + " " + myFastCar.modelName);
  }
}
```

output :
```
Car.java:8: error: cannot inherit from final Vehicle
class Car extends Vehicle {
                  ^
1 error
```
