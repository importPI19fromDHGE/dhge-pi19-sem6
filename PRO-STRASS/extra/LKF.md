# LKF - Computerforensik

## Grundlagen und Beweisführung

### Definition Digitale Forensik

- **Forensik:** systematischenUntersuchung von kriminellen Handlungen
- **Digitale Forensik:**

<!-- ToDo: PPT 1 - Folie 33 -->

### Ziele digitaler Forensik

<!-- PPT 1 - Folie 34  -->

- Identifikation des Angreifers
- Erkennen der Methode
- Ermittlung des Schadens
- Sicherung der Beweise

### Arbeitsgebiete digitaler Forensik

<!-- PPT 1 - Folie 35 -->

- Datenträger-Forensik
- Mobilfunk-Forensik
- Netzwerk-Forensik
- Multimedia-Forensik
- Cloud-Forensik
- Memory-Forensik
- Car Forensik
- IoT-Forensik
- Forensische Linguistik

#### Multimedia-Forensik

- Feststellung von Spuren bzw. Manipulationen in Bildern/Videos/Audio
- Arbeitsgebiet der digitalen Forensik

### Dunkelfeld

Der Bereich, der Cyber-Straftaten, die nicht in der polizeilichen Kriminalstatistik erfasst wird, da es nicht entdeckt wird.

#### Gründe für nicht entdecken

- gute Angreifer (wird nicht entdeckt)
- mangelnde Schutzvorkehrung
- Firmen melden Vorfälle wegen Imageschäden/Zeitdruck (schnell wieder einsatzfähig sein)
- Kein Interesse an forensischer Aufarbeitung nicht

### Digitale Spuren

Metadaten/Computerdaten, die aufgrund unseres Verhalten angelegt werden (Arbeitsspeicher, auf Datenbanken etc.)

#### Unterschiede im Gegensatz zu analogen Spuren

- digitale Spuren entstehen im Hintergrund
- können flüchtig sein, sind leicht änderbar
- können verschlüsselt sein
- liegen physisch auf Datenträger vor und müssen dann logisch interpretiert werden um lesbar zu werden

#### Spurenträger

<!-- ToDo -->

### Locard'sche Prinzip

Keine Person (Täter/Opfer/Ermittler) kann einen Tatort betreten & verlassen ohne Spuren zu hinterlassen

Jeder der mit Tatort interagiert hinterlässt/verändert Spuren oder nimmt etwas mit. Auch bei digitalen Spuren

### Forensischer Arbeitsplatz

<!--ToDo-->

### Forensic Readiness

Wenn etwas passiert, auf strategischer und operativer Ebene, bereit sein für forensische Prozesse durch forensischen Arbeitsplatz

Systeme sollen so konfiguriert sein, dass man digitale Spuren sammeln kann, schneller im Ernstfall agieren, Kosten sparen

#### Drei Säulen

- forensische Workstation (sehr potente Hardware)
- Office Computer für schriftliche Sachen (Dokumentation) ohne Verbindung zum Netzwerk oder nur interne Verbindung, aber kein Internetzugang
- Internetcomputer für Recherche

→ im Idealfall drei physische Rechner

### Schreibschutzadapter

Gerät zwischen Datenträger und Auslesegerät, verhindert dass Auslesegerät den Inhalt auf dem Datenträger verändern kann.

#### Datenintegrität

- Sichern: nach gewissen Vorgehen, damit man nichts verändert

- Analysieren: Wer/Wann/Wo/Wie/Was

- Präsentieren bzw. Aufbereiten: Ergebnisse so aufarbeiten, dass sie Auftraggeber pärsentieren kann

### Vorgehensmodelle

#### BSI-IT-Forensik-Leitfaden

#### S-A-P-Modell

<!-- ToDo: ein Schwerpunkt! -->

#### Post-moretem-Forensik

“nach dem Tod” Hierbei werden nach einem Vorfall Daten erhoben und analysiert z.B. Datenträger-Forensik

Wenn Rechner ausgeschaltet ist & Festplatte ausbaubar, dann an forensische Maschine anschließen & Daten 1:1 kopieren kann

#### Live-Forensik

Während das System noch läuft, findet die Untersuchung eines Vorfalls statt

Daten live abziehen, wenn das System noch läuft

Wenn kein physischer Zugriff/man weiß nicht was drauf läuft/evtl. Verschlüsselung bei herunterfahren

### logische vs. physikal Sicherung

<!-- ToDo -->

### Post-Mortem vs. Live-Forensik

<!-- ToDo -->

## ISO 27037 und Tatorfotografie

### Beteiligte Akteuere in der ISO 27037

<!-- ToDo -->

