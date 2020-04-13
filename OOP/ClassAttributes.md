# Class Attributes


Pada bab sebelumnya, kami menggunakan istilah "variabel" untuk x dalam contoh (seperti yang ditunjukkan di bawah). Ini sebenarnya adalah atribut dari kelas. Atau Anda bisa mengatakan bahwa atribut kelas adalah variabel dalam kelas:

> "MyClass" dengan dua atribut: x dan y
```java
public class MyClass {
  int x = 5; 
  int y = 3;
}
```

Mengakses Atribut
Anda bisa mengakses atribut dengan membuat objek kelas, dan dengan menggunakan sintaks dot (.):
Contoh berikut akan membuat objek kelas MyClass, dengan nama myObj. Kami menggunakan atribut x pada objek untuk mencetak nilainya:

```java

public class MyClass {
  int x = 5;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}

```
outout : 
```
5
```

Ubah Atribut
Anda juga dapat mengubah nilai atribut:
```java
public class MyClass {
  int x;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    myObj.x = 40;
    System.out.println(myObj.x);
  }
}
```
output :
```java
40
```

Atau timpa nilai yang ada:
```java
public class MyClass {
  int x = 10;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    myObj.x = 25; // sekarang nilainya 25
    System.out.println(myObj.x);
  }
}

```
output:
```
25
```

Jika Anda tidak ingin kemampuan untuk menimpa nilai yang ada, nyatakan atribut sebagai `final`:
```java
public class MyClass {
  final int x = 10;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    myObj.x = 25; // maka error karena final tidak bisa ditimpa
    System.out.println(myObj.x); 
  }
}

```
ouput :
```
MyClass.java:6: error: cannot assign a value to final variable x
    myObj.x = 25;
         ^
1 error
```

Banyak Objek
Jika Anda membuat beberapa objek dari satu kelas, Anda bisa mengubah nilai atribut di satu objek, tanpa memengaruhi nilai atribut di yang lain:

```java
public class MyClass {
  int x = 5;

  public static void main(String[] args) {
    MyClass myObj1 = new MyClass();
    MyClass myObj2 = new MyClass();
    myObj2.x = 25;
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```
output :
```
5
25
```


Anda dapat menentukan atribut sebanyak yang Anda inginkan:

```java

public class Person {
  String fname = "OCHI";
  String lname = "ganteaang";
  int age = 20;

  public static void main(String[] args) {
    Person myObj = new Person();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Age: " + myObj.age);
  }
}

```
output:
```
Name: OCHI ganteaang
Age: 20
```
<hr>


