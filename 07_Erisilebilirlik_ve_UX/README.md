# 07. Erişilebilirlik ve UX: "Herkes İçin Tasarım"

> **"Bir eğitimi erişilebilir yapmak 'iyilik' değil, zorunluluktur. Eğer klavye kullanan bir engelli eğitiminizde ilerleyemiyorsa, o eğitim bozuktur."**

Burası "Kurumsal ve Global" ligin başladığı yerdir. Bankalar, devlet kurumları ve global şirketler, **WCAG 2.1 (Web Content Accessibility Guidelines)** standartlarına uymayan hiçbir işi teslim almazlar.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Tab Order (Odak Sırası):** Görme engelliler fare kullanmaz, `Tab` tuşuyla gezer. Sıralama doğru mu?
2.  **Alt Text (Alternatif Metin):** Resimleri ekran okuyucuya (Screen Reader) nasıl betimlersiniz?
3.  **Closed Captions (CC):** Videolara altyazı eklemek ve stilini yönetmek.
4.  **Renk Kontrastı:** Renk körleri butonlarınızı görebiliyor mu?

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Tab Order (Sarı Çerçeve)
Storyline'da `Home > Tab Order` menüsü hayati önem taşır.
- **Kural:** Slayttaki her nesne bu listededir. Ama dekoratif olanlar (arka plan süsü, çizgi vb.) listeden **ÇIKARILMALIDIR**.
- **Nasıl:** Sadece etkileşimli (Buton, Giriş Kutusu) ve bilgi veren (Başlık, Metin) öğeleri bırakın. Çöp kutusuna basarak diğerlerini gizleyin.

### 2. Alt Text (Görünmez Metinler)
Ekran okuyucu (JAWS, NVDA) resim görünce "Image" der geçer.
- **Çözüm:** Resme sağ tıklayın > `Accessibility`.
- **Object is visible to accessibility tools:** İşaretleyin.
- **Alt Text:** "Mutlu bir ofis çalışanı" değil, "Müşteri hizmetleri temsilcisi Ahmet Bey" yazın (Bağlama uygun).
- **Dekoratif ise:** Kutucuğun tikini kaldırın (Artifact).

### 3. Focus Indicator (Odak Rengi)
Klavye ile gezen kullanıcı o an nerede olduğunu bilmelidir.
- **Modern Player Ayarı:** `Player > Colors & Effects > Accessibility Settings`.
- **Focus Color:** Genelde parlak sarı veya turuncu seçilir (Siyah zemin üstünde görünsün diye).

---

## 🚫 UX Günahları (Asla Yapmayın)

| Hata | Neden? | Çözüm |
| :--- | :--- | :--- |
| **"Click Here" (Buraya Tıkla)** | Ekran okuyucu listelerken sadece "Buraya tıkla" diye okur, ne olduğu anlaşılmaz. | "Raporu İndirmek İçin Tıklayın" yazın (Descriptive Link). |
| **Hover Only Bilgi** | Klavye veya Dokunmatik ekranda Hover yoktur. | Hover ile gelen bilgiyi tıklama (Click) veya her zaman görünür yapın. |
| **Süre Sınırı (Timed Quiz)** | Disleksik kullanıcılar yavaş okur, süre bitince stres olur. | Süre sınırını kaldırın veya uzatma opsiyonu koyun. |

---

## 🧪 Laboratuvar Görevi: "Karanlık Test"

1.  **Projeyi Yayımla:** Hazırladığınız herhangi bir modülü Web olarak yayınlayın.
2.  **Fareyi Bırak:** Fareyi masanın altına atın.
3.  **Sadece Klavye:** Sadece `Tab`, `Space` ve `Enter` tuşlarını kullanarak eğitimi bitirmeye çalışın.
4.  **Sonuç:** Eğer butonlara ulaşamıyor veya sırası karışıyorsa (Önce Buton, Sonra Başlık geliyorsa), Tab Order ayarlarını düzeltin.
