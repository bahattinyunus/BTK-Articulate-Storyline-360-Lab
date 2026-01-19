# 🧠 Mantık Kütüphanesi (Logic Patterns)

> **"Her interaktif öğe, basit bir mantık desenidir. Bu desenleri ezberleyin, gerisi legoları birleştirmektir."**

Storyline tasarımcılarının sürekli kullandığı standart mantık (Logic) yapıları buradadır.

---

## 🎚️ Toggle Switch (Aç/Kapa Anahtarı)
Bir butona basınca açılsın, tekrar basınca kapansın.
1.  **Değişken:** `isMenuOpen` (Boolean: False)
2.  **Trigger 1:** `Set isMenuOpen to NOT Assignment` (Değeri tersine çevir. True ise False, False ise True yap).
    - *When:* User clicks Button.
3.  **Trigger 2:** `Show Layer [Menu]`.
    - *Condition:* If `isMenuOpen` == True.
4.  **Trigger 3:** `Hide Layer [Menu]`.
    - *Condition:* If `isMenuOpen` == False.

---

## 📶 Custom Progress Bar (İlerleme Çubuğu)
Storyline'ın kendi barını değil, kendi tasarımımızı kullanmak.
1.  **Değişken:** `TotalSlides` (Örn: 10), `CurrentSlide` (Örn: 1).
2.  **Şekil:** Ekrana bir dikdörtgen (Bar) koyun.
3.  **Variable (Slider):** Dikdörtgen yerine bir "Slider" kullanmak en kolayıdır. Slider'ın "Thumb" (Düğme) kısmını gizleyin.
4.  **Logic:**
    - Her slaytın başına Trigger koyun: `Set Slider1 to SlideNumber`.
    - Slider'ın maksimum değerini `TotalSlides` (10) yapın.
    - Slayt ilerledikçe Slider otomatik dolacaktır.

---

## 🔒 Accordion Menu (Akordeon Menü)
Bir başlığa tıklayınca içeriği açılsın, diğerleri kapansın.
1.  **Katmanlar:** Her başlık için bir katman (Layer 1, Layer 2).
2.  **Katman Ayarı:** Her katmanın ayarlarında **"Hide other slide layers"** seçeneğini işaretleyin.
3.  **State:** Tıklanan başlığın rengini değiştirmek için "Selected" durumunu kullanın.
    - Button Set: Tüm başlık butonlarını seçip sağ tık > **Button Set** yapın. Böylece biri seçilince diğerinin seçimi otomatik kalkar.

---

## 🎲 Random Number Generator (Zar Atma)
1.  **Değişken:** `DiceResult` (Number).
2.  **Trigger:** `Generate Random Number`.
    - *Variable:* DiceResult.
    - *Min:* 1, *Max:* 6.
    - *When:* User clicks Button.
3.  **Görsel:** 6 tane Katman yapın (Zar 1, Zar 2...).
4.  **Show Logic:**
    - Show Layer [Zar 1] if `DiceResult` == 1.
    - Show Layer [Zar 2] if `DiceResult` == 2...

> **Not:** Bu desenleri bir kere kurup "Master Slide" veya "Template" olarak saklarsanız hızınız 10 kat artar.
