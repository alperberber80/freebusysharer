# 📅 FreeBusy Sharer — Yayın Paketi

## Dosya Yapısı

```
FreeBusySharer-Publish/
├── taskpane.html     ← Ana uygulama (EWS entegrasyonlu)
├── manifest.xml      ← Office Add-in tanım dosyası
├── commands.html     ← Manifest için gerekli (boş)
├── support.html      ← Destek sayfası
├── privacy.html      ← Gizlilik politikası
└── assets/
    ├── icon-16.png   ← 16x16 px ikon
    ├── icon-32.png   ← 32x32 px ikon
    ├── icon-64.png   ← 64x64 px ikon (HighRes)
    └── icon-80.png   ← 80x80 px ikon
```

---

## Yayın Öncesi Yapılacaklar

### 1. manifest.xml Güncelle

```xml
<!-- a) Yeni GUID üret: guidgenerator.com -->
<Id>BURAYA-YENI-GUID</Id>

<!-- b) Tüm YOUR_HOST değerlerini değiştir -->
<!-- Örnek GitHub Pages: -->
https://kullaniciadi.github.io/freebusysharer/
```

### 2. support.html ve privacy.html

```
destek@sizinalaniniz.com → kendi e-postanızla değiştirin
```

### 3. İkonları Ekle

`assets/` klasörüne 4 adet PNG ikon koyun:
- Boyutlar: 16x16, 32x32, 64x64, 80x80
- Format: PNG, şeffaf arka plan
- Ücretsiz ikon: flaticon.com veya icons8.com

---

## GitHub Pages ile Yayın (Ücretsiz)

```bash
# 1. GitHub'da yeni repo oluştur: freebusysharer (Public)

# 2. Tüm dosyaları yükle (drag-drop veya git push)

# 3. Settings → Pages → Branch: main → Save

# 4. manifest.xml içindeki YOUR_HOST'u değiştir:
#    https://KULLANICIADUN.github.io/freebusysharer

# 5. Güncellenmiş manifest.xml'i repoya yükle
```

---

## Test (Outlook Web)

```
1. outlook.office.com → herhangi bir e-posta aç
2. Sağ üst "..." → Eklentileri Al
3. Özel Eklentiler → + → Dosyadan Ekle
4. manifest.xml seç
5. Outlook'u yenile → Ribbon'da buton görünmeli
```

---

## Şirket İçi Dağıtım (M365 Admin)

```
admin.microsoft.com
→ Settings → Integrated apps
→ Upload custom apps → manifest.xml
→ Kullanıcıları seç → Deploy
```

---

## AppSource'a Gönder

```
partner.microsoft.com
→ Marketplace offers → New offer → Office add-in
→ manifest.xml + screenshots + privacy URL
→ İnceleme: 3-5 iş günü
```

---

## Gereksinimler

- Microsoft 365 veya Exchange 2016+
- Outlook 2016+ (Desktop) veya Outlook Web
- HTTPS hosting (GitHub Pages ücretsiz)
