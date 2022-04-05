# LKF - Computerforensik

## Grundlagen und Beweisführung

### Definition Digitale Forensik

<!-- ToDo: PPT 1 - Folie 33 -->

- **Forensik:** systematische Untersuchung von kriminellen Handlungen

**Digitale Forensik:**

- **streng methodisch vorgenommene Datenanalyse** auf Datenträgern und in Computernetzen
- zur **Aufklärung von Vorfällen**
- unter Einbeziehung der Möglichkeiten der strategischen Vorbereitung insbesondere aus der Sicht des Anlagenbetreibers eines IT-Systems.

### Ziele digitaler Forensik

<!-- PPT 1 - Folie 34  -->

- Identifikation des Angreifers
- Erkennen der Methode
- Ermittlung des Schadens
- Sicherung der Beweise

### Arbeitsgebiete digitaler Forensik

<!-- PPT 1 - Folie 35 -->

- **Datenträger**-Forensik
- **Mobilfunk**-Forensik
- **Netzwerk**-Forensik
- **Multimedia**-Forensik
- **Cloud**-Forensik
- **Memory**-Forensik
- **Car** Forensik
- **IoT**-Forensik
- Forensische **Linguistik**

#### Überschneidungen zu anderen Gebieten der Informationssicherheit

<!-- HELP: Findet ihr das relevant? -->

- Forensic Intelligence (predictive Policing, Untersuchung von Radikalisierung im Internet)
- Informationssicherheitsmanagement
- Schadsoftware-Analyse / Reverse Engineering
- Untersuchungen im Darknet
- Kryptowährungen / Blockchain-Untersuchung

#### Multimedia-Forensik

- Feststellung von Spuren bzw. Manipulationen in Bildern/Videos/Audio
- Arbeitsgebiet der digitalen Forensik

### Herausforderungen der digitalen Forensik

- Massendaten in der Datenträger-Forensik: **Datenmengen immer größer**, Speicherplatz immer günstiger
- **Faktor Zeit:** bis zur Entdeckung eines Vorfalls vergehen oft Monate

### Dunkelfeld

> **Bereich der Cyber-Straftaten, die nicht in der polizeilichen Kriminalstatistik erfasst wird**, da sie nicht entdeckt werden.

#### Gründe für Nicht-Entdecken

- gute Angreifer (wird nicht entdeckt)
- mangelnde Schutzvorkehrung
- Firmen melden Vorfälle wegen Imageschäden/Zeitdruck (schnell wieder einsatzfähig sein)
- Kein Interesse an forensischer Aufarbeitung

### Spuren

- materielle **Veränderungen an Personen oder Objekten**
- stehen **im Zusammenhang mit relevanten Ereignissen**
- **können zur Tataufklärung beitragen** (geben Rückschlüsse auf Tatablauf und Täter)

#### Digitale Spuren

- basieren auf Daten, welche in Computersystemen gespeichert sind bzw. übertragen wurden (Metadaten/Computerdaten $\rightarrow$ RAM, DBs, ...)
- werden erst durch ihre Interpretation von physischen Spuren über unterschiedliche Interpretationsebenen zu verwertbaren Spuren

#### Unterschiede im Gegensatz zu analogen Spuren

- digitale Spuren entstehen im Hintergrund
- können flüchtig sein, sind leicht änderbar
- können verschlüsselt sein
- liegen physisch auf Datenträger vor und müssen dann logisch interpretiert werden um lesbar zu werden

#### Spurenträger

Spurenträger können mobile und immobile digitale Geräte mit deren flüchtigen und nichtflüchtigen Speichern sein:

- Desktop-PC
- Notebook
- Datenträger:
  - interne/externe Festplatte
  - SD-Karten
  - SIM-Karten
  - Disketten
  - CDs
  - USB-Sticks
- Drucker
- Kameras
- Smartphones
- Spielekonsolen

### Locard'sche Prinzip

> Es gibt keinen Tatort ohne Spuren!

- keine Person (Täter/Opfer/Ermittler) kann einen Tatort betreten und verlassen ohne Spuren zu hinterlassen
- Jeder der mit Tatort interagiert hinterlässt/verändert Spuren oder nimmt etwas mit.

> auch bei digitalen Spuren!

### Forensischer Arbeitsplatz

