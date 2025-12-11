[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Javada Program Çalıştırma

Javada program çalıştırmak için 
- önce java dosyası class'a dönüştürülür. 
- daha sonra main bulunan class çalıştırılır.

```
javac Deneme.java User.java Main.java
java Main 
```
Böylelikle projemiz çalıştırılmış oldu. 



# Javada Projeyi jar a çevirme

```
javac Deneme.java User.java Main.java
jar cfe program.jar Test *.class
```


# Jar dosyasını .exe’ye çevirmek 

Bunun için ek araçlar kullanılır:

*Launch4j → Jar dosyasını Windows .exe haline getirir.
*JSmooth → Benzer şekilde jar’ı exe’ye dönüştürür.
*Inno Setup / NSIS → Jar’ı paketleyip kurulum dosyası yapabilirsin.
