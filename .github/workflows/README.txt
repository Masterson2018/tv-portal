TvPortal – menyapp for Android TV (Navidrome / Emby)

Bygg APK:
1. Åpne mappen i Android Studio (File > Open). La den synkronisere Gradle.
2. Build > Build Bundle(s) / APK(s) > Build APK(s)
3. APK: app/build/outputs/apk/debug/app-debug.apk

Endre adresser: app/src/main/java/no/hjemme/portal/MainActivity.kt (øverst)

Installer på TV:
- Slå på utviklermodus + USB/nettverksfeilsøking, og kjør: adb connect <tv-ip>  og  adb install app-debug.apk
- Eller legg APK på minnepinne/nettsky og installer med en filbehandler (f.eks. "Send Files to TV" / "X-plore").

Bygg uten Android Studio (GitHub, kun nettleser):
1. Lag en gratis konto på github.com og opprett et nytt repository (New repository).
2. "Add file" > "Upload files": dra inn ALT innholdet i denne mappen, inkludert .github-mappen. Trykk Commit.
   (Om .github-mappen ikke følger med: "Add file" > "Create new file", skriv .github/workflows/build.yml som filnavn og lim inn innholdet fra filen.)
3. Gå til fanen "Actions". Bygget starter selv (ca. 3-5 min). Åpne den ferdige kjøringen.
4. Last ned "TvPortal-apk" under Artifacts (zip-fil med app-debug.apk i).
