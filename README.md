# maze_with_dikstra


Bu proje ile nesneye yönelik programlama ve veri yapıları algoritmalarını kullanarak Şirinler oyunu tasarlanması amaçlanmıştır. Seçilen oyuncunun Labirent 
içerisinde puanlarını bitirmeden önce Şirine’ye ulaşması gerekmektedir. Kullanıcı oyun başlamadan önce seçtiği oyunculardan birini klavye yardımı ile kontrol edecek 
ve Şirine’ye ulaştırmaya çalışacaktır. Düşman karakterler ise oyuncuyu Dijkstra Algoritması yardımı ile yakalamaya çalışacaktır.

Java dili, Netbeans IDE ‘si ve  JFRAME arayüz kütüphanesi yardımı ile yazılmış programımızda –tuşlarla oyuncu kontrolü için KeyEvent sınıfı ve bu sınıfın getirdiği 
VK_RIGHT, VK_LEFT, VK_DOWN, VK_UP özellikleri kullanılır. en kısa yol bilgisine ulasmak için dijisktra algoritmasından faydalanılmıstır.  

Sınıf hiyerarşisi üzerine kurulan oyun mimarisi ana sınıf olan soyut karakter sınıfının temel ıd,lokasyon, vb bilgileri ile olusturulması ile baslar. düşman ve 
oyuncu sınıfları karakter sınıfından kalıtım alırlar ve getter setter marifetleri ile ve kendilerine has parametrelerle özelleştirilirler. 

Seçim ekranı butonlar ile tembel veya gözlüklü olarak oyuncuya karakterini seçme sansı sunar. Oyuncu sınıfından türetilen tembel ve gözlüklü sınıfları
özelleştirilmiştir. (örn adımSayisi)  oyuncu karakteri sabit baslangıc noktasında baslamak üzere oyuncuObje.setlokX() gibi metotlarla oyuna hazırlanır.

Dışarıdan 0 ve 1 ler seklinde kodlanan labirent bilgisi  ve string halde sunulan düşman ve düşmanın başlangıc durum bilgileri okunarak labirent çizimi sağlanır. 
Düşman okunan lokasyonlarda yerini almıs ve en kısa yol algoritması ile oyuncunun güncel lokasyonuna göre en kısa mesafeyi bulur, ekrana çizer ve sırası geldiğinde 
hamlesini yapar.

Oyun view sınıfı içerisinde oynanmakta main metodumuzda dosya okuma islemleri yapılmaktadır. 

Puan durumu güncel olarak hesaplanmakta, ve ekrana yansıtılmaktadır. Oyun şirineye ulasıldıgını veya puanın 0 a düştüğünü yakalarsa sona ermektedir.

<img width="439" alt="Screenshot_1" src="https://user-images.githubusercontent.com/43906043/175386865-e1ff2169-f125-4e65-9d44-9bbdb951a22c.png">

<img width="509" alt="Screenshot_2" src="https://user-images.githubusercontent.com/43906043/175386869-88028535-e1e7-4010-a966-b622c23e01cc.png">

<img width="513" alt="Screenshot_3" src="https://user-images.githubusercontent.com/43906043/175386872-c0efa419-54a2-4fc7-b36b-d83041a67f1e.png">

<img width="511" alt="Screenshot_4" src="https://user-images.githubusercontent.com/43906043/175386874-8bf4c762-c3a9-4d0e-a68f-d6898949dbfc.png">

<img width="513" alt="Screenshot_5" src="https://user-images.githubusercontent.com/43906043/175386876-a3a691c3-e7d1-4d9a-9781-5a2855c05a8a.png">

<img width="511" alt="Screenshot_6" src="https://user-images.githubusercontent.com/43906043/175386879-646b8245-3cc5-4a35-aa28-bf9e45e01fdb.png">

<img width="513" alt="Screenshot_7" src="https://user-images.githubusercontent.com/43906043/175386882-836376df-0837-432b-8379-529650e75aa7.png">

## SONUÇ :

tembel ya da gözlüklü şirini seçebildiğimiz bir ekranla oyuna başlarız. seçimimizi yaptıktan sonra oyun ekranı(görsel harita) karşımıza çıkar. bu ekran dosya 
bilgilerine göre dinamik olarak okutulur. 1 ve 0 durumuna göre duvarların ve geçilebilecek patikaların yazdırılması sağlanır. bunun yanında okunan string değerlere 
göre azman ve gargamelin ya da azman veya gargamelin oyuna başlamasına karar verilir. azman tek birim, gargamel ise 2 birim hareket eder. zamana bağlı olarak altınlar 
ve hazine ekranda belirip kaybolur. puanlar dinamiktir, hazinenin kaç puan ifade ettiği kod üzerinde değişebilecek şekilde tasarlanmıştır. her puan karakterimizin 
yaşaması için ek puan sağlayacaktır. dijkstra algoritmasıyla bizi en kısa sürede yakalamaya çalışan düşman karakter/karakterler bize ulaşmadan şirineye ulaşılması 
durumunad oyun kazanılır. aksi takdirde oyun kaybedilir. programda abstract sınıflar, get ve setot metotları, encapsulation gibi nesneye yönelik konseptlerin hepsi 
kullanılmıştır. 13 adet sınıf view'e bağlıdır ve bu sınıf üzerinden programın işleyişi kontrol edilir.


