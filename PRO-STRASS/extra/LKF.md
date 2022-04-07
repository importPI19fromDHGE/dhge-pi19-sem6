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

<!-- ToDo: HELP -> Findet ihr das relevant? -->

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
- Firmen melden Vorfälle wegen Imageschäden/Zeitdruck nicht (schnell wieder einsatzfähig sein)
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

<!-- ToDo: HELP PPT1 - Folie 45? -->

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

##### Datenintegrität

<!--ToDo: Prüfen -->

- Sichern: nach gewissen Vorgehen, damit man nichts verändert
- Analysieren: Wer/Wann/Wo/Wie/Was?
- Präsentieren bzw. Aufbereiten: Ergebnisse so aufarbeiten, dass Auftraggeber sie präsentieren kann

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

<!-- ToDo: ein Schwerpunkt! -->

#### Post-mortem Forensik

- *"nach dem Tod"* werden nach einem Vorfall Daten erhoben und analysiert (z.B. Datenträger-Forensik)
- wenn Rechner ausgeschaltet und Festplatte ausbaubar $\rightarrow$ komplettes Datenträgerabbild mit forensischer Maschine erstellen
- komplette Datenträgerkopie erstellen, alles vollumfänglich gesichert
- können immer wieder neue Wege zur Ermittlung einschlagen durch die vollumfänglichen Kopien

#### Live Forensik

- *während das System noch läuft* findet die Untersuchung eines Vorfalls statt
- Daten live abziehen, wenn das System noch läuft (z.B. RAM)
- wenn kein physischer Zugriff/man weiß nicht was drauf läuft/evtl. Verschlüsselung bei herunterfahren
- Vorteil: geht deutlich schneller

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

<!-- ToDo: Auf Duplikat prüfen-->

- **Ersteinschreiter für digitale Beweismittel (DEFR):** Befugt ist die ersten Maßnahmen am Tatort/an den Systemen vorzunehmen, der über Sicherungsmethode entscheidet & über Methode der Mitnahme
- **Spezialist für digitale Beweismittel (DES):** kümmert sich um Analyse, kann Aufgaben des DEFR übernehmen, aber zusätzlich noch Analysen

### Allgemeine Schritte nach ISO 27037

- Sichern und Kontrollieren des Bereichs, in dem sich die Geräte befinden
- Bestimmung der Person, die für den Ort die fachliche Verantwortung trägt
- Sicherstellen, dass Personen von den Geräten und von der Stromversorgung ferngehalten werden
- Alle Personen dokumentieren, die Zugang zum Ort haben oder für die ein Motiv für eine Beteiligung am Untersuchungsort vorliegen könnte
- Ist das Gerät eingeschaltet, darf das Gerät nicht ausgeschaltet werden und umgekehrt, falls das Gerät ausgeschaltet ist, darf es nicht eingeschaltet werden
- Untersuchungsort mit allen Komponenten und Kabeln in seiner ursprünglichen Position dokumentieren
- Falls zulässig: Bereiche nach Gegenstände, wie Haftnotizen, Terminkalender, Akten, Laptops oder Handbücher für Hard- und Software durchsuchen

### Grundsätzliche Regeln am Tatort

<!-- ToDo -->

### Durchführung einer Risikobeurteilung

- Ersteinschreiter für digitale Beweismittel (DEFR):
  - befugt die ersten Maßnahmen am Tatort/an den Systemen vorzunehmen
  - Entscheidung über Sicherungsmethode und Methode der Mitnahme
- Spezialist für digitale Beweismittel (DES)
  - kann Aufgaben des DEFR übernehmen, führt zusätzliche Analysen durch

### Grundsätze der digitalen Beweisführung

Relevanz, Vollständigkeit, Verlässlichkeit

- alle Maßnahmen dokumentieren
- Methoden anwenden, mit welchen die Fehlerfreiheit und Verlässlichkeit der Kopie von potentiellen digitalen Beweismitteln festgestellt werden kann
- Erkennen, dass der Vorgang der Erhaltung von potentiellen digitalen Beweismitteln nicht immer eingriffsfrei erfolgen kann

### Identifikationsphase

