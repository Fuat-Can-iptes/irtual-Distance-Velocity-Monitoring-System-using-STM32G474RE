# Virtual-Distance-Velocity-Monitoring-System-using-STM32G474RE
Bu proje, STM32G474RE mikrodenetleyicisi kullanılarak sanal bir mesafe ölçümü ve ortalama hız hesaplama sistemini simüle eder. Sistem, mesafe değerlerine göre bir LED ile uyarı verir ve UART üzerinden haberleşme sağlanarak termitte anlık veriler görünecek şekilde durumu raporlar.

Projenin amacı, gerçek bir sensör olmadan bir nesnenin mesafesini ve hareket hızını sanal olarak simüle etmektir. Kodda:

generate_virtual_distance() fonksiyonu, nesnenin yaklaşıp uzaklaşmasını ve rastgele gürültüyü simüle eder.Rastgele gürültü üretilerek daha gerçekçi bir simulasyon ortamı sağlar.

update_average_velocity() fonksiyonu, mesafe değişimine bağlı olarak ortalama hız hesaplar.

LED (PA5) mesafe durumuna göre:

mesafe < 30 m → Kritik durum olarak değerlendiriliyor.Led sürekli yanıp sönüyor ve sisteme kritik uzaklık olarak mesaj gönderiliyor
30<mesafe<60 m → Uyarı durumunda LED yanıp sönüyor ve sisteme tehlikeli uzaklık olarak mesaj gönderiliyor.
60 m → Güvenli durum olarak değerlendiriliyor ve sisteme güvenli uzaklık olarak mesaj gönderiliyor. (LED kapalı)

UART üzerinden mesafe ve ortalama hız değerleri sürekli olarak gönderilir ve termitte anlık veriler gösteriliyor.

STM32CubeIDE ve termite kullanıldı.

Sistemin test edilmesi için herhangi bir fiziksel mesafe sensörü gerekmez; tamamen sanaldır.




