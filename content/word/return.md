[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# return

-fonksiyonlara geri dnöüş yapması için kullanılır.
-fonksiyonları sonlandırmak için kullanılabilir.
-main metodunda kullanılırsa program kapatılır.

-fonksiyonlara geri dönüş yapması için kullanılır.
```
public String deneme(){
	String kelime="merhaba"+dünya;
	return kelime;
}
```
```
public int deneme(){
	int a=2;
	return a;
}
```



-fonksiyonları sonlandırmak için kullanılabilir.
```
public void deneme(){


}
```

-main metodunda kullanılırsa program kapatılır.
```
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sayi = scanner.nextInt();
        if (2 == sayi) {
            System.out.println(2);
            return;
        } else {
            System.out.println(3);
        }
        System.out.println("error");
}
```



