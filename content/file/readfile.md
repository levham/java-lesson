[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Dosyayı oku

```
File file =new File("C:\\javafile\\test.txt");
try {
    Scanner reader = new Scanner(file);
    while (reader.hasNextLine()){
        String line = reader.nextLine();
        System.out.println(line);
    }
    reader.close();
} catch (FileNotFoundException e) {
    e.printStackTrace();
}
```
 