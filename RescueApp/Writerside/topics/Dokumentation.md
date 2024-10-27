# Documentation_RescueWebApp

<tabs>
<tab title="Protokollierung">

</tab>

<tab title="Planung">
<h3>Pages (HTTP)</h3>
<list type="bullet">
  <li>Login-Page</li>
  <li>Main-Page</li>
  <li>Admin-Page</li>
  <li>Job-Page</li>
  <li>Hilfe-Rufen-Page</li>
</list>

<h3>Login-Page</h3>
<list type="bullet">
  <li>Lehrer oder Sanitäter - Die Main-Page ist je nach Benutzer unterschiedlich aufgebaut</li>
  <li>Username und Passwort - Was wird benötigt? (IServ Verknüpfung erstmal nicht verfügbar)</li>
  <li>Personenbezogene Daten aufs Nötigste reduzieren</li>
</list>

<h3>Main-Page</h3>
<list type="bullet">
  <li>Header (Eingeloggt als ... / "Hilfe rufen" - Button (nur bei Lehrern)</li>
  <li>Tabelle aller Aufträge (offene Notfälle = rot; erledigte Notfälle = grün)</li>
  <li>Anzeige von verfügbaren Teams je Standort (Smart Overview)</li>
</list>

<h3>"Hilfe rufen" - Button</h3>


Neue Page, um Informationen zum Notfall einzugeben

<list type="bullet">
  <li>Standort (Haspel, Kothen, Ritterstraße, ...) -> Schaltflächen zum Auswählen</li>
  <li>Raumnummern (per Tasten/Touch eingeben</li>
  <li>Wie viele Sanis werden benötigt? (2 Teams pro Standort möglich auszuwählen - Schaltflächen)</li>
</list>

Die Notfallbeschreibung wird nach Absenden des Hilferufs verfasst.

<h3>Admin-Page </h3>
<list type="bullet">
  <li>Bearbeiten von Usern - Der Admin muss die User anlegen</li>
  <li>Löschen von Usern</li>
  <li>Dienstplan pflegen</li>
</list>

<h3>Userverwaltung</h3> 
Die Userverwaltung ist nicht im Mock-Up enthalten, wir werden jedoch höchstwahrscheinlich eine API mit C# nutzen.

<h3>Server </h3>
<list type="bullet">
  <li>Apache, freier Web-Server, GitHub-Pages, JSON</li>
</list>

<h3>Design</h3>
<list type="bullet">
  <li>Darkmode</li>
  <li>Farbe - Status der Notfälle</li>
  <li>Buttons - ...</li>
</list>
</tab>

<tab title="MockUp">

![Login.png](Login.png)

*Abb. Iphone 13/14*

Möchte man die Schule auswählen, so wird dem User eine Liste aller Schulnamen angezeigt, oder aber eine Seite mit allen
Schulen und deren Logos. 


</tab>

<tab title="Diagramme">
<h3>Aktivitätsdiagramm </h3>

<h3>Klassendiagramm</h3>

![KlassendiagrammS.png](KlassendiagrammS.png)

<h3>Sequenzdiagramm</h3>
<h5> Anmeldung/Abmeldung zum Server</h5>

![SequenzAnmeldungAbmeldungServer.png](SequenzAnmeldungAbmeldungServer.png)

</tab>


<tab title="Tabellen">
Die folgenden Tabellen geben Informationen zu Designentscheidungen und dem UX-Design der Web-App.


<h3>Interaktionsprinzipien</h3>

| Interaktionsprinzipien               | Ausprägungen                                        | Begründung der Designentscheidung                                               |
|--------------------------------------|-----------------------------------------------------|---------------------------------------------------------------------------------|
| Aufgabenangemessenheit               | Identifizierbarkeit der Aufgaben                    |                                                                                 |
|                                      | Aufwandoptimierung                                  |                                                                                 |
|                                      | Defaults                                            |                                                                                 |
| Selbstbeschreibungsfähigkeit         | Vorhandensein/Offensichtlichkeit von Informationen  |                                                                                 |
|                                      | Eindeutige Anzeige des Systemstaus                  |                                                                                 |
| Steuerbarkeit                        | Unterbrechbarkeit                                   |                                                                                 |
|                                      | Flexibilität                                        |                                                                                 |
|                                      | Individualisierbarkeit                              |                                                                                 |
| Erwartungskonformität                | System reagiert wie erwartet                        |                                                                                 |
|                                      | Konsistenz (intern und extern)                      |                                                                                 |
|                                      | Authentische Anpassung an den Nutzungskontext       |                                                                                 | 
| Robustheit gegenüber Nutzungsfehlern | Fehlervermeidung                                    |                                                                                 |
|                                      | Fehlertoleranz                                      |                                                                                 |
|                                      | Fehlermanagement                                    |                                                                                 |
| Benutzerbindung                      | Motivation                                          |                                                                                 |
|                                      | Vertrauenswürdigkeit                                |                                                                                 |
|                                      | Benutzerintegration                                 |                                                                                 |
| Erlernbarkeit                        | Unterstützung beim Entdecken der Bedienfunktionen   | Wenig Buttons, Aussagekräftig (Text/Farben)                                     |
|                                      | Unterstützung beim Ausprobieren der Bedienfunktionen| Buttons oder andere Eingabemöglichkeiten disabled bis die Anforderungen stimmen |
|                                      | Unterstützung beim Erinnern von Bedienfunktionen    | Erinnerungen sollten nicht benötigt werden aufgrund den vorigen Punkten         |


<h3>Grundprinzipien des UX-Designs</h3>

| Prinzip                         | Geplante Umsetzung                                                                            | Begründung                                                                                                                |
|---------------------------------|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Vermeidung von Informationsflut | Es sollen nur relevante Informationen angezeigt werden.                                       | Aufgrund von Notfällen sich auf das Wichtigste beschränken                                                                |
| Konsistenz                      | Interne Konsistenz                                                                            | Eine Individuelle Schullösung für die Stadt Wuppertal für jedes Gerät                                                     |
| Universelle Bedienbarkeit       | Web-App (PC, Smartphones)                                                                     | Die Verfügbarkeit zu jeder Zeit gewährleisten                                                                             |
| Informative Rückmeldungen       | Anfrage für Teams; Informationen für Teams; Aufbruchsbestätigung an Lehrer;                   | Sanitäter sollen nur entscheidende Informationen erhalten (Sanitäter = Standort und Beschreibung; Lehrer = Aufbruchsinfo) |
| Abgeschlossenheit der Dialoge   | Auf jede Anfrage folgt eine Bestätigung und auf jede Bestätigung erfolgt eine Benachrichtigung | Sanitäter sowie Lehrer sollen stets auf dem aktuellsten Stand bleiben (Schutz vor Unwissenheit)                           |
| Einfache Fehlerbehandlung       | Wenig Interaktionsmöglichkeiten innerhalb der Web App                                         | Eingaben/Nutzen der UI so gering wie möglich halten = Fehlerbehandlungen überschaubar                                     |
| Widerrufbarkeit von Aktionen    | Fehlerhafter Notfall = Abbruchmöglichkeit z.B. in der Notfallübersicht)                       | Um die Verfügbarkeit der Teams schnell zu gewährleisten;                                                                  |
| Kontrollvermittlung             | Eindeutige Optionen/Abbruchfunktion/Transparenz                                               | Verständliche Aktionen; Abbruch z.B. fehlerhaftem Notfall; Information der Benutzer über aktuellen Status von Notfällen   |


<h3>Begründung der Designentscheidung</h3>

| Designauswahl              | Geplante Umsetzung                                                                | Begründung                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Steuerelemente             | Buttons; Tabelle/Liste?;                                                          |                                                                                                                           |
| Farbauswahl                | Darkmode mit dunkelgrünen Elementen                                               |                                                                                                                           |
| Textgestaltung             | Typografie = Helvetica; Visuelle Hierarchien                                      |                                                                                                                           |
| Rückmeldungen              | Pop-Up Benachrichtigungen; E-Mail; Alarm-Sound                                    |                                                                                                                           |
| Abstände und Gruppierungen | Visuelle Hierarchie; Gruppierungen; Konsistenz; Lesbarkeit; Balance und Anordnung |                                                                                                                           |
| Icons                      |                                                                                   |                                                                                                                           |
| Navigation                 | Maus oder Touch                                                                   | PC/Handy Nutzung über das Web                                                                                             |
| Barrierefreiheit           | Texte Kontrastreich; Bedienbarkeit; Verständlichkeit; Robustheit                  | Für alle Benutzer wahrnehmbar, bedienbar, intuitiv verständlich. Der Code ist zudem sauber, effizient und standardkonform |
| Mehrsprachigkeit           | Deutsch; Englisch(?); (Arabisch?)                                                 | Um ausländische Kräfte nutzen zu können                                                                                   |

</tab>


<tab title="Code"></tab>

</tabs>









