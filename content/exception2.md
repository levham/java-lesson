[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Exceptionlar


|Kategori	|Exception Türü		|Açıklama		|Ne Zaman Karşına Çıkar?|
|---|---|---|---|
|Checked	|IOException					|Dosya okuma/yazma hatalarında oluşur		|Dosya işlemleri, stream kullanımı|
|.			|SQLException					|Veritabanı bağlantı ve sorgu hataları		|JDBC, SQL sorguları|
|.			|ClassNotFoundException			|Olmayan sınıfı yüklemeye çalışıldığında	|Reflection, dinamik yükleme|
|.			|FileNotFoundException			|Dosya bulunamadığında						|Dosya açma işlemleri|
|Unchecked	|NullPointerException			|Null referansa erişim yapıldığında			|Nesneye erişmeden önce kontrol yapılmazsa|
|.			|ArrayIndexOutOfBoundsException	|Dizi sınırları dışına çıkıldığında			|Yanlış indeks kullanımı|
|.			|ArithmeticException			|Matematiksel hatalar (ör. sıfıra bölme)	|Hesaplama işlemleri|
|.			|IllegalArgumentException		|Metoda geçersiz argüman verildiğinde		|Parametre kontrolü yapılmazsa|
|Error (yakalanmaz)|	OutOfMemoryError	|Bellek tükenmesi							|Çok büyük veri yüklemeleri|
|.			|StackOverflowError				|Sonsuz özyineleme (recursive) çağrılar		|Yanlış recursive algoritmalar|