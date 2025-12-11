[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Composition (Bileşim)

>"içerir mi ? sahip mi ? "

Composition (bileşim), kodun daha esnek olmasını sağlar çünkü bir sınıfın bileşenleri değişebilir ve değişiklikler sınıf hiyerarşisini etkilemez.Örneğin:
- Bir Araba sınıfı bir Motor sınıfını içerebilir. Bu durumda, Araba bir Motor içerir, ancak Motor sınıfı Araba sınıfından türetilmez

```
// Motor sınıfı (bağımsız bir sınıf)
class Motor {
    int beygirGucu;

    Motor(int beygirGucu) {
        this.beygirGucu = beygirGucu;
    }

    void calistir() {
        System.out.println("Motor çalışıyor... Beygir gücü: " + beygirGucu);
    }
}

// Araba sınıfı (Motor içerir)
class Araba {
    String marka;
    Motor motor; // composition: Araba bir Motor içerir

    Araba(String marka, Motor motor) {
        this.marka = marka;
        this.motor = motor;
    }

    void arabaBilgi() {
        System.out.println("Araba markası: " + marka);
        motor.calistir(); // Motor’un metodunu kullanıyoruz
    }
}

// Test sınıfı
public class Main {
    public static void main(String[] args) {
        Motor motor = new Motor(150);
        Araba araba = new Araba("Toyota", motor);

        araba.arabaBilgi();
    }
}