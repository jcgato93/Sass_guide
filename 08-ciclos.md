# Ciclos

Existen controladores de flujo dentro de Sass como : each , for , while 


## Each

Ejemplo simple 

```scss
@each $font in (normal, bold, italic){
    #{$font} {font-weight: $font;}
}
```


Ejemplo complejo

```scss
$black: black
$white: white

$green: green

$general: ('black', $black), ('white', $white), ('green', $green);

@each $color in $general
    // seleccionar cada valor
    $name: nth($color, 1)
    $value: nth($color, 2)

    .hw-bg-#{$name}
        background-color: $value
    .hw-color-#{$name}
        color: $value
        td
            color: $value
    .hw-color-#{$name}-hover
        &:hover,
        &.hw-active
            color: $value
    .hw-color-#{$name}-active
        color: $value
        font-weight: bold
    .hw-border-#{$name}
        border-color: $value
```


## For 

```scss
/* Z INDEX */
$hw-index: 20;
@for $i from 1 through $hw-index{
    .hw-index-#{$i}
        z-index: $i
}
```

# While

```scss
/* OPACITY */
$i : 0;
@while $i <= 1
    .custom-opacity-#{round($i*10)}
        opacity: $i !important
    $i : $i + 0.1
```