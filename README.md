# **YOURLS** – Deutsche Übersetzung
*(**YOURLS** – german translation)*


## Versionsstand

- Übersetzungs-Release: **1.9.0**
- Zielversion von YOURLS: **1.9**
- POT-Basis: `YOURLS.pot` **1.9**, erstellt am 2022-04-22.

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

## Mitwirken

### Übersetzung beitragen

Forken Sie dieses Repository, nehmen Sie Ihre Änderungen vor und erstellen Sie einen Pull Request.

### Fehler melden

Prüfen Sie zunächst, ob das Problem bereits in den vorhandenen [Issues](https://github.com/DJaeger/YOURLS-de_DE/issues) beschrieben ist. Falls nicht, [eröffnen Sie ein neues Issue](https://github.com/DJaeger/YOURLS-de_DE/issues/new) und beschreiben Sie Problem und Lösungsvorschlag möglichst genau.

### PO-Dateien

Die Kataloge werden anhand der im Versionsstand genannten offiziellen YOURLS-POT gepflegt. Eine eigene POT-Erzeugung aus dem YOURLS-Quellcode ist nicht Teil dieses Repositories.

Der Validate-PO-Workflow prüft PO-Dateien bei Pull Requests, Pushes und auf manuelle Anforderung mit gettext auf Syntax und Format-Platzhalter.

### MO-Dateien

Der Validate-MO-Workflow prüft direkt geänderte MO-Dateien in Pull Requests und Pushes auf Lesbarkeit; er kann auch manuell gestartet werden. Der Compile-MO-Workflow prüft jedes neu erzeugte MO direkt nach der Kompilierung und vor dem Commit mit `msgunfmt`.

Der Compile-MO-Workflow wird durch PO-Pushes ausgelöst, auch auf PR-Branches; ein Merge und direkte PO-Änderungen über die GitHub-Webseite erzeugen ebenfalls einen Push. Er kompiliert die MO-Dateien und committet sie auf denselben Branch. Die Kompilierung aller PO-Dateien lässt sich außerdem unter **Actions > Compile MO catalogs > Run workflow** manuell starten, um fehlende MO-Dateien zu erzeugen.

### Releases

Ein per Git gepushter Tag im Format `vMAJOR.MINOR.PATCH` erstellt automatisch ein GitHub-Release. Wenn Sie eine Release im GitHub-Webinterface veröffentlichen, ergänzt der Release-Workflow die Notizen der bereits angelegten Release. Die Notizen listen die Commit-Nachrichten seit dem vorherigen Versionstag auf. Alternativ können Sie unter **Actions > Release > Run workflow** einen Tag eingeben. Falls der Tag noch nicht existiert, legt ihn der Workflow am im Dialog ausgewählten Branch oder Commit an und erstellt die Release samt Notizen.

## Credits

Die deutsche Übersetzung wird gepflegt von [@DJaeger](https://github.com/DJaeger).

Dieser Fork basiert auf der Arbeit von [DerSev](https://github.com/DerSev) mit korrigierten Trennzeichen von [agru](https://github.com/agru).\
Die Du-Variante wurde von [@DJaeger](https://github.com/DJaeger) hinzugefügt.

## Lizenz

Dieses Repository steht unter der [MIT-Lizenz](LICENSE).
