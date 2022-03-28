# LKF - Computerforensik

## Grundlagen der Beweisführung

### Multimedia-Forensik

<!-- ToDo -->

### Dunkelfeld

<!-- ToDo -->

### Digitale Spuren

<!-- ToDo -->

### Locard'sche Prinzip

<!-- ToDo -->

### Forensic Readiness

<!-- ToDo -->

### Schreibschutzadapter

<!-- ToDo -->

### S-A-P-Modell

<!-- ToDo -->

### Post-moretem-Forensik

<!-- ToDo -->

### Live-Forensik

<!-- ToDo -->

## ISO27037 und Tatorfotografie

### Beteiligte Akteuere inder ISO27037

<!-- ToDo -->

### Grundsätze der digitalen Beweisführung

<!-- ToDo -->

### Identifikationsphase

<!-- ToDo -->

### Mitnahme vs. Sicherung

<!-- ToDo -->

### Totmannschaltung

<!-- ToDo -->

### Mitnahme von ausgeschalteten digitalen Geräten

<!-- ToDo -->

### Erhebung von nicht digitalen Beweismitteln

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
