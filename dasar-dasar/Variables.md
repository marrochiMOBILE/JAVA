# Variables

Variabel adalah wadah untuk menyimpan nilai data.

Di Java, ada berbagai jenis variabel, misalnya:

1. **String** - menyimpan teks, seperti "Halo". Nilai string dikelilingi oleh tanda kutip ganda
1. **int** - store integer (bilangan bulat), tanpa desimal, seperti 123 atau -123
1. **float** - menyimpan angka floating point, dengan desimal, seperti 19,99 atau -19,99
1. **char** - menyimpan karakter tunggal, seperti 'a' atau 'B'. Nilai-nilai Char dikelilingi oleh tanda kutip tunggal
1. **boolean** - menyimpan nilai dengan dua status: benar/**(true)** atau salah/**(false)**

## Declaring (Creating) Variables

Untuk membuat variabel, Anda harus menentukan tipe dan memberinya nilai:

|  penjelasan | contoh  | 
|---|---|
|**type** variable = value;|**char** myLetter = 'D';|

Anda akan belajar lebih banyak tentang tipe data di bab selanjutnya.

## Variabel Tampilan

Metode `println ()` sering digunakan untuk menampilkan variabel.

Untuk menggabungkan teks dan variabel, gunakan karakter +:

```java
String name = "John";
System.out.println("Hello " + name);
```
Anda juga dapat menggunakan karakter + untuk menambahkan variabel ke variabel lain:

```java
String firstName = "John ";
String lastName = "Doe";
String fullName = firstName + lastName;
System.out.println(fullName);
```

Untuk nilai numerik, karakter + berfungsi sebagai operator matematika (perhatikan bahwa kami menggunakan variabel int (integer) di sini):
```java
int x = 5;
int y = 6;
System.out.println(x + y);  // 11
```

Dari contoh di atas, Anda dapat mengharapkan:

x menyimpan nilai 5
y menyimpan nilai 6
Kemudian kami menggunakan metode println () untuk menampilkan nilai x + y, yaitu 11

### Declare Many Variables
Untuk mendeklarasikan lebih dari satu variabel dari jenis yang sama, gunakan daftar yang dipisahkan koma:
```java
int x = 5, y = 6, z = 50;
System.out.println(x + y + z);
```

## Identifiers
```java
// Good
int minutesPerHour = 60;

// OK, tetapi tidak begitu mudah untuk memahami apa yang sebenarnya
int m = 60;
```

Aturan umum untuk membuat nama untuk variabel (pengidentifikasi unik) adalah:

1. Nama dapat berisi huruf, angka, garis bawah, dan tanda dolar
1. Nama harus dimulai dengan huruf
1. Nama harus dimulai dengan huruf kecil dan tidak boleh mengandung spasi
1. Nama juga dapat dimulai dengan $ dan _ (tetapi kami tidak akan menggunakannya dalam tutorial ini)
1. Nama-nama adalah case-sensitive ("myVar" dan "myvar" adalah variabel yang berbeda)
1. Kata-kata yang dicadangkan (seperti kata kunci Java, seperti int atau boolean) tidak dapat digunakan sebagai nama
