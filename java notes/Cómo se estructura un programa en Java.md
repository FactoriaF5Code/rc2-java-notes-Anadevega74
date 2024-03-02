1- Clase principal y método main

Un programa se construye usando varias clases. La forma más sencilla usa una única clase, que contiene el programa, rutina o método principal: __main()__ y en éste se incluyen las sentencias del programa principal. Estas sentencias se separan entre sí por caracteres de punto y coma.

Estructura de un programa simple en Java:

```java
public class ClasePrincipal {
    public static void main(String[] args) {
        sentencia_1;
        sentencia_2;
        // comentario_1
        ...
        sentencia_N;
    }
}
```

El siguiente ejemplo muestra un mensaje por la pantalla del ordenador llamado __HolaMundo.java__:

```java
/**
 * La clase HolaMundo construye un programa que
 * muestra un mensaje en pantalla
 */
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

  __HolaMundo__ es el nombre de la _clase principal_ y del archivo que contiene el código fuente. Todos los programas o aplicaciones independientes escritas en Java tienen un método main o principal que contiene un conjunto de sentencias.

2- Significado de los términos de la clase principal

    a) Primera parte: definir la clase:

* __public__: modificador de acceso que determina quién puede acceder a las clases o propiedades y métodos de una clase.
* __class__: define una clase. Contiene un conjunto de propiedades y métodos que luego sirven de modelo o plantilla para crear objetos o instancias de esa clase.
* __Greeting__: identifica a la clase pública que se ha creado.

Esta línea define una clase pública identificada como _HolaMundo_.

```java
public class HolaMundo {

}
```

b) Segunda parte: definición del método main 

* __public__: el método puede ser accedido desde cualquier otro método que tenga una instancia de esta clase.

* __static__: un método puede ser de instancia o de clase. Un método no estático es un método de instancia (que necesita una instancia de la clase donde se declara para ser invocado) y un método estático es un método de clase (no necesita una instancia de la clase donde se declara para ser invocado).
* __void__: Los métodos pueden devolver algo, por ejemplo, un método que suma dos números, devuelve el resultado de la suma; pero hay métodos que no devuelven nada y que sólo ejecutan acciones. Dichos métodos se declaran con la palabra reservada _void_ (vacío) como tipo de retorno.
* __main()__: Es el nombre del método que la máquina virtual de Java busca para comenzar a ejecutar un programa. Siempre ha de llamarse _main_.
* __String__: Es una clase que define cadenas de caracteres. Gracias a la clase String, Java puede manipular textos.
* __StringString[]__: Cualquier clase que se declara con corchetes “[]”, quiere decir que lo que tienes no es una instancia de esa clase, sino un array de objetos de dicha clase. Por ejemplo, _String[] meses_ contendría los nombres de los meses del año. El método _main()_ de Java necesita un String[] porque el usuario de nuestro programa puede pasar _parámetros extra_ desde la línea de comando a nuestro programa. Esos parámetros, el programador los recibe a través de ese array.

```java
public static void main(String[] args) {

}
```

c) Tercera parte: las sentencias:

* __System.out.println()__: es una método contenido en la _API de Java SE_ que imprime por pantalla el texto que se le pasa entre paréntesis, en este caso imprimirá el mensaje _Hello World!_:

```java
System.out.println("Hello World!");
```

Documentación Oracle sobre [cómo crear la aplicación "Hello World!" en Java](https://docs.oracle.com/javase/tutorial/getStarted/application/)
