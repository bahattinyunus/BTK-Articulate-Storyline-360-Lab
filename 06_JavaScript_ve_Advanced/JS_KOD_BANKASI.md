# 🏦 JavaScript Kod Bankası (Copy/Paste Ready)

> **"Tekerleği yeniden icat etmeyin. Buradaki kodları kopyalayın, değişken isimlerini değiştirin ve kullanın."**

Bu dosya, sahada en çok ihtiyaç duyulan ve hayat kurtaran JavaScript kod parçacıklarını içerir.

---

## 📅 Tarih ve Zaman İşlemleri

### 1. Basit Tarih (GG/AA/YYYY)
Storyline'da bir `%SystemDate%` değişkeni oluşturun ve bu kodu tetikleyin.
```javascript
var date = new Date();
var day = String(date.getDate()).padStart(2, '0');
var month = String(date.getMonth() + 1).padStart(2, '0');
var year = date.getFullYear();
var player = GetPlayer();
player.SetVar("SystemDate", day + "/" + month + "/" + year);
```

### 2. Canlı Saat (HH:MM)
Ekranda saatin ilerlemesini istiyorsanız. (Not: Bu kodu her saniye tetiklemek performans yer, sadece açılışta kullanmak daha iyidir).
```javascript
var d = new Date();
var hours = String(d.getHours()).padStart(2, '0');
var minutes = String(d.getMinutes()).padStart(2, '0');
var player = GetPlayer();
player.SetVar("SystemTime", hours + ":" + minutes);
```

---

## 🖨️ Çıktı ve Paylaşım

### 3. Sadece Sertifikayı Yazdır (CSS Hack)
Kullanıcı "Yazdır" dediğinde butonların çıkmasını istemiyorsanız.
```javascript
var printStyle = document.createElement('style');
printStyle.innerHTML = '@media print { .story-player-frame { display: none !important; } #slide-window { position: absolute; top: 0; left: 0; width: 100%; height: 100%; } }';
document.head.appendChild(printStyle);
window.print();
```
*(Not: Bu kod modern oynatıcıda (Modern Player) farklılık gösterebilir, test edin.)*

### 4. Panoya Kopyala (Copy to Clipboard)
Kullanıcıya özel bir kod verdiniz ve tek tıkla kopyalamasını istiyorsunuz.
```javascript
var player = GetPlayer();
var textToCopy = player.GetVar("ReferansKodu");
navigator.clipboard.writeText(textToCopy).then(function() {
  alert("Kod kopyalandı: " + textToCopy);
}, function(err) {
  alert("Kopyalanamadı: " + err);
});
```

---

## 💾 Veri Saklama (Local Storage)

### 5. İsmi Hatırla (Save)
```javascript
var player = GetPlayer();
var name = player.GetVar("UserName");
localStorage.setItem("user_name_cached", name);
```

### 6. İsmi Geri Getir (Load)
```javascript
var savedName = localStorage.getItem("user_name_cached");
if(savedName) {
    var player = GetPlayer();
    player.SetVar("UserName", savedName);
}
```

---

## 🔊 Metin Okuma (Text-to-Speech - Browser API)

### 7. Basit Konuşma
Storyline'ın kendi TTS'i var ama tarayıcınınkini (Google Voice) kullanmak isterseniz:
```javascript
var player = GetPlayer();
var text = player.GetVar("OkunacakMetin");
var msg = new SpeechSynthesisUtterance(text);
msg.lang = 'tr-TR'; // Türkçe
window.speechSynthesis.speak(msg);
```
