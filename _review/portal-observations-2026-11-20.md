# Portalbeobachtungen vom 20.11.2026

Quelle: angemeldetes HXA.io-Portal in der vom Benutzer bereitgestellten Edge-Sitzung; Organisation „NetTask GmbH“, UI-Sprache English. Der Benutzer hat die Fortsetzung mit dieser geöffneten Sitzung bestätigt. Eine konkrete Benutzerrolle und Portalversion wurden bislang nicht verifiziert. Der Footer weist auf BETA-Status hin.

Erfassungsmethode: lesender Zugriff über die Benutzeroberfläche. Keine gespeicherten Konfigurationswerte wurden geändert. Personenbezogene Daten, Lizenzschlüssel und Objekt-IDs sind hier nicht übernommen. Sichtbare gespeicherte Werte gelten nicht als Produktstandard. Aussagen über die tatsächliche Wirkung einer Einstellung sind nur soweit belegt wie ausdrücklich beschrieben.

## P01 – Navigation

Sichtbar: Home; Account mit Organization Profile, Payment methods, Subscriptions, Users, Roles, Groups, Invoices, Reset password; Connectors; Calendars; Resources; Automation; Floor Plans; Room service mit Category und Item; Insights; News stream; Devices; Licenses; Shop; Knowledge base; Settings mit Event log.

Automation verweist auf `https://automation.portal.hxa.io/`. Die übrigen hier geprüften Ansichten liegen unter `https://portal.hxa.io/`.

## P02 – Organisationsprofil

Route: `#/account/organizationprofile`, Menü Account > Organization Profile.

- Primary Contact (Owner): First name, Last name, Email, Language. Die ersten drei Felder sind in der beobachteten Ansicht nicht editierbar.
- Company information: Company name, Street, Zipcode, State, Floor, Building etc., City, Country, Phone, Fax; Save and Update; Delete organization.
- Branding settings: Bild-Upload per Klick oder Drag-and-drop; Hinweis „Images must not exceed 1MB“; Logo-Seitenverhältnis „2:3 (W:H)“.
- Emergency and safety settings: First Aid, Schalter Enable für First Aid helpers, Select a group, separater Save-and-Update-Button.

Es wurde weder gespeichert noch eine Notfallfunktion eingeschaltet. Die historische Aussage zum Eigentümerwechsel stammt weiterhin aus dem bestehenden Artikel, nicht aus einem geprüften Änderungsprozess.

## P03 – Connectoren

Route: `#/connector`, Menü Connectors. Create connector führt auf `#/connector/add-connector`.

Übersicht: Search, Filter, Columns option; Spalten Options, Connector ID, Type, Application, Registered from, Status, Created, Service URL. Bei aktiven Einträgen ist der Status „Active“ als zugängliche Beschreibung vorhanden.

Auf der Auswahlseite stehen:

- HXA.io Local Connector: Text erklärt, dass er automatisch für die Organisation angelegt wird und HXA als Kalenderhost mit eigenen Kalenderressourcen verwendet werden kann; in dieser Sitzung „Connected“.
- Microsoft Exchange.
- Microsoft Exchange Sparo.
- Microsoft Office 365 Resources: Beschreibung nennt Microsoft Graph, Raum-/Equipment-Postfächer, Room Booking und Room Board.
- Microsoft Entra ID (Microsoft 365 Azure Active Directory): Beschreibung nennt Sparo-Zugriff.
- Office 365 - Teams.

Beim ersten Durchlauf wurde die Microsoft-365-Connect-Aktion von der automatischen Freigabeprüfung vor Ausführung abgelehnt. Nach ausdrücklicher Benutzerfreigabe wurden die ersten Panels in P15–P18 geprüft. Microsoft-Anmeldung, konkrete Berechtigungen und ein erfolgreicher Verbindungsabschluss sind weiterhin nicht verifiziert. Der HXA.io Local Connector ist nicht mit dem lokalen EWS-Zugriff eines HXA Displays gleichzusetzen.

