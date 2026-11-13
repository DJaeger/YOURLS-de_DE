# **YOURLS** – Deutsche Übersetzung
*(**YOURLS** – german translation)*


## Versionsstand

- Übersetzungs-Release: **1.8.0**
- Zielversion von YOURLS: **1.8**
- POT-Basis: `YOURLS.pot` **1.8**, erstellt am 2021-02-22.

## Installation

1. Laden Sie das aktuelle Repository als ZIP herunter: Wählen Sie auf GitHub **Code > Download ZIP**.
2. Kopieren Sie das gewünschte Dateipaar aus dem Archiv in das Verzeichnis `user/languages`:
	- Formelle Ansprache: `de_DE.po` und `de_DE.mo`
	- Du-Ansprache: `de_DE_x_du.po` und `de_DE_x_du.mo`
3. Tragen Sie in Ihrer `config.php` den zum kopierten Dateipaar passenden Wert ein:

	**Formelle Ansprache**
	```php
	define( 'YOURLS_LANG', 'de_DE' );
	```

	**Du-Ansprache**
	```php
	define( 'YOURLS_LANG', 'de_DE_x_du' );
	```

Das `x` leitet den Private-Use-Zusatz `du` nach BCP 47 ein. So ergibt sich im HTML das gültige Sprachkennzeichen `de-DE-x-du`; außerdem muss `YOURLS_LANG` exakt dem Namen der `.mo`-Datei ohne Endung entsprechen.

### Alternative: Download unter Linux

Statt des ZIP-Downloads können Sie das gewünschte Dateipaar mit Bash direkt in das Sprachverzeichnis herunterladen. Passen Sie den Pfad an Ihre YOURLS-Installation an und setzen Sie anschließend `YOURLS_LANG` wie oben beschrieben.

**Formelle Ansprache**
```bash
wget -P /var/www/YOURLS/user/languages/ https://raw.githubusercontent.com/DJaeger/YOURLS-de_DE/main/de_DE.{po,mo}
```

**Du-Ansprache**
```bash
wget -P /var/www/YOURLS/user/languages/ https://raw.githubusercontent.com/DJaeger/YOURLS-de_DE/main/de_DE_x_du.{po,mo}
```

Falls die Dateien bereits existieren, legt `wget` standardmäßig zusätzliche Dateien mit Endungen wie `.1` an, statt die vorhandenen zu ersetzen.

## Es liegt ein Fehler vor / Ich habe eine bessere Übersetzung anzubieten!

Idealerweise *forken* Sie dieses *Repository*, ändern die Datei und erstellen einen *Pull request*.

Prüfen Sie zunächst, ob das Problem bereits in den vorhandenen *Issues* beschrieben ist. Öffnen Sie andernfalls ein neues *Issue* und beschreiben Sie das Problem sowie Ihren Lösungsvorschlag möglichst genau.

Nach einem Push mit Änderungen an PO-Dateien erstellt der GitHub-Actions-Workflow die zugehörigen MO-Dateien und committet sie auf denselben Branch. Unter **Actions > Compile translations > Run workflow** lässt sich die Kompilierung aller PO-Dateien auch manuell starten, um fehlende MO-Dateien zu erzeugen. GitHub Actions muss dafür aktiviert sein und Schreibzugriff auf den Branch haben.

## Credits

Die deutsche Übersetzung wird gepflegt von [@DJaeger](https://github.com/DJaeger).

Die Du-Variante wurde von [@DJaeger](https://github.com/DJaeger) zum DerSev-Fork hinzugefügt.

## Lizenz

Dieses Repository steht unter der [MIT-Lizenz](LICENSE).
