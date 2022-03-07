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
-->
# Prüfungsleistung

- schriftliche Klausur (60 min)
- wird zu 50% verrechnet (Rest `NET-BARIE` aus Semester 5)
- eine DIN-A4-Seite beidseitig beschriftet als Cheatsheet erlaubt

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
