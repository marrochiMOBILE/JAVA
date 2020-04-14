# Polymorphism


Polimorfisme berarti "banyak bentuk", dan itu terjadi ketika kita memiliki banyak kelas yang terkait satu sama lain melalui pewarisan.

Seperti yang kami sebutkan di bab sebelumnya; Warisan memungkinkan kita mewarisi atribut dan metode dari kelas lain. Polimorfisme menggunakan metode-metode itu untuk melakukan tugas yang berbeda. Ini memungkinkan kami untuk melakukan satu tindakan dengan berbagai cara.

Sebagai contoh, pikirkan superclass bernama Animal yang memiliki metode yang disebut animalSound (). Subkelas Hewan dapat berupa Babi, Kucing, Anjing, Burung - Dan mereka juga memiliki implementasi sendiri dari suara binatang (babi oinks, dan kucing mengeong, dll.):

```java
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}
```

> Ingat dari bab Warisan bahwa kami menggunakan kata kunci `extends` untuk mewarisi dari suatu kelas.

Sekarang kita dapat membuat objek Babi dan Anjing dan memanggil metode animalSound () pada keduanya:
```java
// nama file MyMainClass.java

class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class MyMainClass {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();
    Animal myPig = new Pig();
    Animal myDog = new Dog();
        
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}

```

output:
```
The animal makes a sound
The pig says: wee wee
The dog says: bow wow
```

#### Mengapa dan Kapan Menggunakan "Warisan" dan "Polimorfisme"?
- Berguna untuk penggunaan kembali kode: menggunakan kembali atribut dan metode dari kelas yang ada saat Anda membuat kelas baru.
