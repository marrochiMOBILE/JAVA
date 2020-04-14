# Abstract Classes and Methods
Abstraksi data adalah proses menyembunyikan detail tertentu dan hanya menampilkan informasi penting kepada pengguna.
Abstraksi dapat dicapai dengan kelas atau antarmuka abstrak (yang akan Anda pelajari lebih lanjut di bab selanjutnya).

Kata kunci abstrak adalah pengubah non-akses, digunakan untuk kelas dan metode:

1. Abstract class: adalah kelas terbatas yang tidak dapat digunakan untuk membuat objek (untuk mengaksesnya, itu harus diwarisi dari kelas lain).

1. Abstract method: hanya dapat digunakan dalam kelas abstrak, dan tidak memiliki tubuh. Tubuh disediakan oleh subclass (diwarisi dari).

Kelas abstrak dapat memiliki metode abstrak dan reguler:

```java
abstract class Animal {
  public abstract void animalSound();
  public void sleep() {
    System.out.println("Zzz");
  }
}
```

Dari contoh di atas, tidak mungkin membuat objek kelas Hewan:

```java
Animal myObj = new Animal(); // akan menghasilkan kesalahan
```

Untuk mengakses kelas abstrak, itu harus diwarisi dari kelas lain. Mari kita konversi kelas Animal yang kita gunakan di bab Polimorfisme menjadi kelas abstrak:

> Ingat dari bab Warisan bahwa kami menggunakan kata kunci extends untuk mewarisi dari suatu kelas.

```java
// Abstract class
abstract class Animal {
  //  Metode abstrak (tidak memiliki tubuh)
  public abstract void animalSound();
  
  // Regular method
  public void sleep() {
    System.out.println("Zzz");
  }
}

// Subclass (inherit from Animal)
class Pig extends Animal {
  public void animalSound() {
    // Tubuh hewan () disediakan di sini
    System.out.println("The pig says: wee wee");
  }
}

class MyMainClass {
  public static void main(String[] args) {
    Pig myPig = new Pig(); // membuat object
    myPig.animalSound();
    myPig.sleep();
  }
}
```

output:
```
The pig says: wee wee
Zzz
```
