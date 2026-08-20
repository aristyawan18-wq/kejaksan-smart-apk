# Kejaksan Smart - Build APK via HP

## Isi ZIP
- index.html = File asli + patch hidden admin (7x tap version & 4s hold header)
- package.json
- capacitor.config.json
- .github/workflows/build-apk.yml = Build Debug APK
- .github/workflows/build-release.yml = Build Release Signed APK
- .github/workflows/generate-keystore.yml = Generate keystore dari HP (1x saja)

## Cara Upload via HP
1. Buat repo baru di GitHub: kejaksan-smart-apk
2. Extract ZIP ini di HP pakai ZArchiver
3. Di GitHub repo > Add file > Upload files > upload semua file & folder .github
4. Commit

## Build Debug (cepat)
Actions > Build APK - Kejaksan Smart > Run workflow

## Build Release Signed (untuk petugas)
1. Actions > Generate Keystore > Run > download artifact > extract > buka release.jks.base64.txt
2. Settings > Secrets and variables > Actions > New secret:
   - KEYSTORE_BASE64 = isi base64
   - KEYSTORE_PASSWORD = kejaksan123
   - KEY_ALIAS = kejaksan
   - KEY_PASSWORD = kejaksan123
3. Actions > Build RELEASE Signed APK > Run

## Hidden Triggers
- Tap 7x pada teks Versi v2.0.0 = Dashboard Admin Pelacakan Lokasi
- Long-press 4 detik pada judul header = Panel AI Config

Pelacakan tetap aktif sesuai file asli.
