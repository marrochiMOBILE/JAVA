# Inner Classes

Di Java, mungkin juga untuk kelas sarang (kelas dalam kelas). Tujuan dari kelas bersarang adalah untuk mengelompokkan kelas-kelas yang termasuk bersama, yang membuat kode Anda lebih mudah dibaca dan dipelihara.

Untuk mengakses kelas dalam, buat objek dari kelas luar, dan kemudian buat objek dari kelas dalam:
```java
class OuterClass {
  int x = 10;

  class InnerClass {
    int y = 5;
  }
}

public class MyMainClass {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```
output:
```
15
```
Tidak seperti kelas "reguler", kelas dalam bisa bersifat pribadi atau dilindungi. Jika Anda tidak ingin objek luar mengakses kelas dalam, nyatakan kelas sebagai pribadi/private:

##  Private Inner Class

```java
class OuterClass {
  int x = 10;

  private class InnerClass { // disini akan terjadi error karena class diakses dariluar class
    int y = 5;
  }
}

public class MyMainClass {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}
```

output:
```
MyMainClass.java:12: error: OuterClass.InnerClass has private access in OuterClass
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
 
```

## Static Inner Class

Kelas dalam juga bisa statis, yang berarti bahwa Anda dapat mengaksesnya tanpa membuat objek dari kelas luar:
```java
class OuterClass {
  int x = 10;

  static class InnerClass {
    int y = 5;
  }
}

public class MyMainClass {
  public static void main(String[] args) {
    OuterClass.InnerClass myInner = new OuterClass.InnerClass();
    System.out.println(myInner.y);
  }
}
```
output :
```
5
```
Catatan: sama seperti atribut dan metode statis, kelas dalam statis tidak memiliki akses ke anggota kelas luar.
## Access Outer Class From Inner Class

Salah satu keuntungan dari kelas dalam, adalah mereka dapat mengakses atribut dan metode dari kelas luar:
```java
class OuterClass {
  int x = 10; 

  class InnerClass {
    public int myInnerMethod() {
      return x;
    }
  }
}

public class MyMainClass {
  public static void main(String args[]) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.myInnerMethod());
  }
}
```

output :
```
10
```