- nach ISO: Ersteinschreiter wird tätig und sucht nach Beweismitteln, diese können in physischer und logischer Form vorliegen
- physisch: Vorhandensein auf konkreten Gerät, die Zustände der einzelnen Datenträgern auf Bitebene
- logisch: physische Form interpretieren z.B. Mithilfe Betriebssystem oder Dirttanwendersoftware
- logische Form soll dargestellt und gesichert werden
- soll Speichermedien und alle datenverarbeitenden Geräte identifizieren (die Vorfall-relevant sein können)
- Priorisierung der Beweismittelerhebung auf Grundlage der Flüchtigkeit der Daten
- Ein- oder ausgeschalteter Zustand der Geräte

### Leitfäden nach ISO 27037

![Leitfaden: Sicherung/Mitnahme digitaler Geräte](/assets/iso27037-leitfaden-1.png)

#### Mitnahme von eingeschaltenen digitalen Geräten

![Leitfaden: Mitnahme von eingeschaltenen digitalen Geräten](/assets/iso27037-leitfaden-2.png)

#### Mitnahme von ausgeschalteten digitalen Geräten

![Leitfaden: Mitnahme von ausgeschalteten digitalen Geräten](/assets/iso27037-leitfaden-3.png)

#### Sicherung von eingeschalteten digitalen Geräten

![Leitfaden: Sicherung von eingeschalteten digitalen Geräten](/assets/iso27037-leitfaden-4.png)

#### Sicherung von ausgeschalteten digitalen Geräten

![Leitfaden: Sicherung von ausgeschalteten digitalen Geräten](/assets/iso27037-leitfaden-5.png)

### Mitnahme vs. Sicherung

> Entscheiden, ob man das Gerät an sich braucht oder nur Daten auf der Festplatte
>
> Wichtiges Entscheidungskriterium: ist das Gerät aus oder an? Wenn es an ist $\rightarrow$ Live Forensik vor Ort mögl. oder mit Stromzufuhr Mitnahme oder Sicherung vor Ort vornehmen (gerade bei schweren Geräten, die man erst ausschalten müssen oder so, bei systemkritischer Technik)

### Totmannschaltung

- Mechanismus, der ausgelöst wird wenn die Bestätigung durch einen Menschen ausbleibt
- im digital forensischen Umfeld Manipulationen am Tatort: ausschalten/abziehen eines Geräts, entfernen eines Tokens (z.B. abziehen eines USB-Sticks) kann zur Verschlüsselung des Systems führen

### Grundlegende Maßnahmen für ausgeschaltete digitale Geräte

- **Zustand prüfen:** Gerät WIRKLICH ausgeschaltet? (Status-LEDs, Maus bewegen, ...)
  - besonders bei Laptops! anschließend Akku entfernen
- **Stromzufuhr trennen:** zunächst am Gerät (damit keine unterbrechungsfreie Stromzufuhr ausgelöst wird)
- **Alle Kabel trennen, sichern und kennzeichnen** die mit dem Gerät verbunden sind
  - Beim Entfernen von Komponenten auf Erdung achten
- **Dokumentieren**, ob CD/DVD-Laufwerke leer und vollständig eingefahren sind
- **Transport-Sicherung:** Beschädigungen des Gerätes vermeiden $\rightarrow$ Anti-Statik Beutel, ...
  - Ein-/Aus-Knopf überkleben $\rightarrow$ Zustandsänderung verhindern

> In den meisten Fällen sollte das Speichermedium bis zum Zeitpunkt der Sicherung nicht aus dem digitalen Gerät entfernt werden, da das Entfernen das Risiko der Beschädigung oder Störung durch andere Speichermedien erhöhen kann.

### Grundlegende Maßnahmen für eingeschaltete digitale Geräte

- Sicherung der flüchtigen Daten in Betracht ziehen
  - Verschlüsselungscodes können im aktiven und inaktiven Speicher vorhanden sein
  - Wenn Verschlüsselung vermutet wird, dann logischer Sicherung in Betracht ziehen
  - Analyse, ob das Gerät durch normales Herunterfahren ausgeschalten werden sollte oder mittels Netzstecker
  - Beim Trennen des Netzsteckers darauf achten, dass die Seite am Gerät zuerst getrennt wird und nicht auf Seiten der Steckdose
- Netzschalter mit Klebeband abkleben!

