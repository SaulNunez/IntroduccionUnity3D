---
layout: post
title:  "Clases"
---

C# es un lenguage que soporta diferentes paradigmas de programación.
Uno de ellos es la *programación orientada a objetos*.

¿Que es la programación orientada a objetos te preguntaras? Esta emula igual que la vida real el hecho hay objetos que cumplen distintos propositos. Para funcionar un carro no necesita saber como funciona la bomba en la gasolinera, siempre que haya una interfaz en la que ambos se puedan conectar (el hollito para la gasolina), podemos desconocer como funciona todo a nuestro alrededor. Con estas interfaces, no tenemos que cambiar algo del carro si queremos usar un sifón si nos alejamos mucho, igual un programa si cambian algunos requisitos puede conectarse con otras cosas que tengan una interfaz similar.

Y aunque exista una misma variedad, estos pueden variar según sus propiedades. Como hay montruos azules y otros rojos, de baja vida, otros son minijefes, unos lanzan flamas.

En C# sera increiblemente comun encontrarnos con clases, en Unity son el pan de cada día en la forma de un **Monobehavior**. Hablaremos de estos más adelante.

Para hacer una clase en C# la sintaxis es.

```C#
public class Monstruo {

}
```

Y ahora para tener nuestro propio monstro... \(una instancia de un monstruo\)

```C#
    Monstruo monstruo = new Monstruo();
```

Pero esta algo vacia, hagamos que nuestro monstruo tenga una vida de tres. (Regresaremos a que significa `private` en un tema o dos)

```C#
public class Monstruo {
    private int vida = 3;
}
```

Ahora que lancé llamas.
```C#
public class Monstruo {
    private int vida = 3;

    public void LanzarLlamas(){
        particulas.crear("Llamas", Direccion.Enfrente);
    }
}
```
Regresamos a nuestras viejas funciones. Estas añaden funcionalidad a nuestras clases, definiendo comportamientos para nuestros objetos, justo como en la vida real. Notese que el nombre correcto para son metodos, de aquí en adelante así nos referiremos a ellas.

Podemos cambiar cosas fundamentales de nuestros objetos cuando los creamos de una manera elegante con un constructor. Hagamos que podamos crear monstruos con diferentes valores de `vida`.

```C#
public class Monstruo {
    private int vida;

    public Monstruo (int vida){
        this.vida = vida;
    }

    public void LanzarLlamas(){
        particulas.crear("Llamas", Direccion.Enfrente);
    }
}

Monstruo jefe = new Monstruo(5);
Monstruo normal = new Monstruo(3);
```

`this` sirve como una forma de referirnos cosas dentro de esa clase. Lo usamos porque `vida` en el constructor \"opaca\" al miembro de `Monstruo`. `this` nos permite volver a usarlo. 