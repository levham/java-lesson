[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Enum

>içinde sabit değerler olan bir classtır 

-tanımlarken 
```
enum Gunler {
	PAZARTESI,SALI,CARSAMBA,PERSEMBE,CUMA,CUMARTESI,PAZAR
	} 
```
çağırırken 
```
Gunler gunler=Gunler.PAZARTESI; 
```

tanımlarken değişken, metod alabilir
```
enum Gunler {
	PAZARTESI(1),SALI(2),CARSAMBA(3),PERSEMBE(4),CUMA(5),CUMARTESI(6),PAZAR(7);

	private final int gun;
	public Gunler(int gun){
		this.gun=gun;
	} 

	public int getValue(){
		return gun;
	

	} 
	// Başka classtayken
	//System.out.println(Gunler.CARSAMBA.getValue()); // 3
```

>gelişmiş örnek
```
public class E13 {

    public static void main(String[] args) {
        Gunler bugun = Gunler.CARSAMBA;

        System.out.println("Bugün: " + bugun + " (" + bugun.getGunNo() + ")");
        if (bugun.isWorkDay()) {
            System.out.println("Bugün iş günü.");
        } else {
            System.out.println("Bugün tatil!");
        }
        
    }
}


enum Gunler {
    PAZARTESI(1, true),
    SALI(2, true),
    CARSAMBA(3, true),
    PERSEMBE(4, true),
    CUMA(5, true),
    CUMARTESI(6, false),
    PAZAR(7, false);

    private final int gunNo;
    private final boolean isWorkDay;

    Gunler(int gunNo, boolean isWorkDay) {
        this.gunNo = gunNo;
        this.isWorkDay = isWorkDay;
    }

    public int getGunNo() {
        return gunNo;
    }

    public boolean isWorkDay() {
        return isWorkDay;
    }
}
```
