# Mixins

Los mixins son basicamente clases que se pueden utilizar dentro del mismo html

Ejemplo 


```scss
// Declarar mixin

@mixin max-width
    max-width: 800px


// llamar mixin
section
    @include max-width


```

## Mixins con parametros

Los mixins tambien pueden recibir parametros para que sean mucho mas dinamicos


```scss
// Declarar mixin

@mixin max-width($maxwidth: 800px)
    max-width: $maxwidth


// llamar mixin
section
    @include max-width(1200px)


```