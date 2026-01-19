# ✅ Kontrol Listesi: Tetikleyiciler ve Değişkenler

Mantık hataları en zor bulunan hatalardır. Dikkatli olun.

## ⚡ Trigger (Tetikleyici) Sıralaması
- [ ] **Jump En Sonda:** "Jump to slide" komutu listenin EN SONUNDA mı? (Önce hesapla, sonra git).
- [ ] **Çakışma:** Aynı butona tanımlı çakışan iki trigger var mı?
- [ ] **Sahipsiz Trigger:** Kırmızı ile işaretlenmiş "Unassigned" trigger var mı? (Silin bunları).

## 🧮 Değişkenler (Variables)
- [ ] **Default Value:** Değişkenlerin başlangıç değerleri doğru mu? (Puan 0 mı, 100 mü?).
- [ ] **İsimlendirme:** `Var1`, `Var2` gibi anlamsız isimler var mı? (Varsa hemen düzeltin: `isMenuOpen`, `UserScore`).
- [ ] **Reference:** Ekranda `%Degisken%` yazdırıyorsanız, fontun Türkçe karakterleri desteklediğinden emin misiniz?

## 🧠 Logic Testi
- [ ] **Edge Cases:** Puan tam 0 veya tam 100 olursa ne oluyor? (Sınırları test edin).
- [ ] **Tekrar:** Kullanıcı bu sayfaya ikinci kez gelirse değişkenler sıfırlanıyor mu, yoksa eski değerde mi kalıyor?

> **Pilot Notu:** Bilgisayarlar aptaldır, ne derseniz onu yaparlar. Ne "demek istediğinizi" anlamazlar.
