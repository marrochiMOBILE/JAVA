# Switch

## Switch Statements
Gunakan pernyataan beralih untuk memilih salah satu dari banyak blok kode yang akan dieksekusi.

```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```
Begini Cara kerjanya:
  <ul>
       <li>Ekspresi sakelar dievaluasi sekali.</li>
       <li>Nilai ekspresi dibandingkan dengan nilai setiap kasus.</li>
       <li>Jika ada kecocokan, blok kode terkait dijalankan.</li>
       <li>Istirahat dan kata kunci default adalah opsional, dan akan dijelaskan nanti dalam bab ini</li>
   </ul>

Contoh di bawah ini menggunakan nomor hari kerja untuk menghitung hari kerja:
```java
int day = 4;
switch (day) {
  case 1:
    System.out.println("Monday");
    break;
  case 2:
    System.out.println("Tuesday");
    break;
  case 3:
    System.out.println("Wednesday");
    break;
  case 4:
    System.out.println("Thursday");
    break;
  case 5:
    System.out.println("Friday");
    break;
  case 6:
    System.out.println("Saturday");
    break;
  case 7:
    System.out.println("Sunday");
    break;
}
// Outputs "Thursday" 
```

### The break Keyword
Ketika Java mencapai kata kunci istirahat/break, itu keluar dari blok saklar.

Ini akan menghentikan pelaksanaan lebih banyak kode dan pengujian kasus di dalam blok.

Ketika kecocokan ditemukan, dan pekerjaan selesai, saatnya istirahat/break. Tidak perlu pengujian lebih lanjut.

```
Istirahat/break dapat menghemat banyak waktu eksekusi karena "mengabaikan" eksekusi semua kode lainnya di blok sakelar.
```

### The default Keyword

Kata kunci default menentukan beberapa kode untuk dijalankan jika tidak ada kecocokan huruf:

```java
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
// Outputs "Looking forward to the Weekend"
```



