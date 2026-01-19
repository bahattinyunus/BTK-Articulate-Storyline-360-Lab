# 🎬 Proje Senaryosu: Adaptif Sınav Sistemi

## 🏢 Bağlam
Eğitim departmanı, "Bilenle bilmeyeniayırt edelim" diyor. Sınavda herkes aynı soruları çözmesin. Konuyu bilenler "Hızlı Geçiş" (Test-out) yapsın, bilmeyenler eğitime geri dönsün.

## 📝 Gereksinimler (Spec Sheet)

### 1. Ön Test (Pre-Test)
- Eğitimin en başına 5 soruluk bir sınav koy.
- **Soru Bankası A:** Bu sınav için zor soruları içeren bir havuz kullan.
- **Sonuç:**
    - Puan >= %80 ise: "Tebrikler, eğitimi geçtiniz!" (Eğitimi bitir).
    - Puan < %80 ise: "Eğitime yönlendiriliyorsunuz..." (Ders slaytlarına git).

### 2. Son Test (Post-Test)
- Eğitimin sonuna 10 soruluk bir sınav koy.
- **Soru Bankası B:** Kolay ve Orta sorular.
- **Randomize:** Her kullanıcıya havuzdan farklı 10 soru gelsin.

### 3. Result Slide Manipülasyonu
- Başarısız olan kullanıcı "Tekrar Dene" dediğinde:
    - Sadece yanlış yaptığı soruları sormak zorunda değilsin (Storyline bunu yapabilir ama biz bunu istemiyoruz).
    - **Tüm sınavı sıfırla (`Reset Results`)** ve Soru Bankasından **YENİ** 10 soru çek. (Kullanıcı ezberleyemesin).

## 🚀 Görev
Question Bank kullanarak bu "Çift Aşamalı" ve "Rastgele" sınav yapısını kur.
