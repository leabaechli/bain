---
title: "Markdown-Merkblatt"
permalink: /markdown/
date: 2020-09-22
---

Dies ist eine von mir für mich zusammengestellte Version der Markdown-Befehle, die ich wohl für diesen Blog am meisten nutzen werde (und dient auch gleich zur Übung). 
Die Quelle sowie weiterführende Befehle sind [hier](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) zu finden. 


### Textformatierung
* `*kursiv*` = *kursiv* 
* `**fett**` oder `__fett__` = **fett** 
* `**_fett und kursiv_**` = **_fett und kursiv_**
* `~~durchgestrichen~~` = ~~durchgestrichen~~
* `Code` = `Code`(lässt sich nicht wirklich darstellen, braucht aber zwei Backticks (`) um das Codestückchen und der Code wird inline angezeigt)

### Überschriften
* `# H1`
* `## H2`
* `### H3`
* `#### H4`
* `##### H5`
* `###### H6`

Leerschlag zwischen # und H nicht vergessen!

### Listen und Aufzählungen

* `*` = ungeordnete Liste, auch hier auf den Leerschlag achten, sonst kommen sich die *kursiv*-Asterisks und die Listen-Asterisks in die Quere
2. `1.` = geordnete Liste -- wobei es nicht darauf ankommt, mit welcher Zahl die Liste anfängt

Es gibt noch mehr Arten von Listen, ich nehme aber an, dass mir diese zwei Varianten genügen werden. Falls nicht, sind weitere Varianten [hier](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists) aufgeführt. 

### Links

`[Bezeichnung](URL)`

Mehr Arten von Links gibt es [hier](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links).

### Bilder
Es gibt zwei Wege, wie man Bilder darstellen kann: 
* im Fliesstext selbst, ähnlich wie ein Link `![Alternativtext](https://static.thenounproject.com/png/212328-200.png "Bild-Titel")` 
* oder zuerst das Bild definieren `[eindeutige Variable für Bild]: https://static.thenounproject.com/png/212328-200.png "Bild-Titel"` und dann mit `![Alternativtext][eindeutige Variable für Bild]` aufrufen 

### Tabellen

```
| Spalte 1    |  Spalte 2  |     Spalte 3 |
| ----------- | :--------: | -----------: |
| linksbündig |  zentriert | rechtsbündig |

```

Wichtig ist bei Tabellen vor allem, dass die erste Reihe immer von mindestens drei Bindestrichen von der nächsten Spalte getrennt ist. Die `|` sind optional, helfen aber sicherlich bei der Orientierung. Und die Spalten müssen im Code auch nicht gleich breit sein: Das zweite Beispiel unten ergibt die genau gleiche Tabelle wie das Beispiel oben. 

```
| Spalte 1 | Spalte 2 | Spalte 3 |
| --- | :---: | ---: |
| linksbündig | zentriert | rechtsbündig |
```

Die Spaltenbreite passt sich unabhängig von der Anzahl `-` immer am Inhalt an. 
