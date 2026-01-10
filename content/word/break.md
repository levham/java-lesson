[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Break 

for, switch, while ve do while döngülerini kırmak(sonlandırmak ) için kullanılabilir.

```
for(int i ;i <10 ;i++){
	if (i==5) {
		System.out.println("a=5 dir");
		break;
		}
}
```

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

```
int i=0;
while(i<5)
{
	System.out.println( "sayi:"+i );
	if (i==5) {
		System.out.println("a=5 dir");
		break;
	}
	i++;
}
```

```
int i =1;
do{
	if (i==5) {
		System.out.println("a=5 dir");
		break;
	}
	i++
}
while(i<3)
```