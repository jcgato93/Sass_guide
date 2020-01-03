# Extend

Extend es la funcionalidad que permite heredar las propiedades de otro elemento 

Ejemplo: 

Tener las mismas propiedades de las clase .btn y agregar unos propios

```scss
.btn{
    display: inline-block
    color: $buttoncolor
    background-color: $buttonbackgroundcolor
    line-height: 2.5
    border-radius: $border-radius
    font-size: $buttonfontsize
}


/*
de este modo la clase .btn--info tiene las mismas propiedades de .btn , con una variacion
este ayuda a que solo se tenga que llamar a .btn--info y no ambas clases

*/
.btn--info{
        @extend .btn
        background-color: $color-info
}
```