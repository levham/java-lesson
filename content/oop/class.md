[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Sınıflar ve Nesneler
sınıflar özellikler ve metodları toplu şekilde göstermemizi sağlar.
``` class ``` anahtar kelimesiyle kullanılır

Deneme sınıfı aşağıdaki gibidir
```
class Deneme{
}
```

Özellik ve metod ekliyelim:
```
class Deneme{
	String isim;
	int yas;

	public void bilgi(){
		System.out.println("İsim:"+isim);
		System.out.println("Yaş:"+yas);
	}
}
```

Sınıfları çağırırken aşağıdaki gibi kullanırız.
```
Deneme deneme=new Deneme();
```

Sınıflara veri gönderirken veya metod çağırırken aşağıdaki gibi kulllanırız.
```
Deneme deneme=new Deneme();
deneme.isim="Ali";
deneme.yas=20,
deneme.bilgi();
```
