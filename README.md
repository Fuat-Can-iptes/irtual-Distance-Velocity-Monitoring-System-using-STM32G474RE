# Virtual-Distance-Velocity-Monitoring-System-using-STM32G474RE

**Kodun bulunduğu main dosyasına Core -> Src -> main.c  aracılığıyla ulaşabilirsiniz. **

Bu proje, STM32G474RE mikrodenetleyicisi kullanılarak sanal bir mesafe ölçümü ve ortalama hız hesaplama sistemini simüle eder. Sistem, mesafe değerlerine göre bir LED ile uyarı verir ve UART üzerinden haberleşme sağlanarak termitte anlık veriler görünecek şekilde durumu raporlar.

Projenin amacı, gerçek bir sensör olmadan bir nesnenin mesafesini ve hareket hızını sanal olarak simüle etmektir. Kodda:

generate_virtual_distance() fonksiyonu, nesnenin yaklaşıp uzaklaşmasını ve rastgele gürültüyü simüle eder.Rastgele gürültü üretilerek daha gerçekçi bir simulasyon ortamı sağlar.

update_average_velocity() fonksiyonu, mesafe değişimine bağlı olarak ortalama hız hesaplar.

LED (PA5) mesafe durumuna göre:

mesafe < 30 m → Kritik durum olarak değerlendiriliyor.Led sürekli yanıyor ve sisteme kritik uzaklık olarak mesaj gönderiliyor
30<mesafe<60 m → Uyarı durumunda LED yanıp sönüyor ve sisteme tehlikeli uzaklık olarak mesaj gönderiliyor.
60 m → Güvenli durum olarak değerlendiriliyor ve sisteme güvenli uzaklık olarak mesaj gönderiliyor. (LED kapalı)

UART üzerinden mesafe ve ortalama hız değerleri sürekli olarak gönderilir ve termitte anlık veriler gösteriliyor.

STM32CubeIDE ve termite kullanıldı.

Sistemin test edilmesi için herhangi bir fiziksel mesafe sensörü gerekmez; tamamen sanaldır.

// PROJE GÖRSELLERİ //



![Projeye kuşbakışı](https://github.com/user-attachments/assets/d4bdff14-976a-499d-93a5-770ba6d786c1)


<img width="1918" height="1137" alt="Sistemin anlık verisi 1" src="https://github.com/user-attachments/assets/24827652-72eb-481a-8f46-af6e36e5f67c" />

<img width="1919" height="1136" alt="Sistemin anlık verisi 2" src="https://github.com/user-attachments/assets/e3ff28cc-5ef8-4d64-8112-036c299c3911" />