> Beim Trennen der Stromzufuhr werden verschlüsselte Daten ohne passenden Schlüssel unzugänglich gemacht. Live-Daten können verloren gehen, was zu Schadensersatzansprüchen oder zu Verlusten von Menschenleben führen kann!

### Erhebung von nicht digitalen Beweismitteln

- digitaler Ersteinschreiter sollte nicht nur digitale Beweismittel erhalten, sondern auch nicht digitale Beweismittel berücksichtigen
- z.B. Personen, die für das Büro vor Ort verantwortlich sind, Zugänge von diesen Personen herausgeben lassen
- diese Personen können zusätzliche Infos für Doku herausgeben $\rightarrow$ relevante Details aus Gesprächen mit aufnehmen, Name und Position der Person dokumentieren
- Hinweise die z.B. Passwort herausgeben (Post It Zettel), andere weitere Notizen

### Besonderheiten bei der Sicherung digitaler Beweismittel

Spuren entstehen im Hintergrund, können flüchtig sein, sind leicht änderbar, können verschlüsselt sein, liegen physisch auf Datenträger vor und müssen dann logisch interpretiert werden um lesbar zu werden

### Hashwerte

- Ein einzigartiges Rechenergebnis aus einer Bitfolge
- Für Überprüfung von Datenmanipulation (Integrität sicherstellen)
- Illegale Daten finden z.B. Kinderporngrafie
- Systemspezifische Daten gleich ausblenden

## Bekämpfung der Computerkriminalität

### Die sechs Schritte des SANS-Institut

- **1. Vorbereitung:** Die Organisation sensibilisiert die Mitarbeiter und trainiert sie darauf, auf Computer-und Netzwerk-Sicherheits-Zwischenfälle schnell und korrekt zu reagieren.
- **2. Identifizierung:** Das Response Team entscheidet, ob ein bestimmtes Ereignis eine Bedrohung darstellt. Das Team kann sich an das CERT CoordinationCenter wenden, welche aktuelle Spuren im Internet auf Sicherheitsvorfälle untersucht und hat die Möglichkeit die aktuellsten Informationen über Viren und Würmer zu erhalten.
- **3. Eingrenzung:** Das Team bestimmt, wie weit das Problem bereits Schaden verursacht hat und nimmt alle betroffenen Systeme und Geräte zur Verhinderung weiterer Schäden offline.4.Beseitigung: Das Team untersucht die Herkunft des Vorfalls und beseitigt die Ursache des Problems.
- **5. Recovery:** Daten und Software sind sauber von Backup-Systemen wiederherzustellen. Um sicherzustellen, dass keine Lücken bleiben, werden diese überprüft. Systeme werden für weitere Anzeichen von Kompromittierung oder eines erneuten Auftretens überwacht.
- **6. Nachbesprechung:** Das Team untersucht den Vorfall und wie er behandelt wurde und versucht die Vorfallbehandlung und Prävention zu verbessern, um ein erneutes Auftreten des Problems zu verhindern.

### CERT

- Computer Emergency Response Team
- größere Unternehmen, extern ausgelagert, auch auf Landesebene (pro Bundesland eins)
- Kontaktstellen bei größeren IT-Sicherheitsvorfall

### Sechs Schritte des SANS-Institut

1. Vorbereitung: Die Organisation sensibilisiert die MA und trainiert sie darauf, auf Computer- und Netzwerk-Sicherheits-Zwischenfälle schnell und korrekt zu reagieren.
2. Identifizierung: Das Response Team entscheidet, ob ein bestimmtes Ereignis eine Bedrohung darstellt. Das Team kann sich an der CERT Coordination Center wenden, welche aktuelle Spuren im Internet auf Sicherheitsvorfälle untersucht und hat die Möglichkeit die aktuellsten Informationen über Viren und Würmer zu enthalten.
3. Eingrenzung: Das Team bestimmt, wie weit das Problem bereits Schaden verursacht hat und nimmt alle betroffenen Systeme und Geräte zur Verhinderung weiterer Schäden offline.
4. Beseitigung: Das Team untersucht die Herkunft des Vorfalls und beseitig die Ursache des Problems.
5. Recovery: Daten und Software sind sauber von Backup-Systemen wiederherzustellen. Um sicherzustellen, dass keine Lücken bleiben, werden diese überprüft. Systeme werden für weitere Anzeichen und Kompromittierung oder eines erneuten Auftretens überwacht.
6. Nachbesprechung: Das Team untersucht den Vorfall und wie er behandelt wurde und versucht die Vorfallbehandlung und Prävention zu verbessern, um ein erneutes Auftreten des Problems zu verhindern.

