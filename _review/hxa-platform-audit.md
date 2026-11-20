# HXA.io: Dokumentationsanalyse und Abgleich mit dem Demomandanten

Stand: 20.11.2026. Arbeitsdokument für die Redaktion; die Kundenartikel bleiben in der bestehenden englischen Sprache.

## Quellenlage und Bearbeitungsstand

Die Ausgangsanalyse beruht auf dem lokalen Repository. Anschließend wurde die vom Benutzer bereitgestellte angemeldete Edge-Sitzung auf [portal.hxa.io](https://portal.hxa.io) erfolgreich lesend geprüft. Ausgewählte Organisation: **NetTask GmbH**, UI-Sprache English. Eine konkrete Portalversion und die genaue Rolle des angemeldeten Kontos waren nicht verifiziert.

Die anonymisierten Ergebnisse liegen in [Portalbeobachtungen vom 20.11.2026](portal-observations-2026-11-20.md), Abschnitte P01–P18. Die Connector-Panels wurden in einer Nachprüfung nach ausdrücklicher Benutzerfreigabe geöffnet. Es wurden keine Benutzer, Gruppen, Kategorien, Artikel, Kalender oder Connectoren angelegt und keine gespeicherten Konfigurationen geändert. Formulare wurden ohne Speichern verlassen. Die vorherigen Zugriffsprobleme sind damit für diese Prüfung überwunden.

Die Tabellen unterscheiden nachgewiesene Lücken im Repository von Fragen, die erst im Portal oder durch den Produktverantwortlichen geklärt werden können. Eine Release Note belegt eine angekündigte Funktion, aber weder aktuelle Standardwerte noch die Verfügbarkeit im Demomandanten.

Dieses Dokument liegt unter `_review/`. Retype schließt Dateien und Ordner mit führendem Unterstrich standardmäßig vom Build aus, siehe [Retype: exclude](https://retype.com/configuration/project/#exclude). Der Bericht ist damit redaktionelles Arbeitsmaterial und kein Kundenartikel.

## Priorisierte Lücken: Ausgangsbefund

P1: Grundkonfiguration, Zugriffsrechte und Datenfluss. P2: Produktkonfiguration und Bedienung. P3: Ergänzende Begriffe und redaktionelle Konsistenz.

| ID | Priorität | Befund vor der Ergänzung | Prüfbedarf | Zielartikel |
| --- | --- | --- | --- | --- |
| HXA-01 | P1 | Microsoft 365 Initial Setup enthält nur „Coming soon...“. Die Connector-Übersicht beschreibt bereits Application- und Service-Konten. | Aktuelle Connector-Auswahl, genaue Bezeichnungen, Pflichtfelder, Anmeldeablauf, Abschlussanzeige und Kalenderauswahl. Tatsächlich erforderliche Microsoft-Berechtigungen separat belegen. | [Microsoft 365 Initial Setup](../setup/connector-setup/microsoft-365/initial-setup.md) |
| HXA-02 | P1 | Exchange Initial Setup enthält einen Platzhalter und einen Verweis auf lokale EWS-Verbindungen. | Portalbasierter Exchange-Connector: Felder, Authentifizierung, Verbindungstest und Status. Abgrenzung zum direkt am Display eingerichteten lokalen EWS-Modus. | [Exchange Initial Setup](../setup/connector-setup/microsoft-exchange/initial-setup.md) |
| HXA-03 | P1 | User Setup beschreibt den Import, aber keine Rollenmatrix, Benutzerbearbeitung oder Rechtevergabe. | Verfügbare Rollen und deren sichtbare Rechte; lokale und importierte Benutzer; Lizenzzuweisung. Tatsächliche Zugriffsbeschränkungen benötigen bei Bedarf einen Test mit passender Rolle. | [User Setup](../setup/user-setup.md), [Assign License](../license/assign-license.md) |
| HXA-04 | P1 | Getting Started behauptet pauschal, Microsoft-365-Daten würden nicht unabhängig gespeichert und es gebe keine Datenduplizierung. Der lokale EWS-Artikel unterscheidet mehrere Kommunikationswege. | Verbindungsmodus im Demo erfassen. Speicherung, Cache, Aufbewahrung und Datenfluss durch technische Produktunterlagen bestätigen; aus einer Portalansicht allein nicht ableiten. | [Getting Started](../getting-started.md), [Local EWS Connection](../setup/connector-setup/microsoft-exchange/local-ews-connection.md) |
| HXA-05 | P1 | Die Produktbeschreibung enthält umfangreiche Graph-Berechtigungstabellen; die Connector-Übersicht erwähnt Application Impersonation für Exchange Online. | Tatsächlichen Connector und dokumentierten Berechtigungsbedarf abgleichen. Exakte Scopes, Berechtigungstypen und aktuelle Microsoft-Vorgaben anhand offizieller Quellen prüfen. Keine zusätzlichen Rechte aus den bestehenden Tabellen ableiten. | [Room Booking Description](../appendix/product-descriptions/app-description-roombooking.md), [Connector Setup](../setup/connector-setup/connector-setup.md) |
| HXA-06 | P1 | Beim lokalen EWS-Add-on sind Mindestversion und genaue Konfigurationsschritte ausdrücklich als TODO markiert. | Add-on-Verfügbarkeit im Portal prüfen. Mindestversion und tatsächliche Menüs, Felder und Schritte am HXA Display separat bestätigen; das Portal allein reicht dafür nicht. | [Local EWS Connection](../setup/connector-setup/microsoft-exchange/local-ews-connection.md), [HXA System](../setup/device-setup/room-booking/hxa-system.md) |
| HXA-07 | P2 | Room Booking Resource Setup beschränkt sich auf Erstellen, Bearbeiten und Löschen. | Alle Konfigurationsabschnitte, Pflichtfelder, Lizenz-/Connector-/Kalenderzuordnung, Check-in/out, Buchungsgrenzen, NFC und Gerätezuordnung, soweit vorhanden. | [Room Booking Resource Setup](../setup/resource-setup/room-booking-setup/resource-setup.md) |
| HXA-08 | P2 | Quick Meeting Title Setup verweist auf „My Devices“, Background Image Setup auf Ressourcen. | Heutiger Einstellungsort und Geltungsbereich: Gerät, Ressource oder Organisation; verfügbare Branding-Felder und Uploadgrenzen. | [Quick Meeting Titles](../setup/resource-setup/room-booking-setup/quick-meeting-title-setup.md), [Background Images](../setup/resource-setup/room-booking-setup/background-image-setup.md) |
| HXA-09 | P2 | Room Service Setup enthält nur „Coming soon...“. Release Notes nennen Room Service als Add-on. | Falls im Demo verfügbar: Lizenzvoraussetzung, Aktivierung, Angebot/Kategorien, Zustellung und Statusanzeigen. Einen Bestellvorgang nur mit eigens freigegebenen Testdaten prüfen. | [Room Service Setup](../setup/room-service-setup.md), [Room Booking Release Notes](../Changelog/release-notes-roombooking.md) |
| HXA-10 | P2 | Room Board Setup beschreibt die Geräteregistrierung, aber kaum die Ressourcenkonfiguration. | Kalender-/Ressourcenauswahl, Anzeigeoptionen, Branding und Gerätezuordnung, soweit vorhanden. | [Room Board Setup](../setup/resource-setup/room-board-setup.md) |
| HXA-11 | P2 | Die Sparo-Dokumentation nennt Karten, Ressourcenverknüpfung und Notfallteams. Eine zusammenhängende administrative Einrichtung fehlt. | Vorhandene Menüs, Kartenformate, Verknüpfung zu Ressourcen, Sichtbarkeit und Konfiguration von Notfallteams. | [Sparo Usage](../usage/sparo-user-documentation.md), [Sparo Description](../appendix/product-descriptions/app-description-sparo.md); anschließend ggf. eigener Setup-Artikel |
| HXA-12 | P2 | Door Connect beschreibt Schaltflächen und Teams, aber Chat- und Call-Konfiguration nicht durchgängig. | Auswahl des Chat-/Call-Connectors, Zielauswahl, Nachrichten, Fotooptionen und vorhandene Geräteeinstellungen. Keine Benachrichtigungen auslösen und keine Türen ansteuern. | [Door Connect Setup](../setup/resource-setup/door-connect-for-microsoft-teams-setup.md), [Teams Initial Setup](../setup/connector-setup/microsoft-teams/initial-setup.md) |
| HXA-13 | P2 | Event Logs enthält allgemeine Fehlerkategorien, aber keine konkrete Navigation oder dokumentierte Feld-/Filterliste. | Menüpfad, Filter, Zeitangaben, Schweregrade, IDs und Detailansicht. Fehlercodes nur übernehmen, wenn tatsächlich angezeigt und ihre Bedeutung belegt ist. | [Event Logs](../maintenance/event-logs.md) |
| HXA-14 | P2 | Organization Settings beschreibt nur Kontoinhaber und Firmeninformationen; Lizenzartikel beschreiben das Zuweisungsmodell, aber kaum Zustände. | Sichtbare Organisationsfelder, Mandantenwechsel, Abonnements, Lizenzstatus und Add-ons. Geschäftsregeln und Preise durch zusätzliche Produktquellen bestätigen. | [Organization Settings](../setup/organization-settings.md), [Assign License](../license/assign-license.md) |
| HXA-15 | P2 | Automation und Environment Control sind beschrieben; Ereignisse, Abhängigkeiten und Feldgrenzen bleiben teilweise offen. | Verfügbare Modultypen, Ereignisse, Aktionen, Feldgrenzen und Ressourcenzuordnung. Keine Relais, Schlösser oder sonstigen Aktoren schalten. | [Triggers](../setup/automation-setup/triggers.md), [Environment Control](../setup/resource-setup/environment-control-resource-setup.md) |
| HXA-16 | P3 | Definitions enthält fünf „...“-Platzhalter: Teams team, Teams channel, Microsoft resources, equipment mailbox, workspace mailbox. | Microsoft-Begriffe aus offiziellen Microsoft-Unterlagen ergänzen; HXA-Begriffe mit den tatsächlich sichtbaren Ressourcentypen abgleichen. | [Definitions](../definitions.md) |
| HXA-17 | P3 | Die Room-Booking-Produktbeschreibung nennt Version 4.3 / 2025-10-20; die Release Notes enthalten spätere, teils plattformspezifische Versionen. | Bedeutung der Versionsangabe klären: Dokumentversion oder App-Version. Versionen je Plattform dokumentieren und weder Portal- noch Displayversion aus einer anderen Versionsnummer ableiten. | [Room Booking Description](../appendix/product-descriptions/app-description-roombooking.md), [Room Booking Release Notes](../Changelog/release-notes-roombooking.md) |

## Bereits umgesetzte Korrekturen

Diese Änderungen beruhen ausschließlich auf vorhandenen Repository-Dateien, nicht auf einer Portalprüfung:

- Getting Started: ungültige weiterführende Links durch vorhandene Zielartikel ersetzt; Lizenzzuweisung und lokale EWS-Verbindung verlinkt.
- Room Board: falschen Pfad zur Connector-Übersicht korrigiert.
- Connector-Übersicht: Einleitung mit der tatsächlich aufgeführten Liste in Einklang gebracht.
- Teams Initial Setup und Required Permissions: bestehende Dokumente direkt verlinkt; unverbundene Verweise auf separate Chat-/Call-Artikel durch den vorhandenen Door-Connect-Setup-Artikel ersetzt. Der Bedarf an detaillierten Chat-/Call-Anleitungen bleibt HXA-12.

## Ablauf für die Portalprüfung

1. Zugriff auf den Browser herstellen und den vom Benutzer benannten Demomandanten auswählen. Organisationsname, UI-Sprache, Datum und sichtbare Portalversion festhalten. Eine nicht sichtbare Versionsnummer bleibt „nicht angezeigt“.
2. Sichtbare Navigation erfassen und den Themen dieser Analyse zuordnen. Fehlende Menüs zunächst als „in diesem Mandanten/mit dieser Rolle nicht sichtbar“ markieren.
3. Vorhandene Demoobjekte und Formulare lesend prüfen. Konfigurationsformulare ohne Speichern verlassen. Keine Connectoren erstellen, Einwilligungen erteilen, Lizenzen kaufen, Testbuchungen erzeugen oder Automationen auslösen.
4. Je Thema Feldbeschreibungen, sichtbare Auswahlwerte und Abhängigkeiten erfassen. Ein gespeicherter Demowert ist kein belegter Produktstandard.
5. Technische Aussagen, die sich aus der UI nicht belegen lassen, gezielt mit Produktverantwortlichen bzw. offiziellen Microsoft-Quellen klären.
6. Belegte Informationen in die bestehenden englischen Artikel einarbeiten; neue Artikel nur für eigenständige Abläufe anlegen und aus dem passenden Einstieg verlinken.
7. Relative Links und Formatierung prüfen; nach Möglichkeit Retype bauen. Den Bearbeitungsstatus je Thema aktualisieren.

## Erfassung je Beobachtung

| Feld | Inhalt |
| --- | --- |
| Lücken-ID | Zum Beispiel HXA-07 |
| Quelle | Portalansicht, bestehender Artikel, Release Note oder bestätigte Produktauskunft |
| Prüfumgebung | Demomandant, Rolle, UI-Sprache, sichtbare Version, Prüfdatum |
| Navigation | Tatsächlich beobachteter Menüpfad und Abschnitt |
| Funktion/Feld | Exakte sichtbare Bezeichnung und Zweck |
| Eingabe | Pflichtfeld, Datentyp, Einheit, Auswahlwerte und sichtbare Grenzen |
| Abhängigkeiten | Sichtbare Voraussetzungen wie Lizenz, Connector, Ressourcentyp oder Rolle |
| Wertart | Gespeicherter Demowert, beobachteter leerer Formularwert oder separat bestätigter Standard |
| Ergebnis | Beobachtete Anzeige; erwartetes Verhalten nur mit benannter Quelle |
| Nachweis | Anonymisierter Ausschnitt oder präzise Textnotiz; keine Zugangsdaten, Tokens oder personenbezogenen Inhalte |
| Ziel und Status | Artikelpfad; offen / beobachtet / ergänzt / geprüft |

Eine Lücke gilt als geschlossen, wenn der Artikel Voraussetzungen, Ablauf, relevante Felder, Ergebnisprüfung und belegte Einschränkungen enthält und die Quelle nachvollziehbar ist. Eine ergänzte Feldbeschreibung ist kein ausgeführter Funktionstest.

## Bearbeitungsstand nach der Portalprüfung

| ID | Status | Ergänzung und verbleibender Prüfbedarf |
| --- | --- | --- |
| HXA-01 | Teilweise ergänzt | Microsoft-365-Einstieg und Kontotypauswahl geprüft: erster Connect-Klick öffnet Application Account / User/Service Account mit einem zweiten Connect-Button (P03/P15). Dokumentation präzisiert. Microsoft-Anmeldung, Consent, genaue Scopes und vollständiger Einrichtungstest bleiben offen. |
| HXA-02 | Teilweise ergänzt | Die leeren Initialformulare von Exchange und Exchange Sparo mit Mailbox Address, Password, Connect und Back geprüft (P16). Kein separates EWS-URL-Feld sichtbar. Authentifizierungsverfahren, Endpoint-Ermittlung, spätere Felder und Verbindungstest bleiben offen. |
| HXA-03 | Teilweise ergänzt | Users, Roles, Groups, Profilfelder, Lizenzzuordnung und Rollenbereiche dokumentiert (P08–P10). Admin ist im beobachteten Rollenmenü nicht bearbeitbar. Wirkungsprüfung unter anderen Rollen sowie Import/Synchronisation bleiben offen. |
| HXA-04 | Teilweise geklärt | Pauschale Aussagen zu Nicht-Speicherung/keiner Duplizierung aus Getting Started entfernt; Kalenderhosts und direkte EWS-Verbindung differenziert. Verbindliche Speicher-, Cache- und Aufbewahrungsregeln benötigen technische Produktquellen. |
| HXA-05 | Offen | Veraltete pauschale Application-Impersonation-Anforderung für den Microsoft-365-Service-Connector aus der Übersicht entfernt. Exakte Graph-Berechtigungstabellen in den Produktbeschreibungen sind weiterhin zu verifizieren; aus den UI-Ansichten wurde kein neuer Scope-Bedarf abgeleitet. |
| HXA-06 | Offen | Mindestversion und Menüs des lokalen EWS-Add-ons erfordern Prüfung am HXA Display bzw. Bestätigung des Produktverantwortlichen. |
| HXA-07 | Teilweise ergänzt | Ressourcendetails und alle sechs Advanced-settings-Register erfasst und dokumentiert (P05). Weitere bedingte Felder, NFC-Abläufe und operative Buchungs-/Anwesenheitstests bleiben offen. |
| HXA-08 | Teilweise ergänzt | Aktuellen Titelpfad korrigiert; Statushintergründe, Ressourcenbilder und Organisationslogo unterschieden (P02/P05). Bestehende Hintergrundempfehlung 1920x1080 / 1024 kB wurde erhalten, der Uploaddialog dafür aber nicht erneut geprüft. |
| HXA-09 | Teilweise ergänzt | Platzhalter durch Kategorie-, Artikel- und Ressourcenanleitung ersetzt (P05–P07). Preiswährung, bedingte Preisfelder, tatsächliche Geräteselektion und Bestellzustellung sind nicht getestet. |
| HXA-10 | Konfiguration ergänzt | Room Board um Lizenz/Connectoren, Zimmerauswahl, Felder, Anzeigeoptionen und Präsentationsinhalte erweitert (P04). Keine Speicherung oder Clientprüfung ausgeführt. |
| HXA-11 | Teilweise ergänzt | Eigener Floor-Plan-Artikel für Metadaten und Einstieg in Verknüpfungen angelegt (P12). Linkeditor meldet fehlenden Microsoft-Entra-ID-Connector; Upload-, Zeichen- und Verknüpfungsdetails sowie Sparo-spezifische Administration bleiben offen. |
| HXA-12 | Teilweise ergänzt | Teams-Auswahlpanel mit User/Service Account und Teams Calling Agent (User/Service Account) bestätigt (P18); Einstiegsnavigation und zwei Connect-Schritte dokumentiert. Microsoft-Anmeldung/Consent sowie Door-Connect-Zielauswahl und Chat-/Call-Konfiguration bleiben offen. |
| HXA-13 | Feldreferenz ergänzt | Navigation, sechs Tabellenspalten und Filter inklusive Datumswahl dokumentiert (P14). Zeitzone, Aufbewahrung und vollständiger Fehlercodekatalog sind offen. Bestehende generische Fehlertitel als Kategorien statt als exakte Meldungen eingeordnet. |
| HXA-14 | Teilweise ergänzt | Organisationsprofil um Branding, First Aid und differenzierte Primary-Contact-Angaben erweitert (P02/P08). Menüaktion zur Kontaktübertragung sichtbar, nicht ausgeführt. Subscriptions, Lizenzzustände, Vertragsregeln und Preise bleiben offen. |
| HXA-15 | Offen | Automation und Aktoren wurden nicht bedient. Detailprüfung von Modultypen, Ereignissen, Feldgrenzen und Zuordnungen steht aus. |
| HXA-16 | Ergänzt und quellengeprüft | Alle fünf Microsoft-Platzhalter durch kurze Definitionen mit offiziellen Microsoft-Quellen ersetzt; HXA.io Local Connector und Kalenderbegriff ergänzt. |
| HXA-17 | Offen | Geräte melden in einer Room-Booking-Ressource App-Version 5.5.0 (P05). Bedeutung der Produktbeschreibungs-Version 4.3 bleibt zu klären; nicht automatisch durch die Geräteversion ersetzt. |

## Zusätzlich dokumentierte Bereiche

- [Portal Navigation](../setup/portal-navigation.md): aktuelle Bereiche und Einstiegswege.
- [Role Setup](../setup/role-setup.md): Rollenbereiche und getrennte User-Berechtigungen.
- [Calendar Setup](../setup/calendar-setup.md): Kalenderübersicht, Hosts und Ressourcenzuordnung. Im Anlageformular war die Auswahl des lokalen Connectors nicht sichtbar bestätigt; daraus wurde keine erfolgreiche Kalenderanlage abgeleitet.
- [Floor Plan Setup](../setup/floor-plan-setup.md): Metadaten und Entra-ID-Voraussetzung des Linkeditors.
- [Device Monitoring](../maintenance/device-monitoring.md): Versions-, Plattform-, Status- und Last-online-Felder.
- [Microsoft Entra ID Initial Setup](../setup/connector-setup/microsoft-entra-id/initial-setup.md): eigener Einstieg mit bestätigtem Application-Account-Panel und Verweisen zu Benutzerimport und Floor Plans (P17).

## Nächste fachliche Klärungen

1. Microsoft-365-/Exchange-Authentifizierungsabläufe und die tatsächlich erforderlichen Scopes mit einem freigegebenen Setup oder verbindlichen Produktunterlagen prüfen. Die frühere Ablehnung des ersten Connect-Klicks wurde durch ausdrückliche Benutzerfreigabe und Nachprüfung der Panels überholt; Anmeldung und Verbindungsabschluss wurden dabei nicht ausgeführt.
2. Für den Floor-Plan-Linkeditor eine bereits mit Entra ID verbundene Demo bereitstellen; dadurch werden keine neuen Berechtigungen allein für die Dokumentationsarbeit eingerichtet.
3. Kalenderanlage und weitere bedingte Formulare prüfen, ohne die beobachtete erfolglose Auswahl als Produktstandard oder allgemeine Fehlfunktion zu verallgemeinern.
4. Lokales EWS-Add-on am Display prüfen: Mindestversion, Aktivierung, Felder, Screenshots und Kalenderprüfung.
5. Datenfluss-/Speicherregeln und Dokument-/App-Versionen durch den Produktverantwortlichen bestätigen; anschließend gezielt Clienttests, Door Connect und Automation ergänzen.

## Technische Prüfung der Ergänzungen

- 24 Kundenartikel ergänzt oder aktualisiert, davon sechs neu; zusätzlich llms.txt aktualisiert. Zwei YAML-Navigationsdateien hatten unzulässige Dokumentbegrenzer, die entfernt wurden; zwei weitere alte Connector-Links in Android/iOS-Anleitungen wurden korrigiert.
- Retype 4.6.0 temporär über das offizielle Paket retypeapp-win-x64 verwendet: nach der Connector-Nachprüfung 64 Seiten gebaut, 0 Fehler, 0 Warnungen. Ausgabe ausschließlich im Temp-Verzeichnis, keine Veröffentlichung. Die neue Entra-ID-Seite ist im Build enthalten.
- 143 lokale Markdown-/Bildverweise und vorhandene Sprungmarken geprüft: keine fehlenden Ziele oder unaufgelösten Überschriftenanker.
- Alle in llms.txt verlinkten Dokumentationsrouten existieren im generierten Build.
- Geprüft, dass `_review/` nicht im generierten Build enthalten ist.
- Die ergänzten Kundenartikel enthalten keine übernommenen Demo-Lizenzschlüssel, Kundennummern oder persönlichen Benutzer-/Mailboxkennungen.
- git diff --check ohne Befund. Keine Commits und kein Push ausgeführt.
- Diese Prüfungen bestätigen die Dokumentationsstruktur und den Build. Konfigurationen, Berechtigungen, Buchungen, Aufträge und Gerätefunktionen wurden nicht operativ getestet.
