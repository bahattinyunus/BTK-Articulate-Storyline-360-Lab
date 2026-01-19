# 03. Multimedya İçerik (Multimedia Content)

> **"İçerik kraldır, ama sunum vezirdir."**

Bu modül, metin tabanlı sıkıcı eğitimlerden kurtulup; ses, video, web objeleri ve karakterlerle zenginleştirilmiş deneyimler tasarlamayı öğretir.

## 🎯 Hedefler
- Video ve Ses dosyalarını yönetmek ve tetikleyicilerle bağlamak.
- Timeline (Zaman Çizelgesi) senkronizasyonu.
- Web Objects ile dış dünyayı içeri almak.
- Erişilebilirlik (Accessibility) ve Alt Text kullanımı.

## 🛠️ Teknik Detaylar

### 1. Medya Tetikleyicileri (Media Triggers)
Video bittiğinde ne olacak? Storyline bunu otomatik yapmaz.
- **Trigger:** `Change state of Next Button to Normal` (İleri butonunu aktif et)
- **When:** `Media Completes` (Medya tamamlandığında)
- **Object:** `Video 1`
*Bu desen, kullanıcının videoyu izlemeden geçmesini engellemek için standarttır.*

### 2. Timeline Senkronizasyonu (Cue Points)
Ses dosyasıyla ekrandaki metinleri eşleştirmek için **Cue Points** (İşaret Noktaları) kullanın.
- Timeline'da `C` tuşuna basarak işaret koyun.
- Trigger: `Show [Image 1] when timeline reaches Cue Point 1`.

### 3. Web Objects
Storyline içine canlı web sitesi, PDF veya HTML5 animasyon gömmek için kullanılır.
- *Dikkat:* Web objeleri "Preview" modunda bazen çalışmaz. Tam testi "Publish" ettikten sonra yapın.

### 🧪 Laboratuvar Görevi
1. Slayta bir mp4 video ekleyin.
2. Videonun altına özel bir "Play/Pause" butonu yapın ve trigger ile videoyu kontrol edin.
3. Videonun üzerine, belirli saniyelerde (Cue Points) beliren bilgi balonucukları ekleyin.
