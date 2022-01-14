# Event-Checkin (de.systopia.eventcheckin)

## Fokus

Mit dieser CiviCRM-Erweiterung ist es möglich, Check-in-Links und QR-Codes für
Veranstaltungsteilnehmer*innen zur Verfügung zu stellen. Diese können genutzt
werden um Personen bei der Veranstaltung einzuchecken oder Teilnehmer*innen
die Möglichkeit zu bieten dies selbst zu tun. 

Wenn ein Check-in-Link verwendet wird (z.B. durch Scannen eines QR-Codes),
erhalten Benutzer*innen mit mit den entsprechenden Berechtigungen eine Maske
mit Informationen sowie der Möglichkeit zum Chek-in angezeigt. Beim
Einchecken wird der Status angepasst (z. B. auf "teilgenommen"). Die
Erweiterung bietet auch eine API, die es ermöglicht dies mit Hilfe externer
Systeme zu tun.

## Funktionen

* Generierung von Check-in-Links und QR-Codes für Teilnehmende
* Formular mit dem Benutzer*innen mit entsprechenden Berechtigungen
  Teilnehmer*innen bspw. durch Scannen des QR-Codes einzuchecken
* Möglichkeit die Links und/oder QR-Codes in CiviCRM in E-Mails und Dokumente
  einzufügen

## Abhängigkeiten

Die Erweiterung "event messages" (de.systopia.eventmessages) wird benötigt, um
die Links und QR-Codes in von CiviCRM generierte E-Mails und/oder Dokumente
einzubinden. Mit der Kombination der beiden Erweiterungen kann man bspw. auch
Eintrittskarten mit QR-Codes erstellen und automatisierte Workflows
für den Versand per E-Mail einrichten, die auf der Rolle und/oder dem
Anmeldestatus der Teilnehmenden basieren.

Die Erweiterung verwendet[Chillerlans QR-Code-Generator]
(https://github.com/chillerlan/php-qrcode), um QR-Codes zu erzeugen.