### Allgemeine Schritte nach ISO 27037

<!-- ToDo -->

### Durchführung einer Risikobeurteilung

Ersteinschreiter für digitale Beweismittel (DEFR): Befugt ist die ersten Maßnahmen am Tatort/an den Systemen vorzunehmen, der über Sicherungsmethode entscheidet & über Methode der Mitnahme

Spezialist für digitale Beweismittel (DES): kümmert sich um Analyse, kann Aufgaben des DEFR übernehmen, aber zusätzlich noch Analysen

### Grundsätze der digitalen Beweisführung

Relevanz, Vollständigkeit, Verlässlichkeit

- alle Maßnahmen dokumentieren
- Methoden anwenden, mit welchen die Fehlerfreiheit und Verlässlichkeit der Kopie von potentiellen digitalen Beweismitteln festgestellt werden kann
- Erkennen, dass der Vorgang der Erhaltung von potentiellen digitalen Beweismitteln nicht immer eingriffsfrei erfolgen kann

### Identifikationsphase

nach ISO Ersteinschreiter wird tätig und sucht nach Beweismitteln, diese können in physischer und logischer Form vorliegen

physischer: Vorhandensein auf konkreten Gerät, die Zustände der einzelnen Datenträgern auf Bitebene

logischer: physische Form interpretieren z.B. Mithilfe Betriebssystem oder Dirttanwendersoftware

logische Form soll dargestellt und gesichert werden

- soll Speichermedien und alle datenverarbeitenden Geräte alle identifizieren (die vorfallrelevant sein können)
- Priorisierung der Beweismittelerhebung auf Grundlage der Flüchtigkeit der Daten
- Ein- oder ausgeschalteter Zustand der Geräte

### Leitfäden nach ISO 27037

<!-- ToDo -->

### Mitnahme vs. Sicherung

Entscheiden, ob man das Gerät an sich braucht oder nur Daten auf der Festplatte

Wichtiges Entscheidungskriterium: ist das Gerät aus oder an? Wenn es an ist → Live Forensik Vorort mögl. oder mit Stromzufuhr Mitnahme oder Sicherung Vorort vornehmen (gerade bei schweren Geräten, die man erst ausschalten müssen oder so, bei systemkritischer Technik)

### Totmannschaltung

Mechanismus, der ausgelöst wird wenn die Bestätigung durch einen Menschen ausbleibt

im digital forensischen Umfeld Manipulationen am Tatort: ausschalten/abziehen eines Geräts, entfernen eines Tokens (z.B. abziehen eines USB-Sticks) kann zur Verschlüsselung des Systems führen

### Grundlegende Maßnahmen für ausgeschaltete digitale Geräte

<!-- ToDo -->

### Grundlegende Maßnahmen für eingeschaltete digitale Geräte

- drauf achten, ob Gerät WIRKLICH ausgeschaltet ist z.B. durch Status-LED, Maus bewegen
- Ein- und Ausschaltknöpfe abkleben → während Transport keine Zustandsänderungen
- Kabel etc. vom Gerät trennen, kennzeichnen an welchem Port diese waren
- Stromzufuhr trennen: zunächst am Gerät trennen, damit keine unterbrechungsfreie Stromzufuhr ausgelöst wird
- bei Transport: Anti-Statik Beutel, keine Beschädigungen des Gerätes

### Erhebung von nicht digitalen Beweismitteln

- digitaler Ersteinschreiter sollte nicht nur digitale Beweismittel erhalten, sondern auch nicht digitale Beweismittel berücksichtigen
- z.B. Personen, die für das Büro Vorort verantwortlich sind, Zugänge von diesen Personen herausgeben lassen
- diese Personen können zusätzliche Infos für Doku herausgeben → relevante Details aus Gesprächen mit aufnehmen, Name und Position der Person dokumentieren
- Hinweise die z.B. Passwort herausgeben (Post It Zettel), andere weitere Notizen

### Besonderheiten bei der Sicherung digitaler Beweismittel

<!-- ToDo -->

### Hashwerte

Ein einzigartiges Rechenergebnis aus einer Bitfolge

Für Überprüfung von Datenmanipulation (Integrität sicherstellen)

Illegale Daten finden z.B. Kinderporngrafie

Systemspezifische Daten gleich ausblenden

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

- Framework zum analysieren von RAM Abbildern

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
- FAT32 → kann überall beginnen, meist in den Sektoren direkt nach der FAST
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
- Cluster wird nicht komplett durch eine Datei ausgefüllt, ist aber komplett ausgefüllt -> verbleiende Bereich = Slackspeicher (kann alte Daten beinhalten)
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
