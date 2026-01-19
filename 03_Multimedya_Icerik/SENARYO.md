# 🎬 Proje Senaryosu: İnteraktif İş Güvenliği Videosu

## 🏢 Bağlam
Fabrika çalışanları için "Yangın Güvenliği" eğitimi hazırlanıyor. Elde 3 dakikalık bir video var ama kimse izlemiyor. İK departmanı, "Video sırasında durup soru sorsun, cevap vermezse ilerlemesin" diyor.

## 📝 Gereksinimler (Spec Sheet)

### 1. Video Entegrasyonu
- Videoyu slayta göm.
- Videonun kendi kontrollerini (Play bar) **KAPAT**. (Kullanıcı ileri saramasın).
- Kendi "Play/Pause" butonunu yap ve trigger ile videoyu kontrol et.

### 2. Kritik Müdahale (Cue Points)
- **Saniye 00:45:** Yangın alarmı çalıyor. Videoyu otomatik durdur (`Pause Media`).
- Ekrana bir soru (Katman) getir: "Şu an ne yapmalısın? A) Kaç B) Sakin ol".
- Doğru cevap verilirse katmanı kapat ve videoyu kaldığı yerden devam ettir (`Play Media`).

### 3. Web Object Bonusu
- Eğitimin sonunda "Hata Raporu Formu"nu göstermen gerekiyor.
- Şirketin intranetindeki formu (veya Google Forms) slaytın içine `Web Object` olarak göm.

## 🚀 Görev
Pasif bir MP4 videosunu, "Durdur-Soru Sor-Devam Et" kurgusuyla interaktif bir deneyime dönüştür.
