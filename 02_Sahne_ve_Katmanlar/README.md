# 02. Sahne ve Katmanlar (Scenes & Layers)

> **"Derinlik, karmaşıklığı yönetmenin anahtarıdır."**

Bu modül, Storyline'ı PowerPoint'ten ayıran en büyük özellik olan **Katman (Layer)** mantığını ve **Slide Master** mimarisini işler.

## 🎯 Hedefler
- Slide Master ile global tasarım şablonları oluşturmak.
- Katmanlar (Layers) ile tek sayfada çoklu içerik sunmak.
- Base Layer (Ana Katman) etkileşimlerini yönetmek.

## 🛠️ Teknik Detaylar

### 1. Slide Master: "Bir Kere Yap, Her Yerde Kullan"
Her slayta tek tek logo, başlık, ileri/geri butonu koymak amatörlüktür.
- **View > Slide Master** menüsünden ana şablonu tasarlayın.
- "Feedback Master" ile Doğru/Yanlış pop-up'larının tasarımını standartlaştırın.

### 2. Layers (Katmanlar) Mantığı
Katmanlar, şeffaf asetat kağıtları gibi ana slaytın üzerine biner.
- **Show Layer:** Bir tetikleyici ile katmanı gösterirsiniz.
- **Hide Layer:** Katmandaki bir buton (genelde "X") ile katmanı gizlersiniz.
- **Layer Properties:** En kritik ayarlar buradadır:
    - *Prevent user from clicking on the base layer:* Katman açıkken arkadaki butonlara basılmasını engeller (Modal Dialog mantığı).
    - *Pause timeline of base layer:* Katman açıldığında ana slayttaki videoyu/sesi dondurur.

### 🧪 Laboratuvar Görevi
1. **Slide Master**'a gidip kurumsal bir tema (Logo + Renkler) oluşturun.
2. Ana slayta 3 adet buton koyun (Konu A, Konu B, Konu C).
3. Her buton için bir **Layer** oluşturun.
4. Butonlara tıklandığında ilgili katmanı açacak tetikleyicileri yazın.
5. Katmanlar açıkken ana sahneye tıklanmasını engelleyin.
