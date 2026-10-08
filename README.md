# Audio Extractor – Android

Kleine Kotlin/Jetpack-Compose-App zur Audioextraktion aus vom Nutzer bereitgestellten Medien. Die erzeugte MP3 wird automatisch über MediaStore im öffentlichen Android-Ordner `Download/` abgelegt – ohne „Speichern unter“-Dialog.

## Voraussetzungen

- Android Studio
- JDK 17
- Android SDK 36
- Gradle 8.13+

## Build

Projekt in Android Studio öffnen und `app` als Run-Konfiguration starten. Beim ersten Build wird die FFmpegX-Android-Abhängigkeit über JitPack bezogen.

## Technischer Aufbau

- Kotlin + Jetpack Compose
- FFmpegX-Android 2.2.1 für Audio-/MP3-Transkodierung
- Android MediaStore für `Download/`
- Kein manueller Speicherpfad nötig

## Rechtlicher/technischer Hinweis

Die App enthält absichtlich keine YouTube-Scraping- oder DRM-/Schutzumgehungslogik. Für Inhalte, die du selbst besitzt, bereitstellen darfst oder deren Download vom jeweiligen Dienst ausdrücklich erlaubt wird, kann die lokale Audioextraktion genutzt werden.

Die FFmpegX-Abhängigkeit enthält laut Projektangaben FFmpeg/LAME unter GPL-Komponenten. Vor einer Veröffentlichung solltest du die Lizenzbedingungen und die konkrete Distribution der nativen Bibliotheken prüfen.