## P04 – Room Board

Quelle: Resources > Options > Edit Resource einer vorhandenen Demo-Room-Board-Ressource. Es wurde nur das Formular geöffnet.

- Allgemeine Angaben: Display name, Sprache, Street, Post Code, Country, City, State, Building, Floor, Floorlabel; Save and Update.
- Ressourcenbild: empfohlen 800x800 Pixel; erlaubte Typen jpeg, jpg, png; Choose File, Upload, Load standard picture.
- Licensing; Licensing - Add-ons mit Select add-on Licenses.
- Connector mit Haupt- und Optional Connector; sichtbare Disconnect-Aktionen nicht ausgeführt.
- Application/ Devices: Add; Tabelle mit Serial No., Device ID, Register date, Online, App-Version, Platform, Last online und Options.
- Rooms to be displayed: Load; Spalten Display, Room Name, Building, Calendar und Direction-Auswahl; Save.
- Advanced settings: Switching time between the pages (in seconds), Enable floor plan, Display weather forecast, Add location.
- Table View Configuration: Room Name, Organizer, Subject, Start, End, Direction, Floor Plan; Save and Update.
- Advertising and information presentation: drei sichtbare Plätze für image, Web URL oder video; Bilder maximal 1 MB. Ein Versionshinweis in diesem Abschnitt nennt 1.5.0.
- Zusätzlich wird in Advanced settings ein Hinweis auf ein Gerät mit fehlender Funktionsunterstützung und Mindest-App-Version 1.7.0 angezeigt. Die genaue Zuordnung dieses Hinweises zu einer einzelnen Funktion wurde noch nicht visuell geprüft.

Nicht geprüft: Speichern, Load, Geräteverknüpfung, Auswahländerungen und Darstellung auf einem Room-Board-Endgerät.

## P05 – Room Booking

Quelle: Resources > Options > Edit Resource einer vorhandenen Room-Booking-Ressource mit PREMIUMDEMO-Lizenz. Es wurde nur gelesen und zwischen Registern gewechselt.

- Allgemein: Display name, Category, Sprache; Kalender-Metadaten Street, Post Code, Country, City, State, Building, Capacity, Window Orientation, Floor, Floorlabel. In dieser verbundenen Ressource sind die Postfach-Metadaten größtenteils nicht editierbar.
- Connector und Calendar: jeweils vorhandene Zuordnung; Disconnect nicht ausgeführt.
- Application/ Devices: Connect; Interactive Displays mit Serial No., Device ID, Register date, Online, App-Version, Platform, Last online, Options. Die App-Version der hier verbundenen Geräte ist 5.5.0; daraus folgt keine Mindestversion für einzelne Funktionen.
- Resource images: bis zu drei Bilder, jeweils maximal 1 MB.
- Branding settings > Device background image: Status Available, Pending, Busy; getrennte Bilder. Gimmicks > Christmas Mode mit From-/to-Zeitraum.
- Resource QR Code mit Download QR Code.
- Separates Ressourcenbild: empfohlen 800x800 Pixel; jpeg, jpg, png; Choose File, Upload, Load mailbox profile picture, Load standard picture.
- Licensing und Licensing - Add-ons: zugewiesene Lizenzen mit Ablaufdatum.

Advanced settings enthält sechs Register:

| Register | Beobachtete Felder |
| --- | --- |
| Dashboard settings | Select Design; Select colorset; Enable Screen Saver; Select clock type; Display screensaver after (Seconds); Display weather forecast; Add location; Enable floor plan |
| Energy & Power management | Enable energy saving mode for HXA Devices. In der beobachteten ausgeschalteten Konfiguration sind keine weiteren Felder sichtbar. |
| Booking & interaction | Enable quick booking; Allow attendees; Maximum duration als Slider; angezeigte Endpunkte 2 h und 12 h. Keine Änderung und keine Grenzwertvalidierung vorgenommen. |
| Events display options | Display period of planned events (days in future); Maximum planned events to be displayed (in the future); Name of directly booked events on the display; Name of scheduled events on the display |
| Custom titles & event meta data | Activate additional titles; Additional names for events; Add; Liste vorhandener Titel mit Reihenfolge-/Entfernen-Steuerelementen; Allow custom title |
| Automation & attendance | Activate check-in / check-out for events; Activate early check-in to events; Show check-in Button before event starts; Cancel events automatically; Automatically cancel after; Activate only check-out for events; Activate extend event functionality; Geräteauswahl für Extend mit Manage Devices; Checkout Authentication |

