## Installation

Eine gepackte[Veröffentlichung]
(https://github.com/systopia/de.systopia.eventcheckin/releases) herunterladen
und [wie jede andere CiviCRM-Erweiterung installieren]
(https://docs.civicrm.org/user/en/latest/introduction/extensions/#installing-extensions)
.

Um eine nicht als stabil gekennzeichnete Version zu installieren
(z.B. eine Alpha-Version, oder beim Auschecken eines bestimmten Commits),
muss `composer update` im Verzeichnis der Erweiterung ausgeführt werden, damit
die Abhängigkeiten installiert werden.

## Anforderungen

* PHP v7.0+
* CiviCRM 5.35

## API-Erweiterung

Die Erweiterung bietet zwei neue API-Aktionen:

* `EventCheckin.verify` empfängt und verifiziert das Token und gibt Daten sowie
  mögliche Teilnehmerstatus-Optionen zum Einchecken zurück
* `EventCheckin.confirm` empfängt und verifiziert (erneut) das Token und checkt
  den Teilnehmenden an