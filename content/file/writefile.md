[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Dosyaya Yazdır

## Dosyanın üzerine yazdır
```
try {
    BufferedWriter writer =new BufferedWriter(
    	new FileWriter("C:\\javafile\\test.txt",true));
    writer.newLine();
    writer.write("Ahmet");
    System.out.println("Dosyaya yazıldı");
    writer.close();
} catch (IOException e) {
    e.printStackTrace();
}
```

## Dosyanın tamamına yazdır
```
try {
    BufferedWriter writer =new BufferedWriter(
    	new FileWriter("C:\\javafile\\test.txt"));
    writer.newLine();
    writer.write("Ahmet");
    System.out.println("Dosyaya yazıldı");
    writer.close();
} catch (IOException e) {
    e.printStackTrace();
}
```
