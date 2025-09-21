# GitHub Pages Kurulum Rehberi

Bu dosya, privacy policy'nizi GitHub Pages'da yayınlamak için adım adım rehberdir.

## 1. GitHub Repository Oluşturma

1. GitHub'da yeni bir repository oluşturun:
   - Repository adı: `gemini-rss-reader` (veya istediğiniz ad)
   - Public olarak ayarlayın
   - README.md ile başlatın

## 2. Dosyaları Upload Etme

Repository'e şu dosyaları yükleyin:
- `privacy-policy.md` (hazırladığımız dosya)
- `README.md` (isteğe bağlı: eklenti açıklaması)
- `index.html` (ana sayfa için)

## 3. GitHub Pages Aktifleştirme

1. Repository Settings'e gidin
2. Sol menüden "Pages" seçin  
3. Source olarak "Deploy from a branch" seçin
4. Branch: `main` (veya `master`)
5. Folder: `/ (root)` 
6. Save butonuna tıklayın

## 4. URL'yi Almak

GitHub size şu formatta URL verecek:
```
https://[kullanici-adi].github.io/[repo-adi]/
```

Privacy policy için:
```
https://[kullanici-adi].github.io/[repo-adi]/privacy-policy
```

## 5. manifest.json Güncelleme

`manifest.json` dosyasında şu kısmı güncelleyin:

```json
"homepage_url": "https://[gerçek-kullanici-adi].github.io/[gerçek-repo-adi]/"
```

## Örnek index.html

Repository ana sayfası için basit bir index.html:

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gemini RSS Reader</title>
    <style>
        body { font-family: Arial, sans-serif; max-width: 800px; margin: 0 auto; padding: 20px; }
        .header { text-align: center; margin-bottom: 40px; }
        .links { text-align: center; }
        .links a { margin: 0 20px; padding: 10px 20px; background: #007bff; color: white; text-decoration: none; border-radius: 5px; }
    </style>
</head>
<body>
    <div class="header">
        <h1>🔖 Gemini RSS Reader</h1>
        <p>RSS akışlarınızı düzenli takip edin</p>
    </div>
    
    <div class="links">
        <a href="privacy-policy">Gizlilik Politikası</a>
        <a href="https://chrome.google.com/webstore/category/extensions">Chrome Web Store</a>
    </div>
</body>
</html>
```

## Not

GitHub Pages'ın aktif olması 5-10 dakika sürebilir. URL'yi aldıktan sonra `manifest.json`'ı mutlaka güncelleyin.
