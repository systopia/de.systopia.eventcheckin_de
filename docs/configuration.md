## Grundlegende Konfiguration

Auf der Seite ``civicrm/admin/eventcheckin/settings`` sollten zumindest folgende
Einstellungen vorgenommen werden:

* Teilnehmerstatus, die für den Check-in in Frage kommen.
* Status, den Anmeldungen beim Einchecken erhalten können (pro Status wird ein
  Button erzeugt)
* Daten, die auf dem Checkin-Bildschirm angezeigt werden sollen

Anschließend sollte mindestens eine Nachrichtenvorlage angelegt werden, die den
Platzhalter für die QR-Codes oder Checkin-Links enthält (z.B.
`{$event_checkin_code_img}`). Dieser kann dann in automatisierten Event-E-Mails
oder beim manuellen Versand von E-Mails oder Erzeugen von Dokumenten genutzt
werden, z.B. um Veranstaltungstickets manuell zu erstellen.

Folgende Platzhalter werden von der Erweiterung bereitgestellt:

* `{$qr_event_checkin_code}` - erzeugt einen eindeutigen Check-in-Link
* `{$qr_event_checkin_code_img}` - erzeugt einen eindeutigen Check-in-Link,
  der als QR Code mit fester Größe ausgegeben wird
* `{$qr_event_checkin_code_data}` - erzeugt einen einmaligen Check-in-Link, der
  als QR-Code ausgegeben wird - die Darstellung kann mit Hilfe der
  Bild-Attribute angepasst werden

In der [Dokumentation der Erweiterung "Event Communication"](https://github.com/systopia/de.systopia.eventmessages) 
sind mehr Informationen über die Verwendung der Platzhalter und weiterer 
Funktionen zu finden.

## Berechtigungen

Um Teilnehmer einchecken zu können, ist die Berechtigung
"Check-In Event Participants" (``event checkin``) sowie die "Access CiviCRM"
-Berechtigungen erforderlich. Bspw. kann eine separate Rolle mit dem Namen
"Event Check-in Staff" erstellt werden, deren Benutzer dann nur
Veranstaltungsteilnehmer einchecken können aber keinen Zugriff auf andere
CiviCRM-Daten haben.

Wenn Sie mit Hilfe eines externen Systems über die API einen "Remote Check-in"
vornehmen möchten, muss der API-Benutzer über die Berechtigung "RemoteContacts:
Check-In Event Teilnehmer" (`remote event checkin`) verfügen. Weiterhin muss
der via `remote_contact_id` identifizierte Kontakt die CiviRemote-Rolle
"Remote Check-In User" haben.
