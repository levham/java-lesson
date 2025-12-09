[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Switch Case

İf Else gibi ama belli değerlerde karşılaştırma yapmak için kullanabildiğiniz bir yapı. 
Switch içinde değişken olur.
Case içindeki değer değişkene eşitse o casedeki kodlar break a kadar çalıştırılır. 
Hiçbir case çalışmazsa default kısmı çalışır 
```
int a=1
switch(a) { 
	case 1:
		System.out.println("a=1 dir")
	 	break;
	case 2:
		System.out.println("a=2 dir")
	 	break;
	default:
		System.out.println("a bilinmiyor")
	 	break;
}
```

Eğer case içinde break yoksa diğer case de çalıştırılır.
```
int a=1
switch(a) { 
	case 1:
	case 2:
		System.out.println("a=1 veya a=2 dir")
	 	break;
	default:
		System.out.println("a bilinmiyor")
	 	break;
}
```
