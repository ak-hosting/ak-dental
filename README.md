# AK Dental - Ankara Elit Diş Kliniği Web Sitesi Şablonu

![AK Dental Banner](assets/images/ak-dental-banner.png)

Ankara'daki elit diş klinikleri için ücretsiz, SEO dostu ve mobil uyumlu web sitesi şablonu. Bootstrap 5 ile geliştirildi, birkaç saniyede klonlayıp çalıştırabilirsiniz!

**[🚀 Canlı Demo](https://ak-hosting.github.io/ak-dental/)** | **[📧 Destek için İletişime Geçin](mailto:ak@ak-pro.com)**

## 🚀 Özellikler

- **Lüks Tasarım**: Mobil öncelikli, Bootstrap 5 ile responsive ve elit görünüm
- **Hizmetler Bölümü**: Estetik diş hekimliği, implant, diş beyazlatma ve daha fazlası
- **İletişim/Randevu Formu**: SMTP entegrasyonlu, kolay yapılandırma
- **Galeri**: Lightbox özellikli klinik görselleri
- **SEO Optimize**: Ankara için anahtar kelimeler (ör. "diş kliniği Çankaya")
- **Hızlı Yükleme**: Optimize edilmiş görseller ve kod
- **Smooth Scroll**: Zarif sayfa geçişleri
- **AOS Animasyonları**: Scroll tabanlı animasyonlar
- **Türk Lirası Fiyatlandırma**: ₺ sembolü ile fiyat gösterimi

## 📸 Ekran Görüntüleri

![Ana Sayfa](assets/images/screenshot-homepage.png)
![Hizmetler](assets/images/screenshot-services.png)
![İletişim](assets/images/screenshot-contact.png)

## 📜 Kredi Zorunluluğu

Bu şablonu kullanıyorsanız, lütfen footer'da şu ibareyi ekleyin:

```html
Geliştirici: a.koc - https://github.com/ak-hosting
```

## 🛠️ Kurulum

### 1. Depoyu Klonlayın

```bash
git clone https://github.com/ak-hosting/ak-dental.git
cd ak-dental
```

### 2. İçerikleri Özelleştirin

- `index.html` dosyasındaki metinleri ve görselleri güncelleyin
- `assets/css/style.css` dosyasındaki renkleri değiştirin
- `assets/images/` klasörüne kendi klinik görsellerinizi ekleyin

### 3. İletişim Formu Yapılandırması

`.env.example` dosyasını `.env` olarak kopyalayın:

```bash
cp .env.example .env
```

`.env` dosyasına SMTP ayarlarınızı ekleyin:

```env
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
FROM_EMAIL=your-email@gmail.com
TO_EMAIL=info@yourbusiness.com
```

### 4. Yerel Sunucuda Çalıştırın

```bash
python -m http.server 8000
```

Tarayıcıda `http://localhost:8000` adresine gidin.

## 🎨 Özelleştirme Rehberi

### Renkler

`assets/css/style.css` dosyasındaki CSS değişkenlerini güncelleyin:

```css
:root {
    --primary-color: #003087; /* Lacivert */
    --secondary-color: #FFD700; /* Altın tonu */
    --accent-color: #FFFFFF; /* Beyaz vurgu rengi */
}
```

### Görseller

1. `assets/images/` klasörüne kendi klinik görsellerinizi ekleyin
2. `index.html` dosyasında görsel yollarını güncelleyin:

```html
<img src="assets/images/your-image.jpg" alt="Klinik Görseli">
```

### Hizmetler

`index.html` dosyasındaki hizmet kartlarını kendi hizmetlerinize göre düzenleyin:

```html
<div class="service-card">
    <div class="service-icon">
        <i class="fas fa-smile"></i>
    </div>
    <h4>Ortodonti</h4>
    <p>Tel tedavisi ve şeffaf plaklar ile düzgün diş dizilimi</p>
    <div class="service-price">₺10.000 - ₺30.000</div>
    <a href="#contact" class="btn btn-outline-primary btn-sm">Detay Bilgi</a>
</div>
```

### İletişim Bilgileri

`index.html` dosyasındaki iletişim bilgilerini güncelleyin:

```html
<div class="contact-item">
    <i class="fas fa-map-marker-alt text-primary me-3"></i>
    <div>
        <strong>Adres:</strong><br>
        Sizin Adresiniz<br>
        Çankaya / Ankara
    </div>
</div>
```

## 📱 Mobil Uyumluluk

Şablon tüm cihazlarda mükemmel görünür:

- **Desktop**: 1200px ve üzeri
- **Tablet**: 768px - 1199px
- **Mobile**: 767px ve altı

## 🔧 Teknik Özellikler

- **HTML5**: Semantik markup
- **CSS3**: Modern stiller ve animasyonlar
- **JavaScript**: ES6+ özellikleri
- **Bootstrap 5**: Responsive framework
- **Font Awesome**: İkonlar
- **AOS**: Scroll animasyonları
- **Lightbox**: Galeri görüntüleme

## 📊 SEO Optimizasyonu

### Meta Etiketler

```html
<meta name="description" content="Ankara'da elit diş hekimliği hizmetleri. Estetik diş hekimliği, implant, ortodonti ve daha fazlası.">
<meta name="keywords" content="Ankara diş kliniği, estetik diş hekimliği Çankaya, implant Ümitköy">
```

### Anahtar Kelimeler

- Ankara diş kliniği
- Estetik diş hekimliği Çankaya
- İmplant Ümitköy
- Diş beyazlatma Ankara
- Ortodonti Çayyolu
- Diş hekimi Ankara

## 🚀 Performans Optimizasyonu

- **Lazy Loading**: Görseller için
- **CSS/JS Minifikasyonu**: Hızlı yükleme
- **Browser Caching**: Tekrar ziyaretler için
- **Optimize Görseller**: WebP formatı desteği

## 📞 Destek ve İletişim

### Ücretsiz Destek

- GitHub Issues: Sorularınız için
- E-posta: ak@ak-pro.com

### Ücretli Özelleştirme Hizmetleri

- **Logo Tasarımı**: ₺500 - ₺1.500
- **Renk Tema Değişimi**: ₺200 - ₺500
- **Online Randevu Sistemi**: ₺1.000 - ₺3.000
- **Ödeme Entegrasyonu**: ₺2.000 - ₺5.000
- **Özel Özellikler**: Fiyat teklifi için iletişime geçin

## 📄 Lisans

MIT lisansı ile lisanslanmıştır. Ticari kullanım için `LICENSE` dosyasını inceleyin.

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Commit yapın (`git commit -m 'Add some AmazingFeature'`)
4. Push yapın (`git push origin feature/AmazingFeature`)
5. Pull Request açın

## 📋 Changelog

### v1.0.0 (2024-01-15)
- İlk sürüm
- Bootstrap 5 entegrasyonu
- Responsive tasarım
- SEO optimizasyonu
- İletişim formu
- Galeri bölümü

## 🔗 Faydalı Linkler

- [Bootstrap 5 Dokümantasyonu](https://getbootstrap.com/docs/5.3/)
- [Font Awesome İkonları](https://fontawesome.com/icons)
- [AOS Animasyon Kütüphanesi](https://michalsnik.github.io/aos/)
- [Lightbox Galeri](https://lokeshdhakar.com/projects/lightbox2/)

## ⭐ Yıldız Verin

Bu projeyi beğendiyseniz, GitHub'da yıldız vermeyi unutmayın!

---

**Geliştirici**: a.koc  
**GitHub**: https://github.com/ak-hosting  
**İletişim**: ak@ak-pro.com  
**Lisans**: MIT 