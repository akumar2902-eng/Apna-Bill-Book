# Apna Bill Book: Android APK

App offline bhi chalti hai, kyunki saari files APK ke andar hoti hain.

## Tareeka A: Computer par Android Studio ke bina (GitHub se, free)
1. github.com par free account banayein.
2. Naya repository banayein (naam: apna-bill-book, Public ya Private).
3. Is zip ko extract karein. Uske andar ki SAARI files (package.json, www, capacitor.config.json, .github waghairah) repository mein upload karein ("Add file" > "Upload files").
   Dhyan dein: `.github` folder bhi upload hona chahiye. Agar wo na jaye, to "Add file" > "Create new file" mein naam `.github/workflows/build-apk.yml` likhkar is zip wali file ka text paste kar dein.
4. Upar "Actions" tab kholein. "Build APK" chunein aur "Run workflow" dabayein.
5. 4 se 6 minute mein hara tick aayega. Us run ko kholein, neeche "Artifacts" mein "Apna-Bill-Book-APK" download karein.
6. Zip extract karne par `app-debug.apk` milegi. Use phone mein bhejein aur install karein ("Unknown sources" allow karna pad sakta hai).

## Tareeka B: Android Studio se
1. Node.js 18+ aur Android Studio install karein.
2. `npm install`, `npx cap add android`, `npx cap sync android`, `npx cap open android`
3. Build > Build APK(s). APK: `android/app/build/outputs/apk/debug/app-debug.apk`

## App badalna ho to
`www/index.html` edit karein. Tareeka A mein dobara upload karke "Run workflow" chalayein.

## Dhyan dein
- Data phone ke andar save hota hai. App uninstall karne par chala jayega, isliye "Backup download karein" rakhein.
- Cloud backup (claude.ai login wala) sirf claude.ai link par chalta hai, APK mein nahi.
- Bill ka JPG/PDF share menu se jata hai. Pehle test kar lein.
- Play Store ke liye signed release build alag se chahiye.