- **forensische Workstation** (sehr potente Hardware)
- **Office Computer** für schriftliche Sachen (Dokumentation) ohne Verbindung zum Netzwerk oder nur interne Verbindung, aber kein Internetzugang
- **Internetcomputer** für Recherche (aktuelle Virenscanner und Firewall!)

> $\rightarrow$ im Idealfall drei physische Rechner (forensische Workstation immer physisch getrennt)

### Forensic Readiness

> -**bereit sein** für forensische Prozesse durch forensischen Arbeitsplatz **(strategischer und operativer Ebene)**
> - Systeme sollen so konfiguriert sein, dass man digitale Spuren sammeln, schneller im Ernstfall agieren und Kosten sparen kann

- **Transportable Workstations** für Außeneinsätze (Beweismittel vor Ort erheben)
- **Schreibschutzadapter** für Datensicherung (Außen- und Laboreinsatz)
- **Technische Maßnahmen:** Gruppenrichtlinien konfigurieren (Server), Logging aktivieren
- **Organisatorische Maßnahmen:** Response-Teams, Hard- und Software beschaffen, Prozesse aufbauen (Verantwortliche, Budget, Kompetenzen, Räumlichkeiten, ...)

#### Schreibschutzadapter

- Gerät zwischen Datenträger und Auslesegerät
- verhindert dass Auslesegerät den Inhalt auf dem Datenträger verändern kann (blockiert Schreibzugriffe)
- verhindert versehentliches Vertauschen von Quelle und Ziel

##### Datenintegrität garantieren

Integrität der Beweiskette sichern:

- Writeblocker zum Schreibschutz einsetzen
- Hashing des forensischen Duplikats vor der weiteren Untersuchung

### Hashwerte

Ein einzigartiges Rechenergebnis aus einer Bitfolge

Für Überprüfung von Datenmanipulation (Integrität sicherstellen)

Illegale Daten finden z.B. Kinderporngrafie

Systemspezifische Daten gleich ausblenden

### Vorgehensmodelle

#### Anforderungen an forensische Vorgehensweisen

- **Akzeptanz:** Methoden sind in der Fachwelt anerkannt
- **Glaubwürdigkeit:** Funktionalität der Methoden ist nachweisbar
- **Wiederholbarkeit:** Ergebnisse ist durch Dritte reproduzierbar
- **Integrität:** Spuren werden durch Untersuchung nicht verändert
- **Ursache und Auswirkungen:** Verbindung zwischen digitalen Spuren, Ereignissen und Personen sindherstellbar
- **Dokumentation:** Ermittlungsprozess ist nachvollziehbar dokumentiert

#### BSI-IT-Forensik-Leitfaden

#### S-A-P-Modell

<!-- ein Schwerpunkt! -->

- Sichern: Strategische und operative Vorbereitungen und Erfassung aller relevanter Daten
- Analysieren: Wer/Wann/Wo/Wie/Was?
- Präsentieren bzw. Aufbereiten: Ergebnisse so aufarbeiten, dass sie dem Auftraggeber präsentiert werden können

#### Post-mortem Forensik

- *"nach dem Tod"* werden nach einem Vorfall Daten erhoben und analysiert (z.B. Datenträger-Forensik)
- wenn Rechner ausgeschaltet und Festplatte ausbaubar $\rightarrow$ komplettes Datenträgerabbild mit forensischer Maschine erstellen

#### Live-Forensik

- *während das System noch läuft* findet die Untersuchung eines Vorfalls statt
- Daten live abziehen, wenn das System noch läuft (z.B. RAM)
- wenn kein physischer Zugriff/man weiß nicht was drauf läuft/evtl. Verschlüsselung bei herunterfahren

#### logische Sicherung

- auf Betriebssystemebene
- mit Mitteln des Betriebssystems
- mit Drittanwendersoftware
- erfolgt abhängig von Betriebssystem

#### physikalische Sicherung

- auf Hardwareebene
- mit hardware- und softwaretechnischen Hilfsmitteln
- erfolgt betriebssystemunabhängig

## ISO 27037 und Tatorfotografie

### Beteiligte Akteuere in der ISO 27037

- Ersteinschreiter für digitale Beweismittel (DEFR)
- Spezialist für digitale Beweismittel (DES)

### Allgemeine Schritte nach ISO 27037

<!-- ToDo: Prüfen Folie 2/7-->

