# 🏥 Laboratuvar Test Sonuçları Takibi

Bu proje, hastaların tıbbi laboratuvar test sonuçlarını kaydetmek, listelemek, düzenlemek ve kalıcı olarak saklamak amacıyla geliştirilmiş bir masaüstü uygulamasıdır. **Java** programlama dili ve **JavaFX** arayüz kütüphanesi kullanılarak tasarlanmıştır.

Projenin temel amacı, manuel kağıt işlemlerini azaltarak hasta test verilerinin dijital ortamda düzenli bir tablo yapısında tutulmasını sağlamaktır.

## 🚀 Proje Özellikleri

Uygulama aşağıdaki temel fonksiyonlara sahiptir:

* **Veri Girişi:** Hasta adı, test adı (Örn: Hemoglobin, Glukoz), sonuç değeri, referans aralığı ve birim bilgileri sisteme girilebilir.
* **Otomatik Durum Belirleme:** Girilen sonuçlara göre basit bir mantıkla (şimdilik simülasyon amaçlı) test durumu sistem tarafından atanır.
* **Veri Listeleme:** Eklenen tüm kayıtlar detaylı bir tablo üzerinde görüntülenir.
* **Kalıcı Veri Saklama (Dosya İşlemleri):** Uygulama kapatıldığında veriler kaybolmaz. Arka planda `veriler.txt` adlı bir dosyaya yazılır ve uygulama tekrar açıldığında bu kayıtlar otomatik olarak geri yüklenir.
* **Kayıt Silme:** Tablodan seçilen herhangi bir test sonucu silinebilir ve bu işlem dosyadan da güncellenir.
* **Raporlama:** Mevcut listeyi konsol ekranına döküm olarak yazdırma seçeneği bulunur.
* **Özelleştirilmiş Arayüz:** Standart JavaFX görünümü yerine CSS (`stil.css`) dosyası ile modern ve kullanıcı dostu bir tasarım uygulanmıştır.

## 🛠 Kullanılan Teknolojiler

Bu proje geliştirilirken aşağıdaki teknolojiler kullanılmıştır:

* **Java (JDK 21):** Programın ana mantığı ve backend işlemleri.
* **JavaFX:** Grafiksel kullanıcı arayüzü (GUI) tasarımı.
* **FXML:** Arayüz bileşenlerinin XML formatında tanımlanması.
* **CSS:** Arayüz bileşenlerinin renklendirilmesi ve stil işlemleri.
* **Dosya İşlemleri (Java I/O):** Verilerin metin dosyası üzerinde okunup yazılması.

## 💻 Kurulum ve Çalıştırma

Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1.  Bu depoyu (repository) bilgisayarınıza indirin veya klonlayın.
2.  Proje dosyasını **IntelliJ IDEA** veya **Eclipse** gibi bir IDE ile açın.
3.  Bilgisayarınızda JavaFX kütüphanesinin kurulu olduğundan ve IDE ayarlarının yapıldığından emin olun.
4.  `src/application/LaboratuvarApp.java` dosyasını bulun ve projeyi bu sınıf üzerinden çalıştırın.

## 📂 Proje Yapısı

Proje, kodun okunabilirliğini ve yönetilebilirliğini artırmak için **MVC (Model-View-Controller)** yapısına benzer bir mimaride düzenlenmiştir:

* `model`: Veri yapısını temsil eden sınıflar (**TestSonucu.java**).
* `view`: Kullanıcı arayüzü dosyaları (**laboratuvar_arayuzu.fxml**, **stil.css**).
* `controller`: Arayüz ve veri arasındaki mantığı yöneten sınıf (**LaboratuvarController.java**).
* `application`: Uygulamanın başlatıcı sınıfı (**LaboratuvarApp.java**).
