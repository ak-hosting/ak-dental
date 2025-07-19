# AK Dental - Özelleştirme Rehberi

Bu dosya, AK Dental web sitesi şablonunu özelleştirmek için detaylı talimatlar içerir.

## 🎨 Renk Teması Değiştirme

### Ana Renkler

`assets/css/style.css` dosyasındaki CSS değişkenlerini güncelleyin:

```css
:root {
    --primary-color: #003087; /* Ana renk - Lacivert */
    --secondary-color: #FFD700; /* İkincil renk - Altın */
    --accent-color: #FFFFFF; /* Vurgu rengi - Beyaz */
    --text-dark: #2C3E50; /* Koyu metin */
    --text-light: #6C757D; /* Açık metin */
    --bg-light: #F8F9FA; /* Açık arka plan */
    --bg-dark: #1A1A1A; /* Koyu arka plan */
}
```

### Önerilen Renk Kombinasyonları

#### 1. Klasik Mavi-Altın (Varsayılan)
```css
--primary-color: #003087;
--secondary-color: #FFD700;
```

#### 2. Modern Yeşil
```css
--primary-color: #28A745;
--secondary-color: #FFC107;
```

#### 3. Lüks Mor
```css
--primary-color: #6F42C1;
--secondary-color: #FFD700;
```

#### 4. Profesyonel Gri
```css
--primary-color: #495057;
--secondary-color: #17A2B8;
```

## 🖼️ Görsel Değiştirme

### 1. Hero Arka Plan Görseli

`assets/css/style.css` dosyasında:

```css
.hero-section {
    background: linear-gradient(rgba(0, 48, 135, 0.8), rgba(0, 68, 170, 0.8)), 
                url('YENİ_GÖRSEL_URL');
}
```

### 2. Galeri Görselleri

1. `assets/images/` klasörüne yeni görsellerinizi ekleyin
2. `index.html` dosyasında görsel yollarını güncelleyin:

```html
<a href="assets/images/yeni-gorsel1.jpg" data-lightbox="gallery" data-title="Yeni Başlık">
    <img src="assets/images/yeni-gorsel1.jpg" alt="Açıklama" class="img-fluid rounded shadow">
</a>
```

### 3. Favicon

`assets/images/favicon.ico` dosyasını kendi favicon'unuzla değiştirin.

## 📝 İçerik Değiştirme

### 1. Klinik Bilgileri

`index.html` dosyasında şu bölümleri güncelleyin:

#### Logo ve İsim
```html
<a class="navbar-brand fw-bold" href="#home">
    <i class="fas fa-tooth me-2"></i>KLİNİK ADINIZ
</a>
```

#### Hero Bölümü
```html
<h1 class="display-4 fw-bold text-white mb-4">
    KLİNİK ADINIZ - Ankara'da Elit Diş Hekimliği
</h1>
<p class="lead text-white mb-4">
    Klinik açıklamanız buraya gelecek.
</p>
```

#### İletişim Bilgileri
```html
<div class="contact-item">
    <i class="fas fa-map-marker-alt text-primary me-3"></i>
    <div>
        <strong>Adres:</strong><br>
        SOKAK ADI, MAHALLE<br>
        İLÇE / ANKARA
    </div>
</div>
<div class="contact-item">
    <i class="fas fa-phone text-primary me-3"></i>
    <div>
        <strong>Telefon:</strong><br>
        <a href="tel:+903121234567">0312 123 45 67</a>
    </div>
</div>
<div class="contact-item">
    <i class="fas fa-envelope text-primary me-3"></i>
    <div>
        <strong>E-posta:</strong><br>
        <a href="mailto:info@kliniginiz.com">info@kliniginiz.com</a>
    </div>
</div>
```

### 2. Hizmetler

Her hizmet kartını şu şekilde düzenleyin:

```html
<div class="service-card">
    <div class="service-icon">
        <i class="fas fa-[İKON-ADI]"></i>
    </div>
    <h4>HİZMET ADI</h4>
    <p>Hizmet açıklaması buraya gelecek.</p>
    <div class="service-price">₺FİYAT</div>
    <a href="#contact" class="btn btn-outline-primary btn-sm">Detay Bilgi</a>
</div>
```

### 3. İstatistikler

Hero bölümündeki istatistikleri güncelleyin:

```html
<div class="stat-item">
    <h3 class="text-white fw-bold">SAYI</h3>
    <p class="text-white-50">AÇIKLAMA</p>
</div>
```

## 🔧 Teknik Özelleştirmeler

### 1. SEO Meta Etiketleri

`index.html` dosyasının `<head>` bölümünde:

```html
<title>KLİNİK ADINIZ - Ankara Elit Diş Kliniği | Estetik Diş Hekimliği & İmplant</title>
<meta name="description" content="Ankara'da elit diş hekimliği hizmetleri. KLİNİK AÇIKLAMASI.">
<meta name="keywords" content="Ankara diş kliniği, KLİNİK ADI, estetik diş hekimliği Çankaya">
```

### 2. Google Analytics

`index.html` dosyasının `<head>` bölümüne ekleyin:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 3. Facebook Pixel

