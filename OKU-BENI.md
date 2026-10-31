# Kalorim APK

Bu klasör, Kalorim uygulamasını Android APK'ya çeviren hazır bir projedir.
Bilgisayarına Android Studio kurmadan, GitHub'ın ücretsiz derleme sunucusuyla APK alabilirsin.

## Yol 1: GitHub ile (kurulum gerektirmez)

1. github.com'da ücretsiz hesap aç, yeni bir depo oluştur (Private olabilir).
2. Bu klasörün İÇİNDEKİ her şeyi (www, .github, package.json, capacitor.config.json) depoya yükle.
   "Add file > Upload files" ile sürükle-bırak yeterli. `.github` klasörünün de yüklendiğinden emin ol.
3. Depoda "Actions" sekmesine gir. "APK derle" çalışmaya başlar (yaklaşık 4-6 dakika).
   Başlamazsa soldan "APK derle" > "Run workflow" de.
4. Bitince çalışmanın sayfasının en altındaki "Artifacts" kısmından `kalorim-apk` dosyasını indir, zip'ten çıkar.
5. `app-debug.apk` dosyasını telefona at ve aç. "Bilinmeyen kaynaklardan yükle" iznini ver.

## Yol 2: Android Studio ile

1. Node.js ve Android Studio kur.
2. Bu klasörde terminal aç:
   npm install
   npx cap add android
   npx cap sync android
   npx cap open android
3. Android Studio'da Build > Build APK(s) de.

## Notlar

- Yazı tipleri internetten yüklenir. İnternet yoksa sistem yazı tipine döner, uygulama yine çalışır.
- Kayıtlar telefondaki uygulamanın içinde saklanır. Uygulamayı silersen kayıtlar da silinir.
- Bu bir test (debug) APK'sıdır. Play Store'a koymak için ayrıca imzalamak gerekir.
