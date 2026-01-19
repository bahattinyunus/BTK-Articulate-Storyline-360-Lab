# 05. Quiz ve Sınavlar (Quizzes & Assessments)

> **"Ölçülmeyen şey geliştirilemez."**

Eğitimin ne kadar etkili olduğunu anlamanın yolu ölçme ve değerlendirmeden geçer. Bu modül, Storyline'ın güçlü sınav motorunu ele alır.

## 🎯 Hedefler
- Graded (Puanlı) ve Survey (Anket) soruları arasındaki farkı anlamak.
- **Question Banks (Soru Bankaları)** ile dinamik sınavlar oluşturmak.
- **Result Slide (Sonuç Ekranı)** değişkenlerini yönetmek ve LMS'e (Learning Management System) veri göndermek.

## 🛠️ Teknik Detaylar

### 1. Soru Tipleri
- **Hotspot:** Resim üzerinde "Hatalı kabloyu bulun" gibi görsel sorular için harikadır.
- **Drag and Drop:** Eşleştirme soruları için kullanılır. En interaktif soru tipidir.
- **Pick One:** Kendi özel butonlarınızla soru yapmak istiyorsanız "Freeform" Pick One kullanın.

### 2. Question Banks (Soru Bankaları)
Her kullanıcıya aynı sırayla aynı soruları sormak kopya çekmeyi kolaylaştırır.
- Soruları bir havuza atın.
- "Draw questions randomly": Havuzdan rastgele 10 soru seç ve karışık sırayla sor.

### 3. Result Slide ve LMS
Sınav bittiğinde Storyline otomatik olarak özel değişkenler üretir:
- `%Results.ScorePoints%` (Alınan Puan)
- `%Results.PassPercent%` (Geçme Notu)
LMS (SCORM), eğitimin bittiğini ve başarısını bu sayfadaki tetikleyiciler sayesinde anlar.

### 🧪 Laboratuvar Görevi
1. 5 soruluk bir Soru Bankası oluşturun.
2. Yeni bir sahnede bu bankadan rastgele 3 soru çektirin.
3. Sonunda bir "Result Slide" ekleyin.
4. Başarısız olanlar için "Sınavı Tekrarla" (Retry Quiz) butonu ekleyin.
