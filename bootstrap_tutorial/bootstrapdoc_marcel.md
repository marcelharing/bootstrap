# Bootstrap - eine kleine Zusammenfassung

## Container
Container sind ein Grundgerüst in Bootstrap. Es gibt zwei wesentliche Container:
+ Fixed Container: nutzt eine festgelegte width, je nach Bildschirmgröße `<div class="container">`
+ Fluid Container: nutzt die volle width `<div class="container-fluid">`

Mit `.container-sm|md|lg|xl` lassen sich responsive Container erzeugen, je nachdem ob sie schon bei kleinen Bildschirmen (sm) oder bei großen (xl) die Weite auf 100% stellen sollen.

## Grid 
Die responsive Griddarstellung erlaubt bis zu 12 Spalten.
Entweder selber die Spaltenanordnung festlegen, dabei sollte der erste Stern die responsivness (sm|md|lg|xl) darstellen, der zweite die Spaltenposition/Spaltenausdehnung (1-12; in Summe sollte dann jede Reihe 12 ergeben):

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


Oder Bootstrap die Spaltenposition selber einteilen lassen, bei 3 Spalten nimmt jede zB 33% ein:

    <div class="container">
        <div class="row">
            <div class="col"></div>
            <div class="col"></div>
            <div class="col"></div>
        </div>
    </div>

# Typologie
<abbr title="World Health Organization">WHO</abbr>