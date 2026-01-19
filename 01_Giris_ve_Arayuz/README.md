# 01. Giriş ve Arayüz: "Kokpiti Tanımak"

> **"Bir pilot, hangi düğmeye basacağını düşünmez; sadece basar. Çünkü kokpit onun uzvudur. Storyline arayüzü de sizin elinizin bir uzantısı olmalıdır."**

Bu modül, Articulate Storyline 360'ın arayüzüne (UI) ve projenin başlangıç ayarlarına odaklanır. Çoğu geliştirici "Hadi slayt yapalım" diyerek balıklama dalar, ancak projenin temelleri (Resolution, Player, Scene Structure) burada atılır. Temel çürükse, bina yıkılır.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Story View vs Slide View:** Büyük resim ile detay arasındaki geçişi yönetmek.
2.  **Scene (Sahne) Mimarisi:** Projeyi yönetilebilir parçalara bölmek.
3.  **Story Size (Tuval Ayarları):** Piksellerle dans etmek ve responsive tasarımın sınırları.
4.  **Player (Oynatıcı) Özelleştirme:** Storyline'ın standart çerçevesinden kurtulup "Invisible Interface" yaratmak.

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Story View: "Projenin Google Maps'i"
Storyline'ı açtığınızda karşınıza çıkan kuş bakışı görünümdür. Burası sadece slaytları listelemez; **ilişkileri (relationships)** gösterir.
- **Dallanma (Branching) Kontrolü:** Sahneler arasındaki oklar, kullanıcının nereye gidebileceğini gösterir. Eğer bir ok "çıkmaz sokağa" (bağlantısız slayt) gidiyorsa, burada bir kopukluk vardır.
- **Starting Scene:** Bayrak (Flag) ikonu projenin nereden başlayacağını belirler. Modüler çalışırken, test etmek istediğiniz sahneye bayrağı taşıyarak sadece o kısmı preview yapabilirsiniz.

### 2. Slide View: "Atölye"
Burası pikselleri itip kaktığımız, triggerları yazdığımız yerdir.
- **Paneller:** Triggers (Sağ), Slide Layer (Sağ Alt), Timeline (Alt), States (Alt). Bu panellerin yerini ezbere bilmek hız kazandırır.
- **Kısayol:** `F12`'ye basarak hızlıca "Preview This Slide" yapabilir, yaptığınız değişikliği saniyeler içinde test edebilirsiniz.

### 3. Story Size (Kritik Karar Anı)
`Design > Slide Size` menüsünden ulaşılır. Bu ayar, projenin **çözünürlüğünü** ve **en-boy oranını** belirler.
- **Junior Hatası:** Projeyi bitirdikten sonra boyutu değiştirmek. Bu, tüm tasarımların sünmesine, resimlerin bozulmasına (pixelation) yol açar.
- **Önerilen Ayar:** **16:9** oranında, özel boyut olarak **1280x720 (HD)** veya **1920x1080 (Full HD)**.
- **Neden 16:9?** Çünkü dünyadaki tüm laptop ve monitörler 16:9'dur. 4:3 (kare ekran) kullanan kimse kalmadı.

### 4. Player (Oynatıcı) Stratejisi
Storyline varsayılan olarak projenizin etrafına gri bir çerçeve (Player) koyar. İçinde "Menu", "Resources", "Volume" butonları vardır.
- **Modern Tasarım:** Artık trend, "Chromeless" (Çerçevesiz) tasarımdır. İçerik öne çıkmalı, araç çubuğu değil.
- **Nasıl Yapılır?** `Home > Player` menüsüne gidin. "Menus & Controls" sekmesinden hepsini **KAPATIN**. Kendi "İleri/Geri" butonlarınızı slayt içine tasarlayın. Bu size tam görsel kontrol sağlar.

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **İsimsiz Sahneler** | "Untitled Scene 1, 2, 3..." | Sahneleri "Giriş", "Modül 1", "Sınav" olarak adlandırın. |
| **Yanlış Çözünürlük** | Bulanık metinler ve görseller. | Proje başında Story Size'ı kilitleyin (Lock). |
| **Default Player** | Hantal, "Eğitim gibi görünen" eğitimler. | Player çerçevesini temizleyin (Invisible Player). |

---

## 🧪 Laboratuvar Görevi: "Temiz Başlangıç"

1.  Yeni bir Storyline projesi açın.
2.  **Story Size** ayarını `1280x720` piksel yapın.
3.  **Scene** yapısını kurun:
    - Sahne 1: "00_Intro" (Giriş)
    - Sahne 2: "01_Konu_Anlatimi" (Ders)
    - Sahne 3: "02_Final_Sinav" (Test)
4.  **Player** ayarlarını açın:
    - Menü, Glossary, Resources tiklerini kaldırın.
    - Colors & Effects'ten arka planı şeffaf (veya web sitenize uygun renk) yapın.
5.  Dosyayı `Lab_01_Setup.story` olarak kaydedin.
