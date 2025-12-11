[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Try Catch Finally

## Try Catch 

```
try {
    int sayi = 1/0;
    System.out.println("Sayı: " + sayi);
} catch (Exception e) {
    System.out.println("Hata:!"+ e);
}
```
try -> hata var mı diye bakılır
catch->hata varsa çalışır
Exception ile hata bir değişkene atanır. Hata görüntülenir


## Try Catch Finally

try -> hata var mı diye bakılır
catch->hata varsa çalışır
finally-> hata olsa da olmasa da çalışır 

```
try {
    int sayi = 1/0;
    System.out.println("Sayı: " + sayi);
} catch (Exception e) {
    System.out.println("Hata:!"+ e);
} finally {
    System.out.println("Program sonlandı.");
}
```


## Try() Catch Finally (try-with-resources yapısı )

Dosya veya bağlantı gibi AutoCloseable nesneleri otomatik kapatmak için kullanılır:
```
try (FileReader fr = new FileReader("dosya.txt")) {
    // dosya okuma işlemleri
} catch (IOException e) {
    e.printStackTrace();
} finally {
    System.out.println("İşlem tamamlandı.");
}
```

