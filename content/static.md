[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# static

Static, bir şeyin sınıfa ait olduğunu belirtir. Yani nesneye değil, doğrudan sınıfa bağlıdır.
static → sınıfa ait, ortak, nesne oluşturmadan erişilebilir.

Değişken global davranır 
```
class Counter {
    static int count = 0;
    public Counter() {
        count++;
    }
}
public class Test {
    public static void main(String[] args) {
        new Counter();
        new Counter();
        System.out.println(Counter.count); // 2
    }
}
```


Sınıf yüklenirken bir kez çalışır.
```
class Demo {
    static {
        System.out.println("Sınıf yükleniyor...");
    }
}
```


Nesne oluşturmadan kullanmayı sağlar
```
class MathUtil {
    public static int kare(int x) {
        return x * x;
    }
}
public class Test {
    public static void main(String[] args) {
        System.out.println(MathUtil.kare(5)); // 25
    }
}
```
