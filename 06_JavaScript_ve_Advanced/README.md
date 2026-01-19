# 06. JavaScript ve Advanced: "Karanlık Sanatlar"

> **"Storyline'ın bittiği yerde JavaScript başlar. Arayüzün size sunduğu sınırlara hapsolmayın."**

Tebrikler, buraya kadar geldiyseniz artık standart bir "Eğitim Tasarımcısı" değil, bir "E-Öğrenme Geliştiricisi" (E-Learning Developer) olma yolundasınız. Bu modül, Storyline'ın kaputunu açıp motora müdahale ettiğimiz yerdir.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Execute JavaScript:** Storyline içinden tarayıcıya komut göndermek.
2.  **Get/Set Variables:** Storyline değişkenlerini JS ile okumak ve değiştirmek.
3.  **Local Storage:** Tarayıcı önbelleğini kullanarak veri saklamak.
4.  **Print Certificate:** Tek tıkla ekrandaki sertifikayı yazdırmak.

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Storyline ve JS Köprüsü
Storyline ile JavaScript konuşurken `GetPlayer()` fonksiyonu kullanılır.
```javascript
var player = GetPlayer();
var myName = player.GetVar("UserName"); // Storyline'dan isim al
alert("Merhaba " + myName); // Tarayıcıda uyarı göster
player.SetVar("Score", 100); // Storyline'daki puanı 100 yap
```

### 2. Sertifika Yazdırma (Print Window)
Kullanıcılar "Sertifikayı İndir" butonuna bastığında aslında olan şey şudur: Tarayıcının yazdırma penceresini açarız.
- **Trigger:** Execute JavaScript
- **Code:** `window.print();`
*Pro Tip:* CSS `@media print` kullanarak sadece sertifikayı yazdırıp, butonları gizleyebilirsiniz (ama bu ileri seviye web bilgisi gerektirir).

### 3. Tarih ve Saat Çekme
Storyline'da "Bugünün Tarihi" diye bir özellik yoktur. JS ile yaparız.
```javascript
var date = new Date();
var day = date.getDate();
var month = date.getMonth() + 1;
var year = date.getFullYear();
var fullDate = day + "/" + month + "/" + year;
var player = GetPlayer();
player.SetVar("SystemDate", fullDate);
```
Bu kodu "Timeline Starts" triggerına eklerseniz, `%SystemDate%` değişkeni bugünün tarihini gösterir.

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **Preview Modu** | Kod çalışmaz. | JavaScript Storyline'ın **Preview** modunda ASLA çalışmaz. Mutlaka **Publish** edip (Web veya LMS) denemeniz gerekir. |
| **Syntax Hatası** | Hiçbir şey olmaz. | Bir noktalı virgül (;) eksikse tüm kod durur. Kodu önce bir JS editöründe deneyin. |
| **Değişken Adları** | Veri gelmez. | JS içindeki değişken adı (`UserName`) ile Storyline'daki (`username`) birebir aynı olmalıdır (Büyük/Küçük harf duyarlı). |

---

## 🧪 Laboratuvar Görevi: "Dinamik Sertifika Motoru"

1.  **Sertifika Tasarımı:** Bir slayta süslü bir sertifika yapın.
2.  **Değişkenler:** `%AdSoyad%`, `%Tarih%`, `%Puan%` değişkenlerini sertifika üzerine yerleştirin.
3.  **JS Entegrasyonu:**
    - Bir JS kodu yazarak bugünün tarihini alıp `%Tarih%` değişkenine atayın.
4.  **Yazdır Butonu:** Bir butona `window.print();` komutunu atayın.
5.  **Test:** Projeyi Publish edin (Web olarak) ve çalışıp çalışmadığını tarayıcıda görün.
