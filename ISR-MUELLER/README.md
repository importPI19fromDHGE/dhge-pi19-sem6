<!----------
title: "IT-Infrastrukturen"
date: "Semester 6"
keywords: [IT, Infrastruktur, Recht, Sicherheit, DHGE, Semester 6]
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

IT-Infrastrukturen / Sicherheit / Recht
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Governance, Compliance und Legal Tech](#governance-compliance-und-legal-tech)
- [Rechtsfragen in der IT](#rechtsfragen-in-der-it)
- [Rechtsstaatlichkeit](#rechtsstaatlichkeit)
  - [Besonderheiten im Umgang mit Rechtstexten](#besonderheiten-im-umgang-mit-rechtstexten)
  - [ePrivacy-Verordnung](#eprivacy-verordnung)
- [Urheberrecht](#urheberrecht)
- [Domänenrecht](#dom%C3%A4nenrecht)
- [Telemediengesetz](#telemediengesetz)
- [E-Government](#e-government)
- [Informationsfreiheitsgesetz](#informationsfreiheitsgesetz)
- [IT-Sicherheitsgesetz](#it-sicherheitsgesetz)
  - [Cyber Security Act](#cyber-security-act)
- [Haftung](#haftung)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

Haupt-Editoren für dieses Dokument: ZeroPointMax<!--Toll jetzt hab ich das an der Backe, ich musste ja unbedingt mitschreiben :D-->

<!--newpage-->

# Governance, Compliance und Legal Tech

- Governance heißt, dass Richtlinien empfohlen einzuhalten sind
- Compliance heißt, dass Richtlinien verpflichtend einzuhalten sind
- Legal Tech: Technologien zur Behandlung von Rechtsthemen, z.B. Weiterleitung von Whistleblowing

# Rechtsfragen in der IT

- Pflichtenlage: Wer muss welche Maßnahmen ergreifen?
- Haftungslage: Wer haftet?
- Beweislage: Wer muss im Streitfall welche Tatsachen wie beweisen?

# Rechtsstaatlichkeit

- ...verspricht Schutz der Grundrechte von Personen gegenüber von
  - Staaten
  - Dritten
- verspricht Recht auf **informationelle Selbstbestimmung**
  - gilt für alle **personenbezogenen Daten**
- Informationstechnische Systeme haben Anspruch auf Vertraulichkeit und Integrität:
  - Recht auf sichere Verschlüsselung
  - Recht auf Selbstschutz, z.B. vor "Quellen-TKÜ"
- **IT-Grundrecht** gilt für **alle Daten**

## Besonderheiten im Umgang mit Rechtstexten

- für die IT gilt aufgrund oft veralteter Gesetzesbücher überwiegend Richterrecht
- oft liegen Erwägungsgründe bei: erläuternde Kommentare zu Artikeln
- in der DSGVO können Anpassungen auf nationaler Ebene durch Öffnungsklauseln erlaubt werden

## ePrivacy-Verordnung

- Privacy by Design
- Kommunikationsdaten sind besonders vertraulich und durch eigenes Grundrecht geschützt
- sollte mit der DSGVO kommen, wurde verzögert, kommt also bald™

# Urheberrecht

- Software ist ein Werk und damit urheberrechtlich geschützt
- Urheberrecht hat den Zweck, Werke wirtschaftlich zu verwerten und zu schützen
- höchstrichterlich entschieden: gebrauchte Software, Musik, etc. kaufen und verkaufen ist erlaubt
  - **aber:** Nachweis der Löschung beim Verkäufer ist erforderlich
  - **Achtung:** der Verkauf von _gebrauchten_ Nutzungsrechten, wie bei E-Books der Fall, ist nicht gestattet. Das steht falsch auf der Folie!
- ab einer gewissen Schöpfungshöhe sind auch Datenbanken urheberrechtlich geschützt

# Domänenrecht

- Gesetze hierzu sehr liberal in Deutschland
- [Domain-Squatting](https://de.wikipedia.org/wiki/Cybersquatting) ist illegal
  - Basis: [§12 BGB](https://www.gesetze-im-internet.de/bgb/__12.html)

# Telemediengesetz

- ein Impressum muss unmittelbar und immer erreichbar sein
- sobald man mit personenbezogenen Daten interagiert, ist eine Datenschutzerklärung erforderlich
  - Hinweis: IP-Adressen sind auch personenbezogen
- alle Datenerhebungen müssen auf das Notwendige beschränkt sein (siehe [Datensparsamkeit](https://de.wikipedia.org/wiki/Datenvermeidung_und_Datensparsamkeit)) sowie zweckgebunden sein
- i.d.R. gilt eine Mithaftung bei illegalen Inhalten in bspw. Foren, digitalen Gästelisten, etc.
  - Hinweis: nur für deutsche Betreiber

# E-Government

- neben De-Mail-Adressen ist ein zusätzlicher elektronischer Kommunikationskanal erforderlich<!--nicht, dass jemand De-Mail hätte...-->
- elektronische Rechnungen sind erforderlich
- Prozessdokumentation ist für Behörden verpflichtend
- Datenbestände von Behörden müssen offen sein: [Open Data](https://de.wikipedia.org/wiki/Open_Data#Open-Data-Gesetz)

# Informationsfreiheitsgesetz

- es gibt kein Behördengeheimnis mehr<!--Deine Daten? UNSERE Daten!-->
- sorgt für mehr Transparenz ([Videotipp](https://media.ccc.de/v/rc3-2021-chaosstudiohamburg-359-frag-den-berwachungsstaat))

# IT-Sicherheitsgesetz

- betrifft KRITIS-Betreiber
- Angriffe sind meldepflichtig, sobald sie mindestens nicht automatisiert abgewehrt werden konnten

## Cyber Security Act

- setzt einheitliche EU-Maßstäbe für IT-Sicherheit
- aktuell ist eine EU-einheitliche Zertifizierung für IT-Sicherheit in Arbeit

# Haftung

- Bei Regel-Missachtungen und unzureichenden Sicherheitsmaßnahmen können Schäden für Dritte entstehen
- In der Wirtschaft gelten Haftungsbeschränkungen zugunsten des Arbeitnehmers:
  - leichte Fahrlässigkeit: Arbeitnehmer haftet nicht
  - normale Fahrlässigkeit: Arbeitnehmer haftet teilweise
  - grobe Fahrlässigkeit und Vorsatz: Arbeitnehmer haftet voll
- IT-Sicherheitsbeauftragte haften auch für Unterlassung
