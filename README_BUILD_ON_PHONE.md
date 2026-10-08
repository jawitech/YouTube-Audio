# AudioExtractAndroid

## GitHub Actions APK-Build

Dieses Projekt enthält einen Workflow zum Erstellen einer Android-APK ohne Android Studio.

### WICHTIG

Beim Hochladen nach GitHub müssen die **Dateien innerhalb dieser ZIP** hochgeladen werden.

Das Repository muss danach direkt diese Struktur haben:

    .github/workflows/build-apk.yml
    app/build.gradle.kts
    app/src/
    build.gradle.kts
    gradle.properties
    settings.gradle.kts

Die ZIP-Datei selbst darf NICHT einfach als Datei in das Repository hochgeladen werden.

Ebenso darf der komplette Projektinhalt nicht in einem zusätzlichen Unterordner liegen.

### Build starten

GitHub → Actions → Build Android APK → Run workflow.

Der Workflow:
1. prüft die Gradle-Projektdateien,
2. installiert Java 17,
3. installiert das Android SDK,
4. lädt Gradle 8.13 direkt herunter,
5. baut `app-debug.apk`,
6. stellt die APK als Artifact bereit.

### APK

Nach erfolgreichem Build:

Actions → den erfolgreichen Lauf → Artifacts →
`AudioExtractAndroid-debug-apk`
