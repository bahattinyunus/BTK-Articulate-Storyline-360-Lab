# 🎬 Proje Senaryosu: Kurumsal Şablon Kurulumu (The Foundation)

## 🏢 Bağlam
"Global Tech" adlı bir şirket, yeni işe başlayanlar için bir oryantasyon eğitimi hazırlatmak istiyor. Senden, tüm ekibin kullanabileceği standart bir **Storyline Şablonu (.storytemplate)** hazırlamanı istiyorlar.

## 📝 Gereksinimler (Spec Sheet)

### 1. Teknik Ayarlar
- **Çözünürlük:** Ultra Widescreen değil, standart Laptop dostu **1280x720 (16:9)**.
- **Player:**
    - Menü: **Kapalı** (Kendi menümüzü yapacağız).
    - Resources: **Açık** (Şirket politikası PDF'i eklenecek).
    - Renkler: Şirket rengi olan **Lacivert (#003366)** ve **Beyaz**.
    - Font: **Roboto** veya **Open Sans**.

### 2. Sahne (Scene) Yapısı
Proje iskeletini şu şekilde kurmalısın:
- **00_Intro:** Kapak sayfası ve Kullanıcı Adı girişi.
- **01_Main_Content:** Ana menü ve 3 alt bölüm.
- **02_Quiz:** Sınav giriş ekranı ve sorular.
- **99_Assets:** Kullanılacak ikonların ve resimlerin durduğu "Çöplük" sahnesi (Asla yayınlanmaz, depo olarak kullanılır).

### 3. İsimlendirme Kuralları (Convention)
- Articulate'in verdiği "Untitled Scene" isimlerini kabul etmiyoruz.
- Her sahneyi kodlarıyla (`00_...`, `01_...`) isimlendir.

## 🚀 Görev
Bu projeyi oluştur, ayarlarını yap ve `GlobalTech_Template_v1.story` olarak kaydet.
