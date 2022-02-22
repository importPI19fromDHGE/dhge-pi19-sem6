<!----------
title: "Wahlfplichtmodul Unity"
date: "Semester 6"
keywords: [Unity, Echtzeitvisualisierung, DHGE, Semester 6]
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

Unity Echtzeitvisualisierung
===========================================

<!-- md2apkg ignore-card -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Inhaltsverzeichnis**

- [Platzhalter](#platzhalter)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!--newpage-->


# Unity-Glossar

<!-- md2apkg ignore-card -->

Im Kurs tauchen Begriffe von CAD,CG auf. Dazu bitte im Sem 5 nachschauen.

## Geometrische Schnittstelle

Realisierung des Datenaustauschs z. B. bei CAD- und DCC-Systemen

## Beispiele Geometrische Schnittstelle

- JT
- STEP
- IGES
- FBX
--OBJ
- glTF
- Alembic

## Grafikpipeline

Schritte zur Umsetzung einer Grafischen Darstellung aus dem zwei- oder dreidimensionalen Raum [siehe Wikipedia](https://de.wikipedia.org/wiki/Grafikpipeline); als Beispiel die [Rendering Pipeline von Direct3D](https://docs.microsoft.com/en-us/windows-hardware/drivers/display/rendering-pipeline)


Schritte zur Umsetzung einer Grafischen Darstellung aus dem zwei- oder dreidimensionalen Raum (siehe https://de.wikipedia.org/wiki/Grafikpipeline )


## Beispiele Grafikpipeline

- Koordinatensysteme
- Definition des Objektes
- Tesselation
- Transformationen
- Perspektiven
- Clipping
- Rasterisierung
- Shader

## Grafische Schnittstelle und Beispiele

Plattform- und programmiersprachenübergreifenden Programmierschnittstelle zur Entwicklung von 2D- und 3D-Computergrafikanwendungen.

- DirectX/Direct3D
- OpenGL
- Vulkan
- Metal

## Koordinatentransformationen (Auswahl)

- Translation
- Rotation
- Skalierung
- Spieglung
- Scherung

[siehe](https://de.wikipedia.org/wiki/Koordinatentransformation) bzw. [allgemein](https://de.wikipedia.org/wiki/Liste_von_Transformationen_in_der_Mathematik)

Vertiefung für Drehung mit Anwendung z. B: in PLM-Systemen und in 3ds max in Animationen: Eulersche Winkel [siehe](https://de.wikipedia.org/wiki/Eulersche_Winkel)

## Level of Detail (LOD)

TODO

## Lichtquellen

TODO

## Materialbeschreibung

Parameter zur Beschreibung der optischen Eigenschaften eines Werkstoffs.

- abhängig vom eingesetzten Berechnungsverfahren (Renderer)
- Anforderungen an den Datenaustausch (siehe auch Geometrische Schnittstellen)
- neue Anforderungen für Echtzeitvisualisierungen
- einfache Modelle z. B. für Phon Beleuchtungsmodell und Phong Shading

Wechsel zu physikbasierten Materialbeschreibungen (PBR-Materialien) z. B. NVIDIA Material Definition Language (MDL)  https://developer.nvidia.com/mdl-sdk oder MaterialX https://www.materialx.org/ oder auch glTF

## Metadaten

Zusätzliche Informationen z. B. in Dateien (3D-Modelle und Pixelbilder). Beispiele für Fotos z. B. EXIF (Exchangeable Image File Format). Siehe auch geometrische Schnittstellen wie JT und STEP.

Ablage z. B. auch in Datenbanksystemen wie z. B. für PDM, PLM und Assetmanagement.

Alternativbegriffe: Attribute/Eigenschaften

## Renderer

Software zur Berechnung der Bilder (siehe auch Bildsynthese bei Wikipedia: https://de.wikipedia.org/wiki/Bildsynthese )

z. B. Vergleich CPU vs. GPU: https://knowledge.autodesk.com/de/support/3ds-max/troubleshooting/caas/sfdcarticles/sfdcarticles/DEU/3ds-Max-Differences-between-GPU-and-CPU-based-rendering.html

## Shader

Hardware- bzw. Softwaremodule zur Berechnung im Umfeld der Computergrafik. https://en.wikipedia.org/wiki/Shader

siehe Aufgabe Grafikkarten und Grafikpipeline

siehe Grafische Schnittstellen (API)

siehe Beleuchtungsmodelle

## Tesselierung


Zerlegung einer exakten Geometrie in ebene Flächen (meist Dreiecke oder Vierecke -"triangulated or quadrangulated polygon Meshes" ).

a) beim Datenaustausch (z. B. JT-Format oder Formate aus dem DCC-Bereich)

b) in Echtzeit siehe Grafische Schnittstellen

siehe: https://en.wikipedia.org/wiki/Tessellation_(computer_graphics)

siehe  z. B. https://www.khronos.org/opengl/wiki/Tessellation


