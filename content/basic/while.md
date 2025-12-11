[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# While, Do While Döngüsü

## While Döngüsü

While içindeki koşul kadar While bloğunbdaki kodlar çalışır 

```
int i=0
while(i<5)
{
	System.out.println( "sayi:"+i );
	i++
}
```

Eğer While içindeki koşul doğruysa program sonsuz kez çalıştırılır.

```
while(true)
{
	System.out.println( "sonsuz döngü" );
}
```

```
int i=0
while(i<1)
{
	System.out.println( "sonsuz döngü" );
}
```

## Do While Döngüsü

Önce do içindeki kodlar çalıştırılır.
Eğer Whiledeki koşul doğruysa do bloğu koşul kadar çalıştırlır
```
int i =1
do{
	System.out.println( i )
	i++
}
while(i<3)
```