---
title: "Exkurs zu OpenRefine"
date: 2020-11-20
header:
  image: /assets/images/EXKURS.png
  teaser: "/assets/images/EXKURS.png"
---
Als Aufgabe mussten wir unsere DOAJ-Daten mit zusätzlichen Informationen aus lobid-gnd anreichern und das entsprechende Template erweitern sowie die so entstandene Datei exportieren. Dieser Eintrag soll von meinen Erfahrungen mit dieser Aufgabe berichten. 

## Anreicherung mit lobid-gnd
Im [lobid-Tutorial](https://blog.lobid.org/2018/08/27/openrefine.html) werden sehr rudimentäre Beispieldaten verwendet. Wir können hier auf unseren Datensatz mit ca. 1000 Einträgen, den wir bereits für die Library Carpentry Lesson verwendet haben, zurückgreifen. 

Wie in der Anleitung beschrieben, starten wir in der Spalte "Authors" den Reconciliation-Prozess. Da müssen wir die Service-URL `https://lobid.org/gnd/reconcile` angeben, damit die lobd-gnd-Datenbank überhaupt abgerufen werden kann. Lässt man den Prozess dann laufen, bietet sich bei mir dieses Bild:

![Reconciliated Data](https://raw.githubusercontent.com/leabaechli/bain/master/assets/images/OR_reconciliated.png)

Es hat bei mir für 46% der Einträge  Matches gefunden. Der Rest der Daten muss noch reconciliated werden. Ich denke, das ist darauf zurückzuführen, dass es a) entweder keinen entsprechenden Eintrag in der lobid-gnd gibt, oder dass die von mir verwendetetn Daten zum Teil fehlerhaft sein könnten. Ich könnte mich jetzt hier bei jedem einzelnen EIntrag durchklicken und dem auf den Grund gehen, da es sich aber um eine Übung handelt, verzichte ich aus Zeitgründen darauf. 

Stattdessen mache ich mit dem Tutorial weiter. Hier kann ich bei den reconciliierten Daten auswählen, welche dass ich "matchen" will. Das sieht dann bspw. so aus:

![matched](https://raw.githubusercontent.com/leabaechli/bain/master/assets/images/OR_match.png)

So fahre ich weiter und versuche, immer die von der Form her übereinstimmenden Matches auszuwählen - meistens gibt's ja mehrere Optionen. Was mir auffällt, ist dass bei diesem Prozess die Werke, die mehrere Autoren haben, dann nur noch einen Autor haben. Vermutlich hätte ich zuerst die Zellen noch mal mit GREL splitten sollen, damit keine Mehrfachnennungen in einer Zelle sind. Für "echte" Daten wäre das natürlich ein absolutes No-Go. Für Übungszwecke drücke ich hier ein Auge zu. 

Nachdem die Matches ausgewählt worden sind, kann die Tabelle um die reconciliierten Daten erweitert werden. 

![add columns](https://raw.githubusercontent.com/leabaechli/bain/master/assets/images/OR_addcolumns.png)

Ich habe mich für Berufsbezeichnung, Geburts- und Sterbedatum, Geburtstort sowie die GND-Nummer entschieden. 

Daraufhin kann die Auswahl bestätigt werden, worauf die entsprechenden neuen Spalten zu der bestehenden Tabelle hinzugefügt und mit den GND-Daten befüllt werden. 

## Templating
