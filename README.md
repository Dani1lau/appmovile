### Documentación 

En este documento se presentara la investigacion que fue pedida, lo que se pidio fue:
- Variables.
- Constantes.
- Opcionales.
- Manejos de nulos.

#### Variables 
Una variable en programación es un espacio de memoria con un nombre simbólico (identificador) que se utiliza para
almacenar datos. Estos datos pueden ser números, texto, valores booleanos, o cualquier otro tipo 
de información que el programa necesite procesar.

 -  *var*: Palabra clave para declarar variables mutables, cuyo valor puede cambiarse después de la inicialización.
 - *val*: Palabra clave para declarar variables inmutables, cuyo valor no puede cambiarse después de la inicialización.

#### Tipos de Datos Básicos en Kotlin:
- *Int*: Representa números enteros, como 1, -5, 1000, etc.
- *Long*: Representa números enteros más grandes que Int, como 10000000000L.
- *Short*: Representa números enteros pequeños, como 10, -500, etc.
- *Byte*: Representa números enteros muy pequeños, como -128 a 127.
- *Double*: Representa números de punto flotante de doble precisión.
- *Float*: Representa números de punto flotante de precisión simple, como 3.14, -0.001, etc.
-  *Boolean*: Representa valores booleanos true o false.
- *Char*: Representa un solo carácter Unicode, como 'a', '!', etc.
- *String*: Representa una secuencia de caracteres, como "Hola", "123", etc.
- *Nullability: Cualquier tipo de dato puede ser nullable añadiendo ? al final del tipo (Int?, **String?, **etc*.), lo que significa que puede contener un valor nulo.

#### Constantes val
Las constantes val son variables inmutables en Kotlin, lo que significa que una vez que se les asigna un valor, no se puede cambiar. Estas son similares a las variables declaradas con final en Java o const en otros lenguajes de programación. Algunas características clave incluyen:

- *Inmutabilidad*: Una vez inicializada, no se puede cambiar su valor.
- *Declaración*: Se definen utilizando la palabra clave val, seguida de un nombre y un tipo opcional si Kotlin no puede inferirlo automáticamente.
- *Uso*: Ideal para valores que no necesitan cambiar durante la vida útil de un objeto o programa, como constantes matemáticas, configuraciones estáticas, o valores que se inicializan una vez y no se modifican.

#### Funciones

En Kotlin, las funciones se definen utilizando la palabra clave fun. Pueden aceptar parámetros y devolver valores, o simplemente realizar tareas específicas sin devolver ningún valor.

#### Interpolación de Cadenas ($)

Kotlin permite insertar valores de variables o expresiones dentro de cadenas literales utilizando la sintaxis** ${}**. Esto facilita la creación de cadenas dinámicas que incluyen valores de variables.

## Análisis del Código

##### Parte #1

class Constantes {
    companion object {
        const val PI = 3.14159  
    }
}


#### Clase Constantes
 - *Constantes*: Define una clase que agrupa constantes relacionadas.
 - *companion object*: Objeto compañero que permite definir miembros estáticos en Kotlin. Dentro de él, se define la constante PI con valor 3.14159, de tipo Double.

##### Parte #2

var edad: Int? = 25 

fun saludar(nombre: String, saludo: String = "HOLII") {
    println("$saludo $nombre")
}


#### Variables y Funciones:
teniendo en cuenta la explicacion tenemos aqui un ejemplo donde:

 - * edad: Variable que puede contener un entero* (Int)* o ser null *(Int?)**. Se utiliza para representar la edad de una persona, con la posibilidad de que no se conozca (null).
 - *saludar: Función que imprime un saludo (saludo) seguido del nombre proporcionado (nombre). El saludo tiene un valor predeterminado de *"HOLII"** si no se proporciona explícitamente.

##### Parte #3


fun main() {
   
    val count: Int = 10  

    println("El valor guardado en la variable count = $count.")

    
    var nombre: String = "Sofia"  
    nombre = "Petunia"  
    println("El nombre guardado es = $nombre")

    // Acceso a la constante PI definida en la clase Constantes
    println("El valor de PI es: ${Constantes.PI}")


    if (edad != null) {
        println("La edad es $edad")
    } else {
        println("La edad es null")
    }

    saludar("Tulio", "Quemass¡¡¡")
    saludar("Julia", "Quiubo")
}


#### Función main

- *main()*: Punto de entrada principal del programa.
  - *count*: Variable local de tipo Int inicializada con el valor 10. Representa la cantidad específica utilizada en el contexto del programa.
  - *nombre: Variable mutable de tipo String inicializada como *"Sofia"* y luego modificada a *"Petunia"**. Representa el nombre de una persona que puede cambiar.

- *Impresiones*:
  - Imprime el valor de count.
  - Imprime el valor de nombre.
  - Accede e imprime la constante PI utilizando la sintaxis *${Constantes.PI}*.
  - Verifica si edad no es null y lo imprime si tiene un valor. Si es null, imprime que la edad es null.

- Llamadas a saludar:
  - Llama a la función saludar dos veces con diferentes combinaciones de nombres y saludos.
