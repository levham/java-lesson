[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Dosya Bilgisi

```
File file =new File("C:\\javafile\\test.txt");
if(file.exists()){
    System.out.println("Dosya adı : " + file.getName());
    System.out.println("Dosya yolu : " + file.getAbsolutePath());
    System.out.println("Dosya yazılabilir mi : " + file.canWrite());
    System.out.println("Dosya okunabilir mi : " + file.canRead());
    System.out.println("Dosya boyutu (byte) : " + file.length());
}
```