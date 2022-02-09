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

- [Platzhalter](#platzhalter)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!--newpage-->

# Digitale Rettungskette

digitale Ersthelfer $\rightarrow$ Vorfall-Experten $\rightarrow$ IT-Sicherheits-Dienstleister

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

- liegt ein Datenschutzvorfall vor, besteht eine Meldepflicht (beim BSI)
- kritische Infrastrukturen sind stärker meldepflichtig, als einfache private Unternehmen
- der Vorfall-Experte ist **nicht** für die Meldung verantwortlich!
- die Meldepflicht liegt immer bei der Geschäftungsführung des Unternehmens
- als Vorfall-Experte niemals ohne Zustimmung melden!

# Was ist Forensik?

beschäftigt sich mit der systematischen Untersuchung von kriminellen Handlungen

# Was ist digitale Forensik?

ist die streng methodisch vorgenommene Datenanalyse auf Datenträgern und Computernetzen zur Aufklärung von Vorfällen unter Einbeziehung der Möglichkeiten der strategischen Vorbereitung insbesondere aus der Sicht des Anlagenbetreibers eines IT-Systems [BSI-Leitfaden IT-Forensik, 2011]

# Worum geht es bei der Computer Forensik?

- Nachweis und Ermittlung von Straftaten aus dem Bereich der Computerkriminalität

# Ziele der forensischen Analyse

- Identifikation des Angreifers
- Erkennen der Methode
- Ermittlung der Schadens
- Sicherung der Beweise

# Arbeitsgebiete der digitalen Forensik

- Datenträger-, Multimedia-, Car-, Mobilfunk-, Cloud-, IoT-, Netzwerk-, Memory-Forensik
- Forensische Linguistik
- Überschneidungen zu anderen Gebieten der Informationssicherheit
  - Forensic Intelligence (Predictive Policing, Untersuchung von Radikalisierung im Internet)
  - Informationssicherheitsmanagement
  - Schadsoftware-Analyse / Reverse Engineering
  - Untersuchungen im Darknet
  - Kryptowährungen / Blockchain-Untersuchung

# Herausforderungen der digitalen Forensik

- Massendaten in der Datenträger-Forensik: Datenmengen immer größer, Speicherplatz immer günstiger
- Faktor Zeit: bis zur Entdeckung eines Vorfalls vergehen oft Monate

# Klassifizierung der Täter

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

# Indikatoren für gefährdete Mitarbeiter

- Unzufriedenheit am Arbeitsplatz
- fehlende Identifikation mit dem Unternehmen
- Auffällige Neugier
- Nutzung von Spionagehilfsmitteln (z.Bsp. Bild- und Tonaufzeichnungsgeräte, mobile Datenträger)
- Auffälligkeiten im persönlichen Umfeld (aufwändiger Lebensstil, Anzeichen für Alkohlsuch etc.)
- ...

# Was sind Spuren?

- sind materielle Veränderungen an Personen oder Objekten
- stehen im Zusammenhang mit relevanten Ereignissen
- können zur Tataufklärung beitragen, da sie Rückschlüsse auf den Tatablauf und den Täter geben

# Was sind digitale Spuren?

- basieren auf Daten, welche in Computersystemen gespeichert sind oder übertragen wurden
- werden erst durch ihre Interpretation von physischen Spuren über unterschiedliche Interpretationsebenen zu verwertbaren Spuren

# Was beschreibt das Locard'sche Prinzip?

Es gibt keinen Tatort ohne Spuren!

# Primäres und sekundäres Ziel des Vorgehensmodells der digitalen Forensik

- Primär: Aufklärung
- Sekundär: Vorsorge

# Ziele der IT-Forensik

- Sicherstellung von belastendem und entlastendem Beweismaterial
- sichergestellte Daten sollen systematisch analysierbar sein
- Rekonstruktion zuvor stattgefundener Ereignisse
- Daten müssen gerichtsverwertbar aufbereitet und analysiert werden

# Zwei Varianten der IT-Forensik (auf jeden Fall merken!)

- Post-mortem Forensik
- Live-Forensik

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
