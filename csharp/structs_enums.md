---
layout: post
title:  "Estructuras y otras magías negras para trabajar con datos de manera ordenada"
--- 

# Estructuras
Los `struct` o estructuras son un tipo que conmunmente se usan para encapusular un grupo de variables relacionadas. Como por ejemplo, los `Vector2` o los `Vector3` de unity, o cosas como las coordenadas y dimensiones de un rectangulo.
Para declararlos usamos la siguiente sintaxis:

```C#
public struct Rectangulo {
    public float x;
    public float y;
    public float ancho;
    public float largo;
}
```

Y para usarlos:
```C#
Rectangulo r1;
// o
Rectangulo r2 = new Rectangulo();
```

# Enumeraciones
Las enumeraciones \(o `enums`\) son un tipo que podemos usar en casos que las opciones son un pequeño grupo de constantes.
De manera predefinida, los enumeradores inician en 0 y su valor sucesivo aumento por 1. Aunque podemos cambiar sus valor usando un signo de igual.
La sintaxis es la siguiente:

```C#
//Aqui Lunes = 0 y Martes = 1
enum Dias { Lunes, Martes, Miercoles, Jueves, Viernes, Sabado, Domingo }

// Iniciar la semana desde 1
enum Dias { Lunes=1, Martes, Miercoles, Jueves, Viernes, Sabado, Domingo }
```

Información obtenida de:   
<https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/struct>   
<https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/using-structs>   
<https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/enum>   