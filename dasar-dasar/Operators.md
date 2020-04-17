# Operators

Operator digunakan untuk melakukan operasi pada variabel dan nilai.

Dalam contoh di bawah ini, kami menggunakan operator + untuk menambahkan bersama dua nilai:
```java
int x = 100 + 50;
```

Meskipun operator + sering digunakan untuk menjumlahkan dua nilai, seperti dalam contoh di atas, ia juga dapat digunakan untuk menambahkan bersama-sama variabel dan nilai, atau variabel dan variabel lain:

```java
int sum1 = 100 + 50;        // 150 (100 + 50)
int sum2 = sum1 + 250;      // 400 (150 + 250)
int sum3 = sum2 + sum2;     // 800 (400 + 400)
```

Java membagi operator menjadi beberapa grup berikut:

1. Operator aritmatika
1. Operator penugasan
1. Operator pembanding
1. Operator logis
1. Operator bitwise

## Arithmetic Operators

Operator aritmatika digunakan untuk melakukan operasi matematika umum.
```java
    int x = 5;
    int y = 3;
    System.out.println(x + y);
```

|  Operator | Name  | 	Description  | 	Example  | 
|---|---|---|---|
| +  | Addition  | Menambahkan bersama dua nilai |  x + y |  
|  - |  Subtraction | Kurangi satu nilai dari yang lain  | x - y  |  
| *  | Multiplication  | Mengalikan dua nilai  | x * y  |  
| /  | Division  | Membagi satu nilai dengan yang lain  | x / y  |  
| %  |  Modulus | Mengembalikan sisa divisi | x % y  |  
| --  | Decrement  | Mengurangi nilai variabel sebesar 1  | --y  |  
| ++  | 	Increment  | Meningkatkan nilai suatu variabel sebesar 1  | ++x  |  

## Assignment Operators
Operator tugas digunakan untuk menetapkan nilai ke variabel.

Dalam contoh di bawah ini, kami menggunakan operator penugasan (=) untuk menetapkan nilai 10 ke variabel yang disebut x:
```java
int x = 10;
```
Operator penugasan tambahan (+ =) menambahkan nilai ke variabel:
```java
int x = 10;
    x += 5;
    System.out.println(x); // 15
```

A list of all assignment operators:
|Operator  |  	Example | 	Same As  | 
|---|---|---|
|  = | x = 5  | 	x = 5  | 
| +=  | 	x += 3  | x = x + 3  |  
|  -= | 	x -= 3  | x = x - 3  |  
|  *= | 	x *= 3  |  x = x * 3 |  
|  /= | x /= 3  | x = x / 3 |  
|  %= | x %= 3  | x = x % 3  |  
| &=  | x &= 3  | x = x & 3  |    
| ^=  |  	x ^= 3 |  	x = x ^ 3 |  
| >>=  |  	x >>= 3 | 	x = x >> 3 |  
| <<=  | 	x <<= 3  |  x = x << 3 | 


 `|=`   `x |= 3`   `x = x | 3`   
 
 
 ## Comparison Operators
 
Operator perbandingan digunakan untuk membandingkan dua nilai:
| Operator |	Name	 | Example |
|---|---|---|
| ==	| Equal to	| x == y |	
| !=	| Not equal	| x != y |
| >	| Greater than |	x > y	|
| <	| Less than	 | x < y	|

## Operator yang logis
   `| Operator |	Name	| Description	| Example`
1. `&&` 	| `Logical and`	| `Returns true if both statements are true` |	`x < 5 &&  x < 10`	|
1. `||` 	| `Logical or` | 	`Returns true if one of the statements is true` |	`x < 5 || x < 4` |	
1. `!`	 | `Logical not	Reverse the result` |  `returns false if the result is true	` | `!(x < 5 && x < 10)` |

