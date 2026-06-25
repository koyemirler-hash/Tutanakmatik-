# 📋 Tutanakmatik — APK Kurulum Rehberi

## Gereksinimler
- Node.js 16+ (https://nodejs.org)
- Android Studio (https://developer.android.com/studio)
- Java JDK 11+

---

## 🚀 Adım Adım APK Alma

### 1. Bağımlılıkları Kur
```bash
npm install
```

### 2. Android Platformunu Ekle
```bash
npx cap add android
```

### 3. Dosyaları Senkronize Et
```bash
npx cap sync android
```

### 4. Android Studio'da Aç
```bash
npx cap open android
```

### 5. Android Studio'da APK Oluştur
- Üst menü: **Build → Build Bundle(s) / APK(s) → Build APK(s)**
- APK çıktısı: `android/app/build/outputs/apk/debug/app-debug.apk`

---

## 📱 Telefona Yükleme

### USB ile:
```bash
adb install android/app/build/outputs/apk/debug/app-debug.apk
```

### Manuel:
1. APK dosyasını telefona kopyala
2. Dosya yöneticisinden aç
3. "Bilinmeyen kaynaklardan yükle" iznini ver
4. Yükle

---

## 🌐 GitHub Pages ile Web Olarak Kullanma (APK'sız)

1. Bu klasörü GitHub'a yükle
2. Settings → Pages → Branch: main, Folder: / (root)
3. Link: `https://KULLANICI.github.io/tutanakmatik`

---

## 📁 Dosya Yapısı
```
tutanakmatik/
├── index.html          ← Ana uygulama (tüm kod burada)
├── capacitor.config.json
├── package.json
└── README.md
```

---

## ⚙️ Release APK (İmzalı)
Android Studio'da:
- **Build → Generate Signed Bundle / APK**
- Keystore oluştur veya mevcut keystore kullan
- Release APK çıktısı: `android/app/build/outputs/apk/release/`