### BSI IT-Grundschutz Kompendium

- Katalog für die einzelnen Bereiche einer Organisation einzelne Bausteine beschrieben
- Applikation, System, Organisation usw.

## Betriebssysteme

### Stand der Technik

- Rechtsformulierung da sich Gesetze langsamer als die Technik entwickeln
- Hinweise auf Stand der Technik geben bspw. IT-Grundschutz Bausteine

### E-Mail Header

- Folgende Angaben kann der Angreifer manipulieren: From, To, Date, Subject, Message-ID
- praktisch manipulationssicher: Received
- good to know: G Suite Toolbox Nachrichten-Header

#### Aufbau eines E-Mail-Headers

<!--ToDo-->

#### Received-Einträge im E-Mail Header

- jeder Mailrouter, der Mail verarbeitet fügt sich dieser Liste hinzu
- Anomalien leicht feststellbar
- Phishingmails darüber identifizieren

### Windows Registry

- verschiedene Datenbanken (Registry Hives) die dort als Datei vorliegen auf dem Datenträger
- Speicherung von Einstellungen in der Registrierungsdatenbank:
  - gespeicherte Daten in sogenannten Registrierungshives aufgeteilt und in Keys mit Values abgelegt
  - Datenbanken existieren in Form von Dateien im Verzeichnis

### Volume Shadow Copy

- Snapshots eines `NTFS` Volumes (pro `NTFS` Volume 64 Snapshotkopien)
- arbeitet auf `copy` und `write` Basis
- alte Zustände eines Volumes abrufen
- aller 7 Tage, bei Patches, Treibersoftware etc. erstellt

### Alternate DataStream

- `Data`-Attribut mit `DataRuns` mit Clusternummern mit eigentlichen Dateininhalten
- zusätzlich `Alternate Data Streams` anhängen mit weiteren Infos zur Datei
  - z.B. lokaler Ursprung der Datei bzw. aus Internet
- man kann darin Dateien verstecken (wie Schadsoftware)

### Windows SID

- `SID` wird pro Benutzergruppe/Benutzerkonto **eindeutig** vergeben

> $\rightarrow$ nachvollziehen, wer was geändert hat

- Benutzerrechte damit zuweisen
- welcher Nutzer hat Zugriff, wer hat es angelegt und wer hat es geändert
- ob Nutzer gelöscht wurden, die daran etwas gemacht haben
- Log-Dateien bzgl. Löschvorgangs/Änderung an Nutzerkonten
- `SID` bleibt immer identisch

### macOS-Frage

<!--ToDo: Was könnte gefragt werden?-->

### Interessante Linux-Anwendungsprotokolle

- `apache2`
- `httpd`
- `samba`
- `mysqld`

## Techniken der Spurensuche und RAM Analyse

### Dateitypüberprüfung

- Dateien ohne Dateiendung analysieren & Dateityp identifiziert
- durch Header & Footer Informationen

#### Magic-Bytes

<!-- ToDo -->

### FileCarving

- Suche nach Dateien, die gelöscht wurden
- nicht mehr im allokierten Speicher, aber noch drauf sind
- z.B. mit Hex-Editor

### Kernel Level Sicherung

- Systemkern speichert `RAM` Inhalte
- versch. Tools je nach Betriebssystem
- Vorteil zu User Level: gesamter `RAM` gesichert und nicht selektive Sicherung

### Cold Boot

- `RAM` Sicherungsmethode
- `RAM` heruntergekühlt um kurzzeitig Stromzufuhr zu unterbrechen + keine Inhalte verlieren
- mit/ohne Transfer, ohne/mit Livesystem

### Volatility Framework

- Framework zum Analysieren von `RAM`-Abbildern

### Plist-Dateien

- Property List Dateien: Key-Value-Paare
- vorallem unter macOS vorhanden, als Konfigurationsdateien
- vom Aufbau `XML`-Dateien mit spezifischen Schlüsselpaaren
  - welche Konfigurationsparameter, wurden wann und von wem zuletzt geändert

### Hinweise auf einen Einbruch

