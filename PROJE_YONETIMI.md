# 📅 Proje Yönetimi: "Kaosu Yönetme Sanatı"

5 slaytlık projeyi yönetmek kolaydır. 500 slaytlık, 10 modüllük, 3 farklı dildeki banka projesini yönetmek ise sanattır.

---

## 📂 Dosya İsimlendirme ve Versiyonlama

Asla `Proje_Final`, `Proje_Final_Son`, `Proje_Gercekten_Son` diye dosya kaydetmeyin.
Profesyonel isimlendirme şöyledir:
`[MusteriKodu]_[ProjeAdi]_[ModulNo]_v[Versiyon]_[Tarih]`

**Örnek:** `BTK_StorylineLab_M01_v0.4_20240119.story`

- **v0.x:** Taslak, geliştirme aşaması.
- **v1.0:** İlk müşteri onayı (Beta).
- **v1.x:** Revizyonlar.
- **v2.0:** Canlıya çıkış (Gold Master).

---

## 🔄 İnceleme Döngüsü (Review Cycle)

Müşteriden revizyon alırken "Mail" veya "WhatsApp" kullanmayın. Çıldırırsınız.

### Articulate Review 360
Articulate'in kendi bulut aracıdır.
1.  Projeyi `Publish > Review 360` olarak yayınlayın.
2.  Link'i müşteriye atın.
3.  Müşteri tam o saniyeye, ekranın tam o noktasına yorum bırakır ("Bu logo yanlış").
4.  Storyline içinde "Comments" panelini açıp yorumu orada görürsünüz.
5.  Düzelttiğiniz yoruma "Resolved" (Çözüldü) tikini atarsınız.

---

## 🗂️ Yedekleme Stratejisi

Storyline dosyaları büyüktür. Git (GitHub) büyük binary dosyaları (`.story`) sevmez (LFS gerekir).
- **Öneri:** Kaynak kodları (`.story`) OneDrive, Google Drive veya şirket sunucusunda tutun.
- **Version History:** Bulut servislerinin "Sürüm Geçmişi" özelliği hayat kurtarır. Dosya bozulursa dünkü haline dönebilirsiniz.

> **GitHub Ne İçin?** GitHub; buradaki gibi dokümantasyon, JS kodları, CSS dosyaları ve proje yönetim listeleri içindir. `.story` dosyaları için sadece bir "Depo" görevi görür ama version control (Diff) yapamazsınız.
