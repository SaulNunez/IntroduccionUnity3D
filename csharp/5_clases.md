# Clases

C# es un lenguage que soporta diferentes paradigmas de programación.
Uno de ellos es la *programación orientada a objetos*.

?Que es la programación orientada a objetos te preguntaras? Esta emula igual que la vida real el hecho hay objetos que cumplen distintos propositos. Para funcionar un carro no necesita saber como funciona la bomba en la gasolinera, siempre que haya una interfaz en la que ambos se puedan conectar (el hollito para la gasolina), podemos desconocer como funciona todo a nuestro alrededor. De esta forma, también podemos usar un sifón si nos alejamos mucho, igual un programa si cambian algunas cosas puede conectarse con cosas que tengan una interfaz similar.

Y aunque exista una misma variedad, estos pueden variar según sus propiedades. Como hay montruos azules y otros rojos, de baja vida, otros son minijefes, unos lanzan flamas.

En C# sera increiblemente comun encontrarnos con clases, en Unity son el pan de cada día en la forma de un **Monobehavior**. Hablaremos de estos más adelante.

Para hacer una clase en C# usamos

```C#
public class Monstruo {

}
```

Pero esta algo vacia, hagamos que nuestro monstruo tenga una vida de tres.
```C#
public class Monstruo {
    public int vida = 3;
}
```

Ahora que lancé llamas.
```C#
public class Monstruo {
    public int vida = 3;

    public void LanzarLlamas(){
        particulas.crear("Llamas", Direccion.Enfrente);
    }
}
```
Regresamos a nuestras viejas funciones. Estas añaden funcionalidad a nuestras clases