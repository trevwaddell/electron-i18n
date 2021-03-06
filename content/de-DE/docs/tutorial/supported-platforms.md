# Unterstützte Plattformen

Die folgenden Plattformen werden durch Electron unterstützt:

### macOS

Für macOS werden ausschließlich 64bit-Dateien zum Download angeboten. Sie benötigen mindestens macOS 10.9.

### Windows

Windows 7 und neuere Versionen werden unterstützt. Ältere Betriebssysteme werden nicht unterstützt (und funktionieren nicht zusammen mit Electron).

Sowohl `ia32` (`x86`) als auch `x64` (`amd64`)-Dateien werden zum Download angeboten. Die `ARM` Version von Windows wird aktuell nicht unterstützt.

### Linux

Die vorkompilierten `ia32` (`i686`) und `x64` (`amd64`) Dateien von Electron wurden unter Ubuntu 12.04 erstellt, die `arm` Datei wurde auf ARM v7 mit hard-float ABI und NEON für Debian Wheezy kompiliert.

Ob die vorkompilierten Dateien auf einer Distribution laufen, hängt davon ab, ob die Distribution die Bibliotheken enthält, die auf der Build-Plattform verwendet wurden. Deshalb ist nur für Ubuntu 12.04 garantiert, dass es funktioniert, aber die folgenden Plattformen wurden ebenfalls bestätigt, kompatibel mit den vorkompilierten Dateien zu sein:

* Ubuntu 12.04 und neuer
* Fedora 21
* Debian 8