# Balliercup- Website

Diese README-Datei bietet eine Übersicht über die BallierCup-Webseite. Die Webseite ist eine responsive Seite auf Basis von Bootstrap und wurde für das BallierCup-Event entwickelt. Sie zeigt Veranstaltungsdetails, Zeitpläne, Anmeldeinformationen und eine Galerie.


## Bibliotheken und Frameworks
**Bootstrap 5.3.2**: Wird für das Layout, Buttons und die Akkordeon-Komponente verwendet und ermöglicht ein responsives Design.

**CSS**: Benutzerdefinierte Styles zur Verbesserung des Designs und der mobilen Responsivität.

## Seitenabschnitte

### Header und Event-Banner

Das Banner enthält ein Hintergrundbild und einen hervorgehobenen Titel mit Event-Details, die über das Bild gelegt sind.
Das Bild liegt im Hauptordner des Repos.

### Informationsabschnitt
Ein einleitender Text beschreibt die Veranstaltung, gibt Besuchern den Überblick über Datum, Ort und Zweck des Events.

Mit ```<p>```Inhalt ```</p>``` wird eine neue Zeile hinzugefügt.
Soll über der Zeile ein kleiner Abstand sein, bekommt der Paragraf noch eine Klasse. 
```<p class="spacing">```

Ein Link wird folgend eingefügt: ```<a class="link" href="mailto:balliercup@handball.esv-dresden.de">balliercup@handball.esv-dresden.de</a>```

> [!NOTE]
> ```<p></p>``` bzw. ```<p class="spacing"></p>``` für neue Zeilen
> 
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p

> [!NOTE]
> ```<a class="link"></a>``` für neue Links
> 
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a

> [!NOTE]
> ```<b>Fetter Text</b>``` für Fett
> 
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b

> [!NOTE]
> ```<i></i>``` für Kursiv
> 
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i

> [!TIP]
> MDN hat hilfreiche Infos für HTML Elemente
>
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element

### Akkordeon-Abschnitte
Jeder Akkordeon-Abschnitt enthält spezifische Details:

**Ablauf**: Listet die Veranstaltungszeiten und Aktivitäten auf.
**Anmeldung**: Erklärt den Anmeldestatus, die Startgebühr und Informationen zur Fotoerlaubnis.
**Turnierplan**: Platzhalter für den Turnierplan mit einem Button.
**Übernachtung**: Informationen zu Übernachtungsmöglichkeiten und den dazugehörigen Gebühren.

Ein neues Akkordeon wird so eingefügt: 
```
<div class="accordion-item">
  <h2 class="accordion-header">
    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseTwo" aria-expanded="false" aria-controls="flush-collapseTwo">
      <!-- Hier Überschrift einfügen -->
    </button>
  </h2>
  <div id="flush-collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
    <div class="accordion-body">
      <!-- Hier Inhalt einfügen -->
    </div>
  </div>
</div>
```

#### Buttons

__Ausgegrauter Button:__

```
<a class="btn btn-secondary disabled" role="button" target="_blank">Anmeldung (geschlossen)</a>
```

__Button:__
```
<a class="btn btn-secondary" role="button" target="_blank" href=""www.example.com>Anmeldung</a>
```

### Galerie-Bereich
Zeigt Miniaturbilder, die beim Anklicken ein größeres Bild anzeigen.

```
<div class="main-image">
  <img id="mainImg" src="images/image1.jpg" alt="Main Image">
</div>
<div class="thumbnail-images" id="thumbnailContainer">
  <img class="thumbnail" src="images/image1.jpg" alt="Thumbnail 1">
  <img class="thumbnail" src="images/image10.jpg" alt="Thumbnail 2">
  <img class="thumbnail" src="images/image11.jpg" alt="Thumbnail 3">
...
```

Die Bilder liegen im Repo im __images__ Ordner

Mit dem Script
```
<script>
        document.addEventListener("DOMContentLoaded", function() {
          const thumbnails = document.querySelectorAll(".thumbnail");
        
          thumbnails.forEach(thumbnail => {
            thumbnail.addEventListener("click", function() {
              const mainImg = document.getElementById("mainImg");
              mainImg.src = this.src;
            });
          });
        });

 </script>
```

ist die Funktionalität der Galerie umgesetzt.




