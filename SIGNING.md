# Signing the APK (optional)

The GitHub Actions workflow produces an `app-debug.apk` (unsigned debug) which is fine for testing.
If you need a release-signed APK, follow these options:

Option A (recommended):
1. Generate a keystore locally:
   ```
   keytool -genkey -v -keystore release-keystore.jks -alias music17 -keyalg RSA -keysize 2048 -validity 10000
   ```
2. Add the keystore to GitHub Secrets (Settings → Secrets → Actions):
   - `KESTORE_BASE64` : base64 of the keystore file
   - `KEY_ALIAS` : `music17`
   - `KEY_PASSWORD` : the keystore password
   - `KEYSTORE_PASSWORD` : the keystore password
3. Edit `.github/workflows/android-build.yml` to enable release signing steps (comments included).

Option B:
- Download the debug APK produced by the workflow and use `apksigner` to sign locally.

