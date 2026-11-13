# **YOURLS** – Deutsche Übersetzung
*(**YOURLS** – german translation)*


## Version

YOURLS **1.8**

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

## Es liegt ein Fehler vor / Ich habe eine bessere Übersetzung anzubieten!

Idealerweise *forken* Sie dieses *Repository*, ändern die Datei und erstellen einen *Pull request*.

Prüfen Sie zunächst, ob das Problem bereits in den vorhandenen *Issues* beschrieben ist. Öffnen Sie andernfalls ein neues *Issue* und beschreiben Sie das Problem sowie Ihren Lösungsvorschlag möglichst genau.

## Credits

Die deutsche Übersetzung wird gepflegt von [@DJaeger](https://github.com/DJaeger).

Die Du-Variante wurde von [@DJaeger](https://github.com/DJaeger) zum DerSev-Fork hinzugefügt.

## Lizenz

Free to use. Sie können hiermit tun, was Sie wollen.
