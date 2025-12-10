[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# super

Super, üst sınıfı (parent class) temsil eder.  
Kalıtım olduğunda, alt sınıf üst sınıfın özelliklerine veya metodlarına super ile erişebilir.


Üst sınıftaki alanlara erişmek için (eğer protected/public ise):
```
class Person {
    protected String name = "Ayşe";
}

class Student extends Person {
    public void showInfo() {
        System.out.println(super.name); // üst sınıftaki name alanı
    }
}
```


Üst sınıftaki metodu çağırmak için:
```
class Vehicle {
    public void start() {
        System.out.println("Araç çalışıyor...");
    }
}

class Car extends Vehicle {
    @Override
    public void start() {
        super.start(); // önce Vehicle’ın metodunu çalıştırır
        System.out.println("Araba motoru çalıştı!");
    }
}
```


Üst sınıfın constructor’ını çağırmak için:
```
class Company {
    public Company(String companyName) {
        System.out.println("Şirket oluşturuldu: " + companyName);
    }
}

class Employee extends Company {
    public Employee(String companyName) {
        super(companyName); // Company constructor çağrılır
    }
}
```