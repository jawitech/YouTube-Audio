# Audio Extractor – Build-Anleitung

## Voraussetzungen

- Android Studio (aktuelle stabile Version)
- Android SDK Platform 36
- JDK 17 (Android Studio bringt normalerweise ein passendes JDK mit)
- Internetzugang für Gradle-Plugins und die FFmpegX-Android-Abhängigkeit

## Android Studio

1. Diesen Ordner in Android Studio öffnen.
2. Warten, bis Gradle Sync abgeschlossen ist.
3. Falls Android Studio nach einem JDK fragt: das eingebettete JDK bzw. JDK 17 auswählen.
4. **Build → Generate App Bundles or APKs → Generate APKs** wählen.
5. Die APK befindet sich danach unter:

   `app/build/outputs/apk/debug/app-debug.apk`

Für eine Release-APK:

**Build → Generate Signed App Bundle / APK → APK**

## Kommandozeile

Das Projekt benötigt Gradle 8.13+ und Android SDK 36. Die Abhängigkeit
`com.github.mzgs:FFmpegX-Android:v2.2.1` wird über JitPack bezogen.

Beispiel mit einer lokal installierten Gradle-Version:

```text
gradle assembleDebug
```

oder:

```text
gradle assembleRelease
```

## Hinweis zur FFmpeg-Bibliothek

FFmpegX-Android stellt die nativen FFmpeg-Bibliotheken beim Build bereit. Beim
allerersten Build ist deshalb eine Internetverbindung erforderlich.

Die Bibliothek verwendet GPL-Komponenten (unter anderem LAME/x264). Vor einer
Weitergabe oder Veröffentlichung der APK die Lizenzbedingungen prüfen.
