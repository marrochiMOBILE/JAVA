# ArrayList
Kelas ArrayList adalah array resizable, yang dapat ditemukan dalam paket java.util.

Perbedaan antara array bawaan dan ArrayList di Java, adalah ukuran array tidak dapat dimodifikasi (jika Anda ingin menambah atau menghapus elemen ke / dari array, Anda harus membuat yang baru). Sementara elemen dapat ditambahkan dan dihapus dari ArrayList kapan pun Anda mau. Sintaksnya juga sedikit berbeda:


> Buat objek ArrayList bernama mobil yang akan menyimpan string:
```java
import java.util.ArrayList; // import class ArrayList

ArrayList<String> cars = new ArrayList<String>(); // membuat object ArrayList
```

Jika Anda tidak tahu apa itu paket, baca Tutorial Paket Java kami.

### Add Items

Kelas ArrayList memiliki banyak metode yang berguna. Misalnya, untuk menambahkan elemen ke ArrayList, gunakan metode `add ()`:
```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
  } 
}

```

output :
```
[Volvo, BMW, Ford, Mazda]
```
### Access an Item
Untuk mengakses elemen di ArrayList, gunakan metode `get ()` dan lihat nomor indeks:

```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars.get(0));
  } 
}

```

output :
```
Volvo
```

### Change an Item

Untuk memodifikasi elemen, gunakan metode `set ()` dan lihat nomor indeks:
```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    cars.set(0, "Opel");
    System.out.println(cars);
  } 
}

```

output:
```
[Opel, BMW, Ford, Mazda]
```

### Remove an Item

Untuk menghapus elemen, gunakan metode `remove ()` dan lihat nomor indeks:
```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    cars.remove(0);
    System.out.println(cars);
  } 
}

```

output: 
```
[BMW, Ford, Mazda]
```

Untuk menghapus semua elemen di ArrayList, gunakan metode `clear ()`:
```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    cars.clear();
    System.out.println(cars);
  } 
}

```
output:
```
[]
```

## ArrayList Size

Untuk mengetahui berapa banyak elemen yang dimiliki ArrayList, gunakan metode ukuran / `size()`:

```java

import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars.size());
  } 
}

```

output:
```
4
```

## Loop Through an ArrayList


Ulangi elemen ArrayList dengan  for loop, dan gunakan metode `size ()` untuk menentukan berapa kali loop harus dijalankan
```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    for (int i = 0; i < cars.size(); i++) {
      System.out.println(cars.get(i));
    }
  } 
}
```

output :
```
Volvo
BMW
Ford
Mazda
```


Anda juga dapat mengulang melalui ArrayList dengan untuk-setiap loop:

```java
import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    for (String i : cars) {  
      System.out.println(i);
    }
  } 
}
```
output :
```
Volvo
BMW
Ford
Mazda
```
Buat ArrayList untuk menyimpan angka (tambahkan elemen bertipe Integer):

```java

import java.util.ArrayList;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<Integer> myNumbers = new ArrayList<Integer>();
    myNumbers.add(10);
    myNumbers.add(15);
    myNumbers.add(20);
    myNumbers.add(25);
    for (int i : myNumbers) {
      System.out.println(i);
    }
  } 
}
```
output:
```
10
15
20
25
```


## Sort an ArrayList
Kelas lain yang berguna dalam paket java.util adalah kelas Koleksi, yang mencakup metode `sort ()` untuk menyortir daftar berdasarkan abjad atau numerik:

```java
import java.util.ArrayList;
import java.util.Collections;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    
    Collections.sort(cars);

    for (String i : cars) {
      System.out.println(i);
    }
  } 
}
```

output :
```
BMW
Ford
Mazda
Volvo
```

Sortir ArrayList of Integer:
```java
import java.util.ArrayList;
import java.util.Collections;

public class MyClass { 
  public static void main(String[] args) { 
    ArrayList<Integer> myNumbers = new ArrayList<Integer>();
    myNumbers.add(33);
    myNumbers.add(15);
    myNumbers.add(20);
    myNumbers.add(34);
    myNumbers.add(8);
    myNumbers.add(12);

    Collections.sort(myNumbers);

    for (int i : myNumbers) {
      System.out.println(i);
    }
  } 
}
```

output :
```
8
12
15
20
33
34
```
