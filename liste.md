[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Liste Yapıları

|Yapı	|Özellikler	|Kullanım Senaryosu|
|ArrayList	|- Dinamik boyutlu dizi|Sık erişim yapılan, sıralı veri tutmak için|
|		|- Hızlı erişim (index ile)|.|
|		|- Ekleme/silme yavaş olabilir (ortada işlem yapınca)|.|
|LinkedList	|- Çift bağlı liste|Kuyruk (Queue), yığın (Stack) gibi veri yapıları için|
|		|- Ortadan ekleme/silme hızlı|.|
|		|- Index ile erişim yavaş| .|
|Vector	|- ArrayList’e benzer|Çoklu thread ortamında güvenli liste gerekirse|
|		|- Thread-safe (senkronize)|.|
|		|- Eski yapıdır		| .|
|Stack	|- Vector’den türetilmiştir|Geri alma (undo), işlem geçmişi, yığın mantığı gereken durumlar|
|		|- LIFO (Last-In-First-Out) mantığıyla çalışır|	.|	
 
|Yapı	|Özellikler	|Kullanım Senaryosu|
|------|-----|-----|
|ArrayList|-Dinamik boyutlu dizi|Sık erişim yapılan, sıralı veri tutmak|
|.|- Hızlı erişim (index ile)|.|
|.|- Ortada ekleme/silme yavaş|.|
|LinkedList|Çift bağlı liste<br>- Ortadan ekleme/silme hızlı<br>- Index ile erişim yavaş|Kuyruk (Queue), yığın (Stack) gibi veri yapıları|
|Vector|ArrayList’e benzer<br>- Thread-safe (senkronize)<br>- Eski yapı|Çoklu thread ortamında güvenli liste|
|Stack|Vector’den türetilmiştir<br>- LIFO mantığı (Last-In-First-Out)|Undo/geri alma, işlem geçmişi, yığın mantığı|
|Queue|FIFO mantığı (First-In-First-Out)<br>- add, poll, peek metodları|Kuyruk işlemleri, görev sıralama|
|Deque|Çift uçlu kuyruk<br>-Hem Stack hem Queue gibi kullanılabilir| Modern Stack/Queue uygulamaları|
|PriorityQueue|Öncelik sırasına göre çıkarma<br>- Doğal sıralama veya Comparator ile çalışır|Görev önceliği, zamanlama algoritmaları|



ArrayList → En yaygın, hızlı erişim için
LinkedList → Ortadan ekleme/silme için uygun
Vector → Eski ama thread-safe
Stack → LIFO mantığıyla özel kullanım

```
import java.util.ArrayList;
public class ArrayListOrnek {
    public static void main(String[] args) {
        // ArrayList oluşturma
        ArrayList<String> meyveler = new ArrayList<>();

        // Eleman ekleme
        meyveler.add("Elma");
        meyveler.add("Muz");
        meyveler.add("Çilek");

        // Elemanları yazdırma
        System.out.println("Meyveler: " + meyveler);

        // Belirli bir elemana erişim
        System.out.println("İlk meyve: " + meyveler.get(0));

        // Eleman silme
        meyveler.remove("Muz");
        System.out.println("Silindikten sonra: " + meyveler);
    }
}
```


```
import java.util.LinkedList;
public class LinkedListOrnek {
    public static void main(String[] args) {
        // LinkedList oluşturma
        LinkedList<String> sehirler = new LinkedList<>();

        // Eleman ekleme
        sehirler.add("İstanbul");
        sehirler.add("Ankara");
        sehirler.add("İzmir");

        // Elemanları yazdırma
        System.out.println("Şehirler: " + sehirler);

        // Başa ve sona eleman ekleme
        sehirler.addFirst("Bursa");
        sehirler.addLast("Antalya");
        System.out.println("Başa ve sona ekledikten sonra: " + sehirler);

        // İlk ve son elemanı alma
        System.out.println("İlk şehir: " + sehirler.getFirst());
        System.out.println("Son şehir: " + sehirler.getLast());
    }
}
```

```
import java.util.Vector;
public class VectorOrnek {
    public static void main(String[] args) {
        // Vector oluşturma
        Vector<String> dersler = new Vector<>();

        // Eleman ekleme
        dersler.add("Matematik");
        dersler.add("Fizik");
        dersler.add("Kimya");

        // Elemanları yazdırma
        System.out.println("Dersler: " + dersler);

        // Belirli bir elemana erişim
        System.out.println("İlk ders: " + dersler.get(0));

        // Eleman silme
        dersler.remove("Fizik");
        System.out.println("Silindikten sonra: " + dersler);
    }
}
```
Vector, ArrayList’e benzer ama senkronizedir. Yani çoklu thread ortamında güvenlidir, fakat bu yüzden biraz daha yavaştır


```
import java.util.Stack;
public class StackOrnek {
    public static void main(String[] args) {
        // Stack oluşturma
        Stack<String> kitaplar = new Stack<>();

        // Eleman ekleme (push)
        kitaplar.push("Roman");
        kitaplar.push("Şiir");
        kitaplar.push("Tarih");

        // Elemanları yazdırma
        System.out.println("Kitaplar: " + kitaplar);

        // En üstteki elemana erişim (peek)
        System.out.println("En üstteki kitap: " + kitaplar.peek());

        // Eleman çıkarma (pop)
        String silinen = kitaplar.pop();
        System.out.println("Çıkarılan kitap: " + silinen);
        System.out.println("Pop sonrası kitaplar: " + kitaplar);
    }
}
```
Stack, LIFO (Last In First Out) mantığıyla çalışır. Yani en son eklenen eleman ilk çıkarılır.


```
import java.util.LinkedList;
import java.util.Queue;

public class QueueOrnek {
    public static void main(String[] args) {
        // Queue oluşturma (LinkedList kullanarak)
        Queue<String> kuyruk = new LinkedList<>();

        // Eleman ekleme
        kuyruk.add("Ali");
        kuyruk.add("Ayşe");
        kuyruk.add("Mehmet");

        System.out.println("Kuyruk: " + kuyruk);

        // İlk elemana bakma (peek)
        System.out.println("Sıradaki kişi: " + kuyruk.peek());

        // Eleman çıkarma (poll)
        String cikan = kuyruk.poll();
        System.out.println("Çıkarılan kişi: " + cikan);
        System.out.println("Kuyruk (poll sonrası): " + kuyruk);

        // Tekrar çıkarma
        kuyruk.remove();
        System.out.println("Kuyruk (remove sonrası): " + kuyruk);
    }
}
```
Queue (Kuyruk)  eklenen ilk eleman, çıkarılan ilk eleman olur.