- Überblick
- Identifikation
- Mitnahme
- Sicherung
- Erhaltung

### Durchführung einer Risikobeurteilung

Ersteinschreiter für digitale Beweismittel (DEFR): Befugt ist die ersten Maßnahmen am Tatort/an den Systemen vorzunehmen, der über Sicherungsmethode entscheidet & über Methode der Mitnahme

Spezialist für digitale Beweismittel (DES): kümmert sich um Analyse, kann Aufgaben des DEFR übernehmen, aber zusätzlich noch Analysen

### Grundsätze der digitalen Beweisführung

Relevanz, Vollständigkeit, Verlässlichkeit

- alle Maßnahmen dokumentieren
- Methoden anwenden, mit welchen die Fehlerfreiheit und Verlässlichkeit der Kopie von potentiellen digitalen Beweismitteln festgestellt werden kann
- Erkennen, dass der Vorgang der Erhaltung von potentiellen digitalen Beweismitteln nicht immer eingriffsfrei erfolgen kann

### Identifikationsphase

nach ISO: Ersteinschreiter wird tätig und sucht nach Beweismitteln, diese können in physischer und logischer Form vorliegen

physisch: Vorhandensein auf konkreten Gerät, die Zustände der einzelnen Datenträgern auf Bitebene

logisch: physische Form interpretieren z.B. Mithilfe Betriebssystem oder Dirttanwendersoftware

logische Form soll dargestellt und gesichert werden

- soll Speichermedien und alle datenverarbeitenden Geräte identifizieren (die Vorfall-relevant sein können)
- Priorisierung der Beweismittelerhebung auf Grundlage der Flüchtigkeit der Daten
- Ein- oder ausgeschalteter Zustand der Geräte

### Leitfäden nach ISO 27037

<!-- ToDo: Folie 16 ff.? -->

### Mitnahme vs. Sicherung

Entscheiden, ob man das Gerät an sich braucht oder nur Daten auf der Festplatte

Wichtiges Entscheidungskriterium: ist das Gerät aus oder an? Wenn es an ist → Live Forensik vor Ort mögl. oder mit Stromzufuhr Mitnahme oder Sicherung vor Ort vornehmen (gerade bei schweren Geräten, die man erst ausschalten müssen oder so, bei systemkritischer Technik)

### Totmannschaltung

Mechanismus, der ausgelöst wird wenn die Bestätigung durch einen Menschen ausbleibt

im digital forensischen Umfeld Manipulationen am Tatort: ausschalten/abziehen eines Geräts, entfernen eines Tokens (z.B. abziehen eines USB-Sticks) kann zur Verschlüsselung des Systems führen

### Grundlegende Maßnahmen für ausgeschaltete digitale Geräte - Mitnahme

- Stromversorgungskabel zuerst am Gerät trennen
- Alle Kabel werden vom Gerät getrennt, gesichert und gekennzeichnet
- Ein-/Aus-Knopf mit Klebeband überkleben $\rightarrow$ keine Zustandsänderung
- Laptops: Sicherstellen, dass Gerät wirklich ausgeschalten ist $\rightarrow$ Akku entfernen
- Beim Entfernen von Komponenten auf Erdung achten
- Dokumentieren, ob CD/DVD-Laufwerke leer und vollständig eingefahren sind

In den meisten Fällen sollte das Speichermedium bis zum Zeitpunkt der Sicherung nicht aus dem digitalen Gerät
entfernt werden, da das Entfernen das Risiko der Beschädigung oder der Störung durch andere Speichermedien
erhöhen kann.

### Grundlegende Maßnahmen für ausgeschaltete digitale Geräte - Sicherung

- Es ist sicherzustellen, dass das Gerät tatsächlich ausgeschalten ist
- Wenn möglich, ist das Speicherlaufwerk aus dem ausgeschalteten digitalen Gerät zu entnehmen, falls es zuvor noch nicht entnommen wurde.
- Das Speicherlaufwerk wird als Beweismittel gekennzeichnet und alle Details, wie Hersteller, Modellbezeichnung,Seriennummer und Speicherkapazität, werden dokumentiert.
- Es wird eine Imagesicherung mithilfe von validierten Sicherungswerkzeugen erstellt, um eine digitale Beweismittelkopie des verdächtigen Laufwerks zu erhalten

