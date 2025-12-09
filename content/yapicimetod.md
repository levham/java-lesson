[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Yapici Metod

Sınıfa veri gönderdiğimizde bu veriyi yapıcı metod ile de alabiliriz
```
class Deneme{
	private String isim;
	private int yas;

	public Deneme(String isim,int yas){
		this.isim=isim;
		this.yas=yas;

	}

	public void bilgi(){
		System.out.println("İsim:"+isim);
		System.out.println("Yaş:"+yas);
	}
}
```

yukarıdaki classa veri göndeirlrken aşağıdaki kodları kullanırız
```
Deneme deneme=new Deneme("Ali",20);
deneme.bilgi();
```

