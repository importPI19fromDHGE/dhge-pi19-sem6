<!----------
title: "Computerforensik"
date: "Semester 6"
keywords: [Computerforensik, Forensik, DHGE, Semester 6]
header-includes:

  - \usepackage{enumitem}
  - \setlistdepth{20}
  - \renewlist{itemize}{itemize}{20}
  - \renewlist{enumerate}{enumerate}{20}
  - \setlist[itemize]{label=$\cdot$}
  - \setlist[itemize,1]{label=\textbullet}
  - \setlist[itemize,2]{label=--}
  - \setlist[itemize,3]{label=*}

---------->

Computerforensik
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Organisatorisches](#organisatorisches)
- [Intro](#intro)
- [Digitale Rettungskette / Cyber Security Netzwerk (CSN)](#digitale-rettungskette--cyber-security-netzwerk-csn)
- [häufige Angriffsvektoren](#h%C3%A4ufige-angriffsvektoren)
- [Relevante Gesetze](#relevante-gesetze)
- [Datenschutzvorfälle](#datenschutzvorf%C3%A4lle)
  - [Beispiele für meldepflichtige Datenschutzvorfällen](#beispiele-f%C3%BCr-meldepflichtige-datenschutzvorf%C3%A4llen)
- [Was ist Forensik?](#was-ist-forensik)
- [Was ist digitale Forensik?](#was-ist-digitale-forensik)
  - [Worum geht es bei der Computer Forensik?](#worum-geht-es-bei-der-computer-forensik)
  - [Ziele der forensischen Analyse](#ziele-der-forensischen-analyse)
  - [Arbeitsgebiete der digitalen Forensik](#arbeitsgebiete-der-digitalen-forensik)
  - [Herausforderungen der digitalen Forensik](#herausforderungen-der-digitalen-forensik)
  - [Klassifizierung der Täter](#klassifizierung-der-t%C3%A4ter)
  - [Herausforderungen in der IT-Forensik](#herausforderungen-in-der-it-forensik)
- [Indikatoren für gefährdete Mitarbeiter](#indikatoren-f%C3%BCr-gef%C3%A4hrdete-mitarbeiter)
- [Was sind Spuren?](#was-sind-spuren)
  - [Was sind digitale Spuren?](#was-sind-digitale-spuren)
  - [Was beschreibt das Locard'sche Prinzip?](#was-beschreibt-das-locardsche-prinzip)
- [Primäres und sekundäres Ziel des Vorgehensmodells der digitalen Forensik](#prim%C3%A4res-und-sekund%C3%A4res-ziel-des-vorgehensmodells-der-digitalen-forensik)
- [Ziele der IT-Forensik](#ziele-der-it-forensik)
- [Zwei Varianten der IT-Forensik (auf jeden Fall merken!)](#zwei-varianten-der-it-forensik-auf-jeden-fall-merken)
- [Einordnung digitale Forensik](#einordnung-digitale-forensik)
- [S-A-P-Modell](#s-a-p-modell)
- [Grundlage des Ablaufs einer forensischen Untersuchung (BSI-Leitfaden)](#grundlage-des-ablaufs-einer-forensischen-untersuchung-bsi-leitfaden)
- [Anforderungen an eine neue Methode im forensischen Prozess](#anforderungen-an-eine-neue-methode-im-forensischen-prozess)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

Haupt-Editoren für dieses Dokument: RvNovae

<!--newpage-->

# Organisatorisches

<!-- md2apkg ignore-card -->

- Prüfung: 40 min (?)
- Schwerpunkte werden zu Beginn der Veranstaltungen wiederholt
- Theorie, Forensik: Datenträger, Demo und Übung auf VMs

<!--newpage-->

# Intro

<!-- md2apkg ignore-card -->

- Digitalisierung ermöglicht neue Schnittstellen, neue Angriffspunkte und Straftaten
- Nutzung MS Teams <!-- LOL --> steigt exponentiell seit 2019 (auch dank Corona)
- Telekom: Angriffe auf HoneyPots stiegen in letzten Jahren erheblich
- bessere Infrastruktur (viele Menschen haben Mittel um anzugreifen)
- Tools zum Erstellen von Schadprogrammen (Script-Kiddies)
- Rentable Form der Kriminalität
- täglich neue Angriffsmuster

# Digitale Rettungskette / Cyber Security Netzwerk (CSN)

![CSN](assets/Rollen_CSN.png)<!--width=200px-->

- Meldungen gehen an "Digitalen Ersthelfer"
  - ehrenamtliche Arbeit beim BSI
  - telefonischer first Level Support
  - qualifizierte Einschätzung des Vorfalls
  - dokumentiert Vorgang
- Weiterleitung an Vorfall-Experte / IT-Forensiker
  - meist selbstständig oder Dienstleister
  - Telefonsupport, Vor-Ort-Unterstützung
  - zusätzliche forensische Untersuchungen
- Weiterleitung an IT-Sicherheitsdienstleister

# häufige Angriffsvektoren

- technische Sicherheitslücken
- Social Engineering (Analog/Digital)
  - Phishing-Mails
  - Impersonation
- Diebstahl/Verlust von IT-Geräten

# Relevante Gesetze

- IT-Sicherheitsgesetz
- Datenschutzgrundverordnung
- Bundesdatenschutzgesetz
- Telemediengesetz
- Telekommunikationsgesetz
- Gesetz gegen den unlauteren Wettbewerb
- Urheberrechtsgesetz
- IT-Strafrecht im Strafgesetzbuch

# Datenschutzvorfälle

- liegt ein Datenschutzvorfall vor, besteht eine Meldepflicht (beim BSI) $\rightarrow$ ASAP, es darf keine Verzögerung geben
- kritische Infrastrukturen sind stärker meldepflichtig, als einfache private Unternehmen
- der Vorfall-Experte ist **nicht** für die Meldung verantwortlich!
- die Meldepflicht liegt immer bei der Geschäftungsführung des Unternehmens
- als Vorfall-Experte niemals ohne Zustimmung melden, die Verantwortung liegt bei der Geschäftsleitung!
- Meldepflichten können sich aus gesetzlichen oder vertraglichen Vorgaben sowie freiwillig ergeben
- als KRITIS-Betreiber muss jede **Störung** unverzüglich gemeldet werden
- betroffene Personen sind zu informieren

## Beispiele für meldepflichtige Datenschutzvorfällen

- Cyberangriff führte zum Diebstahl von Kreditkartennummern
- Versand von E-Mail-Werbung trotz bestätigter Löschanfrage
- Verlust eines unverschlüsselten USB-Sticks
- fehlende Transportverschlüsselung bei Online-Registrierungen

# Was ist Forensik?

beschäftigt sich mit der systematischen Untersuchung von kriminellen Handlungen

# Was ist digitale Forensik?

ist die streng methodisch vorgenommene Datenanalyse auf Datenträgern und Computernetzen zur Aufklärung von Vorfällen unter Einbeziehung der Möglichkeiten der strategischen Vorbereitung insbesondere aus der Sicht des Anlagenbetreibers eines IT-Systems [BSI-Leitfaden IT-Forensik, 2011]

## Worum geht es bei der Computer Forensik?

- Nachweis und Ermittlung von Straftaten aus dem Bereich der Computerkriminalität

## Ziele der forensischen Analyse

- Identifikation des Angreifers
- Erkennen der Methode
- Ermittlung der Schadens
- Sicherung der Beweise

## Arbeitsgebiete der digitalen Forensik

- Datenträger-, Multimedia-, Car-, Mobilfunk-, Cloud-, IoT-, Netzwerk-, Memory-Forensik
- Forensische Linguistik
- Überschneidungen zu anderen Gebieten der Informationssicherheit
  - Forensic Intelligence (Predictive Policing, Untersuchung von Radikalisierung im Internet)
  - Informationssicherheitsmanagement
  - Schadsoftware-Analyse / Reverse Engineering
  - Untersuchungen im Darknet
  - Kryptowährungen / Blockchain-Untersuchung

## Herausforderungen der digitalen Forensik

- Massendaten in der Datenträger-Forensik: Datenmengen immer größer, Speicherplatz immer günstiger
- Faktor Zeit: bis zur Entdeckung eines Vorfalls vergehen oft Monate

## Klassifizierung der Täter

nach:

- Fähigkeiten
  - Sicherheitsexperten
  - Exploit-Programmierer
  - Script-Kiddies
- Organisationsformen
  - Alleine
  - Gruppe oder vernetzte Gruppe (Peer Groups)
- Motivationslage
  - Sozial, technisch, politisch, finanziell, staatlich

## Herausforderungen in der IT-Forensik

- die Daten werden mehr, damit die benötigte Zeit (oft Monate)
- hohe Dunkelziffer an Angriffen

# Indikatoren für gefährdete Mitarbeiter

- Unzufriedenheit am Arbeitsplatz
- fehlende Identifikation mit dem Unternehmen
- Auffällige Neugier
- Nutzung von Spionagehilfsmitteln (z.Bsp. Bild- und Tonaufzeichnungsgeräte, mobile Datenträger)
- Auffälligkeiten im persönlichen Umfeld (aufwändiger Lebensstil, Anzeichen für Alkohlsuch etc.)
- Diskrepanzen im beruflichen Werdegang (Über/Unter-Qualifizierung)
- zweifelhafte Dateien/PDF bei der Bewerbung (enthält Malware)

# Was sind Spuren?

- sind materielle Veränderungen an Personen oder Objekten
- stehen im Zusammenhang mit relevanten Ereignissen
- können zur Tataufklärung beitragen, da sie Rückschlüsse auf den Tatablauf und den Täter geben

## Was sind digitale Spuren?

- basieren auf Daten, welche in Computersystemen gespeichert sind oder übertragen wurden
- werden erst durch ihre Interpretation von physischen Spuren über unterschiedliche Interpretationsebenen zu verwertbaren Spuren

## Was beschreibt das Locard'sche Prinzip?

Es gibt keinen Tatort ohne Spuren!

# Primäres und sekundäres Ziel des Vorgehensmodells der digitalen Forensik

- Primär: Aufklärung
  - Sicherstellung be- und entlastenden Beweisen
  - sichergestellte Daten müssen systematisch analysierbar und gerichtsverwertbar sein
  - Rekonstruktion der Ereignisse
- Sekundär: Vorsorge
  - KVP!!!
  - Abschreckung vor zukünftigen Straftaten

# Ziele der IT-Forensik

- Sicherstellung von belastendem und entlastendem Beweismaterial
- sichergestellte Daten sollen systematisch analysierbar sein
- Rekonstruktion zuvor stattgefundener Ereignisse
- Daten müssen gerichtsverwertbar aufbereitet und analysiert werden
- W-Fragen klären

# Zwei Varianten der IT-Forensik (auf jeden Fall merken!)

- Post-mortem Forensik
- Live-Forensik

# Einordnung digitale Forensik

- Modell
  - Ablauf für Untersuchungen in vereinfachter, schematischer Weise
- Prozess
  - Ablauf .. in detaillierter Form, Zuständigkeiten
- Methode
  - Vorgabe für einzelne Schritte, Handlungsanweisungen

# S-A-P-Modell

- Secure
  - strategische und operative Vorbereitungen zur Erfassung aller relevanten Daten durchführen
- Analyse
  - hier werden die gesicherten Spuren und Beweise überprüfbar aufgearbeitet, sorgfältig geprüft und objektiv bewertet
- Present
  - hier wird der Ermittlungsprozess nachvollziehabr dargelegt (präsentiert)

# Grundlage des Ablaufs einer forensischen Untersuchung (BSI-Leitfaden)

- basiert auf dem S-A-P-Modell und ergänzt es
- Strategische Vorbereitung $\rightarrow$ Operative Vorbereitung $\rightarrow$ Datensammlung $\rightarrow$ Datenreduktion $\rightarrow$ Datenanalyse $\rightarrow$ Dokumentation

# Anforderungen an eine neue Methode im forensischen Prozess

- Akzeptanz: Methoden sind in der Fachwelt anerkannt
- Glaubwürdigkeit: Funktionalität der Methoden ist nachweisbar
- Wiederholbarkeit: Ergebnisse ist durch Dritte reproduzierbar
- Integrität: Spuren werden durch Untersuchung nicht verändert
- Ursache und Auswirkungen: Verbindung zwischen digitalen Spuren, Ereignissen und Personen sind herstellbar
- Dokumentation: Ermittlungsprozess ist nachvollziehbar dokumentiert
- keine gesetzlichen Vorgaben für forensische Untersuchung

# Forensic Readiness

- beschäftigt sich mit Maßnahmen zur Vorbereitung auf digitale forensische Untersuchungen innerhalb Organisationen
- Ziele:
  - Systeme sollen in der Lage sein, bessere und belastbare digitale Spuren zu sammeln
  - Die Kosten für eine forensische Untersuchung sollen verringert werden
- Aus welchem Grund?
  - Art. 33 DSGVO (Meldung von Verletzung des Schutzes personenbezogener Daten an die Aufsichtsbehörden)

## Zielsetzung eines Betroffenen

- Schnelle Behebung:
  - Im Vordergrund steht dier zeitnahe Wiederverwendung der betroffenen Systeme
  - Die Ursache des Problems tritt in den Hintergrund
  - Es wird keine Sicherung von Beweisen gefordert
  - **Nachteil**: Es besteht die Gefahr, dass nicht in jedem Fall eine vollständige Bereinigung erzielt werden kann
- Vollständige Aufklärung:
  - Ganzheitlicher Ansatz zur gefahrlosen Wiederverwendung der entsprechenden Systeme
  - Es ist eine genaue Analyse durchzuführen, um Schadensausmaß und Angriffswege zu ermitteln
  - Beweissicherung durch Systemabbilder, Log-Dateien und Erfassen des Netzwerkverkehrs
  - **Nachteil**: Heterogene Systemlandschaften erfordern ein hohes Maß an Analyse und Know-How $\rightarrow$ Zeitaufwendig

## Forensic Readiness: Dimensionen

- personelle, technische und organisatorische Maßnahmen und Methoden
- Maßnahmen und Methoden werden durch rechtliche Aspekte beeinflusst

## Der forensische Arbeitsplatz

Die Basis für die Untersuchung der Beweismittel stellt der Analysecomputer dar, welcher als eigenständiges Gerät physikalisch getrennt vom Büro- und Internetcomputer eingerichtet sein sollte.

- Forensische Workstation
  - Sehr gute Hardwareausstattung auf aktuellem Stand der Technik
  - Duales Betriebssystem
  - Virenscanner und Firewall
- Office Computer für Schriftsachen
  - Verschlüsselung nutzen!
  - Interne Netzwerkanbindung, kein Internetzugang!
- Internet Computer
  - Keine sensiblen Daten eingeben oder speichern!
  - Aktuelle Anti-Viren-Software verwenden!
  - Auch als VM einsetzbar!

## Forensic Readiness: Transportable Workstations

Bei Außeneinsätzen bei denen Beweismittel vor Ort erhoben werden müssen, werden geeignete transportable Datensicherungsworkstations notwendig.

## Forensic Readiness: Schreibschutzadapter

- Für die Datensicherung im Labor, wie auch im Außeneinsatz, sind Schreibschutzadapter unerlässlich
- Grundlegend sollten folgende Schnittstellen abgedeckt werden: IDE, SATA, USB 3.0, FireWire
- Nice to have: SAS, SCSI, PCIE

## Forensic Readiness: Technische Maßnahmen

- auf Server-PCs: Logging und Gruppenrichtlinien konfigurieren
- für jeden Benutzer-PC: Betriebssysteme konfigurieren
- Beispiele:
  - Wiederherstellungs-Passworte für Festplatten-Verschlüsselung
  - lokales Logging aktivieren

## Forensic Readiness: Organisatorische Maßnahmen

- Responsive Teams
- Hardware und Sofware beschaffen
  - Forensik-Workstation
  - Forensik-Hardware
  - Forensik-Software
- Weitere Organisatorische Maßnahmen
  - Prozess für forensische Untersuchung aufbauen
  - Verantwortlichen benennen
  - Budget bereitstellen: Personal, Hardware, Software, Fortbildung
  - Kompetenzen aufbauen: für eigene Untersuchungen? für externe Beauftragungen?
  - Räumlichkeiten schaffen: Zutrittssicherheit, Tresor

## Forensic Readiness: Optionale Maßnahmen

- Planen! Untersuchungsziel präzise festlegen (lassen)!
- Vorauswahl an relevanten Datenquellen treffen
- Entscheiden:
  - Post-mortem-Forensik? Live-Forensik?
  - Welche Geräte / Datenträger / Daten?

# ???

# Datensammlung: Beweisführung im Zivil- oder Strafverfahren

- Sicherung digitaler Beweismittel und Spuren
- Die Sicherung von digitalen Beweisspuren kann auf zwei Arten geschehen:
- Logische Sicherung
  - auf Betriebssystemebene
  - mit Mitteln des Betriebssystems
  - Mit Drittanwendersoftware
  - erfolgt Betriebssystemabhängig
- Physikalische Sicherung
  - Auf Hardwareebene
  - mit hardwaretechnischen Hilfsmitteln
  - mit softwaretechnischen Hilfsmitteln
  - erfolgt Betriebssystem unabhängig

# Sicherung besonderer digitaler Beweismittel und Spuren

- Logfiles und Daten im Netzwerk
  - meist erfolgt eine logische Sicherung mit geeigneten Tools
- Flüchtige Daten / Hauptspeicherinhalte
  - kann direkt mittels DMA (Direct Memory Access) erfolgen
  - Cold-Boot
  - Auswertung erfolgt Post-Mortem

# Datensammlung: Die wichtigsten Regeln

- möglichst keine Veränderungen vornehmen an betroffenen digitalen Beweismitteln
- das bedeutet: Änderungen an Datenträgern mit geeigneten technischen Möglichkeiten sofern möglich unterbinden
- eine Dokumentation aller Arbeitsschritte, Veränderungen an Daten, mit konkreten Zeitangaben während der Sicherung von Daten ist unerlässlich
- Schreibblocker verwenden oder Datenträger mit Live-System als Read-Only mounten
- Hashwerte verwenden

# Hashwerte: Einsatzzwecke

- Datenintegritätsprüfungen
  - Überprüfung von Datensicherungen
  - Überprüfung von Passwörtern
- Dateninhaltsvergleiche
  - KiPo-Vergleich von Bildern in Kinderpornographie Verfahren mit Hash Datenbanken
  - Wirtschaftsspionage-Vergleich von Daten eines Unternehmens beim Auffinden in unternehmensfremden Umgebungen
  - NSRL (National Software Reference Library Hash Daten)-Herausfiltern von betriebssystemspezifischen Dateien ohne Relevanz
  - UrhG-Erkennen urheberrechtlich geschützter Werke durch Hash-Abgleich (MD4-Emule)

# mögliche forensische Untersuchungstechniken

- Wiederherstellen gelöschter Objekte
- Hashwertüberprüfungen
- File Carving
- Textsuchen
- Slack-Untersuchungen

# Datensammlung Software

- EnCase von Guidance Software
- FTK von Access Data
- X-Ways Forensics von X-Ways AG (!)
- The Sleuthkit und Autopsy
- DFF - Digital Forensic Framework

**kostenfreie Werkzeuge:**

- dd, ddrescue, dcfldd (Harbour), dc3dd (Kornblum)
- grep, strings, find
- hexdump
- ...

# Datensammlung

- wichtig: Verlaufsdokumentation!
  - Welche Daten gesammelt?
  - Wozu?
  - Wann?
  - Durch wen?
  - Wie?
  - Welches Zwischenergebnis?
  - Wann löschen?
- nützlich für:
  - kritische Nachfragen souverän beantworten
  - Zeitaufwand / Kosten berechnen
