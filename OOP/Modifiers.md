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
### `final` 
Kelas tidak dapat diwarisi oleh kelas lain
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
### `abstract`

Kelas tidak dapat digunakan untuk membuat objek (Untuk mengakses kelas abstrak, itu harus diwarisi dari kelas lain. Anda akan belajar lebih banyak tentang warisan dan abstraksi di bab Warisan/Inheritance dan Abstraksi). sekarang buat file bernama Person.java dan MyClass.java
#### Person.java
```java
// abstract class
abstract class Person {
  public String fname = "John";
  public String lname = "Doe";
  public String email = "john@doe.com";
  public int age = 24;
  public abstract void study(); // abstract method 
}

// Subclass (inherit from Person) / turunan
class Student extends Person {
  public int graduationYear = 2018;
  public void study() {
    System.out.println("Studying all day long");
  }
}

```

kemudian buat lagi file di folder yg sama dengan nama MyClass.java
#### MyClass.java
```java

class MyClass {
  public static void main(String[] args) {
    // membuat object yg bernama myObj dari kelas Student
    Student myObj = new Student(); 
    
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
    System.out.println("Graduation Year: " + myObj.graduationYear);
    myObj.study(); // panggil abstract method
  }
}

Result:
Name: John Doe
Email: john@doe.com
Age: 24
Graduation Year: 2018
Studying all day long
```

output :

```java
Name: John Doe
Email: john@doe.com
Age: 24
Graduation Year: 2018
Studying all day long
```

<hr>

## method & atributes
Untuk atribut dan metode, Anda dapat menggunakan salah satu dari yang berikut:

### `Final`
Jika Anda tidak ingin kemampuan untuk menimpa nilai atribut yang ada, nyatakan atribut sebagai final:
```java
MyClass.java 

public class MyClass {
  final int x = 10;
  final double PI = 3.14;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    myObj.x = 50; // ini akan terjadi error karena final nilainya tidak bisa ditimpah
    myObj.PI = 25; // ini akan terjadi error karena final nilainya tidak bisa ditimpah
    System.out.println(myObj.x); 
  }
}

```

ouput :
```
MyClass.java:7: error: cannot assign a value to final variable x
    myObj.x = 50;
         ^
MyClass.java:8: error: cannot assign a value to final variable PI
    myObj.PI = 25;
         ^ 2 errors
```
### `Static`
Metode statis berarti dapat diakses tanpa membuat objek kelas, tidak seperti publik:
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
    myStaticMethod(); // panggil static method

    MyClass myObj = new MyClass(); // membuat object dari class MyClass
    myObj.myPublicMethod(); // panggil public method
  }
}
```

output :
```
Static methods can be called without creating objects
Public methods must be called by creating objects
```

### `Abstract`
Metode abstrak milik kelas abstrak, dan tidak memiliki tubuh. Tubuh disediakan oleh subclass:
```java
// buat file dipolder yg sama dengan nama Person.java
// abstract class
abstract class Person {
  public String fname = "John";
  public int age = 24;
  public abstract void study(); // abstract method
}

// Subclass (inherit from Person)
class Student extends Person {
  public int graduationYear = 2018;
  public void study() { // the body of the abstract method is provided here
    System.out.println("Studying all day long");
  }
}
// End filename: Person.java

// dan buat lagi difolder yang sama dengan nama MyClass.java
class MyClass {
  public static void main(String[] args) {
    // membuat object dari kelas yg bernama Student
    Student myObj = new Student();

    System.out.println("Name: " + myObj.fname);
    System.out.println("Age: " + myObj.age);
    System.out.println("Graduation Year: " + myObj.graduationYear);
    myObj.study(); // panggil abstract method
  }
}
```

output :
```
Name: John
Age: 24
Graduation Year: 2018
Studying all day long
```

