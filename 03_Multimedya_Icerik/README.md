# 03. Multimedya İçerik: "Hissedilen Deneyimler"

> **"Göz görür, kulak duyar, zihin birleştirir. E-öğrenme sadece okumak değildir; çok duyulu (multi-sensory) bir yolculuktur."**

Storyline'ı güçlü kılan özelliklerden biri, video, ses ve web teknolojilerini sorunsuz bir şekilde harmanlayabilmesidir. Bu modül, statik bir slaytı yaşayan, konuşan ve hareket eden bir deneyime dönüştürmenin yollarını anlatır.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Media Triggers:** Video bittiğinde ne olacağını kodlamak.
2.  **Cue Points (Senkronizasyon):** Sesi ve yazıyı aynı anda dans ettirmek.
3.  **Web Objects:** Storyline'ın sınırlarını aşmak (Web sitelerini içeri gömmek).
4.  **Accessibility (Erişilebilirlik):** Alt Text ve Closed Captions (Altyazı) önemi.

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Video Kontrolü ve Tetikleyiciler
Kullanıcının videoyu sonuna kadar izlemesini (Compliance Training) istiyorsanız, "İleri" butonunu başlangıçta pasif yapmalısınız.
- **Adım 1:** İleri butonunun durumunu (State) `Disabled` veya `Hidden` yapın.
- **Adım 2:** Trigger yazın: `Change state of Next Button to Normal` (Normal hale getir).
- **Adım 3:** When: `Media Completes` (Medya tamamlandığında).
- **Adım 4:** Object: `Video 1`.
*Pro Tip:* Videonun üzerine şeffaf bir şekil (Hotspot) koyarak kullanıcının videoyu durdurmasını/tıklamasını engelleyebilirsiniz.

### 2. Cue Points (Zaman İşaretçileri)
Timeline üzerinde belirli saniyelere "bayrak dikmek" gibidir.
- **Nasıl Eklenir?** Timeline oynarken klavyedeki `C` tuşuna her bastığınızda bir Cue Point (1, 2, 3...) eklenir.
- **Kullanımı:** Metin kutularının giriş animasyonlarını bu noktalara bağlayabilirsiniz. Trigger: `Show [TextBox 1] when Timeline reaches [Cue Point 1]`.
- Bu teknik, sesi dinleyere manuel senkronizasyon yapmaktan 10 kat daha hızlıdır.

### 3. Web Objects: "Pencere İçinde Pencere"
Eğitimin içinden çıkmadan şirketin İK politikasını (PDF) veya canlı bir web sitesini göstermek mümkündür.
- `Insert > Web Object` diyerek URL yapıştırın.
- **Dikkat:** Web objeleri her zaman en üst katmandadır (Always on top). Üzerine bir şekil veya buton koyamazsınız. Web objesini kapatmak için farklı bir slayta veya katmana geçmeniz gerekir.

### 4. Accessibility (Erişilebilirlik)
Modern eğitimin olmazsa olmazı.
- **Closed Captions:** Storyline'ın kendi altyazı editörü vardır. Videonun/sesin üzerine gelip `Options > Add Captions` diyerek altyazı ekleyebilirsiniz.
- **Focus Order:** Tab tuşuyla gezen engelli kullanıcılar için nesnelerin okunma sırasını ayarlayın (`Home > Focus Order`).

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **Ağır Videolar** | Eğitimin geç yüklenmesi. | Videoları Handbrake gibi bir araçla sıkıştırıp yükleyin. |
| **Senkron Kayması** | Ses ile yazının tutmaması. | Timeline'da sürelerle oynamak yerine Cue Points kullanın. |
| **Otomatik Video (Autoplay)** | Tarayıcıların videoyu engellemesi. | Modern tarayıcılar (Chrome) sessiz olmayan videoların otomatik başlamasını engeller. Videoya bir "Play" butonu koyun. |

---

## 🧪 Laboratuvar Görevi: "Video Tabanlı Senaryo"

1.  Slayta bir adet MP4 video ekleyin (bir toplantı sahnesi olabilir).
2.  Video oynarken `C` tuşuyla 3 kritik noktaya (toplantı başı, kavga anı, çözüm anı) Cue Point koyun.
3.  Bu Cue Point'lerde ekrana "Dikkat!" diyen bir uyarı ikonu çıkartın (Trigger ile).
4.  Video bittiğinde "Sonraki Adım" butonunu görünür yapın (`Hidden` to `Normal`).
