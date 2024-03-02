1- Sentencias:

Órdenes rden que se le dan al programa para realizar una tarea específica: mostrar un mensaje en la pantalla, declarar una variable (para reservar espacio en memoria), inicializarla, llamar a una función, etc. 
Acaban con el carácter __;__. Separa una sentencia de la siguiente. Normalmente, las sentencias se ponen unas debajo de otras (una en cada línea), aunque sentencias cortas pueden colocarse en una misma línea. Ejemplos:

```java
int i=1;

import java.awt.*;

System.out.println("Mi primer programa");

rect.mover(10, 20);
```

> __Nota__: En el lenguaje Java, los caracteres __espacio en blanco__ se pueden emplear libremente. Como podremos ver en los siguientes ejemplos, es muy importante para la legibilidad de un programa la colocación de unas líneas debajo de otras empleando tabuladores. El editor del IDE nos ayudará a realizar esta tarea de manera automática sin apenas percibirlo.

2- Bloques de código:

Agrupación de sentencias agrupadas entre llaves { }. 
En el ejemplo anterior __Saludo.java__, el conjunto de sentencias se reduce a tres sentencias, que llaman a los métodos predefinidos en Java __print__ y __println__ que permiten visualizar texto por el dispositivo de salida de datos (por defecto la pantalla).

3- Expresiones

Todo aquello que se puede poner a la derecha del operador de asignación __=__. Por ejemplo:

```java
x = 123;

y = (x+100)/4;

area = circulo.calcularArea(2.5);

Rectangulo r = new Rectangulo(10, 10, 200, 300);
```

* La primera expresión asigna un valor a la variable x.
* La segunda, realiza una operación aritmética y el resultado se asigna a la variable _y_.
* La tercera, es una llamada a una función miembro _calcularArea_ desde un objeto circulo de una clase determinada y el resultado se asigna a la variable _area_.
* La cuarta, reserva espacio en memoria para un objeto de la clase Rectangulo mediante la llamada a una función especial que tienen todas las clases denominada _constructor_.

4- Comentarios:

Texto adicional que se añade al código para explicar su funcionalidad, bien a otras personas que lean el programa, o al propio autor como recordatorio. Los comentarios son una parte importante de la documentación de un programa. Los comentarios son ignorados por el compilador, por lo que no incrementan el tamaño del archivo ejecutable; se pueden por tanto, añadir libremente al código para que pueda entenderse mejor.

a) Comentarios de una sola línea:
 Se utiliza la secuencia de caracteres __//__. El compilador ignora
todo lo que se incluya entre la secuencia de caracteres // y el final de la línea. Por ejemplo:

```java
// Este es un comentario estilo C++, llega al final de la linea
sentencia_1;
```

>  __//__ hay que escribirla sin dejar ningún espacio en blanco entre ellos.

b) Comentarios de múltiples líneas__. __/*__ para abrir el comentario 
 __*/__ para cerrar el comentario. 
Por ejemplo:

```java
/* En este otro comentario estilo C, el final
 lo indica la marca */
 sentencia_1;
```

> Los comentarios pueden incluir cualquier carácter válido en Unicode y no pueden anidarse.

Estos dos formatos de comentario se emplean para los denominados _comentarios de implementación_.
  Se utilizan en el programa fuente para resaltar código o para aclarar un desarrollo en particular.

c) Comentarios de documentación__ (_doc comments_) facilitan la generación de documentación en formato HTML al emplear algunas herramientas de documentación 
__javadoc__ incluida en el __Kit de Desarrollo de Java__). Los comentarios para la documentación se emplean para describir la especificación del código, desde una perspectiva independiente cómo se ha implementado y ser leido por desarrolladores que no tengan necesariamente el código fuente a la vista. Ejemplos de este tipo de comentarios:

```java
/** Comentario estilo javadoc, se incluye
automaticamente en documentacion HTML */
```

```java
/**
 * Muchos programadores
 * suelen incluir un asterisco
 * al principio de cada linea del
 * comentario para facilitar su lectura
 */
```

> Los comentarios deberían contener sólo información relevante para la lectura y comprensión del programa. Todos los programas deben empezar por un comentario que describa el propósito general del programa.

