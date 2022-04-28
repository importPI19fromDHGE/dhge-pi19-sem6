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

- [Klausurvorbereitung](#klausurvorbereitung)
  - [Aufgabe 1](#aufgabe-1)
    - [Lösung](#l%C3%B6sung)
      - [1. Punkte zeichnen](#1-punkte-zeichnen)
      - [2. Parameter für die Ellipse wählen](#2-parameter-f%C3%BCr-die-ellipse-w%C3%A4hlen)
      - [3. Ellipsengleichung und Schwellwertfunktion aufstellen](#3-ellipsengleichung-und-schwellwertfunktion-aufstellen)
      - [4. Überprüfung](#4-%C3%9Cberpr%C3%BCfung)
  - [Aufgabe 2](#aufgabe-2)
    - [Lösung](#l%C3%B6sung-1)
      - [1. ToDo](#1-todo)
      - [2. Optimierungsproblem aufstellen](#2-optimierungsproblem-aufstellen)
      - [Lösung des Optimierungsproblems](#l%C3%B6sung-des-optimierungsproblems)
      - [Trennbarkeit feststellen und Hyperebene aufstellen](#trennbarkeit-feststellen-und-hyperebene-aufstellen)
      - [Überprüfung (2)](#%C3%9Cberpr%C3%BCfung-2)

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

#### 3. Ellipsengleichung und Schwellwertfunktion aufstellen

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

## Aufgabe 2

> Stellen Sie für die vierdimensionalen Punktmengen `G:={(1,2,3,4), (1,1,1,1)}`
> und `B={(1,3,1,2), (2,2,-1,1)}` ein lineares Optimierungsproblem auf,
> welches die Trennbarkeit von `B` und `G` entscheidet. Falls Trennbarkeit
> vorliegt, geben Sie die Gleichung `f(x)=0` der trennenden Hyperebene an.
> Überprüfen Sie, ob `f(x)` auf `G` konstantes Vorzeichen besitzt und auf `B`
> das entgegengesetzte.

### Lösung

#### 1. ToDo

$$
G = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 1 & 1 & 1 & 1 \end{bmatrix}
\qquad
o = \begin{bmatrix} 0 \\ 0 \end{bmatrix}
\qquad
e_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

#### 2. Optimierungsproblem aufstellen

$$A = \text{stapeln}(\text{erweitern}(−G, e_1, o), \text{erweitern}(B, o, −e_1))=
\begin{bmatrix}
-1 & -2 & -3 & -4 & 1 &  0 \\
-1 & -1 & -1 & -1 & 1 &  0 \\
 1 &  3 &  1 &  2 & 0 & -1 \\
 2 &  2 & -1 & -1 & 0 & -1
\end{bmatrix}$$

$$B_1 = \begin{bmatrix}
  0\\
  0\\
  0\\
  0
\end{bmatrix}
\qquad
lb = -\begin{bmatrix}
  1\\
  1\\
  1\\
  1
\end{bmatrix}
\qquad
ub = -lb = \begin{bmatrix}
  1\\
  1\\
  1\\
  1
\end{bmatrix}$$

#### Lösung des Optimierungsproblems

> Die Lösung des Optimierungsproblems wird vorgegeben: *some `Mathlab`-magic*

$$x=\begin{bmatrix}
1 \\
-1 \\
1 \\
0 \\
1 \\
-1 \end{bmatrix}
\qquad
ans = -2$$

#### Trennbarkeit feststellen und Hyperebene aufstellen

Wenn die Differenz $b-a$ negativ ist, dann trennbar sind beide Punktwolken trennbar. Ist die Differenz positiv, dann ist die Trennbarkeit nicht vorhanden. Wenn es keine Differenz gibt $b-a = 0$, so gibt es Punkte, die auf der Hyperebene liegen.

$$b-a = (-1) -1 = -2 \quad \rightarrow\quad\text{Die Mengen sind trennbar}$$

Die Hyperebene ergibt sich ebenfalls aus dem Verktor $x$:

$$f(x_1,x_2,x_3,x_4)= 1 * x_1 - 1 * x_2 + 1 * x_3 + 0 * x_4 - \frac{1-1}{2}$$

> Die letzte Komponente in der Funktion der Hyperebene entspricht dem arithmetischen Mittelwert der letzten beiden Komponenten des Vektors ($\frac{a+b}{2}$).

#### Überprüfung (2)

