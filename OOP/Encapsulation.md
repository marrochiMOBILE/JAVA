# Encapsulation
Arti Enkapsulasi, adalah untuk memastikan bahwa data "sensitif" disembunyikan dari pengguna. Untuk mencapai ini, Anda harus:

1. mendeklarasikan variabel / atribut kelas sebagai pribadi(`private`)
1. memberikan metode `get` dan `set` publik untuk mengakses dan memperbarui nilai variabel pribadi

## Get and Set
Anda telah belajar dari bab sebelumnya bahwa variabel pribadi hanya dapat diakses di dalam kelas yang sama (kelas luar tidak memiliki akses ke sana). Namun, dimungkinkan untuk mengaksesnya jika kami menyediakan metode mendapatkan dan mengatur publik.
Metode get mengembalikan nilai variabel, dan metode set menetapkan nilai.
Sintaks untuk keduanya adalah bahwa mereka mulai dengan get atau set, diikuti dengan nama variabel, dengan huruf pertama dalam huruf besar:

```java
public class Person {
  private String name; // private = akses terbatas

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```
#### Contoh dijelaskan
Metode get mengembalikan nilai nama variabel.

Metode yang ditetapkan mengambil parameter (newName) dan menetapkannya ke variabel nama. Kata kunci ini digunakan untuk merujuk ke objek saat ini.

Namun, karena variabel nama dinyatakan sebagai pribadi/`private`, kami tidak dapat mengaksesnya dari luar kelas ini:
```java
// buat file dengan nama Person.java
public class Person {
   private String name;

   // Getter
   public String getName() {
     return name;
   }

   // Setter
   public void setName(String newName) {
     this.name = newName;
   }
}
// end Person.java

// buat satu lagi di folder yang sama dengan nama MyClass.java
public class MyClass {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.name = "John";
    System.out.println(myObj.name);
  }
}
// end MyClass.java
```
output :
```
MyClass.java:4: error: name has private access in Person
    myObj.name = "John";
         ^
MyClass.java:5: error: name has private access in Person
    System.out.println(myObj.name);
                  ^
2 errors

/*
Namun, saat kami mencoba mengakses variabel pribadi/`private`, kami mendapatkan kesalahan!!
*/
```

Jika variabel dinyatakan sebagai publik/`public`, kami akan mengharapkan output berikut:
```
John
```

> `Sebagai gantinya, kami menggunakan metode getName () dan setName () untuk mengakses dan memperbarui variabel:`
```java
// buat file dengan nama Person.java
public class Person {
   private String name;

   // Getter
   public String getName() {
     return name;
   }

   // Setter
   public void setName(String newName) {
     this.name = newName;
   }
}
// end Person.java

// buat satu lagi di folder yang sama dengan nama MyClass.java
public class MyClass {
  public static void main(String[ ] args) {
    Person myObj = new Person();
    myObj.setName("John");
    System.out.println(myObj.getName());
  }
}
// end MyClass.java
```

output :
```
John
```

## Why Encapsulation?
1. Kontrol atribut dan metode kelas yang lebih baik
1. Atribut kelas dapat dibuat hanya-baca (jika Anda hanya menggunakan metode get), atau hanya-tulis (jika Anda hanya menggunakan metode yang ditetapkan)
1. Fleksibel: programmer dapat mengubah satu bagian kode tanpa mempengaruhi bagian lainnya
1. Peningkatan keamanan data

