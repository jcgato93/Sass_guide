# Anidaciones

Al igual que en CSS , SASS permite la anidacion de selectores


Ejemplo 

```scss
.btn
    display: inline-block
    color: $buttoncolor
    background-color: $buttonbackgroundcolor
    line-height: 2.5
    border-radius: $border-radius
    font-size: $buttonfontsize

    .btn__icon
        font-size: .6em
    
    // El uso de '&' toma el nombre del padre y lo crea como una clase independiente
    &--info
        background-color: $color-info
````