In den meisten Fällen sollte das Speichermedium bis zum Zeitpunkt der Sicherung nicht aus dem digitalen Gerät
entfernt werden, da das Entfernen das Risiko der Beschädigung oder der Störung durch andere Speichermedien
erhöhen kann.

### Grundlegende Maßnahmen für eingeschaltete digitale Geräte

- drauf achten, ob Gerät WIRKLICH ausgeschaltet ist z.B. durch Status-LED, Maus bewegen
- Ein- und Ausschaltknöpfe abkleben → während Transport keine Zustandsänderungen
- Kabel etc. vom Gerät trennen, kennzeichnen an welchem Port diese waren
- Stromzufuhr trennen: zunächst am Gerät trennen, damit keine unterbrechungsfreie Stromzufuhr ausgelöst wird
- bei Transport: Anti-Statik Beutel, keine Beschädigungen des Gerätes

### Erhebung von nicht digitalen Beweismitteln

- digitaler Ersteinschreiter sollte nicht nur digitale Beweismittel erhalten, sondern auch nicht digitale Beweismittel berücksichtigen
- z.B. Personen, die für das Büro vor Ort verantwortlich sind, Zugänge von diesen Personen herausgeben lassen
- diese Personen können zusätzliche Infos für Doku herausgeben → relevante Details aus Gesprächen mit aufnehmen, Name und Position der Person dokumentieren
- Hinweise die z.B. Passwort herausgeben (Post It Zettel), andere weitere Notizen

### Besonderheiten bei der Sicherung digitaler Beweismittel

<!-- ToDo Folie 1/80 und 1/82 Richtung Datenintegrität oder 1/77-->

## Betriebssysteme

### CERT

- Computer Emergency Response Team
- größere Unternehmen, extern ausgelagert, auch auf Landesebene (pro Bundesland eins)
- Kontaktstellen bei größeren IT-Sicherheitsvorfall

### BSI IT-Grundschutz Kompendium

- Katalog für die einzelnen Bereiche einer Organisation einzelne Bausteine beschrieben
- Applikation, System, Organisation usw.

### Stand der Technik

- Rechtsformulierung da sich Gesetze langsamer als die Technik entwickeln
- Hinweise auf Stand der Technik geben bspw. IT-Grundschutz Bausteine

### Received-Einträge im E-Mail Header

- jeder Mailrouter, der Mail verarbeitet fügt sich dieser Liste hinzu
- Anomalien leicht feststellbar
- Phishingmails darüber identifizieren

### Windows Registry

- verschiedene Datenbanken (Registry Hives) die dort als Datei vorliegen auf dem Datenträger

### Volume Shadow Copy

- Snapshots eines NTFS Volumes (pro NTFS Volume 64 Snapshotkopien)
- arbeitet auf copy und write Basis
- alte Zustände eines Volumes abrufen
- aller 7 Tage, bei Patches, Treibersoftware etc. erstellt

### Alternate Data Stream

- Data Attribut mit Data Runs mit Clusternummern mit eigentlichen Dateininhalten
- zusätzlich Alternate Data Streams anhängen mit weiteren Infos zur Datei zB kommt Datei aus lokalen oder aus Internet
- man kann darin Dateien verstecken (wie Schadsoftware)

### Windows SID

- SID pro Benutzergruppe/Benutzerkonto etc. eindeutig vergeben

→ nachvollziehen wer, was geändert hat

- Benutzerrechte damit zuweisen
- welcher Nutzer hat Zugriff, wer hat es angelegt und wer hat es geändert
- ob Nutzer gelöscht wurden, die daran etwas gemacht haben
- Log Dateien bzgl. Löschvorgangs/Änderung an Nutzerkonten
- SID bleibt immer identisch

## Techniken der Spurensuche und RAM Analyse

### Dateitypüberprüfung

- Dateien ohne Dateiendung analysieren & Dateityp identifiziert
- durch Header & Footer Informationen

### FileCarving

- Suche nach Dateien, die gelöscht wurden
- nicht mehr im allozierten Speicher, aber noch drauf sind
- zB mit Hexeditor

### Post Mortem Forensik

- komplette Datenträgerkopie erstellen, alles vollumfänglich gesichert
- können immer wieder neue Wege zur Ermittlung einschlagen durch die vollumfänglichen Kopien

### Live Forensik

