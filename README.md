# media-queries-crash-course

Erste Schritte in CSS mit MediaQueries

## Terminal wichtigste Befehle
|Befehl|Bedeutung|
|---|---|
|`dir`, `ls`| Inhaltsverzeichnis anzeigen|
|`cd`| Verzeichnis wechseln|

### GIT
|Befehl|Bedeutung|
|---|---|
|`git clone`| Klont ein Git-Repo|
|`git add .`| Alle Dateien ins Repo übernehmen|
|`git commit -m "Text zum Commit"`| Commit erstellen |
|`git push`| Commit ins Remote Repo übernehmen|
|`git pull`| Daten vom Remote Repo ziehen |




## Einführung

### Media Queries im CSS
```css
@media ( Bedingung ) {

    /* Hier kommen die CSS Anweisungen hin, 
       die interpretiert werden, 
       wenn die Bedingung erfüllt ist*/
}
```

### Typische Bedingungen

|Bedingung|Bedeutung|
|---|---|
|`max-width`|Stile gelten bis zu dieser Größe|
|`min-width`|Stile gelten ab dieser Größe |
|`orientation`| Bildschirmausrichtung `landscape` oder `portrait`|
|`screen`| Für Bildschirme gültig|
|`print`| Für Drucken gültig |
|`not`| Invertiert die Bedingung |

### Einfaches Beispiel
```html
<!-- index.html -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Erste Schritte mit Media Queries</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
</body>
```

```css
/* style.css */

html, body {
    width: 100%;
    height: 100%;
    background-color: green;
}

/* Alles bis zu einer Maximalen Breite von 1024px*/
@media (max-width: 1024px){
    
    html, body  {
        background-color: red;
    }
}
```

### Breakpoints
Es macht Sinn, vordefinierte Breakpoints zu verwenden. Dies werden zum Beispiel von [Bootstrap](https://getbootstrap.com/docs/5.0/layout/breakpoints/) verwendet.
> ![alt text](./assets/boots-trap-breakpoints.png)
> <br><sub>Breakpoints und Klassen von Bootstrap</sub>


## Aufgaben

### 1. Breakpoints nach Bootstrap

Setze die Breakpoints nach Boottrap so, um das die jeweilige Bildschirmgröße ausgegeben wird.

### 2. Horizontal, Vertikal

Zeige an, ob der Bildschirm Querformat oder Hochformat ist.


### 3. Ausdrucken

Wenn die Seite ausgedruckt wird, soll der `large`-Inhalte ausgegeben werden und das Aussehen angepasst werden:

- Hintergrund Weiss
- Schriftfarbe Schwarz
- Bilder weg

### 4. 3-Spalten Layout

Setze ein 3-Spalten Layout mit `flex` oder `grid` um.

Anforderungen:
- `xl` und größer: 3 Spalten
- `md` und `lg`: 2 Spalten
- `sm` und kleiner: 1 Spalte
