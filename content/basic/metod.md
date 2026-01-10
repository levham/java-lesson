[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Metod

```
public void deneme(){
	System.out.println("parametresiz fonksiyon");
	System.out.println("geri dönüş değeri olmayan fonksiyon");
}
```
```
public void deneme(String mesaj){
	System.out.println("parametreli fonksiyon");
	System.out.println("geri dönüş değeri olmayan fonksiyon");
	System.out.println("Mesaj"+mesaj);
}
```
```
public int deneme(){
	System.out.println("parametresiz fonksiyon");
	System.out.println("geri dönüş olan fonksiyon");
	int a=2;
	return a;
}
```
```
public int deneme(int a,int b){
	System.out.println("parametreli fonksiyon");
	System.out.println("geri dönüş olan fonksiyon");
	int toplam=a+b;
	return toplam;
}
``` 

Mainde kullanırken
```
public class Test1 {
    public static void main(String[] args) {
         System.out.println(karesini_al(3));
    }

	public static int karesini_al(int a){
		int sonuc=a*a;
		return sonuc;
	}
}
``` 

Classlarda çağırırken 
```
class Matematik{
	public int karesini_al(int a){
		int sonuc=a*a;
		return sonuc;
	}
}

public class Test1 {
    public static void main(String[] args) {
         Matematik matematik=new Matematik();
         System.out.println(matematik.karesini_al(3));
    }
}
``` 