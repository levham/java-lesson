[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# final

final, bir şeyin değiştirilemez olduğunu belirtir. 
final → değiştirilemez / miras alınamaz / override edilemez.
Kullanıldığı yere göre farklı anlamları vardır:

Değişkenlerde sabit olduğunu belirtir ve değiştirilemez 
```
final int PI = 3; 
// PI = 4;  // değiştiremeyiz 
```

 
Alt sınıflar tarafından override edilemez.
```
class Animal {
    public final void makeSound() {
        System.out.println("Hayvan ses çıkarıyor");
    }
}
class Dog extends Animal {
    // ❌ override edemezsin
}
```


Başka sınıflar tarafından extend edilemez.
```
final class Utility {
    // Bu sınıftan miras alınamaz
}
```
