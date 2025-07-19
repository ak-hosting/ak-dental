# AK Dental - Görsel Dosyaları

Bu klasör, AK Dental web sitesi şablonu için gerekli görselleri içerir.

## 📁 Gerekli Görseller

### Ana Görseller
- `clinic-interior.jpg` - Klinik iç mekan görseli (1920x1080px)
- `gallery1.jpg` - Galeri görseli 1 (800x600px)
- `gallery2.jpg` - Galeri görseli 2 (800x600px)
- `gallery3.jpg` - Galeri görseli 3 (800x600px)
- `gallery4.jpg` - Galeri görseli 4 (800x600px)
- `gallery5.jpg` - Galeri görseli 5 (800x600px)
- `gallery6.jpg` - Galeri görseli 6 (800x600px)

### Favicon ve İkonlar
- `favicon.ico` - Site favicon'u (32x32px)
- `favicon-16x16.png` - Küçük favicon (16x16px)
- `favicon-32x32.png` - Büyük favicon (32x32px)
- `apple-touch-icon.png` - Apple touch icon (180x180px)

### Banner ve Screenshot'lar
- `ak-dental-banner.png` - GitHub README banner'ı (1200x600px)
- `screenshot-homepage.png` - Ana sayfa ekran görüntüsü
- `screenshot-services.png` - Hizmetler sayfası ekran görüntüsü
- `screenshot-contact.png` - İletişim sayfası ekran görüntüsü

## 🖼️ Görsel Özellikleri

### Önerilen Formatlar
- **JPEG**: Fotoğraflar için (kalite: 80-85%)
- **PNG**: İkonlar ve şeffaf görseller için
- **WebP**: Modern tarayıcılar için optimize edilmiş format
- **SVG**: Vektör ikonlar için

### Boyut Önerileri
- **Hero görseli**: 1920x1080px (16:9 oranı)
- **Galeri görselleri**: 800x600px (4:3 oranı)
- **Favicon**: 32x32px
- **Banner**: 1200x600px (2:1 oranı)

### Dosya Boyutu Limitleri
- **Hero görseli**: Maksimum 500KB
- **Galeri görselleri**: Maksimum 200KB
- **Favicon**: Maksimum 10KB
- **Banner**: Maksimum 300KB

## 📸 Görsel Kaynakları

### Ücretsiz Görsel Kaynakları
- [Unsplash](https://unsplash.com/s/photos/dental-clinic) - Yüksek kaliteli fotoğraflar
- [Pexels](https://www.pexels.com/search/dental/) - Ticari kullanıma uygun görseller
- [Pixabay](https://pixabay.com/images/search/dental/) - Ücretsiz stok fotoğraflar

### Önerilen Arama Terimleri
- "dental clinic"
- "dental office"
- "dentist"
- "dental treatment"
- "modern dental clinic"
- "dental equipment"
- "smile"

## 🎨 Görsel Optimizasyonu

### Manuel Optimizasyon
1. **Boyutlandırma**: Görselleri önerilen boyutlara getirin
2. **Sıkıştırma**: JPEG kalitesini 80-85% arasında ayarlayın
3. **Format Dönüşümü**: WebP formatına dönüştürün
4. **Alt Text**: SEO için açıklayıcı alt text ekleyin

### Otomatik Optimizasyon
```bash
# Node.js ile görsel optimizasyonu
npm install -g imagemin-cli
imagemin assets/images/* --out-dir=assets/images/optimized
```

## 📝 Görsel Kullanım Talimatları

### 1. Kendi Görsellerinizi Ekleyin
1. Görsellerinizi bu klasöre kopyalayın
2. Dosya adlarında Türkçe karakter kullanmayın
3. Dosya boyutlarını kontrol edin
4. Alt text'leri güncelleyin

### 2. HTML'de Görsel Yollarını Güncelleyin
```html
<!-- Örnek görsel kullanımı -->
<img src="assets/images/your-image.jpg" alt="Açıklayıcı metin" class="img-fluid rounded shadow">
```

### 3. CSS'de Arka Plan Görseli
```css
.hero-section {
    background: linear-gradient(rgba(0, 48, 135, 0.8), rgba(0, 68, 170, 0.8)), 
                url('assets/images/your-hero-image.jpg');
}
```

## 🔒 Telif Hakkı Uyarısı

- Sadece ticari kullanıma uygun görseller kullanın
- Telif hakkı olan görselleri kullanmayın
- Görsel kaynaklarını belirtin (gerekirse)
- Unsplash, Pexels gibi platformlardan gelen görseller genellikle güvenlidir

## 📞 Destek

Görsel optimizasyonu veya özel görsel tasarımı için:
- **E-posta**: ak@ak-pro.com
- **Ücretli Hizmet**: Özel görsel tasarımı ve optimizasyonu

---

**Not**: Bu klasördeki görseller örnek amaçlıdır. Kendi klinik görsellerinizle değiştirmeniz önerilir. 