- Vorteil: geht deutlich schneller

### Kernel Level Sicherung

- Systemkern speichert RAM Inhalte
- versch. Tools je nach Betriebssystem
- Vorteil zu User Level: gesamter RAM gesichert und nicht selektive Sicherung

### Cold Boot

- RAM Sicherungsmethode
- RAM heruntergekühlt um kurzzeitig Stromzufuhr zu unterbrechen + keine Inhalte verlieren
- mit/ohne Transfer, ohne mit Livesystem

### Volatility Framework

- Framework zum Analysieren von RAM-Abbildern

### Plist-Dateien

- Property List Dateien: Key-Value-Paare
- vorallem unter macOS vorhanden, als Konfigurationsdateien
- vom Aufbau XML-Dateien mit spezifischen Schlüsselpaaren, können bspw. mit xcode geöffnet werden, welche Konfigurationsparameter gesetzt sind, wer zuletzt etwas geändert hat

### Hinweise auf einen Einbruch

- wenn Rechner auffällig langsam wird
- verdächtige/unbekannte Prozesse im Taskmanager prüfe
- Auffälligkeiten bei Netzwerkverbindungen
- Auffälligkeiten in Log-Dateien (unvollständig/geleert)
- unbekannte Benutzer, besonders Admin Accounts
- Meldungen von Antiviren Software, Protokolldateien der Software prüfen

## Dateisysteme

### Sektoren

- Zusammenfassung von Bytes in einem Block

### Cluster

- Zusammenfassung mehrerer Sektoren
- Clustergröße bei Formatierung festlegbar
- einzelne Bytes zu Block zusammengefasst

- Betriebssystem arbeitet Clusterweise $\rightarrow$ es werden immer ganze Cluster gespeichert

### ROOT-verzeichnis bei FAT

- im Datenbereich beim FAT-Datenträger
- FAT12&16 → direkt im Anschluss an die FAT
- FAT32 → kann überall beginnen, meist in den Sektoren direkt nach der FAT
- Root Verzeichnis finden: boot Sektor ansehen, wie viele reservierte Sektoren, zwei im Offset und ein paar mehr → dann diese Zahl ist das gesuchte ROOT-Datenverzeichnis

### Master File Table

- Teil des NTFS Dateisystem
- Datei auf dem Datenträger die Infos über alle anderen Dateien & Verzeichnisse enthält
- enthält verschiedene Informationen über Aufbau des Datenträgers
- Datenbank mit Adressen zu jeder Datei auf den Datenträger, jede Datei besitzt MFT Eintrag mit verschiedenen Attributen
- wichtigste Attribute: Filename, Standardattribut (Meta Daten, wann wurde es angelegt etc.), Dataattribut (enthält Daten direkt (wenn klein genug, MFT Eintrag ist meist 1024 Bytes groß), sonst DataRuns)

- Datei (vgl. Datenbank) mit Einträgen zu allen Dateien/Verzeichnissen
- Attribute: Filename, Metadaten, Data (Daten selbst oder DataRuns)

### $DATA Attribut

- die tatsächlichen Daten, die in die Datei geschrieben wurden
- NTFS-Dateisystem
- direkte Daten oder DataRuns

### Slackspeicher

- Ursprung: interne Fragmentierung
- Cluster wird nicht komplett durch eine Datei ausgenutzt, ist aber komplett ausgefüllt -> verbleibender Bereich = Slackspeicher (kann alte Daten beinhalten)
- z.B. bei FAT oder NTFS, aber nicht ext

### MAC-Zeitstempel

- jedes Betriebssystem besitzt Zeitstempel
- Modification, Access, Change/Creation-Time

### Superblock

- alle wichtigen Infos zum ext Dateisystem (Adressedes ersten Blocks, Blockgröße, Blockgruppengröße, freie Inodes, ...)

### Umgang mit Dateien im Ext-Dateisystem

- Superblock & Gruppendeskriptortabelle (wie viele freie Blöcke pro Block, weitere Infos zu Inodes z.B. Inode mit 2 ist immer Rootverzeichnis

### DataRuns

- bestehen aus einer Anzahl an Clustern, besitzen Clusternummern die dazugehören
- über diese Clusternummern lässt sich Datei zusammenbauen

- Liste von Clustern

## Windows-Zusatz

<!-- Coming soonTM -->
