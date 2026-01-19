# 🎬 Proje Senaryosu: Gelişmiş Sertifika & Veri Sistemi

## 🏢 Bağlam
Müşteri: "Sertifika veriyoruz ama kullanıcı sayfayı yenileyince ismi gidiyor. Ayrıca sertifikayı PDF olarak kaydetmek istiyorlar."

## 📝 Gereksinimler (Spec Sheet)

### 1. İsmi Hatırla (LocalStorage)
Kullanıcı adını eğitim başında girdiğinde, tarayıcının hafızasına (Local Storage) kaydet.
- **Kayıt Kodu:** `localStorage.setItem("ogrenciAdi", "Ahmet");`
- **Okuma Kodu:** Eğitimi kapatıp açtığında JS, `localStorage.getItem("ogrenciAdi")` ile ismi bulsun ve Storyline'a geri yazsın.
- *Böylece kullanıcı sayfayı yenilese bile sistem onu tanısın.*

### 2. Rastgele Sertifika ID'si
Her sertifikanın benzersiz bir referans kodu olmalı (Örn: #CERT-9382).
- JS `Math.random()` fonksiyonunu kullanarak 4 haneli rastgele bir sayı üret.
- Bunu `%CertID%` değişkenine yaz ve sertifikanın sağ altına koy.

### 3. Print Only Certificate
Ekranda "Tebrikler, Eğitimi Bitirdin" yazıları ve butonlar var. Yazdır deyince bunlar çıkmasın, sadece sertifika çıksın.
- (Opsiyonel): Bunu yapmak için JS ile sayfadaki istenmeyen elementleri `display: none` yapman gerekebilir (Advanced DOM Manipulation).

## 🚀 Görev
Bu "Stateful" (Durum koruyan) sertifika sistemini kur. Kullanıcı sayfayı F5 yapsa bile bilgilerinin orada kaldığını kanıtla.