Articulo de Oracle (en inglés) sobre [cómo escribir Doc Comments para la herramienta Javadoc](http://www.oracle.com/technetwork/articles/java/index-137868.html).

5- Convención para los comentarios al inicio de los programas

Todos los archivos fuente deberían comenzar con un comentario liste el nombre de la clase, información de la versión, fecha y el aviso de copyright:

```java
/**
* The HelloWorld program implements an application that
* simply displays "Hello World!" to the standard output.
*
* @author  Jonay García
* @version 1.0
* @since   22-01-2017
*/
public class HelloWorld {

   public static void main(String[] args) {
      // Immprime el texto Hello, World! en la salida estándar.
      System.out.println("Hello World!");
   }

}
```
6- Identificadores

 Nombres que se les asignan a _variables_, _métodos_, _clases_, ..., en el código fuente de un programa. Los identificadores sólo existen en el código del programa fuente y no en el programa objeto (resultado de la compilación del programa fuente). Todo nuevo identificador que se emplee en un programa Java debe definirse previamente a su utilización. Las normas para la construcción de un identificador empleando el lenguaje de programación Java son las siguientes:

* Un identificador comienza por una letra, un carácter de subrayado ( _ ) o un carácter de dólar ($). Aunque no se recomienda emplear el carácter $, ya que el compilador suele utilizarlos de forma interna para crear identificadores propios.
* Los siguientes caracteres pueden ser también dígitos. Pero no pueden emplearse espacios en
blanco u otros caracteres como el signo de interrogación (?) o el signo del tanto por ciento
(%).
* No hay límite máximo de caracteres.
* En los identificadores del código fuente de un programa en Java se distinguen las mayúsculas de las minúsculas. Por ejemplo, las palabras _casa_, _CASA_ y _Casa_ son tres identificadores diferentes.
* Pueden incluir caracteres Unicode, con lo que se pueden emplear secuencias de escape
/uxxxx para representar estos caracteres.
* No puede emplearse el identificador de una variable o cualquier otro elemento del código
fuente del programa para otro ya existente en el mismo bloque. Excepción: variable miembro
y local con el mismo identificador.
* Existe una serie de palabras reservadas que no pueden emplearse como identificadores por
el programador en el código fuente para otros usos. Por ejemplo, la palabra double se
utiliza para definir un tipo de dato real y la palabra for se emplea para construir un tipo
determinado de bucle.

En la siguiente tabla se muestran las _palabras reservadas_ en Java.

| A-D      | D-I     | I-P         | P-T          | T-Z       |
|----------|---------|-------------|--------------|-----------|
| abstract | do      | implements  | protected    | throw     |
| boolean  | double  | import      | public       | throws    |
| break    | else    | instanceof  | rest         | transient |
| byte     | extends | int         | return       | true      |    
| case     | false   | interface   | short        | try       |
| catch    | final   | long        | static       | void      |
| char     | finally | native      | strictfp     | volatile  |
| class    | float   | new         | super        | while     |
| const*   | for     | null        | switch       | &nbsp;    |
| continue | goto*   | package     | synchronized | &nbsp;    |
| default  | if      | private     | this         | &nbsp;    |

Algunos de estos _identificadores reservados_ no tienen todavía uso en la implementación actual del lenguaje Java. En concreto, los identificadores marcados con un asterisco * no se utilizan actualmente.

Las palabras reservadas se pueden clasificar en las siguientes categorías:

* __Tipos de datos__: boolean, float, double, int, char.
* __Sentencias condicionales__: if, else, switch.
* __Sentencias iterativas__: for, do, while, continue.
* __Tratamiento de las excepciones__: try, catch, finally, throw.
* __Estructura de datos__: class, interface, implements, extends.
* __Modificadores y control de acceso__: public, private, protected, transient.
* __Otras__: super, null, this.

A continuación se muestran los nombre de métodos reservados en Java cuyo significado y utilización se explicará más adelante cuando se menciones la _clase predefinida Object_:

| A-E    | F-G      | H-N      | N-T       | W-Z    |
|--------|----------|----------|-----------|--------|
| clone  | finalize | hashCode | notifyAll | wait   |
| equals | getClass | notify   | toString  | &nbsp; |

7- Recomencaciones a la hora de escribir identificadores



Todos los identificadores han de comenzar con una letra, el carácter subrayado ( _ ) o el carácter dollar ( $ ).
Puede incluir, pero no comenzar por un número
No puede incluir el carácter espacio en blanco
Distingue entre letras mayúsculas y minúsculas
No se pueden utilizar las plabras reservadas como identificadores

Además de estas restricciones, hay ciertas convenciones que hacen que el programa sea más legible, pero que no afectan a la ejecución del programa. La primera y fundamental es la de encontrar un nombre que sea significativo, de modo que el programa sea lo más legible posible. El tiempo que se pretende ahorrar eligiendo nombres cortos y poco significativos se pierde con creces cuando se revisa el programa después de cierto tiempo.


| Tipo de identificador	| Convención | 	Ejemplo |
|---------------------| ----------| ---------|
| Nombre de una clase | Comienza por letra mayúscula | String, Rectangulo, CinematicaApplet |
| Nombre de función	  | Comienza con letra minúscula | calcularArea, getValue, setColor     |
| Nombre de variable  |	comienza por letra minúscula | area, color, carSize                 |
| Nombre de constante | En letras mayúsculas         | PI, MAX_ANCHO                        |

__CamelCase__ es un estilo de escritura que se aplica a frases o palabras compuestas. El nombre se debe a que las mayúsculas a lo largo de una palabra en CamelCase se asemejan a las jorobas de un camello. El nombre _CamelCase_ se podría traducir como Mayúsculas/Minúsculas Camello.

Existen dos tipos de _CamelCase_:

* __UpperCamelCase__, cuando la primera letra de cada una de las palabras es mayúscula. Ejemplo: EjemploDeUpperCamelCase.
* __lowerCamelCase__, igual que la anterior con la excepción de que la primera letra es minúscula. Ejemplo: ejemploDeLowerCamelCase.

8- Convenciones para la Legibilidad del Programa Fuente

Aunque la definición exacta de la indentación (espacios vs tabuladores) no se especifica en el lenguaje Java, se recomienda emplear una secuencia de __cuatro espacios como unidad de indentación__.

Por otro lado se recomienda __evitar las lineas de más de 80 caracteres en el código fuente__ ya que no se manejan correctamente por muchos terminales y herramientas de edición.