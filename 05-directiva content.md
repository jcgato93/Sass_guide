# Uso de la directiva `content`

Una de las características que tienen los mixins es la directiva content. Esta nos permite incluir un bloque de contenido dentro de un mixin.

Ejemplo 

si quisiera que una clase tome valores diferentes segun cierta resolucion 

```scss
@mixin respond-to($width){
    @media only screen and (min-width: $width){
        // sera el contenido cuando se utilice este mixin
        @content
    }
}
```

Uso
```scss
section{
    @include max-width;

    // cuando tenga una resolucion de 800px cambiara el background-color
    @include respond-to(800px){
        // esta seccion es la que hace referencia al @content
        background-color: red
    };

    background-color: $color-lightgrey
    padding: $padding
}
```
