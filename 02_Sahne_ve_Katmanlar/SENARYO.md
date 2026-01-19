# 🎬 Proje Senaryosu: Yazılım Simülasyonu (Single Slide App)

## 🏢 Bağlam
Bir banka, gişe memurları için yeni ATM yazılımını tanıtan bir eğitim istiyor. Ancak kullanıcının sayfalarca "İleri" butonuna basıp ekran görüntüleri izlemesini istemiyorlar. "Kullanıcı gerçekten o ekranı kullanıyormuş gibi hissetsin" diyorlar.

## 📝 Gereksinimler (Spec Sheet)

### 1. Slide Master Tasarımı
- Sol tarafta sabit bir **Navigasyon Paneli** (Login, İşlem Seç, Para Yatır, Çıkış).
- Sağ tarafta **İçerik Alanı** (Ekranın değiştiği yer).
- Bu yapıyı `Slide Master`'da kur. Slayt üzerinde sadece içerik değişsin, menü sabit kalsın.

### 2. Katman (Layer) Mimarisi
Bunu **TEK BİR SLAYTDA** (One Slide Project) yapacaksın.
- **Base Layer:** Banka arkaplanı.
- **Layer_Login:** Kullanıcı adı şifre ekranı.
- **Layer_Menu:** İşlem butonları.
- **Layer_Deposit:** Para yatırma ekranı.
- **Layer_Error:** Yanlış tuşa basarsa çıkan uyarı.

### 3. Etkileşim Kuralları
- **Modal Dialog:** `Layer_Error` açıldığında, kullanıcı arkadaki ATM ekranına dokunamamalı (Prevent user from clicking on base layer).
- **Cross-Layer:** "Para Yatır" katmanındayken "Menü" tuşuna basarsa, "Para Yatır" katmanı kapanmalı, "Menü" katmanı açılmalı (Hide other slide layers).

## 🚀 Görev
Bu "Tek Sayfalık Uygulama"yı (Single Page Application - SPA) katman mantığıyla inşa et.
