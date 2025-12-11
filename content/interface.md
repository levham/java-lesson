[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Interface

-interface soyuttur
-projede hangi fonksiyonları kullanıcağı kurallar listesi gibi bir bölüm 
-kurallar listesi gibi davranır (rnek1,örnek2)

-interface taslaktır 
-classlar bunu doldurur.@Override ile 

-nesne oluşturalamaz(new ile kullanamazsın)
-implements edilirler ama bir sınıf implements i çok kere yapıalbilir 
-gövdesiz fonksiyonu alabilirler
-@Override ile interfacedeki fonksiyonlar tekrar tanımlanır

	örnek1
```
	interface IArac {
	    void hareketEt();   // gövdesiz metod
	    void dur();         // gövdesiz metod
	}

	class Araba implements IArac { //buradaki gibi bağladık
	    @Override
	    public void hareketEt() {
	        System.out.println("Hav Hav!");
	    }
	
	    @Override
	    public void dur() {
	        System.out.println("Köpek mama yiyor.");
	    }
	}
```


	örnek2
```

	interface Animal {
	    void makeSound();   // gövdesiz metod
	    void eat();         // gövdesiz metod
	}
	
	// Dog sınıfı interface'i uygular
	class Dog implements Animal {
	    @Override
	    public void makeSound() {
	        System.out.println("Hav Hav!");
	    }
	
	    @Override
	    public void eat() {
	        System.out.println("Köpek mama yiyor.");
	    }
	}
```

### Diğer Özellikler

Bir sınıfa çok fazla interface’i implements ile uygulayana bilir 
```
	class Bilgisayar implements IDosya, IProgram {
	}
```

Interface metodları publictir ve diğer classlarda tanımlanan fonksiyonlar @Override edilmelidir
```
	interface IArac {
	    void hareketEt();   // gövdesiz metod 
	}

	class Araba implements IArac {  
	           // Override yaptık ezdik
	    public void hareketEt() {
	        System.out.println("Hav Hav!");
	    }
	}	
```



Interface içinde tanımlanan değişkenler public static final olur.
Yani otomatik olarak sabit (constant) kabul edilir.
```
interface OkulKurallari {
    int MAX_OGRENCI = 100; // public static final int MAX_OGRENCI = 100;
}
```


Default metod (java+8) 
Gövdesi olan metot yazabilirsin.
Implement eden sınıflar isterse override eder, istemezse hazır haliyle kullanır.
```
interface Hayvan {
    void sesCikar();
    
    default void yasamAlani() {
        System.out.println("Genel yaşam alanı: Doğa");
    }
}
```

Static Metotlar (Java 8+)
Interface içinde static metot tanımlanabilir.
Sınıflar üzerinden değil, direkt interface adıyla çağrılır.

```
interface Matematik {
    static int topla(int a, int b) {
        return a + b;
    }
}
int sonuc = Matematik.topla(3, 5);
```


Private Metotlar (Java 9+)
Interface içinde private metot tanımlanabilir.
Amaç: default veya static metotların içinde tekrar eden kodları düzenlemek.

Dışarıdan erişilemez, sadece interface içindeki diğer metotlar kullanır.
```
interface Servis {
    default void islemYap() {
        log("İşlem başladı");
    }
    
    private void log(String mesaj) {
        System.out.println("LOG: " + mesaj);
    }
}
```
