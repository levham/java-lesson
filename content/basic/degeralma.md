[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Kullanıcıdan Değer Almak

Scanner sınıfıyla veri alınır.
Alınan verinin değişkene kaydedilmesinde:
*nextLine() -> String
*nextInt() -> Integer
*nextByte() -> Byte
*nextFloat -> Float
*nextDouble -> Double 
Kaydedilmek istenen veri tipine göre kullanılır.
 
### String değer alma 
```
import java.util.Scanner;
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String metin = scanner.nextLine();
        System.out.println("metin: "+metin);
    }
```


### Int değer alma 

```
import java.util.Scanner;
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sayi = scanner.nextInt();
        System.out.println("sayi: "+sayi);
    }
```
