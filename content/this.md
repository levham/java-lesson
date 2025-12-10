[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# this

This, içinde bulunduğun sınıfın mevcut nesnesini temsil eder.

sınıftaki değişkeni temsil eder.
```
public class Car {
    private String marka;

    public Car(String marka) {
        this.marka = marka; // "this.marka" sınıftaki değişken, "marka" parametre
    }
}
```


Aynı sınıf içindeki başka constructor’ı çağırmak için:
```
public Car(String marka) {
    this(marka, 2020); // başka constructor çağrısı
}

public Car(String marka, int yil) {
    this.marka = marka;
    this.yil = yil;
}
```


Mevcut nesneyi başka metoda göndermek için:
```
class Araba {
    String marka;
    int yil;

    Araba(String marka, int yil) {
        this.marka = marka;
        this.yil = yil;
    }

    @Override
    public String toString() {
        return "Araba [marka=" + marka + ", yil=" + yil + "]";
    }
}

public class Main {
    public static void main(String[] args) {
        Araba a = new Araba("BMW", 2020);
        System.out.println(a); // Çıktı: Araba [marka=BMW, yil=2020]
    }
}
```
Araba@6d06d69c gibi bir çıktı yerine
 
Araba [marka=BMW, yil=2020] gibi bir çıktı için toString i override ettik 