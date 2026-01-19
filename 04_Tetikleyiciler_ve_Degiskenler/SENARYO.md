# 🎬 Proje Senaryosu: Gamification (Oyunlaştırma)

## 🏢 Bağlam
Satış ekibi için "Müşteri İkna Teknikleri" eğitimi yapılacak. Ancak ekip rekabetçi. Eğitimi bir "RPG Oyunu" gibi kurgulamanız isteniyor. Puan toplayacaklar, can hakları olacak ve isimleriyle hitap edilecek.

## 📝 Gereksinimler (Spec Sheet)

### 1. Değişken Kurulumu (Variables)
- `%AgentName%` (Text): Oyuncunun adı.
- `%SalesPoints%` (Number): Puan (Başlangıç 0).
- `%MoodMeter%` (Number): Müşterinin memnuniyeti (Başlangıç 50/100).
- `%isDealClosed%` (Boolean): Satış kapandı mı? (False).

### 2. Giriş Ekranı
- "Ajan Adı"nı soran bir input alanı.
- Sonraki slaytta: "Hoşgeldin Ajan %AgentName%. Görevin zorlu."

### 3. Satış Senaryosu (Logic Loop)
- Müşteri bir itirazda bulunur ("Çok pahalı!").
- **Seçenek A:** "Kalite pahalıdır." -> Trigger: `Subtract 10 from MoodMeter`.
- **Seçenek B:** "Size özel indirim yapabiliriz." -> Trigger: `Add 20 to MoodMeter`.
- **Koşul (Condition):**
    - Her seçenekten sonra kontrol et:
    - *EĞER* `%MoodMeter%` >= 100 ise -> `isDealClosed = True` -> "Satış Başarılı" katmanını göster.
    - *EĞER* `%MoodMeter%` <= 0 ise -> "Müşteri Kaçtı" katmanını göster (Game Over).

## 🚀 Görev
Bu değişkenleri ve mantık zincirini kur. Ekranda puanın canlı olarak değiştiğini (Variable Reference) göster.
