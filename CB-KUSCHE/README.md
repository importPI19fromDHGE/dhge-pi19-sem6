<!----------
title: "Wahlpflichtmodul Compilerbau"
date: "Semester 6"
keywords: [Compiler, Compilerbau, DHGE, Semester 6]
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

Wahlpflichtmodul Compilerbau
====================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Grundlagen](#grundlagen)
  - [Aufbau klassischer Compiler](#aufbau-klassischer-compiler)
  - [Begriffe](#begriffe)
- [Parser](#parser)
  - [Entwurf](#entwurf)
  - [Arten](#arten)
- [Lexer-Regeln](#lexer-regeln)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!--newpage-->

# Grundlagen

## Aufbau klassischer Compiler

- **Frontend:** Lexer, Parser
- **Infrastruktur:** Symboltabelle, Syntaxbaum
- **Backend:** Optimierer, Codegenerator

## Begriffe

### Value Propagation

Compiler bestimmt Wertebereich einer Variable

# Parser

## Entwurf

- Voraussetzung: Syntax-Definition
  - wesentlicher Teil der Spezifikation eines Compilers
  - Parser wird 1:1 auf Basis der Syntaxregeln codiert
- Lexer nimmt Zeichenstrom, assoziiert diesen mit Tokens, gibt Tokenstrom aus
  - d.h. keine Semantikprüfung von Namen, Terminalsymbole werden erkannt
  - Kommentare etc. werden entfernt
- Parser nimmt Tokenstrom
  - Tokens sind atomar
  - löst Non-Terminalsymbole auf
  - gibt entweder Syntaxbaum oder Operation wird ausgeführt (Interpreter) oder Code wird erzeugt (Compiler)

## Arten

- Top-Down-Parser: rekursiver Abstieg
  - für einfache Sprachen, normalerweise handcodiert
  - vom Programm-repräsentierenden Symbol wird Funktion aufgerufen, bis alles zu Terminalsymbolen aufgelöst ist
  - jedes Non-Terminalsymbol hat eine eigene Funktion
- Bottom-Up / Shift-Reduce Parser: tabellengesteuert
  - automatisch generiert
  - effizienter
  - Syntax der Sprache nicht im Code, nur in den Tabellen
  - geht von den einzelnen Tokens aus, findet passenden Weg im Baum hoch
  - Erklärung Shift-Reduce: wenn nicht reduziert werden kann, wird geshiftet, d.h. pushe auf Stack
    - solange shiften, bis reduziert werden kann: poppt alles vom Stack und reduzierte Funktion wird auf den Stack gelegt
  - Entscheidung der Aktion durch "wahnwitzige" Tabellen

# Lexer-Regeln

- ganz grundsätzlich muss zwischen alphabetischen und numerischen Zeichen unterschieden werden
- Darstellung mithilfe EBNF
  - Oder-Strich für Alternativen
  - eckige Klammern für optionale Ausdrücke
  - geschweifte Klammern für 0 oder mehr Mal
  - runde Klammern für Gruppierungen

```txt
digit = '0' | '1' ... | '9'
letter = 'a' | 'b' | ... | 'Z'
ident = (letter | '_'){digit | letter | '_'}
integer = digit{digit}
integer = digit[integer]
float = ['+'|'-']digit{digit}['.'{digit}][('e'|'E')['+'|'-']digit{digit}]
```

- der Ausdruck ``integer = {digit}digit`` ist unklug, weil man dann zwei Zeichen Lookahead benötigt
- Für den Float wurde absichtlich kein ``integer`` verwendet<!--didaktische Gründe-->
- TODO: hier Syntaxgraph einfügen
  - Achtung: eigentlich ist der falsch; die Regel kann nicht zwischen Float und Int unterscheiden $\rightarrow$ Zweideutigkeit
- Namenstrenner: Freiräume wie Leertasten, Tabs
