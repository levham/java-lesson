[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Sınıflar Arası İlişkiler
 
### 1)Kalıtım (miras)

>"ortak özellik var mı ?"

Ortak özellikleri kullanmak ve güçlü bağlar için kalıtım kullanırız. extends ve implements kullanılır. Örneğin:
- EvcilHayvan sınıfı hem Köpek hem de Kedi türlerini kapsar ve kalıtım bu bağı daha doğru bir şekilde ifade eder.

```
// Üst sınıf (Base Class)
class EvcilHayvan {
    String isim;

    EvcilHayvan(String isim) {
        this.isim = isim;
    }

    void sesCikar() {
        System.out.println("Evcil hayvan ses çıkarıyor...");
    }

    void bilgiVer() {
        System.out.println("Benim adım " + isim);
    }
}

// Alt sınıf (Subclass) - Köpek
class Kopek extends EvcilHayvan {
    Kopek(String isim) {
        super(isim); // üst sınıfın constructor'ını çağırır
    }

    @Override
    void sesCikar() {
        System.out.println("Hav Hav!");
    }
}

// Alt sınıf (Subclass) - Kedi
class Kedi extends EvcilHayvan {
    Kedi(String isim) {
        super(isim);
    }

    @Override
    void sesCikar() {
        System.out.println("Miyav Miyav!");
    }
}

// Test sınıfı
public class Main {
    public static void main(String[] args) {
        EvcilHayvan hayvan1 = new Kopek("Karabaş");
        EvcilHayvan hayvan2 = new Kedi("Pamuk");

        hayvan1.bilgiVer();
        hayvan1.sesCikar();

        hayvan2.bilgiVer();
        hayvan2.sesCikar();
    }
}
```



### 2)Composition (Bileşim)

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
```

### 3)Aggregation (Toplama)

Bir sınıf başka bir sınıfı içerir, ama içerilen nesne bağımsız yaşayabilir.

"Has-a" ilişkisine benzer ama daha gevşek bağ.

Üniversite öğrencileri vardır, ama öğrenci üniversite olmadan da var olabilir.
```
// Öğrenci sınıfı
class Ogrenci {
    String isim;

    Ogrenci(String isim) {
        this.isim = isim;
    }

    void bilgiVer() {
        System.out.println("Öğrenci: " + isim);
    }
}

// Üniversite sınıfı (Aggregation)
class Universite {
    String ad;
    Ogrenci ogrenci; // aggregation: Üniversite bir Öğrenciye sahiptir

    Universite(String ad, Ogrenci ogrenci) {
        this.ad = ad;
        this.ogrenci = ogrenci;
    }

    void universiteBilgi() {
        System.out.println("Üniversite: " + ad);
        ogrenci.bilgiVer();
    }
}

// Test
public class Main {
    public static void main(String[] args) {
        Ogrenci ogrenci = new Ogrenci("Ahmet");
        Universite uni = new Universite("İstanbul Üniversitesi", ogrenci);

        uni.universiteBilgi();
    }
}
```


### 4)Association (Bağlantı)

Association’da iki sınıf birbirini kullanabilir ama bağımlı değildir.
```
// Hasta sınıfı
class Hasta {
    String isim;

    Hasta(String isim) {
        this.isim = isim;
    }

    void bilgiVer() {
        System.out.println("Hasta: " + isim);
    }
}

// Doktor sınıfı
class Doktor {
    String isim;

    Doktor(String isim) {
        this.isim = isim;
    }

    void tedaviEt(Hasta hasta) {
        System.out.println("Doktor " + isim + " hastayı tedavi ediyor: " + hasta.isim);
    }
}

// Test
public class Main2 {
    public static void main(String[] args) {
        Hasta hasta = new Hasta("Mehmet");
        Doktor doktor = new Doktor("Dr. Ayşe");

        hasta.bilgiVer();
        doktor.tedaviEt(hasta);
    }
}
```


