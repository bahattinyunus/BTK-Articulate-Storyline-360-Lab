# 05. Quiz ve Sınavlar: "Ölçme Mühendisliği"

> **"Eğer ölçemiyorsanız, öğretememişsinizdir. Sınavlar sadece not vermek için değil, öğrenme eksiklerini (Gap Analysis) göstermek içindir."**

Storyline'ın en sağlam motorlarından biri de Quiz motorudur. Bu modül, basit çoktan seçmeli sorulardan, karmaşık Soru Bankası (Question Bank) yapılarına ve SCORM paketleri ile LMS (Learning Management System) entegrasyonuna kadar uzanır.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Graded vs Survey:** Puanlı sınav ile anket arasındaki fark.
2.  **Question Banks:** Soruları havuzdan rastgele çekmek (Kopya engelleme).
3.  **Result Slides:** Sonuç ekranını manipüle etmek ve LMS'e veri göndermek.
4.  **Freeform Questions:** Herhangi bir slaytı (resmi, şekli) soruya dönüştürmek.

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Freeform Questions (Özgür Sorular)
Storyline'ın hazır şablonlarına (A, B, C şıkları) mahkum değilsiniz.
- `Insert > Convert to Freeform` diyerek herhangi bir slaytı soruya çevirebilirsiniz.
- **Pick One:** Ekranda 5 resim var, "Hangisi iş güvenliğine aykırı?" diye sorabilirsiniz. Kullanıcı resme tıklar, Storyline bunu cevap olarak algılar.
- **Drag and Drop:** Eşleştirme soruları için en iyi yöntemdir.

### 2. Question Banks (Soru Bankaları)
50 soruluk bir havuz hazırlayıp, her öğrenciye bu havuzdan rastgele 10 soru sormak... İşte profesyonellik budur.
- `Slides > Question Banks` menüsünden havuzlar oluşturun.
- Sınav sahnesinde `New Slide > Draw from Bank` diyerek "Bu havuza git, rastgele 10 soru çek ve buraya getir" diyebilirsiniz.
- Her seferinde soruların sırası ve şıkların yeri değişir.

### 3. Result Slide ve LMS İletişimi
Sınav bittiğinde bir "Result Slide" eklenmelidir. Bu slaytın gizli bir görevi vardır: **LMS ile konuşmak.**
- Result slide eklendiği anda Storyline şu sistem değişkenlerini oluşturur:
    - `%Results.ScorePoints%` (Puan)
    - `%Results.PassPercent%` (Geçme Notu)
- Sınavı tekrarla (Retry Button) eklediğinizde, `Reset Results` triggerını unutmayın. Yoksa sistem eski puanı hatırlar ve yeni denemeyi kabul etmez.

### 4. Review Quiz (Cevapları İncele)
Result slaytına "Cevapları Gör" butonu koyabilirsiniz. Ancak dikkat:
- Review modunda kullanıcı cevapları değiştirememelidir. Storyline bunu otomatik kilitler ama tasarımı (Review Layer) düzenlemeniz gerekebilir.

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **Reset Unutmak** | "Tekrar Dene" butonu çalışmaz. | Retry butonuna mutlaka "Reset Results [Quiz Name]" triggerı ekleyin. |
| **Limitsiz Hak** | Kullanıcı 100 kere dener. | Değişken ile deneme sayısını (Attempt Count) tutun ve 3 haktan sonra butonu kilitleyin. |
| **Yanlış Result** | Farklı sahnelerin puanları karışır. | Result slide eklerken "Hangi soruları hesaplayayım?" listesinde sadece ilgili soruları seçin. |

---

## 🧪 Laboratuvar Görevi: "Rastgele Sınav Simülasyonu"

1.  **Soru Bankası:** 3 farklı kategoride (Kolay, Orta, Zor) soru bankası oluşturun.
2.  **Draw Slide:** Sınav sahnesine git ve her kategoriden 1'er soru çektir (Toplam 3 soru).
3.  **Freeform:** Bir soruyu standart test değil, "Pick One" (Görsel Seçmece) olarak tasarlayın.
4.  **Result Slide:** Sonuç ekranına "Puanınız: %Results.ScorePercent%%" yazdırın.
5.  **Logic:** Eğer puan 50'nin altındaysa "Eğitimi Tekrar Al" butonu çıksın (Link to Scene 1); üstündeyse "Çıkış" butonu (Exit Course) aktif olsun.