Für Advanced settings gibt es einen Save-and-Update-Button. Nicht geprüft: einzelne Auswahlmenüs, gegenseitige Abhängigkeiten aller Schalter, Speichern und Wirkung auf den Clients.

Add-On Licenses enthält die Register Room Service, Timer und Room Temperature. Das geladene Room-Service-Register zeigt Geräteauswahl mit Manage Devices, E-mail recipient for orders, E-mail copy recipient for orders, eine Artikeltabelle mit Activate, Item Name, Item category, Item price sowie Save and Update. Es wurde keine Bestellung ausgelöst.

## P06 – Room-Service-Kategorien

Route: `#/room-service/categories`, Menü Room service > Category. Übersicht: Add category; Spalten Options, Category name, Sorting.

Das leere Add-category-Formular enthält die Pflichtfelder Name und Sorting. Save ist bei leerem Formular deaktiviert. Das Formular wurde ohne Eingaben über das X geschlossen; es wurde keine Kategorie erstellt.

## P07 – Room-Service-Artikel

Route: `#/room-service/items`, Menü Room service > Item. Übersicht: Add item; Delete selected items; Spalten Options, Item Name, Category, Price, Symbol, Sorting.

Das leere Add-item-Formular enthält Item, Category, Symbol, Sorting in the category und Show price. Save ist bei leerem Formular deaktiviert. In diesem Zustand ist kein Preiseingabefeld sichtbar; Show price wurde nicht umgeschaltet. Das Formular wurde ohne Eingaben über das X geschlossen. Preiswährung, Preisgrenzen und der Versand einer Bestellung sind nicht verifiziert.

## P08 – Benutzer

Route: `#/account/user`, Menü Account > Users. Separate Menüpunkte Roles und Groups.

- Create user öffnet eine Auswahl mit Create user und Import Azure AD User; keine der beiden Aktionen wurde ausgeführt.
- Sync all users und Sync selected users; Search, Filter, Columns option. Keine Synchronisation ausgeführt.
- Spalten: First name, Last name, Email, Entra object ID, Transponder-ID [BETA], Role, Entra ID, License Number, Status, Last login To Portal.
- Zeilenmenü: Edit user, Reset password, Delete User, Set as a Primary contact. Nur Edit user geöffnet.
- Edit user: BASIC INFO mit First name, Last name, Department; CONTACT mit Email, Mobile Phone, Business Phone; PREFERENCES & ACCESS mit Language, PIN (Hinweis 8–16 Ziffern); VEHICLE & IDENTIFICATION mit Vehicle Registration Plate, Transponder-ID [BETA]; PERMISSIONS mit Rollen- und Lizenz-Auswahl; Save and Update.
- Im untersuchten Profil waren E-Mail und Telefonfelder nicht editierbar. Keine allgemeine Aussage über andere Benutzertypen daraus abgeleitet.

Das sichtbare „Set as a Primary contact“ widerspricht zumindest der pauschalen bisherigen Dokumentationsaussage, ein Eigentümerwechsel sei ausschließlich durch Support möglich. Die Aktion wurde nicht ausgeführt; ihre Berechtigungsvoraussetzungen und ihre rechtliche/technische Wirkung sind offen. Die Dokumentation soll die sichtbare Option benennen, aber daraus keine uneingeschränkte Übertragbarkeit ableiten.

## P09 – Rollen

