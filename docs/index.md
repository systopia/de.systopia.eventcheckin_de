# Event-Checkin (de.systopia.eventcheckin)

## Fokus

Mit dieser CiviCRM-Erweiterung ist es möglich, Check-in-Links und QR-Codes für
Veranstaltungsteilnehmer zur Verfügung zu stellen. Diese können genutzt werden,
um Personen bei der Veranstaltung einzuchecken oder Teilnehmer die Möglichkeit
zu bieten, dies selbst zu tun.

Wenn ein Check-in-Link verwendet wird (z.B. durch Scannen eines QR-Codes),
erhalten Benutzer mit den entsprechenden Berechtigungen eine Maske mit
Informationen sowie der Möglichkeit zum Chek-in angezeigt. Beim Einchecken wird
der Status angepasst (z. B. auf "teilgenommen"). Die Erweiterung bietet auch
eine API, die es ermöglicht dies mit Hilfe externer Systeme zu tun.

## Funktionen

* Generierung von Check-in-Links und QR-Codes für Teilnehmer
* Formular, mit dem Benutzer mit entsprechenden Berechtigungen Teilnehmer bspw.
  durch Scannen des QR-Codes einzuchecken
* Möglichkeit die Links und/oder QR-Codes in CiviCRM in E-Mails und Dokumente
  einzufügen

## Abhängigkeiten

Die
Erweiterung ["Event Communication"](https://github.com/systopia/de.systopia.eventmessages)
wird benötigt, um die Links und QR-Codes in von CiviCRM generierte E-Mails
und/oder Dokumente einzubinden. Mit der Kombination der beiden Erweiterungen
können bspw. auch Eintrittskarten mit QR-Codes erstellt und automatisierte
Abläufe für den Versand per E-Mail eingerichtet werden, die auf der Rolle
und/oder dem Anmeldestatus der Teilnehmer basieren.

Die Erweiterung verwendet [Chillerlans QR-Code-Generator](https://github.com/chillerlan/php-qrcode), um QR-Codes zu erzeugen.
