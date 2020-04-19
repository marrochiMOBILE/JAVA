# Method
Metode adalah blok kode yang hanya berjalan ketika dipanggil.

Anda dapat mengirimkan data, yang dikenal sebagai parameter, ke dalam metode.

Metode digunakan untuk melakukan tindakan tertentu, dan mereka juga dikenal sebagai fungsi.

Mengapa menggunakan metode? Untuk menggunakan kembali kode: tentukan kode sekali, dan gunakan berkali-kali.

### Create a Method

Metode harus dideklarasikan dalam kelas. Itu didefinisikan dengan nama metode, diikuti oleh tanda kurung (). Java menyediakan beberapa metode yang telah ditentukan, seperti System.out.println (), tetapi Anda juga dapat membuat metode Anda sendiri untuk melakukan tindakan tertentu:

```java
public class MyClass {
  static void myMethod() {
    // code untuk di eksekusi
  }
}
```

Contoh Dijelaskan
1. `myMethod ()` adalah nama metode
1. `static` berarti bahwa metode tersebut milik kelas MyClass dan bukan objek dari kelas MyClass. Anda akan belajar lebih banyak tentang  objek dan cara mengakses metode melalui objek nanti dalam tutorial ini.
1. `void` berarti bahwa metode ini tidak memiliki nilai balik. Anda akan belajar lebih banyak tentang nilai pengembalian nanti di bab ini


### Call a Method
Untuk memanggil metode di Jawa, tulis nama metode yang diikuti oleh dua tanda kurung () dan tanda titik koma;

Dalam contoh berikut, myMethod () digunakan untuk mencetak teks (tindakan), ketika dipanggil:

```java
public class MyClass {
  static void myMethod() {
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}

// Outputs "I just got executed!"
```


Suatu metode juga dapat dipanggil beberapa kali:
```java
public class MyClass {
  static void myMethod() {
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) {
    myMethod();
    myMethod();
    myMethod();
  }
}

// I just got executed!
// I just got executed!
// I just got executed!
```

# Method Parameters
## Parameters and Arguments

Informasi dapat diteruskan ke metode sebagai parameter. Parameter bertindak sebagai variabel di dalam metode.

Parameter ditentukan setelah nama metode, di dalam tanda kurung. Anda dapat menambahkan sebanyak mungkin parameter yang Anda inginkan, cukup pisahkan dengan koma.

Contoh berikut memiliki metode yang menggunakan String yang disebut fname sebagai parameter. Ketika metode dipanggil, kami memberikan nama depan, yang digunakan di dalam metode untuk mencetak nama lengkap:

```java
public class MyClass {
  static void myMethod(String fname) {
    System.out.println(fname + " Refsnes");
  }

  public static void main(String[] args) {
    myMethod("Liam");
    myMethod("Jenny");
    myMethod("Anja");
  }
}
// Liam Refsnes
// Jenny Refsnes
// Anja Refsnes
```

```
Ketika parameter dilewatkan ke metode, itu disebut argumen. Jadi, dari contoh di atas: fname adalah parameter, sementara Liam, Jenny dan Anja adalah argumen.
```

### Multiple Parameters

Anda dapat memiliki banyak parameter yang Anda inginkan:
```java
public class MyClass {
  static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }

  public static void main(String[] args) {
    myMethod("Liam", 5);
    myMethod("Jenny", 8);
    myMethod("Anja", 31);
  }
}

// Liam is 5
// Jenny is 8
// Anja is 31
```

```
Perhatikan bahwa ketika Anda bekerja dengan beberapa parameter, pemanggilan metode harus memiliki jumlah argumen yang sama dengan parameter, dan argumen harus diteruskan dalam urutan yang sama.
```

### Return Values
The void keyword, used in the examples above, indicates that the method should not return a value. If you want the method to return a value, you can use a primitive data type (such as int, char, etc.) instead of void, and use the return keyword inside the method:

```java
public class MyClass {
  static int myMethod(int x) {
    return 5 + x;
  }

  public static void main(String[] args) {
    System.out.println(myMethod(3));
  }
}
// Outputs 8 (5 + 3)
```


Contoh ini mengembalikan jumlah dari dua parameter metode:
```java
public class MyClass {
  static int myMethod(int x, int y) {
    return x + y;
  }

  public static void main(String[] args) {
    System.out.println(myMethod(5, 3));
  }
}
// Outputs 8 (5 + 3)
```


Anda juga dapat menyimpan hasilnya dalam variabel (disarankan, karena lebih mudah dibaca dan dipelihara)
```java
public class MyClass {
  static int myMethod(int x, int y) {
    return x + y;
  }

  public static void main(String[] args) {
    int z = myMethod(5, 3);
    System.out.println(z);
  }
}
// Outputs 8 (5 + 3)
```

### A Method with If...Else
A Method with If...Else
```java
public class MyClass {

  // membuat method
  static void checkAge(int age) {

    // jika kurang dari 18
    if (age < 18) {
      System.out.println("Access denied - You are not old enough!");

    // jika bukan dari kurang 18
    } else {
      System.out.println("Access granted - You are old enough!");
    }

  }

  public static void main(String[] args) {
    checkAge(20); // memanggil method dengan argumen 20
  }
}

// Outputs "Access granted - You are old enough!"
```

# Method Overloading
Dengan kelebihan metode, beberapa metode dapat memiliki nama yang sama dengan parameter yang berbeda:
```java
int myMethod(int x)
float myMethod(float x)
double myMethod(double x, double y)
```

Pertimbangkan contoh berikut, yang memiliki dua metode yang menambahkan nomor dari tipe yang berbeda:
```java
public class MyClass {
  static int plusMethodInt(int x, int y) {
    return x + y;
  }
  
  static double plusMethodDouble(double x, double y) {
    return x + y;
  }
  
  public static void main(String[] args) {
    int myNum1 = plusMethodInt(8, 5);
    double myNum2 = plusMethodDouble(4.3, 6.26);
    System.out.println("int: " + myNum1);
    System.out.println("double: " + myNum2);
  }
}
```

output :
```
int: 13
double: 10.559999999999999
```

Daripada mendefinisikan dua metode yang harus melakukan hal yang sama, lebih baik membebani satu metode.

Pada contoh di bawah ini, kami membebani metode plusMethod agar bekerja untuk int dan ganda:

```java
public class MyClass {
  static int plusMethod(int x, int y) {
    return x + y;
  }
  
  static double plusMethod(double x, double y) {
    return x + y;
  }
  
  public static void main(String[] args) {
    int myNum1 = plusMethod(8, 5);
    double myNum2 = plusMethod(4.3, 6.26);
    System.out.println("int: " + myNum1);
    System.out.println("double: " + myNum2);
  }
}

```


output:
```
int: 13
double: 10.559999999999999
```
##### warning
```
Catatan: Banyak metode dapat memiliki nama yang sama selama jumlah dan / atau tipe parameternya berbeda.
```
