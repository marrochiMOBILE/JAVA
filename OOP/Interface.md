# Interface

Cara lain untuk mencapai abstraksi di Java, adalah dengan antarmuka.

Antarmuka adalah "kelas abstrak" yang sepenuhnya digunakan untuk mengelompokkan metode terkait dengan tubuh kosong:
```java
// interface / antarmuka
interface Animal {
  public void animalSound(); // metode antarmuka (tidak memiliki tubuh)
  public void run(); // metode antarmuka (tidak memiliki tubuh)
}
```
Untuk mengakses metode antarmuka, antarmuka harus "diimplementasikan" (agak seperti diwariskan) oleh kelas lain dengan kata kunci implement (alih-alih meluas). Isi metode antarmuka disediakan oleh kelas "implement":

```java

interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void sleep(); // interface method (does not have a body)
}

class Pig implements Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
  public void sleep() {
    System.out.println("Zzz");
  }
}

class MyMainClass {
  public static void main(String[] args) {
    Pig myPig = new Pig();
    myPig.animalSound();
    myPig.sleep();
  }
}
```

output :
```
The pig says: wee wee
Zzz
```


Catatan tentang Antarmuka:
Seperti kelas abstrak, antarmuka tidak dapat digunakan untuk membuat objek (dalam contoh di atas, tidak mungkin membuat objek "Hewan" di MyMainClass)
Metode antarmuka tidak memiliki tubuh - tubuh disediakan oleh kelas "implement"
Pada implementasi antarmuka, Anda harus mengganti semua metodenya
Metode antarmuka secara default abstrak dan publik
Atribut antarmuka secara default publik, statis dan final
Antarmuka tidak dapat berisi konstruktor (karena tidak dapat digunakan untuk membuat objek)
Mengapa Dan Kapan Menggunakan Antarmuka?

1. Untuk mencapai keamanan - sembunyikan detail tertentu dan hanya tampilkan detail penting dari suatu objek (antarmuka).

1. Java tidak mendukung "multiple inheritance" (sebuah kelas hanya dapat diwarisi dari satu superclass). Namun, itu dapat dicapai dengan antarmuka, karena kelas dapat mengimplementasikan banyak antarmuka. Catatan: Untuk mengimplementasikan beberapa antarmuka, pisahkan dengan koma (lihat contoh di bawah).

## Multiple Interfaces
Untuk mengimplementasikan beberapa antarmuka, pisahkan dengan koma `,`:
```java

interface FirstInterface {
  public void myMethod(); // interface method
}

interface SecondInterface {
  public void myOtherMethod(); // interface method
}

// contoh "implements" FirstInterface dan SecondInterface
class DemoClass implements FirstInterface, SecondInterface {
  public void myMethod() {
    System.out.println("Some text..");
  }
  public void myOtherMethod() {
    System.out.println("Some other text...");
  }
}

class MyMainClass {
  public static void main(String[] args) {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}

```

output:
```
Some text...
Some other text...
```

