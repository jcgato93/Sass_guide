# Funciones


- Crear funcion
```scss
@function suma($num1, $num2){
    @return  $num1 + $num2;
}
```

- User funcion
```scss
.div {
    padding: suma(10px, 5px);
}
```


Ejemplo: Usos más avanzados

```scss

// Utilizando un mapa (List<T> de sass)
$fs : (
    big: 24px,
    normal: 16px,
    small: 14px,
    x-small: 12px
);

p {
    // map-get funcion predefinida
    font-size: map-get($fs,normal)
}

small {
    color: grey;
    font-size: map-get($fs, x-mall);
}
```

