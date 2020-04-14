# Inheritance (Subclass and Superclass)
Di Jawa, dimungkinkan untuk mewarisi atribut dan metode dari satu kelas ke kelas lain. Kami mengelompokkan "konsep pewarisan" ke dalam dua kategori:

1. subclass (child) - kelas yang mewarisi dari kelas lain
1. superclass (parent) - kelas yang diwarisi dari

Untuk mewarisi dari kelas, gunakan kata kunci extends.

Pada contoh di bawah ini, kelas Car (subkelas) mewarisi atribut dan metode dari kelas vehicles (superclass):
```java
class Vehicle {
  protected String brand = "Ford";
  public void honk() {
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
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
Tuut, tuut!
Ford Mustang
```

Apakah Anda memperhatikan pengubah yang dilindungi di Vehicle ?

Kami menetapkan atribut merek di Vehicle  ke pengubah akses yang dilindungi. Jika disetel ke pribadi, kelas Mobil tidak akan dapat mengaksesnya.

Mengapa Dan Kapan Menggunakan "Warisan"?
- Berguna untuk penggunaan kembali kode: menggunakan kembali atribut dan metode dari kelas yang ada saat Anda membuat kelas baru.

Tip: Lihat juga bab selanjutnya, Polimorfisme, yang menggunakan metode yang diwarisi untuk melakukan tugas yang berbeda

## The final Keyword
Jika Anda tidak ingin kelas lain mewarisi dari suatu kelas, gunakan kata kunci terakhir:

> Jika Anda mencoba mengakses kelas final, Java akan menghasilkan kesalahan
```java
final class Vehicle {
  protected String brand = "Ford";
  public void honk() {
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle { // error final tidak bisa diwariskan
  private String modelName = "Mustang";
  public static void main(String[] args) {
    Car myFastCar = new Car();
    myFastCar.honk();
    System.out.println(myFastCar.brand + " " + myFastCar.modelName);
  }
}
```

output :
```java
Car.java:8: error: cannot inherit from final Vehicle
class Car extends Vehicle {
                  ^
1 error)
```
