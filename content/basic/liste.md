[🢀 Ana Sayfa](https://github.com/levham/java-lesson/blob/main/README.md)

# Liste Yapıları

<table>
  <thead>
    <tr>
      <th>Yapı</th>
      <th>Özellikler</th>
      <th>Kullanım Senaryosu</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ArrayList</td>
      <td>- Dinamik boyutlu dizi<br>- Hızlı erişim (index ile)<br>- Ortada ekleme/silme yavaş</td>
      <td>Sık erişim yapılan, sıralı veri tutmak</td>
    </tr>
    <tr>
      <td>LinkedList</td>
      <td>Çift bağlı liste<br>- Ortadan ekleme/silme hızlı<br>- Index ile erişim yavaş</td>
      <td>Kuyruk (Queue), yığın (Stack) gibi veri yapıları</td>
    </tr>
    <tr>
      <td>Vector</td>
      <td>ArrayList’e benzer<br>- Thread-safe (senkronize)<br>- Eski yapı</td>
      <td>Çoklu thread ortamında güvenli liste</td>
    </tr>
    <tr>
      <td>Stack</td>
      <td>Vector’den türetilmiştir<br>- LIFO mantığı (Last-In-First-Out)</td>
      <td>Undo/geri alma, işlem geçmişi, yığın mantığı</td>
    </tr>
    <tr>
      <td>Queue</td>
      <td>FIFO mantığı (First-In-First-Out)<br>- add, poll, peek metodları</td>
      <td>Kuyruk işlemleri, görev sıralama</td>
    </tr>
    <tr>
      <td>Deque</td>
      <td>Çift uçlu kuyruk<br>- Hem Stack hem Queue gibi kullanılabilir</td>
      <td>Modern Stack/Queue uygulamaları</td>
    </tr>
    <tr>
      <td>PriorityQueue</td>
      <td>Öncelik sırasına göre çıkarma<br>- Doğal sıralama veya Comparator ile çalışır</td>
      <td>Görev önceliği, zamanlama algoritmaları</td>
    </tr>
  </tbody>
</table>

#### ArrayList 

En yaygın, hızlı erişim için

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

#### LinkedList 

Ortadan ekleme/silme için uygun 
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





#### Vector

ArrayList’e benzer ama senkronizedir. Yani çoklu thread ortamında güvenlidir, fakat bu yüzden biraz daha yavaştır
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





#### Stack

LIFO (Last In First Out) mantığıyla çalışır. Yani en son eklenen eleman ilk çıkarılır.
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


#### Queue (Kuyruk)  

eklenen ilk eleman, çıkarılan ilk eleman olur.
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
