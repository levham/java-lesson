[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Abstract

-abstract soyuttur
-nasıl yapıldığını anlatır
-taslak gibi davranır 

-nesne oluşturalamaz(new ile kullanamazsın)
-extend edilirler ama bir sınıf extends i 1 kere yapıalbilir 
-gövdeli veya gövdesiz fonksiyonu olabilri
-super ile üst sınıftaki veriyi alır 

```
abstract class Animal {
    private String isim;

    public Animal(String isim) {
        this.isim = isim;
    }

    // Soyut metod (gövdesiz)
    public abstract void makeSound();

    // Normal metod (gövdesi var)
    public void printName() {
        System.out.println("Hayvan adı: " + isim);
    }
}

class Cat extends Animal {
    public Cat(String isim) {
        super(isim);
    }

    @Override
    public void makeSound() {
        System.out.println("Miyav!");
    }
}

public class ZooApp {
    public static void main(String[] args) {
        Animal dog = new Dog("Karabaş");
        Animal cat = new Cat("Pamuk");
 
        cat.printName();   // Hayvan adı: Pamuk
        cat.makeSound();   // Miyav!
    }
}
```

