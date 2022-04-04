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
  - [Definition verteiltes System](#definition-verteiltes-system)
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
- [Verzeichnisdienste, verteilte Transaktionen](#verzeichnisdienste-verteilte-transaktionen)
  - [Grundbegriffe](#grundbegriffe)
  - [hierarchische Realisierung von Namens-/VZ-Diensten](#hierarchische-realisierung-von-namens-vz-diensten)
  - [Optimierungen von Namens-/VZ-Diensten](#optimierungen-von-namens-vz-diensten)
  - [Systembeispiele](#systembeispiele)
    - [X.500 - Namenseinträge](#x500---namenseintr%C3%A4ge)
    - [LDAP](#ldap)
  - [ACID vs. BASE](#acid-vs-base)
    - [ACID-Prinzip](#acid-prinzip)
    - [BASE](#base)
  - [Zwei-Phasen-Commit-Protokoll](#zwei-phasen-commit-protokoll)
  - [CAP Theorem](#cap-theorem-1)
  - [asynchrone Replikation](#asynchrone-replikation)
  - [synchrone Replikation](#synchrone-replikation)
  - [synchrone Multi-Master-Replikation](#synchrone-multi-master-replikation)
  - [Galera](#galera)
    - [Galera ausgewählte Szenarien](#galera-ausgew%C3%A4hlte-szenarien)
      - [Disaster Recovery](#disaster-recovery)
      - [Rolling Updates](#rolling-updates)
      - [Latenzreduktion](#latenzreduktion)
      - [Galera Konsistenzsicherung](#galera-konsistenzsicherung)

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

- Klausurersatzleistung
- Praktischer Teil: Kubernetes Cluster in 4er-Gruppen aufbauen, Zeitraum zwei Wochen
- Theoretischer Teil: Ausarbeitung zu Fragestellungen, ca. 5 Seiten
  - siehe Markdown-Kommentare

# Einleitung und grundlegende Begriffe

## Definition verteiltes System

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
- Schnittstellen sollten wohl überlegt sein
- Komponenten sollten so entworfen werden, dass hoher Kommunikations-Overhead zwischen Komponenten vermieden wird

> *Don't distribute your objects!*
>
> $\rightarrow$ Schnittstelle nach außen und rein lokale Datenverarbeitung genau abwägen. 

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

# Verzeichnisdienste, verteilte Transaktionen

## Grundbegriffe

- Namensdienst: Grundform, Bilden Namen auf Adressen ab
  - Namen: Standortunabhängige Bezeichnung einer Ressource
  - Adresse / Referenz: eindeutige, physikalische / ortsbezogene Bezeichnung
- Verzeichnisdienst: Finden von Kommunikationspartnern, Ressourcen, Attributen, ...
  - Erweiterung des Namensdienstes

## hierarchische Realisierung von Namens-/VZ-Diensten

- Kontexte sind zur Skalierbarkeit und Effizienz der Interpretation zu versch. organisierten Servern zugeordnet
  - TODO: Screenshot extrahieren
- mehrere Möglichkeiten für Einstiegspunkt und Anfragebearbeitung: Chaining, Referral
  - Chaining löst rekursiv auf, Referral iterativ
  - Referral ermöglicht besseres Caching
  - TODO: Screenshot einfügen

## Optimierungen von Namens-/VZ-Diensten

- Caching: Speicherung von Teilen des Namensraums
  - v.a. auf unteren Ebenen
  - vollst. oder teilw. Namen
  - TODO: Vor-/Nachteile
  - **reaktiv**
- Replikation
  - v.a. auf unteren Ebenen
  - höhere Fehlertoleranz
  - **proaktiv**, geplant
- Problem: Aktualität von Einträgen und Gewährleistung von Konsistenz
- siehe auch: DNS, CDN, X.500, LDAP

<!--Anm. Max: er hat sehr auf Caching vs. Repl hingewiesen - klausurrelevant-->

## Systembeispiele

- Domain Name System (DNS): Auflösung von Domainnamen auf IP-Adressen
- X.500: mächtiger, flexibel einsetzbarer standardisierter Verzeichnisdiesnt
- Lightweight Directory Access Protocol (LDAP): Leichtgewichtiges Protokoll, dass Anfragen und Modifikation von Informationen eines Verzeichnisdienstes ermöglicht

### X.500 - Namenseinträge

- Distinguished Name (DN)
  - Zusammengesetzter Name für einzelnen Eintrag
  - Zusammengesetzt aus Relativ Distinguished Name (RDN)
- Relative Distinguished Name (RDN)

### LDAP

- De-Facto-Standard für den Zugriff auf Verzeichnisdienste
- Vereinfachung des X.600 Directory Access Protocol (DAP)
- eingesetzt für Benutzerverwaltung, Adressverwaltung, Authentifizierung

## ACID vs. BASE

- BASE:
  - Optimierungsziel: Verfügbarkeit
  - Konsistenz nicht garantiert
  - letzter Schreibzugriff "gewinnt"
  - skaliert besser
  - einfachere Implementierung
  - aggressiv / optimistisch / best effort
- ACID:
  - Optimierungsziel: Konsistenz
  - Isolation von Zugriffen
  - Commit-basiert, komplexe Implementierung
  - konservativ / pessimistisch

### ACID-Prinzip

> auf Konsistenz ausgelegt

- **Atomicity:** Entweder vollständige oder keine Ausführung
- **Consistency:** nur Übergänge von konsistentem Zustand zu konsistentem Zustand
- **Isolation:** Keine Überlappung von Transaktionen, die sich gegenseitig beeinflussen können
- **Durability:** Nach Abschluss einer Transaktion werden Daten garantiert dauerhaft in einer Datenbank gespeichert

### BASE

> auf Verfügbarkeit ausgelegt $\rightarrow$ einfach skalierbar (best efford, optimistic)

- **Basically Available:** Lese- und Schreiboperationen sind immer verfügbar
  - `write` bei Konflikten nicht unbedingt persistent
  - `read` liefert nicht unbedingt zuletzt gespeicherte (bzw. konsistente) Daten
- **Soft state:** keine Garantie für Konsistenz (nur Wahrscheinlichkeit)
- **Eventual consistency:** nach ausreichender Zeit kann von einem konsistenten Zustand ausgegangen werden

## Zwei-Phasen-Commit-Protokoll

- Protkoll zur Konsistenzwahrung zwischen verteilten Datenbanken
- zwei Rollen: **Koordinator**, **Teilnehmer**
- Annahme: zu speichernde Daten liegen den Teilnehmern vor
- bei Fehlschlag Rollback
- beide Phasen sind Teil *einer* Transaktion

**Phase 1:**

- **Versenden von Kommandos zur temporären Speicherung**
  - Koordinator befiehlt Teilnehmer nicht-persistente Speicherung der Daten
- **Bestätigung**
  - Teilnehmer bestätigen Erfolg (bzw. Fehlermeldung/Timeout), dass Daten (nicht) temporär gesichert wurden

**Phase 2:**

- **Versenden eines "Commits"** durch Koordinator $\rightarrow$ alle temporären Daten müssen persistent gemacht werden
  - Bedingung: Phase 1 erfolgreich
  - Koordinator versendet Commit-Befehl
  - alle Teilnehmer müssen Daten persistent speichern
- **Bestätigung persistenter Speicherung** gegenüber Koordinator
  - Teilnehmer bestätigen Erfolg

- Problem: wenn Commit-Entscheidung stattgefunden hat, aber ein Teilnehmer nicht bestätigt (z.B. Absturz)
  - betroffener Teilnehmer muss konsistenten Zustand anfordern und *nachholen* (nicht verwechseln mit Roll-forward) <!--Prüfungsrelevant!-->
  - **Commit-Entscheidungen werden nie rückgängig gemacht**

## CAP Theorem

> Beschreibt Relation zwischen Konsistenz, Verfügbarkeit und Partitionstoleranz

- immer (bis zu) zwei möglich: CA, CP, AP
  - CA-Systeme nicht realistisch
- Consistency
  - schreiben auf einem Knoten, lesen von einem anderen
  - es wird nichts zurückgegeben, als was gerade geschrieben wurde
- Availability jeder Request wird beantwortet
- Partitionstoleranz
  - Partitionen sind verschiedene, **voneinander getrennte Knoten** eines verteilten Systems
  - Szenario: z.B. Netzwerkausfall
  - bei Partitionierung, d.h. Zusammenbruch der Synchronisierung, zwei Reaktionsmöglichkeiten auf Schreibvorgänge
    - Schreibvorgänge abweisen (Konsistenz wahren)
    - Schreibvorgang später synchronisieren (Verfügbarkeit wahren)
- siehe auch: Consensus-Protokolle

<!--Darstellung CAP Theorem wahrscheinlich klausurrelevant-->

## asynchrone Replikation

![Asynchrone Replizierung](assets/async-repl.png)<!--width=600px-->

- schnelle Replikation, ACK-Msg wird sofort gesendet
- Verfügbarkeitsoptimiert
- Problem: ACK-Msg wird versandt, Replikation kann dennoch fehlschlagen

## synchrone Replikation

![Asynchrone Replizierung](assets/sync-repl.png)<!--width=600px-->

- Konsistenzoptimiert
- empfindlich gegenüber Latenzen, sonst signifikante Performance-Einbußen
  - daher nicht über große Distanzen geeignet
- ACK-Msg wird erst geschickt, wenn Replikation abgeschlossen

## synchrone Multi-Master-Replikation

![Asynchrone Replizierung](assets/sync-multi-master-repl.png)<!--width=600px-->

- Erweiterung der sync. Repl.
- oft vorgelagerter Load Balancer
- kein Master-Slave-System, sondern gleichberechtigte Master

## Galera

![Galera](assets/galera.png)<!--width=600px-->

- gute Eignung:
  - bei wenigen Schreibvorgängen, da teuer
  - häufige Lesezugriffe
  - keine hauptsächlich lokal relevanten Daten
- schlechte Eignung:
  - viele Schreibzugriff
  - lokal relevante Daten

### Galera ausgewählte Szenarien

#### Disaster Recovery

- problematisch bei nur zwei Sites
- zusätzliche Infrastruktur für Failover benötigt

#### Rolling Updates

- Schritt für Schritt Updates installieren, indem immer nur ein Knoten gestoppt und neu gestartet wird
- Zugriff auf andere Knoten noch möglich
- gestoppter Knoten holt ausstehende Replikation nach

#### Latenzreduktion

Latenz kann abhängig von der Geolokalität durch Load-Balancer optimiert werden, indem Clients den Knoten in physischer Nähe nutzen

#### Galera Konsistenzsicherung

- pessimistisch $\rightarrow$ Konsistenz im Vordergrund
- im Falle einer Partitionierung entstehen mehrere *Komponenten*
- nur eine Komponente kann *primär* sein $\rightarrow$ Quorum-Verfahren
- innerhalb einer Partition müssen >50% absolute Mehrheit vorhanden sein, um ein Quorum zu bilden
- Gewichtung der *Stimmen* auch möglich $\rightarrow$ Arbitratoren
