# 04. Tetikleyiciler ve Değişkenler (Triggers & Variables)

> **"Sihir burada gerçekleşir."**

Storyline'ı bir PowerPoint klonundan, bir yazılım geliştirme ortamına dönüştüren yer burasıdır. Bu modül, programlama mantığının (Logic) görsel arayüzle buluştuğu noktadır.

## 🎯 Hedefler
- 3 temel değişken türünü (Text, Number, Boolean) ustaca kullanmak.
- Koşullu İfadeler (Conditions) ile "Akıllı" senaryolar yazmak.
- Kullanıcıdan veri toplamak (Data Entry).

## 🛠️ Teknik Detaylar

### 1. Değişken Türleri (Kutsal Üçlü)
- **Text (Metin):** İsim, Notlar, Parola saklamak için.
    - *Örnek:* `%UserName%` değişkenini kullanıcının girdiği isme eşitlemek.
- **Number (Sayı):** Skor, Sayaç, İlerleme yüzdesi.
    - *Örnek:* Her doğru cevapta `Score` değişkenini 10 artır (`Add 10 to Score`).
- **Boolean (True/False):** Anahtar/Switch.
    - *Örnek:* `isModuleComplete` değişkeni. Başta `False`'dur. Modül bitince `True` olur.

### 2. Koşullar (Conditions): "Eğer... İse..."
Tetikleyicilerinize IQ katın.
- Trigger: `Jump to slide [Success Slide]`
- When: `User clicks [Submit]`
- **Condition:** `Use if [Score] is greater than or equal to 80`.
*(Eğer puan 80'den büyükse başarı sayfasına git, yoksa hata sayfasına git.)*

### 🧪 Laboratuvar Görevi (Gamification)
1. "İsminiz Nedir?" diye soran bir Data Entry alanı yapın ve bunu bir değişkende saklayın.
2. Sonraki slaytta "Merhaba [İsim], hoş geldin!" yazdırın.
3. Basit bir sayaç yapın: Bir butona her basıldığında ekrandaki sayıyı 1 artıran mekanizmayı kurun.
