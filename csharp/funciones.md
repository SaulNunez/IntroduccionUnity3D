# Funciones

Las funciones son extremadamente utiles en el diseño de lógica en videojuegos dado que nos permite reutilizar código ahorrando tiempo, evitando errores y facilitar añadir nueva funcionalidad.

```C#
float SumarDosNumeros(float a, float b){
    return a + b;
}
```

Las funciones pueden aceptar uno o más parametros. En este caso **a** y **b**. Y pueden retornar un valor, definimos el tipo del valor que va a retornar antes del nombre de la función y usamos el keyword **return** para retornar el valor y regresar a la ejecución normal del programa.

```C#
void Imprimir(){
    Debug.Log("Hola Mundo");
}
```

Se pueden crear funciones donde no retornemos nada, en este caso usamos void antes del nombre de la función para declarar que no retorna nada esta función.

```C#
void Imprimir(){
    Debug.Log("Hola Mundo");
    return;
    //¿Imprimiremos Otra cosa?
    Debug.Log("Otra cosa");
}
```

**Nota:** Podemos hacer el uso del return en aquellas funciones que no retornen nada para simplemente cortar la ejecución y retornar al código que llamo la función.

### Tip para expertos

C# normalmente lo que hace es que pasa los parametros de las funciones **por copia**. A lo que se refiere esto es que C# hace una copia de lo que le pasamos, si  modificamos este  adentro de la función, no pasara absolutamente nada al valor original.

```C#
float numeroAPotenciar = 2;
float resultado = Potenciacion(numeroAPotenciar, 2);

float Potenciacion(float a, float exponente){
    for(int i  = 1; i < exponente; i++){
        a *= a;
    }

    //La pregunta, es que valor tiene numeroAPotenciar en este momento.
    //Si leiste lo anterior, probablemente entendiste que no le paso a nada numeroAPotenciar, estarias en lo correcto.
    return a;
}
```

Cuando empieces en el mundo real a trabajar con código real, puede que te toque trabajar con datos muy grandes, las cuales no es la mejor idea trabajarlos por copia \(¡Imaginate cuanto desperdicio de memoria!\), C# tiene una forma de pasarlos por referencia, lo que significa que estas usando la misma variable que estas pasando el los parametros. Para hacer esto usamos el keyword **ref**.

```C#
float numeroAPotenciar = 2;
float resultado = Potenciacion(numeroAPotenciar, 2);

float Potenciacion(ref float a, float exponente){
    for(int i  = 1; i < exponente; i++){
        a *= a;
    }

    //La pregunta, es que valor tiene numeroAPotenciar en este momento.
    //estamos sobreescribiendo a, y dado que a es el mismo espacio de memoria que la variable numeroAPotenciar, su valor seria igual a 4.
    return a;
}
```