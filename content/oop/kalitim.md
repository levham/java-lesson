[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Kalıtım

Kalıtım ile ortak özellikler veya metodlar sınıflarda toplanabilir.

```
class Kitap{
	String isim;
	int basimYili;

	public void bilgi(){
		System.out.println("Kitabın ismi:"+isim);
		System.out.println("Kitabın basım yılıi:"+basimYili);
		}
}

class Roman extends Kitap{
	String kitapTuru;
}


Roman sınıfı artık Kitap sınıfındaki özellikleri ve metodları aldı.
örnek yapalım main classta buna örnek verelim

class main{
	public static void main(String[] args) {
		Roman roman=new Roman();
		roman.isim=
		roman.basimYili=
		roman.bilgi();
	}
}
```
