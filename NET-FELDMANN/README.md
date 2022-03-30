<!----------
title: "Verteilte Systeme"
date: "Semester 6"
keywords: [NET, Verteilte Systeme, verteilt, DHGE, Semester 6]
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

Verteilte Systeme
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Prüfungsleistung](#pr%C3%BCfungsleistung)
- [Einleitung und grundlegende Begriffe](#einleitung-und-grundlegende-begriffe)
  - [Definition verteiles System](#definition-verteiles-system)
  - [zentrale Zielsetzung verteilter Systeme](#zentrale-zielsetzung-verteilter-systeme)
  - [CAP-Theorem](#cap-theorem)
  - [Basismechanismen verteilter Systeme](#basismechanismen-verteilter-systeme)
  - [Systemarchitekturen und Modelle](#systemarchitekturen-und-modelle)
    - [Mehrstufige Architekturen](#mehrstufige-architekturen)
    - [zentrale Vorteile mehrstufiger Architekturen](#zentrale-vorteile-mehrstufiger-architekturen)
  - [Client-Server-Modell](#client-server-modell)
  - [Objektorientiertes Modell](#objektorientiertes-modell)
  - [Exkurs: Parameterübergabe](#exkurs-parameter%C3%BCbergabe)
  - [Vergleich Client/Server vs. OO-Modell](#vergleich-clientserver-vs-oo-modell)
  - [Komponenten-basiertes Modell](#komponenten-basiertes-modell)
  - [dienstorientiertes Modell](#dienstorientiertes-modell)
  - [P2P-Architektur](#p2p-architektur)
  - [Grid Computing](#grid-computing)
  - [Cloud Computing](#cloud-computing)
    - [Klassifizierung von Clouds](#klassifizierung-von-clouds)
  - [Middleware](#middleware)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->
<!--NET hier, aber haben Sie schon mal eine Firma gegründet?-->

Haupt-Editoren für dieses Dokument: ZeroPointMax, RvNovae

<!--newpage-->

<!--Keywords aus dem Chat

- ACID
- REST
- Erlang
- JBOSS
- J2EE
- https://gitlab.com/rak-n-rok/krake
- Lambda-Kalkül
- secustack.com
- heroku.com
- OpenShift
- OpenStack
- MariaDB (auf Konsistenz optimiert)
- MongoDB (auf Verfügbarkeit optimiert)
- Gaia-X - https://gaia-x.eu/news/events/gaia-x-hackathon-3
- Content Distribution Networks
- Paxos (-Protokoll)
- Consensus-Protokolle
- Edge-Cloud
-->

# Prüfungsleistung

- schriftliche Klausur (60 min)
- wird zu 50% verrechnet (Rest `NET-BARIE` aus Semester 5)
- eine DIN-A4-Seite beidseitig beschriftet als Cheatsheet erlaubt <!--wieder handschriftlich?-->

**Änderung: 30.03.22**

- keine Klausur!
- Ersatzleistung: zwei Teile 
  - Praktisch Kubernetes Cluster aufsetzen und benutzen (Dokumentieren -> als Gruppe)
    - Zeitraum von zwei Wochen
    - VMs werden zur Verfügung gestellt
  - Theoretischer Teil -> kleine Ausarbeitung zu einigen Fragestellungen (4-5 Seiten)
    - CAP-Theorem mit Beispiel erklären
    - Synchrone, Asynchrone Replikation Vergleichen


# Einleitung und grundlegende Begriffe

## Definition verteiles System

<!--prüfungsrelevant-->

Ein verteiltes System ist ein System bestehend aus...

- mehreren Einzelkomponenten
- auf unterschiedlichen Rechnern
- kein gemeinsamen Speicher
- Kooperation mittels Nachrichtenaustausch (Netzwerk)
- gemeinsames Ziel
- TODO: Bildbeispiel von Folie

## zentrale Zielsetzung verteilter Systeme

- Kooperation und Integration von Funktionalität und Daten über Rechnergrenzen hinweg
- gemeinsamer Ressourcenzugriff
- Parallelisierung
- Skalierbarkeit
- Fehlertoleranz, Ausfallsicherheit, Verfügbarkeit

## CAP-Theorem

Ein verteiltes System kann zwei der folgenden Eigenschaften gleichzeitig erfüllen, jedoch nicht alle drei:

- **C**onsistency (Konsistenz)
- **A**vailability (Verfügbarkeit)
- **P**artition Tolerance (Ausfalltoleranz)

## Basismechanismen verteilter Systeme

- dynamisches Binden: über einen Verzeichnisdienst werden Ressourcen dynamisch gefunden und bei Bedarf eine Verbindung hergestellt
- Transparenz: Interaktion mit verteilten Systemen ist nicht unterscheidbar von Interaktion mit lokalem System

## Systemarchitekturen und Modelle

- mehrstufige Architekturen: *"divide et impera"*
- aufeinander aufbauende Modelle:
  - Client/Server Modell
  - objektorientiertes Modell
  - komponentenbasiertes Modell
  - dienstorientiertes Modell
- P2P-Architektur
- Grid Computing, Cloud Computing

### Mehrstufige Architekturen

- Einteilung von Funktionalität in Stufen (Schichten)
- Stufen werden verteilt und kommunizieren mit **klar definierten Schnittstellen**
- weit verbreitet sind:
  - zweistufige Architekturen, z.B. Client-Server-Modell
  - dreistufige Architekturen, z.B.:
    - Präsentationsschicht - User Interface
    - Verarbeitungsschicht - Applikationslogik
    - Persistenzschicht - Datenbank
- klare Trennung in der Praxis schwierig

### zentrale Vorteile mehrstufiger Architekturen

- Definition eindeutiger Schnittstellen
- unabhängige Modifikationen an den Stufen möglich
- Komplexität des Gesamtsystems wird durch Aufteilung reduziert

## Client-Server-Modell

- Grundprinzip: Clientanwendung ruft über ein Rechnernetz (*enger Kanal*) eine Server-Anwendung auf, die eine Funktionalität zur Verfügung stellt
- Beispiel: Remote Procedure Call
- Rollenverteilung abhängig von Kommunikationspartnern

## Objektorientiertes Modell

- ähnlich zum Client-Server-Modell
- Einsatz von Objekten beliebiger Granularität
- TODO: Beispiel-Bild von Folie

## Exkurs: Parameterübergabe

- vgl. "Call-by-value", "Call-by-Reference"
- Wertparametersemantik
  - Kommunikationspartner sendet Werte, die in lokalen Adressraum kopiert werden
  - Inkonsistenzen möglich
- Referenzparametrik
  - Kommunikationspartner erhält Referenz auf entfernten Wert

## Vergleich Client/Server vs. OO-Modell

TODO: Tabelle aus Folie

## Komponenten-basiertes Modell

- Erweiterung des OO-Modells
- Komponenten kapseln Funktionalität und werden beim **Deployment** parametriert
- **Komponenten-Container** dienen als Laufzeitumgebung und interpretieren Parameter
- sind für sich leicht installierbar, meist mit **einfachen, klar definierten APIs** und Entwicklungswerkzeugen

## dienstorientiertes Modell

- Dienste sind durch Schnittstellen definiert
- prozessorientierte Sicht auf ein System, abstrahiert von Implementierung
- Schlagwort *Service Oriented Architectures* (SOA)
- Dienste sind wiederverwendbar
- hohe Granularität und Schnittstellen stehen im Vordergrund
- Basisdienste können zu höheren Diensten *komponiert* werden

## P2P-Architektur

- keine differenzierten Rollen, Peers sind gleichwertige Teilnehmer
- skalierbar, ausfallsicher
- vollwertige P2P-Architektur dezentralisiert Kommunikation, Management, Konfiguration
- Suchaufwand zum Finden des richtigen Teilnehmers ist logarithmisch, d.h. es wird ein zusätzlicher Suchschritt bei verdoppelter Teilnehmerzahl benötigt
  - siehe QuickSort

## Grid Computing

- Konzept zur Aggregation und gemeinsamer Nutzung von heterogenen, vernetzten Ressourcen
- Ressourcen sind geographisch verteilt und im Besitz verschiedener Instanzen
- Unterschiede zum Cluster Computing:
  - dezentrale Administration
  - Verwendung offener Standards
  - umfassende QoS

## Cloud Computing

- passt Ressourcen-Bereitstellung *ad hoc* an Bedarf an
- Infrastruktur ist aus Nutzersicht wie ein lokales System, abstrahiert von Netzwerk
- Verwendung der Infrastruktur über klar definierte Schnittstellen und Protokolle, innerhalb von Programmen genutzt
- spart in aller Regel keine Kosten
- steigert oft Automatisierung

### Klassifizierung von Clouds

- Infrastruktur (IaaS): virtuelle Rechner, Platten, Netze, usw. werden bereitgestellt, aber **selbst verwaltet**
- Plattform (PaaS): vorkonfigurierte Services wie Datenbanken, die für eine Anwendung benötigt werden; Ausführungsumgebung wird zur Verfügung gestellt und automatisch skaliert
- Anwendung (SaaS): Anwendung wird als Komplettpaket zur Verfügung gestellt
- spezielle Dienste wie Function as a Service

<!-- gerne als Klausurfrage (IaaS,PaaS,SaaS)-->

## Middleware

- abstrahiert Netzwerkumgebung für den Client

## Microservice-Anmerkung

> *Don't distribute your objects!*
>
> $\rightarrow$ Schnittstelle nach außen und rein lokale Datenverarbeitung genau abwägen. 

# Suchen in Verteilten Systemen / Verzeichnisdienste und Datenkonsistenz

## Namens-/Verzeichnisdienste

- Suche von Kommunikationspartnern, Ressourcen, Komponenten, Diensten, ... ($\rightarrow$ IPs/Ports)

### Grundbegriffe

#### Namensdienst

- Bilden Namen auf Adressen bzw. (Objekt-)Referenzen ab
- z.B. DNS

#### Name

- logische, in der Regel lokationsunabhängige Bezeichnung einer Instanz

#### Adresse

- bzw. (Objekt-)Referenz
- eindeutige, physikalische bzw. in der Regel ortsbezogene Bezeichnung

#### Verzeichnisdienst (Directory Service)

- Erweiterung
- Bietet Verwaltung zusätzlicher Attribute und entsprechende Suche mittels dieser an
  - z.B. Cloud-Provider mit bestimmten Standort, Zertifizierungen (kryptografisch nachweisbar, in verzeichnisdienst durchsuchbar), ...

#### Namensraum

#### Kontext

#### Namensinterpretation

### Überblick zu Realisierungen

#### Hierarchische Realisierung

- zur Gewährleistung von Skalierbarkeit und Effizienz der Interpretation zu verschiedenen hierarchisch organisierten Servern zugeordnet
- mehrere Möglichkeiten für Einstiegspunkt und Anfragebearbeitung: Chaining, Referral

##### Chaining (verkettete Delegation von Anfragen an andere Dienste)

##### Referral (itterative Delegation zwischen den Diensten)

- Zwischenergebnisse Ablegen (Cache)

### Optimierungskozepte

- **Caching:** Speicherung von teilen des Namensraums auf servern, die ursprünglich für den jeweiligen Namensraum nicht zuständig waren
- **Replikation von Kontexten:** im Vergleich zu Caching geplant und proaktiv $\rightarrow$ höhrere Fehlertoleranz; bei CDNs im Einsatz
- **Allgemeines Problem:** Aktualität von Einträgen / Gewährleistung von Konsistenz

### Systembeispiele

- Domain Name System (DNS): Auflösung von Domainnamen auf IP-Adressen
- X.500: mächtiger, flexibel einsetzbarer standardisierter Verzeichnisdiesnt
- Lightweight Directory Access Protocol (LDAP): Leichtgewichtiges Protokoll, dass Anfragen und Modifikation von Informationen eines Verzeichnisdienstes ermöglicht

#### X.500 - Namenseinträge

- Distinguished Name (DN)
  - Zusammengesetzter Name für einzelnen Eintrag
  - Zusammengesetzt aus Relativ Distinguished Name (RDN)

- Relative Distinguished Name (RDN)

#### LDAP

- De-Facto-Standard für den Zugriff auf Verzeichnisdienste
- Vereinfachung des X.600 Directory Access Protocol (DAP)
- eingesetzt für Benutzerverwaltung, Adressverwaltung, Authentifizierung

## Verteilte Transaktionen

### ACID-Prinzip

> auf Konsistenz ausgelegt

- **Atomicity:** Entweder vollständige oder keine Ausführung
- **Consistency:** nur Übergänge von konsistentem Zustand zu konsistentem Zustand
- **Isolation:** Keine Überlappung von Transaktionen, die sich gegenseitig beeinflussen können
- **Durability:** Nach Abschluss einer Transaktion werden Daten garantiert dauerhaft in einer Datenbank gespeichert

#### BASE

> auf Verfügbarkeit ausgelegt $\rightarrow$ einfach skalierbar (best efford, optimistic)

- **Basically Available:** Lese- und Schreiboperationen sind immer verfügbar
  - `write` bei Konflikten nicht unbedingt persistent
  - `read` liefert nicht unbedingt zuletzt gespeicherte (bzw. konsistente) Daten
- **Soft state:** keine Garantie für Konsistenz (nur Wahrscheinlichkeit)
- **Eventual consistency:** nach ausreichender Zeit kann von einem konsistenten Zustand ausgegangen werden

#### 2-Phasen-Commit-Protokoll

- Protokoll zur konsistenten Ablage von Daten in verschiedenen Datenbanken
- zwei Rollen: **Koordinator, Teilnehmer** 
- Annahme: zu speichernden Daten liegen den Teilnehmern bei Beginn des Protokollablaufs vor
- falls Ablauf fehlschlägt: **Rollback**

**1. Phase**

- **Versenden von Kommandos zur temporären Speicherung** von Daten durch einen Koordinator an alle Teilnehmer
- **Bestätigung**, dass Daten temporär gesichert wurden (bzw. Fehlermeldung/Timeout)

**2. Phase**

- **Versenden eines "Commits"** durch Koordinator $\rightarrow$ alle temporären Daten müssen persistent gemacht werden
- **Bestätigung persistenter Speicherung** gegenüber Koordinator

> Problem: wenn Bestätigung in der 2. Phase ausbleibt, muss dies separat behandelt werden (offene Transaktion)

<!-- 
Regelmäßig gern in Prüfung gefragt -> kein Rollback! 

Commit ist abschließen! 
-> Ausgebliebener Teilnehmer muss nachträglich in konsistenten Zustand überführt werden (nicht immer mit Algorithmus möglich -> manuell nötig)
-->

### CAP-Theorem

> Beschreibt Relation zwischen **Konsistenz**, **Verfügbarkeit** und **Partitionstoleranz**

- **Konsistenz:** Schreiben auf einem Knoten, Lesen von anderem: Es wird nichts Älteres zurückgegeben, als was gerade geschrieben wurde
- **Verfügbarkeit:** jeder Request wird beantwortet
- **Partitionstoleranz:** auch bei Netzwerkfehlern/-ausfällen (Partitionierungen) arbeitet das System weiter

### Asynchrone Replikation

### Synchrone Replikation

> Voraussetzung: keine große Latenz zwischen Primary und Secondary
>
> $\rightarrow$ Synchrone Replikation über große Distanzen nicht möglich

### Datenreplikation am Beispiel Galera

### Galera

- wird von MariaDB (relationale Datenbank) für Replikation genutzt 
