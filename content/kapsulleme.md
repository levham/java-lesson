[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Kapsulleme
Kapsulleme ile private özelliklere public foknsiyonlar sayesinde ulaşırız. 
aşağıdaki örnkete isim ve yas özelliklerine yapıcı metod üzerinden değer atamış olduk.
bilgi metoduyla da isim ve yas özelliklerini kullandık.

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