Route: `#/account/Roles`, Menü Account > Roles. Role management mit Create role, Search, Tabelle Name/Options. Admin und zwei weitere Rollen sind vorhanden; daraus werden keine allgemeinen Standardrollen abgeleitet. Bei Admin sind Edit role und Delete role deaktiviert.

Bei einer anderen vorhandenen Rolle führt Edit role zu User Role Permissions. Portal Permissions enthält aufklappbare Bereiche:

- User permissions; Group permissions; Role permissions; Device Permissions; Connector Permissions.
- Invoice permissions; License Permissions; Organization Profile Permissions; Payment Method Permissions.
- Resource Permissions; Subscription permissions; Room Demands Permissions; News Stream Permissions.
- Trigger Permissions; Floor Plan permissions; Automation Portal Permissions; Control Module Permissions; MQTT Permissions.
- `permissions.Calendars.TITLE` (sichtbarer, offenbar nicht übersetzter UI-Schlüssel).

Es gibt Save. Kein Berechtigungsschalter wurde geändert und Save nicht betätigt. Eine Berechtigungswirkung wurde nicht durch Anmeldung unter einer anderen Rolle getestet.

Im aufgeklappten Bereich User permissions sind die vier Kontrollkästchen Show users, Create users, Edit users und Delete users sichtbar. Die Rechte der vorhandenen Rolle sind keine allgemeine Vorlage für andere Organisationen.

## P10 – Gruppen

Route: `#/account/groups`, Menü Account > Groups. Group Management mit Search, Filter, Columns option; Spalten Options, ID, Name, Type, Entra ID. Create Group öffnet die Auswahl Create Group / Import Azure AD Group. Keine Gruppe erstellt oder importiert und keine Mitglieder geändert.

## P11 – Kalender

Route: `#/calendars`, Menü Calendars. Übersicht: Create calendar; Search, Filter, Columns option; Spalten Options, Display name, UPN, Resource, Connector Type - user. Ein vorhandener Kalender ist mit einer Ressource verknüpft.

Create calendar öffnet ein Formular mit Pflichtauswahl Select Connector und zunächst deaktiviertem Save. Die Auswahl enthält vorhandene Application-/Service-Connectoren und HXA.io Local Connector. Ein Klick auf den lokalen Eintrag führte in dieser Prüfung zu keiner sichtbar bestätigten Auswahl; es erschienen keine weiteren Felder. Das Formular wurde ohne Speichern geschlossen. Die weiteren Schritte der Kalenderanlage sind deshalb weiterhin offen. Keine fehlerfreie Anlage behaupten.

## P12 – Floor Plans

Route: `#/maps`, Menü Floor Plans. Create new floor plan; Search, Filter, Columns option; Übersichtsspalten ID, Display Name, Floor label, Country, City, Street and building number, Floor, Date of last change.

Zeilenmenü: Edit floor plan, Edit floor plan links, Delete floor plan. Edit floor plan öffnet Metadaten: Display Name, Floor label, Country, City, Street and Building Number, Floor; Save floor plan und Back. Keine Metadaten geändert.

Edit floor plan links führte zu „Error! Please add a Microsoft Entra ID Connector.“ mit Add Connector. Der Hinweis wurde über X geschlossen; kein Connector angelegt. Damit ist die Entra-ID-Abhängigkeit dieses Schritts in der Sitzung belegt, der eigentliche Karten-/Verknüpfungseditor jedoch nicht geprüft.

## P13 – Geräteübersicht

Route: `#/devices`, Menü Devices. Devices | Overview, Manage your devices; Search, Filter, Columns option. Spalten Options, Name, Serial No., Device ID, Register date, Status, App-Version, Platform, Last online. Keine Geräteaktionen ausgeführt.

## P14 – Ereignisprotokoll

Route: `#/settings/logs`, Menü Settings > Event log. Event log | Overview, Event display for error analysis; Search, Filter, Columns option. Spalten ID, Method, Path, Connector ID, Status, Date. Knowledge-base-Verweis unter der Tabelle.

