# While Loop

Loop dapat menjalankan blok kode selama kondisi yang ditentukan tercapai.

Loop berguna karena menghemat waktu, mengurangi kesalahan, dan membuat kode lebih mudah dibaca.

```java
while (condition) {
  // code block to be executed
}
```


Dalam contoh di bawah ini, kode dalam loop akan berjalan, berulang-ulang, selama variabel (i) kurang dari 5:
```java
 int i = 0;
    while (i < 5) {
      System.out.println(i);
      i++;
    } 
```

> Catatan: Jangan lupa untuk menambah variabel yang digunakan dalam kondisi tersebut, jika tidak, loop tidak akan pernah berakhir!

## The Do/While Loop

Do / while loop adalah varian dari while loop. Loop ini akan mengeksekusi blok kode sekali, sebelum memeriksa apakah kondisinya benar, maka itu akan mengulangi loop selama kondisinya benar.

```java
do {
  // code block to be executed
}
while (condition);
```

Contoh di bawah ini menggunakan do / while loop. Loop akan selalu dieksekusi setidaknya sekali, walaupun kondisinya salah, karena blok kode dieksekusi sebelum kondisi diuji:

```java
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

> Jangan lupa untuk menambah variabel yang digunakan dalam kondisi tersebut, jika tidak, loop tidak akan pernah berakhir!

