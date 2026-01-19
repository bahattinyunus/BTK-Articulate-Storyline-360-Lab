# 🎬 Proje Senaryosu: "Erişilebilirlik Denetimi (The Audit)"

## 🏢 Bağlam
Müşteri: Global bir banka.
Durum: "Eğitimimizi hazırlayan arkadaş işten ayrıldı. Görme engelli bir çalışanımız 'Eğitimi tamamlayamıyorum, butonlar okunmuyor' diye şikayet etti. Lütfen düzeltin."

## 📝 Gereksinimler (Spec Sheet)

### 1. Tab Order Temizliği
- Slaytta 50 tane nesne var (Logolar, çizgiler, arka plan resimleri).
- **Görev:** Tab Order menüsüne gir. Sadece "Başlık", "Metin" ve "İleri Butonu" kalacak şekilde diğer 47 nesneyi gizle.

### 2. Alt Text Yazımı
- Slaytta bir Grafik (Chart) var. Üzerinde "Satışlar %20 arttı" yazıyor ama resim (PNG) formatında.
- **Görev:** Ekran okuyucunun bu resmi "Ocak ayı satış grafiği, satışların %20 arttığını gösteriyor" şeklinde okumasını sağla.

### 3. Closed Captions (CC)
- Bir CEO konuşma videosu var.
- **Görev:** Videoya Storyline'ın CC editörünü kullanarak senkronize altyazı ekle. Altyazı fontunu okunabilir (Arial, 24px, Sarı) yap.

### 4. Renk Kontrastı
- "Gönder" butonu açık gri zemin üzerine beyaz yazı ile yapılmış. Kimse okuyamıyor.
- **Görev:** WCAG 2.1 AA standardına göre (Contrast Ratio 4.5:1) rengi koyulaştır. (WebAIM Contrast Checker aracını kullan).

## 🚀 Beklenen Çıktı
NVDA veya JAWS (ücretsiz ekran okuyucular) veya Windows Narrator açıkken proje %100 sorunsuz çalışmalı.