Filter enthält ID, Method als Auswahl, Path, Connector ID, Status; Date mit Static date / Date Range, Date, End; Datumsformat DD/MM/YYYY; Apply und Reset. Der Filterdialog wurde ohne Eingaben über X geschlossen. Keine Aufbewahrungsdauer, Zeitzonenregel oder vollständige Fehlercode-Liste verifiziert. Keine Protokollinhalte in die Kundenartikel übernommen.

## Abschluss des ersten UI-Durchlaufs

Alle geöffneten leeren Formulare und Filter wurden geschlossen. Letzte Ansicht: Event log. Kein Benutzer, keine Kategorie, kein Artikel und kein Kalender angelegt; keine gespeicherte Konfiguration, Rolle, Lizenz oder Verbindung geändert. Die Auswahl eines lokalen Kalender-Connectors wurde im ungespeicherten Formular versucht und nicht als erfolgreich bestätigt.

## Nachprüfung der Connector-Dialoge nach ausdrücklicher Freigabe

Der Benutzer hat das Öffnen der Connector-Dialoge ausdrücklich erlaubt. Die frühere Ablehnung des ersten Microsoft-365-Connect-Klicks betrifft daher nicht mehr den Stand der folgenden Prüfung. Die erneute Prüfung erfolgt in derselben bereitgestellten Sitzung. Keine Anmeldedaten eingegeben, keine Einwilligung erteilt und keine Verbindung erstellt.

### P15 – Microsoft Office 365 Resources

Auf `#/connector/add-connector` führt Connect auf der Kachel zu einem vorgeschalteten Auswahlbereich mit:

- Titel Microsoft Office 365 Resources und Beschreibung für Room-/Equipment-Mailboxen via Microsoft Graph.
- Zwei Radiobuttons: Application Account und User/Service Account.
- Einem weiteren Connect-Button und Back.

Kein Kontotyp ausgewählt und den zweiten Connect-Button nicht betätigt; über Back zur Kachelauswahl zurückgekehrt. Der nachfolgende Microsoft-Anmelde-/Consent-Ablauf und konkrete Scopes bleiben ungetestet.

### P16 – Microsoft Exchange und Microsoft Exchange Sparo

Beide Kacheln öffnen jeweils einen eigenen Bereich mit dem entsprechenden Produkttitel und denselben sichtbaren Eingabefeldern Mailbox Address und Password. Darunter Connect, oben Back.

Im jeweils initialen leeren Formular ist kein separates Feld für eine EWS-Service-URL sichtbar. Keine automatische Erkennung oder spätere Serverkonfiguration daraus ableiten. Keine Daten eingegeben, Connect im Formular nicht ausgeführt und jeweils über Back zurückgekehrt. Keine Aussage über unterstützte Authentifizierungsverfahren oder erfolgreiche Verbindungstests aus dieser Formularprüfung ableiten.

### P17 – Microsoft Entra ID

Die Kachel Microsoft Entra ID (Microsoft 365 Azure Active Directory) öffnet nach Connect einen Bereich mit genau einer sichtbaren Kontotypoption: Application Account. Außerdem Connect und Back. Keine Option ausgewählt und Connect im Panel nicht betätigt; über Back zurückgekehrt. Daraus folgt keine Bestätigung konkreter Microsoft-Scopes oder Kontolizenz-Anforderungen.

### P18 – Office 365 - Teams

Connect auf der Kachel öffnet einen Bereich mit zwei Radiobuttons: User/Service Account und Teams Calling Agent (User/Service Account). Außerdem Connect und Back. Die Varianten bestätigen die bereits dokumentierte Trennung von Chat- und Call-Connector. Kein Modus ausgewählt, keine Anmeldung geöffnet und kein zweiter Connect-Klick ausgeführt.

Zum Abschluss über Back zur Kachelauswahl zurückgekehrt und diese Ansicht visuell geprüft. Keine Zugangsdaten eingegeben, keine Microsoft-Einwilligung erteilt und keine Verbindung erstellt. Die zuletzt sichtbare Route ist `#/connector/add-connector`.
