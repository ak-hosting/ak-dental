# AK Dental - Docker Kullanım Talimatları

Bu dosya, AK Dental web sitesi şablonunu Docker ile çalıştırmak için detaylı talimatlar içerir.

## 🐳 Docker Kurulumu

### Gereksinimler
- Docker Desktop (Windows/Mac) veya Docker Engine (Linux)
- Docker Compose

### Kurulum Kontrolü
```bash
docker --version
docker-compose --version
```

## 🚀 Hızlı Başlangıç

### 1. Basit Python Server (Önerilen)
```bash
# Container'ı başlat
docker run -d -p 8000:8000 -v $(pwd):/app -w /app python:3.9-alpine python -m http.server 8000

# Web sitesini görüntüle
# http://localhost:8000
```

### 2. Docker Compose ile (Gelişmiş)
```bash
# Tüm servisleri başlat
docker-compose -f docker-compose.simple.yml up -d

# Web sitesini görüntüle
# http://localhost:8000 (Python server)
# http://localhost:80 (Nginx proxy)
```

## 📋 Docker Komutları

### Container Yönetimi
```bash
# Container'ları listele
docker ps

# Container loglarını görüntüle
docker logs ak-dental-web

# Container'ı durdur
docker stop ak-dental-web

# Container'ı yeniden başlat
docker restart ak-dental-web

# Container'ı sil
docker rm ak-dental-web
```

### Docker Compose Komutları
```bash
# Servisleri başlat
docker-compose -f docker-compose.simple.yml up -d

# Servisleri durdur
docker-compose -f docker-compose.simple.yml down

# Logları görüntüle
docker-compose -f docker-compose.simple.yml logs

# Servisleri yeniden başlat
docker-compose -f docker-compose.simple.yml restart
```

## 🔧 Servis Detayları

### 1. Web Server (Port 8000)
- **Image**: python:3.9-alpine
- **Command**: python -m http.server 8000
- **Volume**: Mevcut dizin /app'e mount edilir
- **URL**: http://localhost:8000

### 2. Nginx Proxy (Port 80)
- **Image**: nginx:alpine
- **Config**: nginx.conf
- **Volume**: Statik dosyalar nginx'e mount edilir
- **URL**: http://localhost:80

### 3. Mail Server (Port 1025/8025)
- **Image**: mailhog/mailhog
- **SMTP**: localhost:1025
- **Web UI**: http://localhost:8025
- **Amaç**: E-posta testleri için

## 🛠️ Geliştirme Ortamı

### Hot Reload
```bash
# Geliştirme için volume mount ile
docker run -d -p 8000:8000 -v $(pwd):/app -w /app python:3.9-alpine python -m http.server 8000
```

### Debug Modu
```bash
# Container'a bağlan
docker exec -it ak-dental-web sh

# Dosyaları kontrol et
ls -la /app

# Python server'ı manuel başlat
python -m http.server 8000 --bind 0.0.0.0
```

## 🔍 Sorun Giderme

### 1. Port Çakışması
```bash
# Mevcut portları kontrol et
lsof -i :8000
lsof -i :80

# Farklı port kullan
docker run -d -p 8080:8000 -v $(pwd):/app -w /app python:3.9-alpine python -m http.server 8000
```

### 2. Dosya İzinleri
```bash
# Container içinde dosya izinlerini kontrol et
docker exec -it ak-dental-web ls -la /app

# İzinleri düzelt
chmod -R 755 .
```

### 3. Network Sorunları
```bash
# Network'leri listele
docker network ls

# Network detaylarını görüntüle
docker network inspect ak_dental_ak-dental-network
```

## 📊 Monitoring

### Container Durumu
```bash
# Tüm container'ları listele
docker ps -a

# Resource kullanımını görüntüle
docker stats
```

### Log Takibi
```bash
# Real-time log takibi
docker logs -f ak-dental-web

# Son 100 log satırı
docker logs --tail 100 ak-dental-web
```

## 🔒 Güvenlik

### Non-Root User
```dockerfile
# Dockerfile'da non-root user oluştur
RUN addgroup -g 1001 -S nodejs
RUN adduser -S nextjs -u 1001
USER nextjs
```

### Security Headers
```nginx
# nginx.conf'da güvenlik başlıkları
add_header X-Frame-Options "SAMEORIGIN" always;
add_header X-XSS-Protection "1; mode=block" always;
add_header X-Content-Type-Options "nosniff" always;
```

## 🚀 Production Deployment

### 1. Nginx ile Production
```bash
# Production nginx konfigürasyonu
docker run -d -p 80:80 -v $(pwd):/usr/share/nginx/html:ro -v $(pwd)/nginx.conf:/etc/nginx/nginx.conf:ro nginx:alpine
```

### 2. SSL Sertifikası
```bash
# Let's Encrypt ile SSL
docker run -d -p 80:80 -p 443:443 \
  -v $(pwd):/usr/share/nginx/html:ro \
  -v $(pwd)/ssl:/etc/nginx/ssl:ro \
  nginx:alpine
```

### 3. Load Balancer
```yaml
# docker-compose.prod.yml
version: '3.8'
services:
  nginx:
    image: nginx:alpine
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf:ro
      - .:/usr/share/nginx/html:ro
    restart: unless-stopped
```

## 📝 Örnek Kullanım Senaryoları

### Senaryo 1: Hızlı Test
```bash
# Tek komutla başlat
docker run -d -p 8000:8000 -v $(pwd):/app -w /app python:3.9-alpine python -m http.server 8000

# Test et
curl http://localhost:8000
```

### Senaryo 2: Geliştirme Ortamı
```bash
# Docker Compose ile tüm servisler
docker-compose -f docker-compose.simple.yml up -d

# Mail test et
curl -X POST http://localhost:1025/send -d "to=test@example.com&subject=Test&body=Hello"
```

### Senaryo 3: Production
```bash
# Nginx ile production
docker run -d -p 80:80 -v $(pwd):/usr/share/nginx/html:ro nginx:alpine

# SSL ile production
docker run -d -p 443:443 -v $(pwd):/usr/share/nginx/html:ro -v $(pwd)/ssl:/etc/nginx/ssl:ro nginx:alpine
```

## 🔗 Faydalı Linkler

- **Docker Documentation**: https://docs.docker.com/
- **Docker Compose**: https://docs.docker.com/compose/
- **Nginx Documentation**: https://nginx.org/en/docs/
- **MailHog**: https://github.com/mailhog/MailHog

## 📞 Destek

Docker konfigürasyonu ile ilgili sorularınız için:
- **E-posta**: ak@ak-pro.com
- **GitHub Issues**: https://github.com/ak-hosting/ak-dental/issues

---

**Not**: Bu talimatlar geliştirme ortamı için optimize edilmiştir. Production ortamı için ek güvenlik önlemleri alınmalıdır. 