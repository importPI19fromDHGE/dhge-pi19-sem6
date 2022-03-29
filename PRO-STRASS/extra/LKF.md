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

<!-- ToDo -->

### Dunkelfeld

<!-- ToDo -->

### Digitale Spuren

<!-- ToDo -->

#### Spurenträger

<!-- ToDo -->

### Locard'sche Prinzip

<!-- ToDo -->

### Forensischer Arbeitsplatz

<!--ToDo-->

### Forensic Readiness

<!-- ToDo -->

### Schreibschutzadapter

<!-- ToDo -->

#### Datenintegrität

<!-- ToDo -->

### Vorgehensmodelle

#### BSI-IT-Forensik-Leitfaden

#### S-A-P-Modell

<!-- ToDo: ein Schwerpunkt! -->

#### Post-moretem-Forensik

<!-- ToDo -->

#### Live-Forensik

<!-- ToDo -->

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

<!-- ToDo -->

### Grundsätze der digitalen Beweisführung

<!-- ToDo -->

### Identifikationsphase

<!-- ToDo -->

### Leitfäden nach ISO 27037

<!-- ToDo -->

### Mitnahme vs. Sicherung

<!-- ToDo -->

### Totmannschaltung

<!-- ToDo -->

### Grundlegende Maßnahmen für ausgeschaltete digitale Geräte

<!-- ToDo -->

### Grundlegende Maßnahmen für eingeschaltete digitale Geräte

<!-- ToDo -->

### Erhebung von nicht digitalen Beweismitteln

<!-- ToDo -->

### Besonderheiten bei der Sicherung digitaler Beweismittel

<!-- ToDo -->

### Hashwerte

<!-- ToDo -->

## Betriebssysteme

### CERT

<!-- ToDo -->

### BSI IT-Grundschutz Kompendium

<!-- ToDo -->

### Stand der Technik

<!-- ToDo -->

### Received-Einträge im E-Mail Header

<!-- ToDo -->

### Windows Registry

<!-- ToDo -->

### Volume Shadow Copy

<!-- ToDo -->

### Alternate Data Stream

<!-- ToDo -->

### Windows SID

<!-- ToDo -->

## Techniken der Spurensuche und RAM Analyse

### Dateitypüberprüfung

<!-- ToDo -->

### FileCarving

<!-- ToDo -->

### Post Mortem Forensik

<!-- ToDo -->

### Live Forensik

<!-- ToDo -->

### Kernel Level Sicherung

<!-- ToDo -->

### Cold Boot

<!-- ToDo -->

### Volatility Framework

<!-- ToDo -->

### Plist-Dateien

<!-- ToDo -->

### Hinweise auf einen Einbruch

<!-- ToDo -->

## Dateisysteme

<!-- ToDo -->

### Sektoren

<!-- ToDo -->

- einzelne Bytes zu Block zusammengefasst

### Cluster

<!-- ToDo -->

- Betriebssystem arbeitet Clusterweise $\rightarrow$ es werden immer ganze Cluster gespeichert

### ROOT-verzeichnis bei FAT

<!-- ToDo -->

### Master File Table

<!-- ToDo -->

- Datei (vgl. Datenbank) mit Einträgen zu allen Dateien/Verzeichnissen
- Attribute: Filename, Metadaten, Data (Daten selbst oder DataRuns)

### $DATA Attribut

<!-- ToDo -->

- NTFS-Dateisystem
- direkte Daten oder DataRuns

### Slackspeicher

- Ursprung: interne Fragmentierung
- Cluster wird nicht komplett durch eine Datei ausgefüllt, ist aber komplett ausgefüllt -> verbleiende Bereich = Slackspeicher (kann alte Daten beinhalten)
- z.B. bei FAT oder NTFS, aber nicht ext

### MAC-Zeitstempel

<!-- ToDo -->

- Modification, Change, Access-Time

### Superblock

<!-- ToDo -->

- alle wichtigen Infos zum ext Dateisystem (Adressedes ersten Blocks, Blockgröße, Blockgruppengröße, freie Inodes, ...)

### Umgang mit Dateien im Ext-Dateisystem

<!-- ToDo -->

### DataRuns

<!-- ToDo -->

- Liste von Clustern

## Windows-Zusatz

<!-- Coming soonTM -->
