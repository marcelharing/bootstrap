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

Buttons:
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