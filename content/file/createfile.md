[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Dosya Oluştur

```
File file =new File("C:\\javafile\\test.txt");
try {
    if (file.createNewFile()){
        System.out.println("Dosya oluşturuldu");
    }else{
        System.out.println("Dosya zaten mevcut");
    }
} catch (IOException e) {
    e.printStackTrace();
}
```
 