<!----------
title: "Wissensbasierte Systeme / Neuronale Netze"
date: "Semester 6"
keywords: [Neuronal, Netz, Wissensbasiert, DHGE, Semester 6]
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

Wissensbasierte Systeme / Neuronale Netze
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Platzhalter](#platzhalter)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!--newpage-->

# Klausurvorbereitung

## Aufgabe 1

> Gegeben seien die drei Punkte `(1,1)`, `(2,1)` und `(4,2)`. Formulieren
> Sie ein Perzeptron mit elliptischer Schwellwertfunktion, sodass
> es auf diesen `3` Punkten eine `1` erzeugt und außerhalb der Ellipse `E`
> eine `0`. Verifizieren für einen Punkt außerhalb von `E`, dass das von
> Ihnen konstruierte Perzeptron eine `Null` annimmt. Wählen Sie die
> Halbachsen von `E` unterschiedlich.

Zusätzlich ist die Gleichung einer Ellipse gegeben:

$$
\frac{(x-x_0)^2}{a^2} + \frac{(y-y_0)^2}{b^2} = 1
$$

### Lösung

#### 1. Punkte zeichnen

$$
xp = \begin{pmatrix} 1 & 2 & 4 \end{pmatrix}\\
yp = \begin{pmatrix} 1 & 1 & 2 \end{pmatrix}
$$

Am Besten sollten man sich die Punkte in einem Graphen anzeigen lassen.

#### 2. Parameter für die Ellipse wählen

Anhand des Graphens sind die Parameter für die Ellipsen-Gleichung zu wählen, sodass die Ellipse die gegebenen Punkte einschließt.

$$
x_0 = 2.5 \\
y_0 = 1.5 \\
a = 2 \\
b = 1.5
$$

Die Bedingung $a \neq b$ muss gelten!

Eine grafische Überprüfung der Parameter ist empfehlenswert.

#### 3. Ellipsengleichung und Aktivierungsfunktion aufstellen

Aus den gewählten Parametern ergibt sich die Ellipsengleichung:

$$
s(x,y) = \frac{(x-x_0)^2}{a^2} + \frac{(y-y_0)^2}{b^2} - 1
$$

$$
\sigma = \begin{cases} 1 & \text{if } x\leq 0 \\ 0 & \text{otherwise} \end{cases}
$$

$$
g(x,y)=\sigma(s(x,y))
$$

#### 4. Überprüfung

Die aufgestellte Funktion $g(x,y)$ muss für alle Punkte innerhalb der Ellipse 1 und für alle Punkte außerhalb der Ellipse 0 ergbene. Die gegebenen Punkte werden zur Überprüfung in die Funktion eingesetzt. Diese Prüfung soll ebenfalls mit einem weiteren Punkt durchgeführt werden, der sich außerhalb der Ellipse befindet.

$$
g(1,1)=1 \\
g(2,1)=1 \\
g(4,2)=1 \\
g(5,5)=0
$$

