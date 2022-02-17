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

- [Überblick](#%C3%9Cberblick)
  - [Governance, Compliance und Legal Tech](#governance-compliance-und-legal-tech)
  - [Rechtsfragen in der IT](#rechtsfragen-in-der-it)
  - [Vorschriften im IT-Recht](#vorschriften-im-it-recht)
  - [Datenschutz-Grundverordnung (DSGVO)](#datenschutz-grundverordnung-dsgvo)
    - [Rechtsstaatlichkeit und Grundrechtsschutz](#rechtsstaatlichkeit-und-grundrechtsschutz)
    - [Grundrecht auf Schutz der Persönlichkeit](#grundrecht-auf-schutz-der-pers%C3%B6nlichkeit)
    - [Besonderheiten im Umgang mit Rechtstexten](#besonderheiten-im-umgang-mit-rechtstexten)
    - [ePrivacy-Verordnung](#eprivacy-verordnung)
  - [Urheberrecht (UrhG)](#urheberrecht-urhg)
    - [Urheberrecht von Software und Datenbanken](#urheberrecht-von-software-und-datenbanken)
    - [Urheberrecht im Arbeitsverhältnis](#urheberrecht-im-arbeitsverh%C3%A4ltnis)
  - [Einrichtung im Internet](#einrichtung-im-internet)
    - [Domänenrecht](#dom%C3%A4nenrecht)
    - [Telemediengesetz (TMG)](#telemediengesetz-tmg)
  - [E-Government-Gesetz](#e-government-gesetz)
  - [Informationsfreiheitsgesetz](#informationsfreiheitsgesetz)
    - [Ziele](#ziele)
    - [Säulen der Umsetzung](#s%C3%A4ulen-der-umsetzung)
  - [IT-Sicherheits-Gesetz](#it-sicherheits-gesetz)
    - [Cyber Security Act (CSA)](#cyber-security-act-csa)
  - [Haftung](#haftung)
- [Datenverarbeitung im Beschäftigungskontext](#datenverarbeitung-im-besch%C3%A4ftigungskontext)
  - [Gestaltungsfelder der Personalvertretung](#gestaltungsfelder-der-personalvertretung)
  - [Interessen der Arbeitgeber](#interessen-der-arbeitgeber)
  - [Betriebs-/Dienstvereinbarungen](#betriebs-dienstvereinbarungen)
    - [Beispiel: Private und dienstliche Internetnutzung](#beispiel-private-und-dienstliche-internetnutzung)
    - [Beispiel: Protokolldateien](#beispiel-protokolldateien)
- [Einführung Datenschutz](#einf%C3%BChrung-datenschutz)
  - [Exkurs - Impulsfragen Datenschutz / Miro-Board](#exkurs---impulsfragen-datenschutz--miro-board)
  - [Recht auf informationelle Selbstbestimmung](#recht-auf-informationelle-selbstbestimmung)
    - [Beeinträchtigung digitaler Rechte](#beeintr%C3%A4chtigung-digitaler-rechte)
    - [Handlungsbedarf (Datenschutz im Kontext moderner Technologien)](#handlungsbedarf-datenschutz-im-kontext-moderner-technologien)
  - [Befugnisse von Datenschutzbeauftragten](#befugnisse-von-datenschutzbeauftragten)
- [EU-Datenschutz Grundverordnung](#eu-datenschutz-grundverordnung)
  - [Geltungsbereich](#geltungsbereich)
  - [Inhalt der DSGVO](#inhalt-der-dsgvo)
    - [Zweck der DSGVO](#zweck-der-dsgvo)
  - [Warum IT-Grundschutz?](#warum-it-grundschutz)
  - [Datenschutz durch Technik und datenschutzfreundliche Voreinstellungen](#datenschutz-durch-technik-und-datenschutzfreundliche-voreinstellungen)
  - [Kriterien zur Bewertung eines Risikos](#kriterien-zur-bewertung-eines-risikos)
  - [Wie wird der Stand der Technik definiert?](#wie-wird-der-stand-der-technik-definiert)
  - [Begriffsbestimmungen](#begriffsbestimmungen)
    - [Stakeholder der DSGVO](#stakeholder-der-dsgvo)
    - [identifizierte vs. identifizierbare Person (Betroffener)](#identifizierte-vs-identifizierbare-person-betroffener)
    - [Verantwortlicher](#verantwortlicher)
    - [Begriff der Verarbeitung](#begriff-der-verarbeitung)
      - [Offenlegen](#offenlegen)
      - [Löschen vs. Vernichten](#l%C3%B6schen-vs-vernichten)
    - [Auftragsverarbeiter](#auftragsverarbeiter)
    - [Dritter](#dritter)
    - [Dateisystem (juristische Definition)](#dateisystem-juristische-definition)
    - [Pseudonymisierung](#pseudonymisierung)
    - [Profiling](#profiling)
  - [Kapitel 2 - Grundsätze](#kapitel-2---grunds%C3%A4tze)
    - [Art. 5 - Grundsätze der Verarbeitung](#art-5---grunds%C3%A4tze-der-verarbeitung)
    - [Art. 6 - Rechmäßigkeit der Verarbeitung](#art-6---rechm%C3%A4%C3%9Figkeit-der-verarbeitung)
    - [Art. 9 - Besondere Datenkategorien](#art-9---besondere-datenkategorien)
  - [Art. 83 - Geldbußen](#art-83---geldbu%C3%9Fen)
  - [Kapitel 3 - Rechte der Betroffenen](#kapitel-3---rechte-der-betroffenen)
    - [Beispiele für technisch-organisatorische Maßnahmen (TOM)](#beispiele-f%C3%BCr-technisch-organisatorische-ma%C3%9Fnahmen-tom)
  - [Kapitel 4 - Verantwortlicher und Auftragsverarbeiter](#kapitel-4---verantwortlicher-und-auftragsverarbeiter)
    - [Art. 24 - Pflichten des für die Verarbeitung Verantwortlichen](#art-24---pflichten-des-f%C3%BCr-die-verarbeitung-verantwortlichen)
    - [Art. 28 - Auftragsverarbeiter](#art-28---auftragsverarbeiter)
      - [Auftragsverarbeitung vs. Funktionsübertragung](#auftragsverarbeitung-vs-funktions%C3%BCbertragung)
    - [Art. 30 - Aufzeichnung der Verarbeitungsaktivitäten](#art-30---aufzeichnung-der-verarbeitungsaktivit%C3%A4ten)
    - [Art. 33 - Meldepflichten von Verletzungen des Schutzes personenbezogener Daten](#art-33---meldepflichten-von-verletzungen-des-schutzes-personenbezogener-daten)
    - [Art. 35 - Datenschutz-Folgeabschätzung](#art-35---datenschutz-folgeabsch%C3%A4tzung)
      - [Inhalt einer Datenschutz-Folgeabschätzung](#inhalt-einer-datenschutz-folgeabsch%C3%A4tzung)
      - [Blacklists](#blacklists)
  - [Aufgaben des Verantwortlichen](#aufgaben-des-verantwortlichen)
  - [Aufgaben des Datenschutzbeauftragten](#aufgaben-des-datenschutzbeauftragten)
  - [Standard-Datenschutzmodell](#standard-datenschutzmodell)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

Haupt-Editoren für dieses Dokument: ZeroPointMax<!--Toll jetzt hab ich das an der Backe, ich musste ja unbedingt mitschreiben :D-->

<!--newpage-->

# Überblick

## Governance, Compliance und Legal Tech

- Governance heißt, dass Richtlinien empfohlen einzuhalten sind
- Compliance heißt, dass Richtlinien verpflichtend einzuhalten sind
- Legal Tech: Technologien zur Behandlung von Rechtsthemen, z.B. Weiterleitung von Whistleblowing

## Rechtsfragen in der IT

- Pflichtenlage: Wer muss welche Maßnahmen ergreifen?
- Haftungslage: Wer haftet?
- Beweislage: Wer muss im Streitfall welche Tatsachen wie beweisen?

## Vorschriften im IT-Recht

- klassisches IT-Recht besitzt nur vereinzelt besondere Gesetze
- relevante Normen größtenteils über viele verschiedene Rechtsquellen verteilt
- u.a.: Zivil- und Urheberrechts; kartell- und strafrechtliche Regelungen; Normen aus AWG, DSGVO, Dual-Use VO, GeschGehG, HGB, InsO, KWG, ...

## Datenschutz-Grundverordnung (DSGVO)

### Rechtsstaatlichkeit und Grundrechtsschutz

> Grundrechte versprechen Schutz von Grundrechtsträgern (Personen) gegenüber Staaten und Dritten.

### Grundrecht auf Schutz der Persönlichkeit

- verspricht Recht auf **informationelle Selbstbestimmung**
  - gilt für alle **personenbezogenen Daten**
- Informationstechnische Systeme haben **Anspruch auf Vertraulichkeit und Integrität**
  - Recht auf sichere Verschlüsselung und Selbstschutz (z.B. vor "Quellen-TKÜ")
- **IT-Grundrecht** gilt für **alle Daten**

### Besonderheiten im Umgang mit Rechtstexten

- für IT gilt aufgrund oft veralteter Gesetzesbücher überwiegend **Richterrecht**
- oft liegen **Erwägungsgründe** bei: erläuternde Kommentare zu Artikeln
- DSGVO ermöglicht Anpassungen auf nationaler Ebene durch **Öffnungsklauseln** (durch BDSGnF, ThürDSGnF berücksichtigt)

### ePrivacy-Verordnung

> *Privacy by Design*

- **Kommunikationsdaten sind besonders vertraulich** und durch eigenes Grundrecht geschützt ([Art. 7 EU-Grundrechte-Charta](https://www.europarl.europa.eu/germany/resource/static/files/europa_grundrechtecharta/_30.03.2010.pdf))
- sollte mit der DSGVO kommen, wurde verzögert, kommt also bald™ <!--Stand Feb. 2022-->

## Urheberrecht (UrhG)

> Urheberrecht ist das Recht auf den **Schutz geistigen Eigentums** in ideeller und materieller Hinsicht.
> Es hat den Zweck, Werke wirtschaftlich zu verwerten und zu schützen.

- Verletzungen können zu hohen Schadensersatzforderungen führen
  - $\rightarrow$ bestimmte Verstöße gegen das Urhebergesetz sind zudem strafbar und mit Freiheitsstrafen bis zu fünf Jahren bedroht

### Urheberrecht von Software und Datenbanken

- Software ist ein Werk und damit urheberrechtlich geschützt (wie Texte, Kompositionen, Gemälde, ...)
- höchstrichterlich entschieden: gebrauchte Software, Musik, etc. kaufen/verkaufen ist erlaubt
  - Grundlage: **Erschöpfungsgrundsatz** $\rightarrow$ Schutzrechte verbrauchen sich sobald der geschützte Gegenstand rechtmäßig in Verkehr gebracht wurde
  - **aber:** Nachweis der Löschung beim Verkäufer ist erforderlich
  - **Achtung:** der Verkauf von _gebrauchten_ Nutzungsrechten ist nicht gestattet (z.B. bei E-Books) <!--steht falsch auf der Folie!-->
- ab einer gewissen Schöpfungshöhe sind auch Datenbanken urheberrechtlich geschützt

### Urheberrecht im Arbeitsverhältnis

- **Schöpferprinzip** $\rightarrow$ Arbeitnehmer als alleiniger Urheber anzusehen
  - Rechtseinräumung zugunsten des Arbeitgebers wird nicht vermutet
- Ausnahme nach § 69b UrhG für die Entwicklung von Computerprogrammen
  - Ausübung aller vermögensrechtlichen Befugnisse an dem geschützten Computerprogramm ausschließlich dem Arbeitgeber zu (wenn nichts anderes vereinbart)

## Einrichtung im Internet

### Domänenrecht

- Adressen sollten zum Namen der Einrichtung passen (Verwechslungen vermeiden!)
- Vergabe von Adressen der TLD `.de` durch DENIC (keine Prüfung auf Rechteverletzung)
- berechtigte Namensträger besitzen Möglichkeit auf Freigabe des Namens zu klagen
  - **[Domain-Squatting](https://de.wikipedia.org/wiki/Cybersquatting) ist illegal** (Basis [§12 BGB](https://www.gesetze-im-internet.de/bgb/__12.html))

### Telemediengesetz (TMG)

- Impressum *(Anbieterkennung)* muss unmittelbar und immer erreichbar sein (Informationspflichten $\rightarrow$ §5,6 TMG)
- sobald personenbezogenen Daten erhoben, verarbeitet oder genutzt werden, sind Datenschutzhinweise erforderlich
  - *Hinweis: IP-Adressen sind auch personenbezogen*
  - alle Datenerhebungen müssen auf das Notwendige beschränkt sein (siehe [Datensparsamkeit](https://de.wikipedia.org/wiki/Datenvermeidung_und_Datensparsamkeit)) sowie zweckgebunden sein
- Mithaftung bei illegalen Inhalten in bspw. Foren, digitalen Gästelisten, ... (Verpflictung zur regelmäßigen Prüfung und Entfernung)

## E-Government-Gesetz

- Eröffnung eines elektronischen Kommunikationskanals und De-Mail-Zugangs (Bundesbehörden) verpflichtend <!--nicht, dass jemand De-Mail hätte...-->
- Grundsätze elektronischer Aktenführung <!--nur für Bundesbehörden verpflichtend ?!-->
- Erleichterung bei der Erbringung von elektronischen Nachweisen
  - Schriftformerfordernis durch elektronischen Signatur (eID-Perso), De-Mail
- Erfüllung von Publikationspflichten durch elektronische Amts- und Verkündungsblätter
- Prozessdokumentation ist für Behörden verpflichtend
- Bereitstellung von maschinenlesbaren Datenbeständen durch die Verwaltung ([Open Data!](https://de.wikipedia.org/wiki/Open_Data#Open-Data-Gesetz))

## Informationsfreiheitsgesetz

### Ziele

- **Transparenz** der Verwaltung (kein Behördengeheimnis mehr!) <!--Deine Daten? UNSERE Daten!-->
- Erhöhung der **Akzeptanz** von Verwaltungshandeln
- Möglichkeiten **aktiver Mitgestaltung** staatlicher Entscheidungen

> [Videotipp](https://media.ccc.de/v/rc3-2021-chaosstudiohamburg-359-frag-den-berwachungsstaat), [fragdenstaat.de](https://fragdenstaat.de/)

### Säulen der Umsetzung

- subjektives Recht der Bürger/innen auf **Informationszugang durch Antragsstellung**
- **aktive Veröffentlichungen von Informationen** durch die Verwaltung und Einrichtung eines zentralen elektronischen Informationsregisters

## IT-Sicherheits-Gesetz

- betrifft alle Betreiber kritischer Infrastrukturen (KRITIS)
- **Meldepflicht bei Angriffen** auf digitale Systeme *(sobald nicht mindestens automatisiert abgewehrt)*
- Unternehmen sollen innerhalb von zwei Jahren Sicherheitsstandards für ihre jeweilige Branche festlegen
- **Zuständigkeit des Bundeskriminalamts (BKA)** für zahlreiche Cyberdelikte
- Etablierung des **BSI als Aufsichtsbehörde**
- Aufstellung aller Sicherheitsaudits, Prüfungen und Zertifizierungen müssen durch Unternehmen alle zwei Jahre an den BSI übermittelt werden

### Cyber Security Act (CSA)

- einheitliche EU-Maßstäbe für IT-Sicherheit
- schafft einheitlichen Rahmen zur EU-Zertifizierung von Cybersicherheit (aktuell in Arbeit)

## Haftung

> bei Regel-Missachtungen und unzureichenden Sicherheitsmaßnahmen können Schäden für Dritte entstehen

- **Amtshaftung** $\rightarrow$ Staat kann für solche Schäden haftbar gemacht werden
- aber: grob fahrlässige oder vorsätzliches verursachen durch Angestellten/Beamten $\rightarrow$ **Zivilrechtliche Haftung**
- In der Wirtschaft gelten Haftungsbeschränkungen zugunsten des Arbeitnehmers:
  - leichte Fahrlässigkeit: Arbeitnehmer haftet nicht
  - normale Fahrlässigkeit: Arbeitnehmer haftet teilweise (zusammen mit Arbeitgeber)
  - grobe Fahrlässigkeit oder Vorsatz: Arbeitnehmer haftet voll (Einzelfallbetrachtung)
- IT-Sicherheitsbeauftragte haften auch für Unterlassung

# Datenverarbeitung im Beschäftigungskontext

- geregelt durch Gesetze oder Kollektivvereinbarung (Betriebs-/Dienstvereinbarungen)
- Betriebs-/Personalrat hat Einfluss auf diese
  - man unterscheidet in Fälle mit voller und normaler Mitbestimmung
- geregelt auf technischer und organisatorischer Ebene mit rechtlicher Gestaltung und Regeltransparenz
  - z.B. wird die private Nutzung des Firmen-Internets eingeschränkt oder verboten

## Gestaltungsfelder der Personalvertretung

- Fälle der vollen Mitbestimmung $\rightarrow$ Betriebs-/Personalrat **muss** zustimmen
- Fälle der Mitwirkung $\rightarrow$ Betriebs-/Personalrat kann mitwirken aber nicht entscheiden

## Interessen der Arbeitgeber

- Sabotage und Datendiebstahl verhindern
- Verlust von Arbeitszeit/Produktivität verhindern
- Bandbreite sparen
- Urheberrechtsverstöße verhindern
- Rechtsverletzungen (z.B. Urheberrechtsverstöße) durch Mitarbeiter verhindern

## Betriebs-/Dienstvereinbarungen

Regelt z.B. Beschränkungen nach Umfang, Dauer, Art und Weise der E-Mail und Internetnutzung

- Aufzählung verbotener Nutzungen (Inhalte, Privat/Dienstlich)
- Umgang mit Protokolldateien
- et cetera

### Beispiel: Private und dienstliche Internetnutzung

**privat**

- Erlaubnis oder Verbot einer privaten Nutzung von Internet muss geregelt werden
- private Nutzung darf keine negativen Auswirkungen auf die Arbeit oder den Arbeitgeber haben
- Wenn private Nutzung gestattet: Arbeitgeber ist Telekommunikationsanbieter
  - Fernmeldegeheimnis!
  - Datenerhebung nur ausnahmsweise, nicht systematisch

**dienstlich**

- kein Fernmeldegeheimnis, aber Datenschutzgesetze gelten
- Verhältnismäßigkeit!
  - Metadaten: ok
  - Inhaltskontrolle unzulässig

> **Bei illegalen Handlungen darf außerordentlich gekündigt werden, ansonsten muss vorher Abmahnung erfolgen**

### Beispiel: Protokolldateien

- DSGVO kennt keine Höchstgrenze zur Aufbewahrungsdauer
- Öffnungklausel: nationales Recht kann Vorschriften festlegen
- Zweck muss klar sein, verhältnismäßige Speicherung
- Artikel 40 DSGVO: Branchen(-Verbände) sollen Standards festlegen $\rightarrow$ Zertifikate

# Einführung Datenschutz

## Exkurs - Impulsfragen Datenschutz / Miro-Board

<!-- md2apkg ignore-card -->

- moderne Technologien und Datenschutz
- Recht auf informationelle Selbstbestimmung (Volkszählung 1983)
- Mephisto-Urteil / Kunstfreiheit
- Gedankenexperiment: Daten als Eigentum
- IT-Grundrecht
- Auskunftssysteme (Privatwirtschaft)
- Scoring (§31 BDSG)
- Big Brother Award
- E-Privacy (Verordnung)
- Informationsfreiheitsgesetz (IFG)

## Recht auf informationelle Selbstbestimmung

- es gibt keine belanglosen Daten
- *"Wer weiß wann und bei welcher Gelegenheit was über mich?"* $\rightarrow$ Grundrecht

> Das Bundesverfassungsgericht stellte fest, dass unter den Verarbeitungs- und Verknüpfungsmöglichkeiten der Informationstechnologie auch ein für sich gesehen belangloses Datum einen neuen Stellenwert bekommen kann und es insoweit keine belanglosen Daten gibt.

- Aufklärungspflicht der verantwortlichen Stelle
- Vorrang der Selbstauskunft
- Einschränkungen des Rechts müssen gesetzlich geregelt sein
- Zweckbindung und Verhältnismäßigkeit der Erhebung und Verarbeitung personenbezogener Daten
- Sammeln auf Vorrat ist nicht erlaubt

### Beeinträchtigung digitaler Rechte

- zunehmend werden vermeintlich kostenfreie Dienste mit Daten bezahlt
- Cloud-Dienste haben den Verlust der Souveränität über die Daten zur Folge
- Big Data und KI

### Handlungsbedarf (Datenschutz im Kontext moderner Technologien)

- Rechtsverletzungen werden nicht effektiv beendet
- das in Planung befindliche IT-Sicherheitsgesetz bleibt hinter den Forderungen zurück
- Zertifizierungsverfahren

## Befugnisse von Datenschutzbeauftragten

- Untersuchungsbefugnisse: darf Serverraum öffnen und Inhalt einsehen
- Abhilfebefugnisse: Anweisung zur Änderung oder Abschaltung eines Servers
- Datenschutzbeauftragten sollten zeitliche und monetäre Mittel zur Verfügung gestellt werden

# EU-Datenschutz Grundverordnung

## Geltungsbereich

- DSGVO ist unmittelbares Gesetz (2016 veröffentlicht)
- Artikel 91: *"Gilt in allen Mitgliedsstaaten verbindlich und unmittelbar."*

## Inhalt der DSGVO

- **Schutz der Grundrechte und -freiheiten** natürlicher Personen
  - damit steht jedes Datum unter dem Schutz des Grundgesetzes

### Zweck der DSGVO

- Ermöglichen einer legalen **Digitalwirtschaft**
  - der freie Verkehr personenbezogener Daten darf weder eingeschränkt noch verboten werden
- Schutz der **Grundrechte**: die DSGVO zwingt lediglich Unternehmen dazu, die Nutzung der Daten transparent zu machen und den Regeln folgen

## Warum IT-Grundschutz?

- Die Einhaltung kann man sich zertifizieren lassen
- Artikel 24 und 32 sagt, dass **alle** Unternehmen den IT-Grundschutz erfüllen sollen (nicht nur kritische Infrastruktur)

## Datenschutz durch Technik und datenschutzfreundliche Voreinstellungen

> *data protection by default and by design*

- erforderliche Sicherheitsmaßnahmen müssen in die Verarbeitung von Anfang an integriert werden
  - unter Berücksichtigung des _Standes der Technik_ und der Implementierungskosten
  - und der Art, des Umfangs, der Umstände und der Zwecke der Verarbeitung
  - sowie der Risiken unterschiedlicher Eintrittswahrscheinlichkeit
- Unternehmen müssen ISMS etablieren

## Kriterien zur Bewertung eines Risikos

- Wahrscheinlichkeit der Gefährdung
- Schwere der Gefährdung
- Implementierungskosten für die Lösung

## Wie wird der Stand der Technik definiert?

Die Bausteine des IT-Grundschutz-Kompendiums (BSI-Dokument) bilden den Stand der Technik ab.

## Begriffsbestimmungen

### Stakeholder der DSGVO

- Betroffene
- Verantwortlicher
- Auftragsverarbeiter
- Dritte
- Datenschutzbeauftragte(r) (DSB)
- Aufsichtsbehörde

### identifizierte vs. identifizierbare Person (Betroffener)

- **identifizierte Person:** Daten können bekannter Person zugeordnet werden
- **identifizierbare Person:** mit zusätzlichen Informationen kann auf die Identität geschlossen werden
  - Bsp.: Kennnummer, Standortdaten, Online-Pseudonym, Eigenschaften einer Person, ...

### Verantwortlicher

- jede Person oder Stelle, die:
  - bei personenbezogenen Daten über Zwecke und Mittel der Verarbeitung entscheidet oder
  - im Auftrag durch Auftragsverarbeiter verarbeiten lässt

### Begriff der Verarbeitung

- egal ob mit oder ohne automatisierter Verfahren
- Beispiele Verarbeitungsarten: Erheben, Speichern, Verändern, Übermitteln (Offenlegen), Einschränken, Löschen (Vernichten)

#### Offenlegen

> Daten werden nach Außen an Dritte übermittelt, verbreitet, etc.

#### Löschen vs. Vernichten

> bezieht sich auf das Restrisiko

- **Löschen:** Datenträger bleibt intakt
- **Vernichten:** Datenträger wird zerstört

### Auftragsverarbeiter

- Auftragnehmer erhält Daten nur für bestimmten Zeitraum
- Art der Nutzung durch Auftraggeber vorgeschrieben (gehnehmigungspflichtig)
- Vertraglich geregelt nach Art. 28 DSGVO (nicht ohne Vertrag!)

### Dritter

> natürliche oder juristische Personen, die befugt sind, die Daten zu verarbeiten.

### Dateisystem (juristische Definition)

> Jede strukturierte Sammlung personenbezogener Daten, die nach bestimmten Kriterien zugänglich ist [...](https://dsgvo-gesetz.de/art-4-dsgvo).

### Pseudonymisierung

- Verarbeitung personenbezogener Daten in einer Weise, dass die P-Daten ohne zusätzliche Informationen nicht mehr einer spezifischen betroffenen Person zugeordnet werden können.

### Profiling

- automatisierte Verarbeitung von personenbezogenen Daten zur Bewertung von bspw. wirtschaftlicher Leistung, Gesundheit, Aufenthaltsort, Vorlieben

## Kapitel 2 - Grundsätze

### Art. 5 - Grundsätze der Verarbeitung

- Verarbeitung muss rechtmäßig und zweckgebunden erfolgen
- auf dem Grundsatz von Treu und Glauben
- Datenminimum
- Richtigkeit der Daten
- Speicherminimum / Datensparsamkeit
- Integrität und Sicherheit mit TOMs
- Rechenschaftspflicht (Verarbeitungsübersicht, SiKo)

### Art. 6 - Rechmäßigkeit der Verarbeitung

> die Verarbeitung Personenbezogener Daten ist Rechmäßig bei:

- Einwilligung des Betroffenen
- Erforderlichkeit zur Vertragserfüllung
- rechtlicher Verpflichtung (Gesetz, Verordnung, Dienstvereinbarung)
- Ausnahme von Zweckbindung ist gegeben, wenn
  - Wahrung der "berechtigten Interessen" (Betroffener kann berechtigtem Interesse allerdings folgen oder ablehnen)
  - lebenswichtige Interessen
  - öffentliches Interesse

### Art. 9 - Besondere Datenkategorien

- Gesundheits- und biometrische Daten
- Politische Meinungen
- Religion
- Ethnie
- Gewerkschaftsangehörigkeit

> Diese sensiblen Daten besitzen einen **hohen Schutzbedarf** und benötigen **besondere technisch-organisatorische Maßnahmen**

## Art. 83 - Geldbußen

- bis **20 Mio. Euro** oder
- bis **4% des weltweiten Jahresumsatz**

> **Höhere** von beiden!

## Kapitel 3 - Rechte der Betroffenen

> Mitteilungen an Betroffene unverzüglich, aber maximal innerhalb von drei Monaten, und unentgeltlich

- Recht auf **Auskunft**
- Recht auf **Berichtigung**
- Recht auf **Löschung**
- Recht auf **Datenübertragbarkeit**
- Recht auf **Widerspruch**

### Beispiele für technisch-organisatorische Maßnahmen (TOM)

- **Verschlüsselung**
- **Pseudonymisierung:** ohne Hinzuziehung zusätzlicher Informationen keiner spezifischen Person zuordbar

## Kapitel 4 - Verantwortlicher und Auftragsverarbeiter

### Art. 24 - Pflichten des für die Verarbeitung Verantwortlichen

- Maßnahmen für den Schutz müssen erbracht und nachgewiesen werden
- sehr viele Überschneidungen zwischen Datenschutz und technischer und organisatorischer Sicherheit
- Schutzmaßnahmen müssen an die Art der Daten angepasst sein (höherer Schutz für sensible Daten $\rightarrow$ Art. 9)
- eine Risikobewertung muss durchgeführt werden
- IT-Grundschutz durchführen!

### Art. 28 - Auftragsverarbeiter

- Auftragsverarbeitung nicht ohne Vertrag
- Verantwortung liegt beim Auftraggeber
- Verarbeitung nur auf dokumentierte Weisung des Verantwortlichen
- Mitarbeiter des Auftragsverarbeiters sind zur Vertraulichkeit zu verpflichten
- Sicherheitsmaßnahmen nach Artikel 32 sind erforderlich
- der Auftragnehmer ist nach Angebot der TOMs sorgfältig zu wählen

#### Auftragsverarbeitung vs. Funktionsübertragung

- Funktionsübertragung nicht mehr in Datenschutzgesetzen zu finden
- Outsourcingpartner agiert so frei, das er nicht mehr als bloßer Auftragnehmer betrachtet werden kann
- wird als selbstständig agierender Dritter angesehen (z.B. Inkasso, ...)
- Verantwortung verbleibt beim Auftraggeber
- Auftragnehmer sorgfältig auszuwählen (unter besonderer Berücksichtigung der rechnischen und organisatorischen Maßnahmen)

### Art. 30 - Aufzeichnung der Verarbeitungsaktivitäten

- Datenschutzbeauftragter
- Zweck der Verarbeitung
- vorgesehene Löschfristen für Kategorien von Daten
- allgemeine Beschreibung der technischen und organisatorischen Maßnahmen
- notwendig für Nachweise (erst ab >250 Mitarbeiter)

> [Hinweise der Datenschutzkonferenz](https://www.datenschutzkonferenz-online.de/media/ah/201802_ah_verzeichnis_verarbeitungstaetigkeiten.pdf)

### Art. 33 - Meldepflichten von Verletzungen des Schutzes personenbezogener Daten

- innerhalb von 72h nach Bekanntwerden (an Aufsichtbehörde)
- Artikel 34: auch betroffene Personen müssen benarichtigt werden (wenn hohes Risiko für diese besteht)

### Art. 35 - Datenschutz-Folgeabschätzung

> Durchzuführen, wenn Verarbeitung voraussichtlich ein
> hohes Risiko für die persönlichen Rechte und Freiheiten
> zur Folge hat.

**Insbesondere:**

- systematische umfassende **Auswertung persönlicher Aspekte** einer natürlichen Person
- umfangreiche **Verarbeitung spezieller Kategorien** von Daten (gemäß Art. 9)
- weiträumige **Überwachung von öffentlich zugänglichen Bereichen**

#### Inhalt einer Datenschutz-Folgeabschätzung

- systematische Beschreibung der Verarbeitungsvorgänge und Zwecke der Verarbeitung
- Bewertung der Notwendigkeit und Verhältnismäßigkeit in Bezug auf Zweck
- Bewertung in Bezug auf Recht und Freiheiten der Betroffenen
- vorgesehene Maßnahmen

#### Blacklists

- Verarbeitungsvorgänge, die eine Risikofolgeabschätzung voraussetzen
- z.B. [Blacklist des Thüringer Datenschutzbeauftragten](https://www.tlfdi.de/fileadmin/tlfdi/datenschutz/dsfa_muss-liste_04_07_18.pdf)

## Aufgaben des Verantwortlichen

- Art. 30: Verarbeitungsübersicht
- Art. 28: Verträge zur Auftragsverarbeitung
- Art. 33, 34: Meldepflichten
- Art. 35: Datenschutzfolgenabschätzung (DSFA) bei Risikoverfahren
- Art. 32: TOMs (technisch-organisatorische Maßnahmen) $\rightarrow$ Informationssicherheitsmanagementsystem <!-- heh --> (ISMS) etablieren

## Aufgaben des Datenschutzbeauftragten

- Art: 37: Konzernprivileg (u.a.)
- Art. 39:
  - Unterrichtung und Beratung des Verantwortlichen
  - Überwachung der Einhaltung dieser Verordnung
  - Zusammenarbeit mit Aufsichtsbehörde
  - Tätigkeiten als Anlaufstelle für Aufsichtsbehörde

## Standard-Datenschutzmodell

- Checkliste für Gewährleistungsziele zum Nachweis der Datenschutzkonformität
- 7 Bereiche
  - Datenminimierung
  - Verfügbarkeit
  - Integrität
  - Vertraulichkeit
  - Nichtverkettung
  - Transparenz
  - Intervenierbarkeit
