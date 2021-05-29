# Bootstrap - eine kleine Zusammenfassung

## Container
Container sind ein Grundgerüst in Bootstrap. Es gibt zwei wesentliche Container:
+ Fixed Container: nutzt eine festgelegte width, je nach Bildschirmgröße `<div class="container">`
+ Fluid Container: nutzt die volle width `<div class="container-fluid">`

Mit `.container-sm|md|lg|xl` bzw. `xxl`(bootstrap5) lassen sich responsive Container erzeugen, je nachdem ob sie schon bei kleinen Bildschirmen (sm) oder bei großen (xl) die Weite auf 100% stellen sollen.

## Grid 
Die responsive Griddarstellung erlaubt bis zu 12 Spalten.
Entweder selber die Spaltenanordnung festlegen, dabei sollte der erste Stern die responsivness `(sm|md|lg|xl)` darstellen, der zweite die Spaltenposition/Spaltenausdehnung (`1-12`; in Summe sollte dann jede Reihe 12 ergeben):
``` html
    <div class="container">
        <div class="row">
            <div class="col-*-*"></div>
            <div class="col-*-*"></div>
        </div>
        <div class="row">
            <div class="col-*-*"></div>
            <div class="col-*-*"></div>
            <div class="col-*-*"></div>
        </div>
    </div>
```

Oder Bootstrap die Spaltenposition selber einteilen lassen, bei 3 Spalten nimmt jede zB 33% ein:

``` html
    <div class="container">
        <div class="row">
            <div class="col"></div>
            <div class="col"></div>
            <div class="col"></div>
        </div>
    </div> 
```

## Typographie
Neben den üblichen HTML-Überschriften gibt es weitere Klassen und HTML-Tags um die Typologie zu gestalten:
+ Abkürzung: 
`<abbr title="World Health Organization">WHO</abbr>`
+ Code: 
`<code>list = [1,2,3]</code>`
+ Displays: werden verwendet um mehr hervorzustechen: 
`<h1 class="display-1">Display 1</h1>`
+ Blockzitat: 
``` html
<blockquote class="blockquote">
    <p>For 50 years, WWF has been protecting the future of nature.</p>
    <footer class="blockquote-footer">From WWF's website</footer>
</blockquote>
```
+ Boldness. Alternativ auch mit bolder, light, lighter und normal: 
` <p class="font-weight-bold">Bold text.</p>`. 
+ Kursiv bzw. italic: 
`<p class="font-italic">Italic text.</p>` 
+ Kleiner Text: 
`<p class="small">This paragraph is smaller.</p>` oder einfach `<small>...</small>`
+ Ausrichtung/Blocksatz. Alternativ auch mit right, center und justify:
`<p class="text-left">Left-aligned text.</p>`
+ Unterstrich ausschalten: 
`<a href="#" class="text-decoration-none">No underline.</a>`
+ Uppercase. Alternativ auch Lowercase:
`<p class="text-uppercase">...</p>`
+ Eigenschaften Von Parents vererben:
`<a href="#" class="text-reset">reset link</a>.</p>`
+ Keine Aufzählungspunkt in Liste:
`<ul class="list-unstyled">...</ul>`

## Tabellen
Alternativ kann auch mit .table-striped oder .table-bordered gearbeitet werden.
``` html
<div class="container-fluid">        
  <table class="table">
    <thead>
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>John</td>
        <td>Doe</td>
      </tr>
      <tr>
        <td>Mary</td>
        <td>Moe</td>
      </tr>
    </tbody>
  </table>
</div>
```

## Bilder
Bilder können folgendermaßen ausgerrichtet werden:
``` html
<img src="paris.jpg" class="float-left">
<img src="paris.jpg" class="float-right"> 
<img src="paris.jpg" class="mx-auto d-block"> <!--margin:auto and display:block = centered-->
```
Responsive können Bilder mit der Klasse `class="img-fluid"` gemacht werden. Dabei wird die Bildgröße an den Bildschirm bzw. das Parent Element angepasst.

## Badges, Buttons, Alerts, Jumbotron

Jumbotrons sind große, aufmerksamkeitserregende Container:
``` html
<div class="container">
  <div class="jumbotron">     
    <p>Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile-first projects on the web.</p>
  </div>  
</div>
```

Alerts zeigen Hinweise an:
``` html
<div class="alert alert-success">
  <strong>Success!</strong> Indicates a successful or positive action.
</div>
```

