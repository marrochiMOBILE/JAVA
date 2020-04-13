# CLASS/OBJECT

Java adalah bahasa pemrograman berorientasi objek.

Segala sesuatu di JAVA dikaitkan dengan kelas dan objek, bersama dengan atribut dan metodenya. Sebagai contoh: dalam kehidupan nyata, mobil adalah objek. Mobil ini memiliki atribut, seperti bobot dan warna, dan metode, seperti drive dan rem.


### membuat class

Untuk membuat kelas, gunakan kelas kata kunci:
```java
public class MyClass {
  int x = 5;
}
```

### membuat object
Di JAVA, objek dibuat dari kelas. Kami telah membuat kelas bernama MyClass, jadi sekarang kita bisa menggunakan ini untuk membuat objek.

Untuk membuat objek MyClass, tentukan nama kelas, diikuti dengan nama objek, dan gunakan kata kunci baru:

```java
public class MyClass {
  int x = 5;

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


Anda dapat membuat beberapa objek dari satu kelas:

```java
public class MyClass {
  int x = 5;

  public static void main(String[] args) {
    MyClass myObj1 = new MyClass();
    MyClass myObj2 = new MyClass();
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```

output:
```
5
5
```

Menggunakan Banyak Kelas
Anda juga bisa membuat objek kelas dan mengaksesnya di kelas lain. Ini sering digunakan untuk organisasi kelas yang lebih baik (satu kelas memiliki semua atribut dan metode, sedangkan kelas lainnya memegang metode main () (kode yang akan dieksekusi)).

Ingat bahwa nama file java harus sesuai dengan nama kelas. Dalam contoh ini, kami telah membuat dua file di direktori / folder yang sama:

####  TesJAVA.java
```java
package tesjava;

/**
 *
 * @author ochi
 */
public class TesJAVA {
    public static void main(String[] args) {
        ochiG x = new ochiG();
        System.out.println(x.x);
    }   
}
```

satu lagi buat file didalam folder yang sama dengan nama dibawah ini
#### ochiG.java
```java
package tesjava;

/**
 *
 * @author ochi
 */
public class ochiG {
    int x = 55;
}
```

