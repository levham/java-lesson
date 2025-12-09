[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Diziler

Boş Dizi
```
int[] a;
```

Eleman sayısı sınırlı olan dizi
```
String[] ogrenciler =new String(3) ;
```

Eleman sayısı sınırlı olmayan diziler Arraylistlerdir
```
ArrayList<String> liste = new ArrayList<>();
```


Dizi elemanlarını atamak
```
String[] ogrenciler =new String(3) ;
ogrenci[0]="";
ogrenci[1]="";
ogrenci[2]="";

//yukarıdaki dizide elemanlar teker teker tanımlanmış.
//ancak ogrenci[3] için bir tanımlama yapılamaz
//çünkü dizinin eleman sayısı 3 ten fazla olamaz 
```

Arraylistlere eleman eklemek
```
ArrayList<String> liste = new ArrayList<>();
liste.add("aa");
liste.add("bb");
```



Diziler üzerinde gezmek
```
//örnek string dizi
String[] ogrenciler ={"aa","bb","cc"};

for (int i :ogrenciler){
	System.out.println( ogrenci[i]);
}
```
 
ArrayList üzerinde gezmek

```
//örnek arraylist
ArrayList<String> liste = new ArrayList<>(Arrays.asList("aa", "bb"));

for (String a : liste) {
    System.out.println(a);
}
```