Einfache Buttons:
``` html
<a href="#" class="btn btn-info" role="button">Link Button</a>
<button type="button" class="btn btn-info">Button</button>
```
Eine leicht andere Funktion als Buttons bieten Dropdownbuttons an:
```html
<div class="container">
  <div class="dropdown">
    <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown"> 
        <!-- dropdown-toggle = zeigt tooglezeichen; btn-primary = Modifier für Erscheinungsbild-->
      Dropdown button
    </button>
    <div class="dropdown-menu">
      <a class="dropdown-item" href="#">Link 1</a>
      <a class="dropdown-item" href="#">Link 2</a>
      <div class="dropdown-divider"></div> <!-- Trennlinie-->
      <a class="dropdown-item" href="#">Another link</a>
    </div>
  </div>
</div>
```

Ein Collapsebutton verbirgt (oft längeren) Content und zeigt ihn beim Aufklappen:
``` html
<div class="container">
  <button type="button" class="btn btn-primary" data-toggle="collapse" data-target="#demo">Collapsebutton</button>
  <div id="demo" class="collapse">
Ein Sampletext, ein Sampletext.
  </div>
</div>
```

Badges sind Fähnchen die Text kennzeichnen:
``` html
  <span class="badge badge-info">Info</span>
  <span class="badge badge-light">Light</span>
  <span class="badge badge-dark">Dark</span>
```

## Pagination (Seitenzahlen)
Ähnelt Buttons und sollte mit einer ul-list genutzt werden:
``` html
<div class="container">              
  <ul class="pagination">
    <li class="page-item"><a class="page-link" href="#">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</div>
```

## Cards
Karten sind rechteckige Boxen. 
Die Grundstruktur lautet wie folgt:
``` html
<div class="card">
  <div class="card-body">Basic card</div>
</div>
```
Cards können mit Bildern, Headern und Footern angereichert werden:
``` html
<div class="container">
  <div class="card" style="width:400px">
    <div class="card-header">Header</div>
    <img class="card-img-top" src="image.png" alt="Card image" style="width:100%">
    <div class="card-body">
      <h4 class="card-title">Max Mustermann</h4>
      <p class="card-text">Mustertextmustertext.</p>
      <a href="#" class="btn btn-primary">See Profile</a>
    </div>
    <div class="card-footer">Footer</div>
  </div>
</div>
```

## Nav Menüs

Navigationsmenüs können durch Listen erstellt werden, dazu einfach `nav` als Klasse bei `<ul>` und `nav-item` bei `<li>` hinzufügen. Der Link in der Navigation sollte mit `nav-link` klassifiziert werden.

Statt `nav` kann auch `nav-tabs` oder `.nav-pills` verwendet werden. Nav Menüs sind übrigens auch toggleable.

## Modals, Tooltip, Toast, Popover
Es gibt auch Modals und Tooltips. Erstere zeigen eine Art Popup an bei einem Mausklick, Zweitere zeigen einen Hinweis beim Drüberfahren der Maus an. Ein Toast zeigt einen kleinen Hinweispopup für eine kurze Zeit an und ein Popover ähnelt dem Tooltip.

## Navbar
Grundsätzlich startet eine Navbar mit folgendem HTML Element:
``` html
<nav class="navbar navbar-expand-sm">
```
`navbar-expand-**` kennzeichnet ab wann die Navbar vertikal gestapelt wird (für die mobile Ansicht) und kann mit `sm|md|lg|xl` bzw. `xxl`(bootstrap5) versehen werden.

Innerhalb des nav-Element befindet sich wiederum eine Liste:
``` html

  <ul class="navbar-nav">
    <li class="nav-item">
      <a class="nav-link" href="#">Link Numero 1</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Link Numero 2</a>
    </li>
  </ul>
  ```
Will man ein Logo benutzen fügt man folgenden Code ein:

``` html
  <a class="navbar-brand" href="#">
    <img src="logobild.jpg" alt="logo" style="width:20px;">
  </a>
```
Sollte ab einer bestimmten Bildschirmgröße die Navbar mit einem Togglebutton versehen werden muss dieser Code für einen Button hinzugefügt werden. Der restliche Inhalt sollte in einem div umhüllt werden auf das auch data-target verweist:
``` html
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#Navleiste">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="Navleiste">...</div>
```