`index.html` dosyasının `<head>` bölümüne ekleyin:

```html
<!-- Facebook Pixel Code -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'PIXEL_ID');
  fbq('track', 'PageView');
</script>
<noscript><img height="1" width="1" style="display:none"
  src="https://www.facebook.com/tr?id=PIXEL_ID&ev=PageView&noscript=1"
/></noscript>
```

## 📱 Mobil Optimizasyon

### 1. Viewport Meta Tag

`index.html` dosyasında zaten mevcut:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 2. Touch Icons

`index.html` dosyasının `<head>` bölümüne ekleyin:

```html
<link rel="apple-touch-icon" sizes="180x180" href="assets/images/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="assets/images/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="assets/images/favicon-16x16.png">
```

## 🚀 Performans Optimizasyonu

### 1. Görsel Optimizasyonu

Görsellerinizi şu boyutlarda optimize edin:

- **Hero görseli**: 1920x1080px
- **Galeri görselleri**: 800x600px
- **Favicon**: 32x32px

### 2. CSS/JS Minifikasyonu

Üretim ortamında CSS ve JS dosyalarını minify edin.

### 3. Browser Caching

`.htaccess` dosyası oluşturun:

```apache
# Browser Caching
<IfModule mod_expires.c>
    ExpiresActive on
    ExpiresByType text/css "access plus 1 year"
    ExpiresByType application/javascript "access plus 1 year"
    ExpiresByType image/png "access plus 1 year"
    ExpiresByType image/jpg "access plus 1 year"
    ExpiresByType image/jpeg "access plus 1 year"
</IfModule>
```

## 📧 E-posta Formu Yapılandırması

### 1. SMTP Ayarları

`.env` dosyasını oluşturun:

```env
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
FROM_EMAIL=your-email@gmail.com
TO_EMAIL=info@yourbusiness.com
```

### 2. Form Handler

`assets/js/script.js` dosyasında form gönderimini güncelleyin:

```javascript
// Gerçek backend entegrasyonu için bu kısmı değiştirin
fetch('/api/contact', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(data)
})
.then(response => response.json())
.then(data => {
    showAlert('Mesajınız başarıyla gönderildi!', 'success');
})
.catch(error => {
    showAlert('Bir hata oluştu. Lütfen tekrar deneyin.', 'error');
});
```

## 🔒 Güvenlik

### 1. HTTPS Zorunluluğu

Üretim ortamında mutlaka HTTPS kullanın.

### 2. Form Güvenliği

CSRF token ekleyin:

```html
<input type="hidden" name="_token" value="{{ csrf_token() }}">
```

### 3. Content Security Policy

`index.html` dosyasının `<head>` bölümüne ekleyin:

```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval' https://cdn.jsdelivr.net https://unpkg.com https://cdnjs.cloudflare.com; style-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net https://cdnjs.cloudflare.com; img-src 'self' data: https:; font-src 'self' https://cdnjs.cloudflare.com;">
```

## 📊 Analytics ve Takip

### 1. Google Search Console

Google Search Console'a sitenizi ekleyin ve sitemap.xml oluşturun.

### 2. Google My Business

Google My Business hesabı oluşturun ve kliniğinizi ekleyin.

### 3. Yandex Webmaster

Yandex Webmaster'a sitenizi ekleyin.

## 🎯 Pazarlama Özelleştirmeleri

### 1. Call-to-Action Butonları

CTA butonlarının renklerini değiştirin:

```css
.btn-cta {
    background: linear-gradient(135deg, var(--secondary-color), #FFA500);
    color: var(--text-dark);
    font-weight: 700;
    padding: 1rem 2rem;
    border-radius: var(--border-radius);
    transition: var(--transition);
}
```

### 2. Sosyal Medya Linkleri

Footer'a sosyal medya linkleri ekleyin:

```html
<div class="social-links">
    <a href="https://facebook.com/kliniginiz" target="_blank"><i class="fab fa-facebook"></i></a>
    <a href="https://instagram.com/kliniginiz" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://twitter.com/kliniginiz" target="_blank"><i class="fab fa-twitter"></i></a>
</div>
```

## 🆘 Sorun Giderme

### 1. Görseller Yüklenmiyor

- Dosya yollarını kontrol edin
- Dosya izinlerini kontrol edin
- Dosya adlarında Türkçe karakter kullanmayın

### 2. Form Gönderilmiyor

- JavaScript konsolunu kontrol edin
- SMTP ayarlarını kontrol edin
- Sunucu loglarını kontrol edin

### 3. Mobil Görünüm Bozuk

- Bootstrap CSS'inin yüklendiğinden emin olun
- Viewport meta tag'ini kontrol edin
- CSS media query'lerini kontrol edin

## 📞 Destek

Özelleştirme konusunda yardıma ihtiyacınız varsa:

- **E-posta**: ak@ak-pro.com
- **GitHub Issues**: https://github.com/ak-hosting/ak-dental/issues
- **Ücretli Destek**: Özel özelleştirmeler için iletişime geçin

---

**Not**: Bu rehber sürekli güncellenmektedir. En güncel versiyon için GitHub'ı kontrol edin. 