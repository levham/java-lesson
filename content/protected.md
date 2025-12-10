[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# protected

```
protected String odemeYontemi;
protected double tutar;
```

Aynı sınıf içinde: protected olarak tanımlanan üyeler, sınıfın içinde erişilebilir.
Aynı paket içinde: Aynı paket içindeki diğer sınıflardan da erişilebilir.
Alt sınıflarda: Bu sınıfı miras alan (subclass) sınıflarda da erişilebilir.
Sınıf dışı kodlardan: Diğer paketlerdeki sınıflardan, bu sınıfın protected üyelerine doğrudan erişilemez.

class Animal {
    protected String name;

    protected void makeSound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    public void display() {
        // 'name' ve 'makeSound' protected olduğu için
        // buradan erişilebilir
        System.out.println(name);
        makeSound();
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.display();  // Erişim mümkün
    }
}

Bu örnekte, Dog sınıfı Animal sınıfını miras alır ve Animal sınıfındaki protected üyelere erişebilir.

Özetle, protected ile erişilen üyeler:
Aynı sınıf içinden.
Aynı paketteki diğer sınıflardan.
Bu sınıfı miras alan alt sınıflardan erişilebilir.