- wenn Rechner auffällig langsam wird
- verdächtige/unbekannte Prozesse im Taskmanager prüfen
- Auffälligkeiten bei Netzwerkverbindungen
- Auffälligkeiten in Log-Dateien (unvollständig/geleert)
- unbekannte Benutzer, besonders Admin Accounts
- Meldungen von Antiviren-Software, Protokolldateien der Software prüfen

## Dateisysteme

### Sektoren

- Zusammenfassung von Bytes in einem Block

### Cluster

- Zusammenfassung mehrerer Sektoren
- Clustergröße bei Formatierung festlegbar
- einzelne Bytes zu Block zusammengefasst <!-- ToDo: vgl. Sektoren^^ -->

> **Betriebssystem arbeitet Clusterweise** $\rightarrow$ es werden immer ganze Cluster gespeichert

### Aufbau FAT-Dateisystem

<!-- Folie 5-15 (done) und Folie 5-21 (TODO) -->

- FAT-Dateisystem = FileAllocationTable (FAT) + DirectoryEntries
- Partition:
  - Bootsektor + Partitionskennung
  - Reservierte Sektoren
  - FAT Bereich
  - Datenbereich mit Verzeichniseinträgen

#### ROOT-verzeichnis bei FAT

- im Datenbereich beim FAT-Datenträger
- `FAT12`, `FAT16` $\rightarrow$ direkt im Anschluss an die FAT
- `FAT32` $\rightarrow$ kann überall beginnen, meist in den Sektoren direkt nach der FAT
- Root Verzeichnis finden: boot Sektor ansehen, wie viele reservierte Sektoren, zwei im Offset und ein paar mehr $\rightarrow$ dann diese Zahl ist das gesuchte ROOT-Datenverzeichnis

### Master Boot Record (MBR)

<!-- ToDo -->

### GUID Partition Table (GPT)

<!-- ToDo -->

### Master File Table

- Teil des `NTFS` Dateisystem
- Datei auf dem Datenträger die Infos über alle anderen Dateien & Verzeichnisse enthält
- enthält verschiedene Informationen über Aufbau des Datenträgers
- Datenbank mit Adressen zu jeder Datei auf den Datenträger, jede Datei besitzt MFT Eintrag mit verschiedenen Attributen
- wichtigste Attribute: Filename, Standard-Attribut (Meta-Daten, wann wurde es angelegt etc.), Data-Attribut (enthält Daten direkt (wenn klein genug, `MFT` Eintrag ist meist 1024 Bytes groß), sonst DataRuns)
- Datei (vgl. Datenbank) mit Einträgen zu allen Dateien/Verzeichnissen
- Attribute: Filename, Metadaten, Data (Daten selbst oder DataRuns)

### $DATA Attribut

- Attribut im `NTFS`-Dateisystem
- die tatsächlichen Daten, die in die Datei geschrieben wurden
- direkte Daten oder `DataRuns`

### Slackspeicher

- Ursprung: interne Fragmentierung
- Cluster wird nicht komplett durch eine Datei ausgenutzt, ist aber komplett ausgefüllt $\rightarrow$ **verbleibender Bereich = Slackspeicher**
- Slackspeicher kann alte Daten beinhalten
- z.B. bei `FAT` oder `NTFS`, aber **nicht bei `ext`**

### MAC-Zeitstempel

<!-- ToDo: HELP -> Hat nichts mit MacOS zu tun, oder? -->

- jedes Betriebssystem besitzt Zeitstempel
- Modification, Access, Change/Creation-Time

### Superblock

> alle wichtigen Infos zum `ext`-Dateisystem

- Adresse des ersten Blocks
- Blockgröße
- Blockgruppengröße
- Anzahl freier Inodes
- ...

### Aufbau ext3 / ext4-Dateisystem

<!--TODO-->

### Umgang mit Dateien im Ext-Dateisystem

- Superblock & Gruppendeskriptortabelle (wie viele freie Blöcke pro Block, weitere Infos zu Inodes z.B. Inode mit 2 ist immer Rootverzeichnis)

### DataRuns

- bestehen aus einer Anzahl an Clustern, besitzen Clusternummern die dazugehören
- über diese Clusternummern lässt sich Datei zusammenbauen
- Liste von Clustern

## Windows-Zusatz

<!-- Coming soonTM -->