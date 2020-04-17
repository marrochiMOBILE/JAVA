# Strings
String digunakan untuk menyimpan teks.

Variabel String berisi kumpulan karakter yang dikelilingi oleh tanda kutip ganda:

```java
String greeting = "Hello";
```

## String Length
String di Java sebenarnya adalah objek, yang berisi metode yang dapat melakukan operasi tertentu pada string. Misalnya, panjang string dapat ditemukan dengan metode `length ()`:

```java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println("The length of the txt string is: " + txt.length()); // The length of the txt string is: 26
```

## More String Methods
Ada banyak metode string yang tersedia, misalnya toUpperCase () dan toLowerCase ():
```java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Outputs "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Outputs "hello world"
```

## Finding a Character in a String
Metode indexOf () mengembalikan indeks (posisi) dari kemunculan pertama dari teks yang ditentukan dalam string (termasuk spasi):
```java
String txt = "Please locate where 'locate' occurs!";
    System.out.println(txt.indexOf("locate")) // 7
```

## String Concatenation

Operator + dapat digunakan di antara string untuk menggabungkannya. Ini disebut penggabungan:
```java
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName); // John Doe
```


Anda juga dapat menggunakan metode concat () untuk menggabungkan dua string:
```java
String firstName = "John ";
String lastName = "Doe";
System.out.println(firstName.concat(lastName)); // John Doe
```
## Special Characters

Karena string harus ditulis dalam tanda kutip, Java akan salah memahami string ini, dan menghasilkan kesalahan:
```java
String txt = "We are the so-called "Vikings" from the north."; // kesalahan
```

Solusi untuk menghindari masalah ini, adalah dengan menggunakan karakter backslash escape.

Karakter pelarian backslash (\) mengubah karakter khusus menjadi karakter string:

| Escape character | 	Result |	Description |
|---|---|---|
| `\'` |	`'`	| Single quote |
| `\"` |	`"`	| Double quote |
| `\\` |	`\` | 	Backslash |



Urutan \ "menyisipkan kutipan ganda dalam sebuah string:
```java
String txt = "We are the so-called \"Vikings\" from the north.";
```

Urutan \ 'memasukkan kutipan tunggal dalam sebuah string:
```java
String txt = "It\'s alright.";
```


Urutan \\ menyisipkan backslash tunggal dalam sebuah string:
```java
String txt = "The character \\ is called backslash.";
```


| Code	| Result |	
|---|---|
| `\n` |	New Line |	
| `\r` |	Carriage Return |	
| `\t` |	Tab  |	
| `\b` |	Backspace	 |
| `\f` |	Form Feed  |

## Adding Numbers and Strings
### WARNING
```
PERINGATAN!

Java menggunakan operator + untuk penambahan dan penggabungan.

Angka ditambahkan. String digabungkan.
```

Jika Anda menambahkan dua angka, hasilnya adalah angka:

```java
int x = 10;
int y = 20;
int z = x + y; // 30
```


Jika Anda menambahkan dua string, hasilnya akan menjadi rangkaian string:
```java
String x = "10";
String y = "20";
String z = x + y; //1020
```

Jika Anda menambahkan angka dan string, hasilnya akan menjadi rangkaian string:

```java
String x = "10";
int y = 20;
String z = x + y; // 1020
```

<h1>Complete String Reference</h1>
