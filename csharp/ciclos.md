---
layout: post
title:  "Ciclos"
---

# For

Común del mundo de C. Usado cuando sabemos en que punto se detendra la ejecución.

```C#
for(int i = 0; i < elementos.Count; i++){
    print(elementos[i]);
}
```

```C#
int i = 0;
```

Puedes omitirla, puedes usarlo como un contador para tu ciclo, esta variable solo sera accesible dentro del ciclo.

```C#
i < elementos.Count;
```

Esta expresión tiene que evaluarse a `true` para continuar con el ciclo.

```C#
i++
```

Esta expresión nos permite para calcular el siguiente elemento.

## i++

`i++` es una forma corta de decir aumenta por uno a `i`. Es equivalente a `i = i + 1`. Adicionalmente podemos usar `i--`, que hace exactamente lo mismo pero restando.

# While

Nos permite correr algo hasta que dejemos de cumplir una condición.

```C#
while(saltando){
    velocidad.y -= 0.1f;
}
```

## Tip para expertos

`saltando` es una forma corta de decir que si una variable booleana equivale a *true*. Expresiones como *if* o *while* prueban aquello dentro de los paréntesis a que nos de un valor booleano. Cuando este esta solo, esta expresión toma el valor único de esta variable.

# Do While

Nos permite correr algo, donde lo primordial es correr el ciclo al menos una vez. La expresión tiene que evaluarse a *falso* para romper el ciclo.

```C#
do {
    //cosas
} while(a > b);
```

# Foreach

Es una forma muy facil realizar operaciones ciclicas donde sabemos que recorreremos cada elemento de una coleccion.

```C#
foreach(var num in arregloNumero){
    //Hacer algo con num
    //Según se recorrra el ciclo num cambia a ese elemento de arregloNumero
}
```
