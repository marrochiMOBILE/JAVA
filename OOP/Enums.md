# Enums
Enum adalah "kelas" khusus yang mewakili sekelompok konstanta (variabel yang tidak dapat diubah, seperti variabel akhir).

Untuk membuat enum, gunakan kata kunci enum (bukan kelas atau antarmuka), dan pisahkan konstanta dengan koma. Perhatikan bahwa mereka harus dalam huruf besar:

```java

enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class MyClass { 
  public static void main(String[] args) { 
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar); 
  } 
}
```
output:
```
MEDIUM
```

Enum adalah kependekan dari "enumerasi", yang berarti "terdaftar secara khusus".

## Enum inside a Class

Anda juga dapat memiliki enum di dalam kelas:
```java
public class MyClass { 
  enum Level {
    LOW,
    MEDIUM,
    HIGH
  }

  public static void main(String[] args) { 
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar); 
  } 
}

```
output :
```
MEDIUM
```

## Enum in a Switch Statement
Enum sering digunakan dalam pernyataan sakelar untuk memeriksa nilai yang sesuai:
```java

Result Size: 668 x 508
MyClass.java 

enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class MyClass { 
  public static void main(String[] args) {
    Level myVar = Level.MEDIUM; 
                
    switch(myVar) {
      case LOW:
        System.out.println("Low level");
        break;
      case MEDIUM:
        System.out.println("Medium level");
        break;
      case HIGH:
        System.out.println("High level");
        break;
    }
  }
}
```

output:
```
Medium level
```

## Loop Through an Enum

Tipe enum memiliki metode nilai (), yang mengembalikan array dari semua konstanta enum. Metode ini berguna ketika Anda ingin mengulangi konstanta enum
```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class MyClass { 
  public static void main(String[] args) { 
    for (Level myVar : Level.values()) {
      System.out.println(myVar);
    }
  } 
}

```

output :
```
LOW
MEDIUM
HIGH
```

### Difference between Enums and Classes / perbedaan antara enums dan class enum
seperti halnya kelas, memiliki atribut dan metode. Satu-satunya perbedaan adalah bahwa konstanta enum bersifat publik, statis dan final (tidak dapat diubah - tidak dapat diganti).

Enum tidak dapat digunakan untuk membuat objek, dan itu tidak dapat memperluas kelas lain (tetapi dapat mengimplementasikan antarmuka).

Mengapa dan Kapan Menggunakan Enum?
Gunakan enum ketika Anda memiliki nilai yang Anda tahu tidak akan berubah, seperti hari bulan, hari, warna, setumpuk kartu, dll.
