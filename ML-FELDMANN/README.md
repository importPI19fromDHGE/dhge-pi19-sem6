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
  - \setcounter{MaxMatrixCols}{20}

---------->

Wissensbasierte Systeme / Neuronale Netze
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Klausurvorbereitung](#klausurvorbereitung)
  - [Aufgabe 1](#aufgabe-1)
    - [Aufgabe 1: Lösung](#aufgabe-1-l%C3%B6sung)
      - [1. Punkte zeichnen](#1-punkte-zeichnen)
      - [2. Parameter für die Ellipse wählen](#2-parameter-f%C3%BCr-die-ellipse-w%C3%A4hlen)
      - [3. Ellipsengleichung und Schwellwertfunktion aufstellen](#3-ellipsengleichung-und-schwellwertfunktion-aufstellen)
      - [4. Überprüfung](#4-%C3%9Cberpr%C3%BCfung)
  - [Aufgabe 2](#aufgabe-2)
    - [Aufgabe 2: Lösung](#aufgabe-2-l%C3%B6sung)
      - [1. Matrizen aufstellen](#1-matrizen-aufstellen)
      - [2. Optimierungsproblem aufstellen](#2-optimierungsproblem-aufstellen)
      - [3. Lösung des Optimierungsproblems](#3-l%C3%B6sung-des-optimierungsproblems)
      - [4. Trennbarkeit feststellen und Hyperebene aufstellen](#4-trennbarkeit-feststellen-und-hyperebene-aufstellen)
      - [5. Überprüfung](#5-%C3%9Cberpr%C3%BCfung)
  - [Aufgabe 3](#aufgabe-3)
    - [Aufgabe 3: Lösung](#aufgabe-3-l%C3%B6sung)
  - [Aufgabe 4](#aufgabe-4)
    - [Aufgabe 4: Lösung](#aufgabe-4-l%C3%B6sung)
      - [1. Punkte aufstellen und optisch auf Trennbarkeit prüfen](#1-punkte-aufstellen-und-optisch-auf-trennbarkeit-pr%C3%BCfen)
      - [2. Vorbereitung des Lernperzeptron-Algorithmus](#2-vorbereitung-des-lernperzeptron-algorithmus)
      - [3. Durchführung des Lernperzeptron-Algorithmus](#3-durchf%C3%BChrung-des-lernperzeptron-algorithmus)
  - [Aufgabe 5](#aufgabe-5)
    - [Aufgabe 5: Lösung](#aufgabe-5-l%C3%B6sung)
      - [1. Funktion $f(x,y,z)$ aufstellen](#1-funktion-fxyz-aufstellen)
      - [2. Aktivierungsfunktion und Perzeptronen definieren](#2-aktivierungsfunktion-und-perzeptronen-definieren)

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

### Aufgabe 1: Lösung

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

### Aufgabe 2: Lösung

#### 1. Matrizen aufstellen

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

#### 3. Lösung des Optimierungsproblems

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

#### 4. Trennbarkeit feststellen und Hyperebene aufstellen

Wenn die Differenz $b-a$ negativ ist, dann trennbar sind beide Punktwolken trennbar. Ist die Differenz positiv, dann ist die Trennbarkeit nicht vorhanden. Wenn es keine Differenz gibt $b-a = 0$, so gibt es Punkte, die auf der Hyperebene liegen.

$$b-a = (-1) -1 = -2 \quad \rightarrow\quad\text{Die Mengen sind trennbar}$$

Die Hyperebene ergibt sich ebenfalls aus dem Verktor $x$:

$$f(x_1,x_2,x_3,x_4)= 1 * x_1 - 1 * x_2 + 1 * x_3 + 0 * x_4 - \frac{1-1}{2}$$

> Die letzte Komponente in der Funktion der Hyperebene entspricht dem arithmetischen Mittelwert der letzten beiden Komponenten des Vektors ($\frac{a+b}{2}$).

#### 5. Überprüfung

Punktemengen nacheinander zeilenweise in die Funktion $f(x_1,x_2,x_3,x_4)$ einsetzen.

$$\begin{matrix}
  G: & f(1,2,3,4)=2 &\quad& f(1,1,1,1)=1 \\
  B: & f(1,3,1,2)=-1 &\quad& f(2,2,-1,-1)=-1
\end{matrix}$$

> G und B besitzen jeweils ein konstantes jedoch nicht das gleiche Vorzeichen.

## Aufgabe 3

> Zeichnen Sie die konvexe Menge der Punkte $(1,1)$, $(1,3)$, $(2,3.5)$, $(3,5)$, $(2,2)$, $(2,3)$.

### Aufgabe 3: Lösung

1. Punkte in einen Graphen zeichnen
2. Äußere Punkte der Punktmenge mit einem geschlossenen Kantenzug umranden
3. ...
4. Profit!!!

## Aufgabe 4

> Stellen Sie für die Punktmengen $G:={(1,1), (1,3), (2,4)}$, und $B:={(3,5),(2,2),(2,1)}$ den
> Lernperzeptron-Algorithmus auf und führen Sie zwei Iterationsschritte ausgehend vom
> Startvektor $w0:=[-2.5,1,4]^T$ aus. Benutzen Sie die Zahlenfolge $\varphi_k:=1-1/(1+k^2)$.
> Zeichnen Sie beide Punktmengen und entscheiden Sie optisch, ob beide Mengen
> linear trennbar sind. Geben Sie im trennbaren Fall, die Gleichung einer Trenngeraden
> an und zeichnen Sie deren Graph zwischen die Punktmengen ein. Ordnen Sie in der
> Trainingsfolge $\xi$ die Punkte aus $G$ und $B$ abwechselnd an, beginnend mit einem
> grünen Punkt. Behalten Sie die Reihenfolge der Elemente von $G$ und $B$ bei.

### Aufgabe 4: Lösung

#### 1. Punkte aufstellen und optisch auf Trennbarkeit prüfen

$$
G_1=\begin{bmatrix}1\\1\end{bmatrix}\quad
G_2=\begin{bmatrix}1\\3\end{bmatrix}\quad
G_3=\begin{bmatrix}2\\4\end{bmatrix}
$$

$$
B_1=\begin{bmatrix}3\\5\end{bmatrix}\quad
B_2=\begin{bmatrix}2\\2\end{bmatrix}\quad
B_3=\begin{bmatrix}2\\1\end{bmatrix}
$$

> Anschließend beide Punktmengen in einem Graphen zeichen.
> Empirisches Bilden einer linearen Funktion ($f(x)=ax+b$) zum Trennen der Punktmengen.
> Ist eine solche Funktion gefunden, werden die Mengen als trennbar betrachtet und es kann fortgefahren werden.

$$f(x)=3x-3$$

#### 2. Vorbereitung des Lernperzeptron-Algorithmus

> Zur Durchführung des Lernperzeptronen-Algorithmus müssen die Punkte zunächst erweitert und zu einer Matrix zusammengeführt werden.

$$
G_{1ext}=\begin{bmatrix}1\\1\\1\end{bmatrix}\quad
G_{2ext}=\begin{bmatrix}1\\3\\1\end{bmatrix}\quad
G_{3ext}=\begin{bmatrix}2\\4\\1\end{bmatrix}
$$

$$
B_{1ext}=\begin{bmatrix}3\\5\\1\end{bmatrix}\quad
B_{2ext}=\begin{bmatrix}2\\2\\1\end{bmatrix}\quad
B_{3ext}=\begin{bmatrix}2\\1\\1\end{bmatrix}
$$

$$
\xi_1 = \begin{bmatrix} G_{1ext} & -B_{1ext} & G_{2ext} & -B_{2ext} & G_{3ext} & -B_{3ext} \end{bmatrix}\\
\quad\\
\xi_1 = \begin{bmatrix}
1 & -3 & 1 & -2 & 2 & -2 \\
1 & -5 & 3 & -2 & 4 & -1 \\
1 & -1 & 1 & -1 & 1 & -1 \\
\end{bmatrix}
$$

#### 3. Durchführung des Lernperzeptron-Algorithmus

> Für zwei Iterationsschritte wird die Matrix $\xi_1$ zweimal aneinander gehangen, um die Trainingsfolge $\xi$ zu erzeugen.

$$
\xi = \begin{bmatrix}
1 & -3 & 1 & -2 & 2 & -2 & 1 & -3 & 1 & -2 & 2 & -2 \\
1 & -5 & 3 & -2 & 4 & -1 & 1 & -5 & 3 & -2 & 4 & -1 \\
1 & -1 & 1 & -1 & 1 & -1 & 1 & -1 & 1 & -1 & 1 & -1 \\
\end{bmatrix}
$$

> Der Startvektor $w^{<0>}$ und die Zahlenfolge $\varphi_k$ werden der Aufgabenstellung entnommen.

$$
w^{<0>} = \begin{bmatrix}-2.5\\1\\4\end{bmatrix} \qquad \varphi_k = 1-\frac{1}{1+k^2}
$$

$$
w^{<k+1>} =
\begin{cases}
  w^{<k>} & \text{if} \quad {w^{<k>}}^T * \xi^{<k>} > 0 \\
  (w^{<k>} + \varphi_k * \xi^{<k>}) & \text{otherwise}
\end{cases}
$$

> Entsprechend $w^{<k+1>}$ werden nun zwei Iterationsschritte ausgeführt.

$$
{w^{<0>}}^T * \xi^{<0>} =
\begin{bmatrix}
  -2.5 & 1 & 4\\
\end{bmatrix} * \begin{bmatrix}
  1 \\ 1 \\ 1
\end{bmatrix} = 2.5
\quad\rightarrow\quad 2.5 > 0 \quad\rightarrow\quad w^{<1>} = w^{<0>} = \begin{bmatrix}-2.5\\1\\4\end{bmatrix}
$$

$$
{w^{<1>}}^T * \xi^{<0>} =
\begin{bmatrix}
  -2.5 & 1 & 4\\
\end{bmatrix} * \begin{bmatrix}
  -3 \\ -5 \\ -1
\end{bmatrix} = -1.5
\quad\rightarrow\quad -1.5 < 0 \quad\rightarrow\quad w^{<2>} = w^{<1>} * \varphi_1 * \xi^{<1>} = \begin{bmatrix}-4\\1.5\\3.5\end{bmatrix}
$$

## Aufgabe 5

> Man simuliere die Boolesche Funktion $f(x,y,z)$ mit folgendem Werteverlauf
> durch ein Neuronales Netz! Kontrollieren Sie die Korrektheit Ihrer Konstruktion
> indem Sie alle möglichen Eingaben auswerten.

$$\begin{bmatrix}x&y&z&f(x,y,z)\\
0 & 0 & 0 & 1\\
0 & 0 & 1 & 0\\
0 & 1 & 0 & 1\\
0 & 1 & 1 & 0\\
1 & 0 & 0 & 0\\
1 & 0 & 1 & 0\\
1 & 1 & 0 & 0\\
1 & 1 & 1 & 0
\end{bmatrix}$$

### Aufgabe 5: Lösung

#### 1. Funktion $f(x,y,z)$ aufstellen

> $f(x,y,z)$ kann sehr einfach über die Konjunktive Normalform (KNF) gebildet werden.
> Dazu werden die Eingangsbelegungen, die $1$ ergeben konjunktiv verknüpft.

$$(\neg x \land \neg y \land \neg z) \lor (\neg x \land y \land \neg z)$$

#### 2. Aktivierungsfunktion und Perzeptronen definieren

$$\sigma(x)=\begin{cases}
  1 & \text{if} \quad 0 \leq x \\
  0 & \text{otherwise}
\end{cases}$$

$$\begin{matrix}
  AND(x,y,z) & = & \sigma(x+y+z-3) \\
  OR(x,y) & = & \sigma(x+y-0.5) \\
  NOT(x) & = & \sigma(-x + 0.5) \\
\end{matrix}$$

#### 3. Perzeptronen entsprechend der logischen Funktion verknüpfen

$$Neu(x,y,z) = OR(AND(NOT(x),NOT(y),NOT(z)),AND(NOT(x),y,NOT(z)))$$

## Aufgabe 6

> Berechnen Sie für die Eingabe (1,2,3) die Ausgabe folgenden Netzwerkes:

*some Netzwerk*

### Aufgabe 6: Lösung

1. Werte in Funktion des Netzwerkes einsetzen
2. ...
3. Profit!!!
