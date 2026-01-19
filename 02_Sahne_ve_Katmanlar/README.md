# 02. Sahne ve Katmanlar: "Derinlik Mühendisliği"

> **"Acemi tasarımcı yanal düşünür (yeni slayt); usta tasarımcı dikey düşünür (katmanlar)."**

Bu modül, Storyline'ın en güçlü silahı olan **Layers (Katmanlar)** ve üretim verimliliğini %500 artıran **Slide Master** yapısını derinlemesine inceler. Articulate Storyline kullanıp da katmanları kullanmıyorsanız, aslında PowerPoint kullanıyorsunuz demektir.

## 🎯 Bu Modülde Neler Öğreneceksiniz?
1.  **Slide Master:** Tasarım sistemleri (Design Systems) kurmak.
2.  **Layer Logic:** Ana sahneyi kirletmeden ek içerik sunmak.
3.  **Modal Dialogs:** Kullanıcıyı odaklayan etkileşimler tasarlamak.
4.  **Feedback Masters:** Sıkıcı "Doğru/Yanlış" pop-up'larını sanat eserine dönüştürmek.

---

## 🛠️ Teknik Derinlik ve Best Practices

### 1. Slide Master: "Tek Merkezden Yönetim"
`View > Slide Master`
Her slaytın arkasında çalışan "görünmez el"dir.
- **Layouts (Düzenler):** "Konu Anlatım Sayfası", "Video Sayfası", "Giriş Sayfası" gibi şablonlar oluşturun. Yeni slayt eklerken "Insert Slide > Basic Layouts" yerine kendi yaptığınız bu düzenleri seçin.
- **Placeholder (Yer Tutucu):** Master slayt üzerine sadece "Text Box" değil, "Content Placeholder" koyun. Böylece slayt aşamasında oraya ister resim, ister video, ister metin koyabilirsiniz.

### 2. Layers (Katmanlar): "Odanın İçindeki Odalar"
Slaytı bir oda gibi düşünün. Katmanlar, o odada ışıkları kapatıp sadece bir köşeye spot ışığı tutmak gibidir.
- **Base Layer (Temel Katman):** Odanın kendisi.
- **Layer Properties (Katman Özellikleri):** (Çark Simgesi)
    - **Hide other slide layers:** Aynı anda sadece bir katman açık olsun istiyorsanız bunu seçin (Tab etkileşimleri için ideal).
    - **Prevent user from clicking on the base layer:** *EN ÖNEMLİ ÖZELLİK.* Bunu seçerseniz, katman açıkken kullanıcı arkadaki butonlara tıklayamaz. Kullanıcıyı katmandaki içeriği okumaya ve oradaki "Kapat" butonuna basmaya zorlarsınız.
    - **Pause timeline of base layer:** Video izlerken bir soru sorduğunuzda, videonun arkada akıp gitmesini istemiyorsanız bunu seçin.

### 3. Feedback Master
Storyline'ın varsayılan "Yeşil Tik / Kırmızı Çarpı" geri bildirimleri çok demodedir.
- `View > Feedback Master` bölümüne giderek kendi modern, şık "Tebrikler" ve "Tekrar Dene" pencerelerinizi tasarlayın. Bu tasarım tüm quiz sorularına otomatik uygulanır.

---

## 🚫 Sık Yapılan Hatalar (Çukurlar)

| Hata | Sonuç | Çözüm |
| :--- | :--- | :--- |
| **Manuel Kopyalama** | Her slayt için logoyu copy-paste yapmak. | Logoyu Slide Master'a koyun. |
| **Katman Karmasası** | Bir katman açılınca diğerinin kapanmaması. | Layer Properties'den "Hide other slide layers"ı işaretleyin. |
| **Görünmez Kilit** | Katman açıkken arkadaki butonun çalışması. | "Prevent user from clicking on the base layer" kutusunu işaretleyin. |

---

## 🧪 Laboratuvar Görevi: "İnteraktif Sekmeler (Tabs)"

1.  Bir Slide Master düzeni oluşturun: Solda menü, sağda içerik alanı.
2.  Normal slayta dönün ve 4 adet buton ekleyin: (Vizyon, Misyon, Değerler, Ekip).
3.  Sağ alt panelden 4 adet **Layer** oluşturun ve isimlerini butonlarla eşleyin.
4.  Her katmana ilgili metni yazın.
5.  **Trigger Yazın:** "Show Layer [Vizyon] when User Clicks [Btn_Vizyon]".
6.  **Kritik Ayar:** Her katmanın özelliklerine girip "Hide other slide layers" seçeneğini aktif edin. Böylece Vizyon'a basınca Misyon kapanır.
