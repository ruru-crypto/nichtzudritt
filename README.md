# Das wichtigste zuerst

## Projektstruktur

- Im Ordner `_fragen` befinden sich die statischen Seiten (die auch in der Navigationsleiste anwählbar sind).
- Im Ordner `_themen` befinden sich die Themenkomplexe ("Fragen zu..").
- Bilder können in den Ordner **bilder** hochgeladen und in den Texten verlinkt werden.

## Markdown

Das Format der Dateien ist Markdown, das dann automatisch in HTML umgewandelt wird.
HTML kann aber auch verwendet werden.
Wie man Github-Markdown schreibt, kann man hier nachlesen:
https://guides.github.com/features/mastering-markdown/

# Änderungen machen

## Für neue Fragen

1. Einen GitHub Account erstellen / einloggen
1. Im Repository `ktiu/nichtzudritt` in den Ordner `_fragen` wechseln
2. Auf **Create new file** klicken
![Create new file](https://raw.githubusercontent.com/ktiu/nichtzudritt/main/bilder/tutorial/create_new_file.png)
4. Datei benennen, am besten mit `kurzer-titel.md`
5. In der Datei ganz oben steht der YAML-Header mit Titel, Tags (=Themen) und Links. Dieses Format muss sehr streng eingehalten werden und sieht z. B. so aus:
```
title: Warum sind die Namen der NSU-Mordopfer kaum bekannt?
tags: opfer rassismus
infos:
  - text: Kolumne. Namen (Süddeutsche Zeitung)
    url: https://www.sueddeutsche.de/politik/kolumne-namen-1.2940345
  - text: Warum uns die Täter mehr interessieren als ihre Opfer (Perspective Daily)
    url: https://perspective-daily.de/article/418/fwF8IU0t
  - text: "Ibrahim Arslan: „Die Opfer-Perspektive muss gestärkt werden“ (Stadtkulturmagazin Darmstadt)"
    url: https://www.p-stadtkultur.de/ibrahim-arslan-die-opfer-perspektive-muss-gestaerkt-werden/
---
```
6. Darunter folgt der Text in Markdown/HTML
3. Auf **Commit new file** klicken
4. Überprüfen und **Create pull request** wählen
5. Ggf. eine kurze Beschreibung / Erklärung der Änderungen verfassen und pull request bestätigen
6. Das war's! Der pull request mit den Änderungen ist für alle sichtbar und kann angenommen werden.

Neue Kategorien können analog im Ordner `_themen` angelegt werden.

## Kleine Änderungen und Korrekturen

1. Einen GitHub Account erstellen / einloggen
1. Im Repository `ktiu/nichtzudritt` die betreffende Datei finden
2. Auf der zu ändernden Datei auf den kleinen Stift im Menü oben rechts klicken:
![Fork this project and edit the file](https://raw.githubusercontent.com/ktiu/nichtzudritt/main/bilder/tutorial/fork_and_edit.png)
3. Änderungen vornehmen und auf **Propose file change** klicken
4. Überprüfen und **Create pull request** wählen
5. Ggf. eine kurze Beschreibung / Erklärung der Änderungen verfassen und pull request bestätigen
6. Das war's! Der pull request mit den Änderungen ist für alle sichtbar und kann angenommen werden.

## Für umfassendere Änderungen...

... (z. B. Designänderungen) ist es besser, zuerst an einer eigenen Kopie des gesamten Projekts Änderungen vorzunehmen und sich anzeigen zu lassen. Das geht so:

1. Im Repository `ktiu/nichtzudritt` auf "Fork" klicken. Das kopiert das komplette Projekt in den eigenen Account. (Das passiert übrigens auch bei der schnellen Methode automatisch im Hintergrund.)
1. Die Datei "CNAME" im eingenen Repository löschen (sonst kommt GitHub bei der Vorschau durcheinander).
1. Im *eigenen* Repository (also `https://github.com/{EIGENER-USERNAME}/nichtzudritt`) auf "Settings" klicken
2. Im Menüpunkt **Pages** die Option **Source** auf **Brach: main** setzen. Damit werden die Änderungen, die im eigenen Repository vorgenommen werden, live (mit einer kleinen Verzögerung) angezeigt.
3. Die Adresse für die Vorschau lautet dann: https://{EIGENER-USERNAME}.github.io/nichtzudritt/
4. Wenn die eigene Kopie soweit ist, dass die Änderungen in die Live-Seite einfließen sollen, muss noch ein pull request erstellt werden. Hierzu auf **New pull request** klicken 
5. Dann als **base repository** auswählen: **ktiu/nichtzudritt** (base: main)
6. Als **head repository**: **{EIGENER-USERNAME}/nichtzudritt** (compare: main)
7. Dann prüft GitHub, ob die Versionen zusammengeführt werden können. Solange nicht in der Zwischenzeit die gleichen Zeilen bearbeitet wurden, sollte das gehen.
8. Auf **Create pull request** klicken und dann nochmal bestätigen. Fertig!

Wenn Ihr in später Aktualisierungen von ktiu/nichtzudritt in euren fork "nachziehen" wollt, könnt ihr den pull request auch in die andere Richtung machen, d.h. "{EIGENER-USERNAME}/nichtzudritt" als base repository und "ktiu/nichtzudritt" als head repository.

# Zum Weiterlesen

- Das Format der Dateien ist Markdown, das dann automatisch in HTML umgewandelt wird. https://guides.github.com/features/mastering-markdown/
- Die Seite ist auf GitHub gehostet, wofür es hier eine schöne Einleitung gibt: https://guides.github.com/introduction/flow/
- Die Profi-Variante für eigene Änderungen ist, sich den [GitHub Desktop](https://desktop.github.com/) (oder sogar nur Git) und [Jekyll](https://jekyllrb.com/) zu installieren, das Repository lokal zu klonen und sich die Änderungen in Echtzeit auf dem eigenen Rechner anzeigen zu lassen, bevor man sie ins eigene repository pusht.
