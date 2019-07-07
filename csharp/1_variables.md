# Variables

Las variables son una parte muy importante de la programación. Nos permiten guardar datos, así como mantener estado de nuestro juego.

Unity3D usa primordialmente usa C#, este es originalmente diseñado por Microsoft. Pero con un poco de magia y programación ingeniosa podemos hacer uso de su facilidad de programación y velocidad para la creación de juegos.

Las variables en C# son *fuertemente tipadas*. ¿Qué significa esto? Que nosotros definimos explicitamente que "cabe" en cada variable. Podemos decirle a nuestro programa que solo cabe un número entero, si posteriormente queremos guardar una cadena de texto, nos mostrará un error porque solo podemos guardar números con esa variable. Y *estáticamente tipadas* porque los tipos que usamos los definimos nosotros.

Las variables en C# se dividen en 2 tipos, las primitivas y las complejas.

Las primitivas son aquellas que estan construidas en el lenguaje y con ellas crear cosas más complejas.

Tipo | Valores Aceptados | Literales | Notas
-----|-------------------|-----------|------
**bool** | true / false | true/false | Valor predefinido es *false*.
**sbyte** | -128 - 127 | -23 | 8 bits. Valor predefinido es 0.
**short** | -32,768 - 32,767 | -123 | 16 bits. Valor predefinido es 0.
**int** | -2,147,483,648 - 2,147,483,647 | 567956 | 32 bits. Valor predefinido es 0.
**long** | -9,223,372,036,854,775,808 - 9,223,372,036,854,775,807 | 569856321L | 64 bits. Valor predefinido 0L.
**byte** | 0 - 255 | 23 | 8 bits. Valor predefinido es 0.
**ushort** | 0 - 65535 | 14 | 16 bits. Valor predefinido 0.
**uint** | 0 - 4294967295 | 512956u | 32 bits. Valor predefinido es 0u.
**ulong** | 0 - 18,446,744,073,709,551,615 | 0u | 64 bits. Valor predefinido 0u.
**float** | -3.402823e38 - 3.402823e38 | 0.0f | 32 bits. Valor predefinido es 0.0f.
**double** | -1.79769313486232e308 - 1.79769313486232e308 | 0.0d | 64 bits. Valor predefinido es 0.0d.
**char** | Carácter unicode | 'u', '\0' | 16 bits.
**decimal** | ±1.0x10e−28 - ±7.9x10e28 | 3.1614m | N/A
**object** | N/A | N/A | Valor predefinido *null*.
**string** | N/A | "Hola Mundo" | Valor predefinido *null*.

Para declarar una variable lo hacemos de la siguiente forma.

```C#
// tipo_de_variable nombre = valor_inicial;
// Ejemplos:
int x = 10;
string saludo = "Hola Mundo";
```

Adicionalmente podemos usar la palabra **var** para que el compilador defina el tipo de variable que tiene más sentido usar. Puede ser muy util para variables temporales.

```C#
// Cadena
var saludo = "Hola Mundo";
// Número entero
var salud = 42;
```

Información obtenida de:   
<http://www.introprogramming.info/english-intro-csharp-book/read-online/chapter-2-primitive-types-and-variables/>
<http://www.jeremyshanks.com/c-variables-primitive-nonprimitive-types/>