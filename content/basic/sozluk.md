[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Sözlük Yapıları

|Yapı	       |Özellikler      |Kullanım Senaryosu|
|--------------|----------------|------------------|
|HashMap|- Anahtarlar benzersizdir|	Genel amaçlı, hızlı arama ve ekleme gereken durumlar|
|.		|- Sıralama yoktur|.|
|.		|- Hızlı erişim sağlar|	.|
|TreeMap|- Anahtarları doğal sırasına göre tutar |Sıralı sözlük, alfabetik veya sayısal sıralama gereken durumlar|
|.		|- Red-Black Tree yapısı kullanır	|.|
|LinkedHashMap|	- Eklenme sırasını korur|Eklenme sırasına göre iterasyon yapmak isteyenler için|
|.		|- HashMap kadar hızlıdır|	.|
|Hashtable	- Eski yapıdır				|Çoklu thread ortamında güvenli kullanım|
|.		|- Thread-safe (senkronize)|.|
|.		|- Null anahtar/değer kabul etmez|	.|
|ConcurrentHashMap|- Thread-safe|Paralel programlama, çoklu thread erişimi gereken durumlar|
|.		|- Segmentlere bölünmüş yapı sayesinde yüksek performanslı	|


HashMap → En yaygın ve hızlı

TreeMap → Sıralı sözlük

LinkedHashMap → Eklenme sırasını korur

Hashtable → Eski, senkronize

ConcurrentHashMap → Modern, thread-safe


#### HashMapOrnek
```
import java.util.HashMap;
import java.util.Map;

public class HashMapOrnek {
    public static void main(String[] args) {
        Map<String, Integer> hashMap = new HashMap<>();
        hashMap.put("elma", 3);
        hashMap.put("armut", 5);
        hashMap.put("muz", 2);

        System.out.println("HashMap: " + hashMap);
    }
}
```
Özellik: Sıralama garantisi yoktur, hızlı erişim sağlar.


#### TreeMapOrnek
```
import java.util.TreeMap;
import java.util.Map;

public class TreeMapOrnek {
    public static void main(String[] args) {
        Map<String, Integer> treeMap = new TreeMap<>();
        treeMap.put("elma", 3);
        treeMap.put("armut", 5);
        treeMap.put("muz", 2);

        System.out.println("TreeMap: " + treeMap);
    }
}
```
Özellik: Anahtarları alfabetik veya doğal sırasına göre tutar.


#### LinkedHashMapOrnek
```
import java.util.LinkedHashMap;
import java.util.Map;

public class LinkedHashMapOrnek {
    public static void main(String[] args) {
        Map<String, Integer> linkedHashMap = new LinkedHashMap<>();
        linkedHashMap.put("elma", 3);
        linkedHashMap.put("armut", 5);
        linkedHashMap.put("muz", 2);

        System.out.println("LinkedHashMap: " + linkedHashMap);
    }
}
```
Özellik: Eklenme sırasını korur.






