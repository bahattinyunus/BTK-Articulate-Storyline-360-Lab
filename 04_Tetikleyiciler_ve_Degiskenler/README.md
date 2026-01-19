# 04. Tetikleyiciler ve Değişkenler: "Storyline'ın Beyni"

> **"Tetikleyiciler 'kas', değişkenler 'beyin'dir. Kası olmayan beyin hareket edemez, beyni olmayan kas ise sadece sallar."**

Bu modül, Storyline'ı statik bir slayt gösterisinden, gerçek bir **yazılıma** dönüştüren kısımdır. Burası, IF (Eğer), THEN (O zaman), ELSE (Değilse) mantığının görsel olarak kurulduğu yerdir. Bir eğitim tasarımcısı ile bir "Storyline Developer" arasındaki fark burada ortaya çıkar.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Variable Types:** Text, Number ve Boolean değişkenlerin simyası.
2.  **Logic & Conditions:** "Akıllı" senaryolar kurmak.
3.  **Data Loop:** Kullanıcıdan bilgi almak, işlemek ve geri sunmak.
4.  **Reference:** Değişkenleri ekrana yazdırmak (`%DegiskenAdi%`).

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Değişken Türleri (Kutsal Üçlü)
Storyline'da sadece 3 tip değişken vardır ama bunlarla dünyayı yönetebilirsiniz.
- **Text (Metin):** İsimler, notlar, açık uçlu cevaplar.
    - *Kullanım:* Sertifikaya isim basmak.
- **Number (Sayı):** Skor, sayaç, sayfa numarası, hak sayısı.
    - *Kullanım:* "Kalan Hakkınız: 2" gibi geri sayımlar yapmak.
- **Boolean (True/False):** En kritik tiptir. Bir şeyin yapılıp yapılmadığını takip eder.
    - *Kullanım:* `isModule1Complete = False`. Modül bitince `True` yap. Menüde Modül 2'nin kilidini bu değişkene bakarak aç.

### 2. Koşullar (Conditions): Algoritma Kurmak
Bir tetikleyiciye (Trigger) "Şart" koşmaktır.
- **Senaryo:** Kullanıcı "Bitir" butonuna bastı.
- **Trigger:** Başarı sayfasına git.
- **Condition:** *EĞER* `Score` değişkeni 70'ten büyükse.
- **Else (Değilse):** Aynı butonun altına ikinci bir trigger ekleyerek (`Score` < 70) başarısız sayfasına yönlendirin.
*Dikkat:* Trigger sırası (Order) hayati önem taşır. Storyline triggerları yukarıdan aşağıya işler. Jump (Git) triggerı en sonda olmalıdır, çünkü gidince diğer triggerlar çalışmaz.

### 3. Değişken Referansı (References)
Bir değişkenin içindeki değeri ekranda göstermek için `%` işaretleri arasına adını yazın.
- Metin kutusuna: `Tebrikler %UserName%, toplam puanınız: %UserScore%.`
- Storyline bunu yayınlandığında (Publish) otomatik olarak "Tebrikler Ahmet, toplam puanınız: 90." şekline çevirir.

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **Sonsuz Değişken** | Her slayt için yeni değişken yaratmak. | Değişkenleri global düşünün. `Score` tek bir tanedir, her slayt için `Score1`, `Score2` yapmayın. |
| **Trigger Sıralaması** | Hesaplama yapmadan sayfadan gitmek. | "Jump to slide" triggerını her zaman listenin EN ALTINA koyun. Önce hesapla, sonra git. |
| **Case Sensitive** | Referansların çalışmaması. | Değişken adı `Puan` ise `%puan%` çalışmaz. `%Puan%` yazmalısınız. |

---

## 🧪 Laboratuvar Görevi: "Gamified Kilit Sistemi"

1.  **Değişkenler:** `isLevel1Complete` (False), `isLevel2Complete` (False), `PlayerName` (Text) oluşturun.
2.  **Giriş Ekranı:** Kullanıcı adını girsin ve `PlayerName` değişkenine kaydolsun.
3.  **Menü Ekranı:**
    - Level 1 butonu açık.
    - Level 2 butonu kilitli (State: Disabled).
4.  **Level 1 Sonu:** Bir butonla `isLevel1Complete` değişkenini `True` yapın.
5.  **Menüye Dönüş:** Menü slaytına bir trigger ekleyin:
    - *Action:* Change state of Level 2 Button to Normal.
    - *When:* Timeline starts (Sayfa açıldığında).
    - *Condition:* If `isLevel1Complete` is equal to `True`.
6.  Böylece Level 1 bitmeden Level 2 açılamaz.
