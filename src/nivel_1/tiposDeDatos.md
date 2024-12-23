# Tipos de Datos

Primero que nada debemos de entender el concepto de variable. Entonces _¿qué es una variable?_ Bueno, podemos pensar en una variable como una caja donde guardamos algo. Aunque esta analogía es fácil de entender, en realidad estamos almacenando ese valor en algún lugar de la **memoria principal**, o **RAM** (Random Access Memory).  

Ahora bien, **declarar una variable** significa establecer un nombre y un tipo de dato para esa variable. Es importante recordar que C++ es un **lenguaje fuertemente tipado**, lo que significa que cada variable debe ser declarada con su tipo de dato desde el inicio, y este no puede cambiar posteriormente. El valor de la variable si puede cambiar, a menos que se defina como una **constante**, en este caso, el valor _**nunca cambiará**_. Además, el valor de la variable puede ser asignado en el momento de su declaración. Esto es importante en algunos contextos, ya que la dirección de memoria asociada a una variable puede contener **basura**, es decir, información residual que no nos importa y que podría afectar el comportamiento del programa si no se inicializa correctamente.

La manera de declarar una variable o una constante en C++ es muy sencilla. Se comienza con el **tipo de dato** de la variable que deseamos declarar, seguido del **nombre** de la variable. Si es necesario inicializarla con un valor, usamos el operador ``=``, cada declaración debe terminar con un punto y coma (``;``), que indica el fin de la instrucción en C++.

En caso de querer declarar varias variables del mismo tipo, es posible hacerlo en una sola línea, separándolas por una coma ``,``.

### Programa de ejemplo

````C++
#include <iostream>
#define PI 3.1416 //Definiendo una constante PI
using namespace std;

int main(){
    const float G = 9.81; // otra forma de definir constantes
    int edad = 18, horas = 157680; //declaracion de 2 variables de un mismo tipo en una linea
    cout<<"Edad: "<<edad<<"\t Horas vividas: "<<horas<<"\n";
    cout<<"Constantes \n"<<"G: "<<G<<"\nPI: "<<PI;
    return 0;
}
````

Es importante que, antes de programar para resolver algún problema, reflexionemos sobre qué tipo de dato será más útil para asignar a una variable.   

Por ejemplo:  
- Si queremos almacenar una entrada _numérica entera_  para hacer un contador, podemos declarar esa variable como un ``int``.
- Si queremos almacenar una entrada _numérica decimal_ para calcular un salario, podemos declarar esa variable como un ``float``.

A continuación se presenta una tabla de tipos de datos en C++, mencionando las características o usos de cada tipo:

| **Tipo de dato**  | **Tamaño**      | **Rango de valores**                 | **Descripción**                                           |
|-------------------|-----------------|--------------------------------------|-----------------------------------------------------------|
| `int`             | 4 bytes         | Depende de la arquitectura (usualmente -2,147,483,648 a 2,147,483,647 en sistemas de 32 bits) | Tipo de dato entero. Se usa para almacenar números enteros. |
| `float`           | 4 bytes         | Aproximadamente -3.4E+38 a 3.4E+38   | Tipo de dato de punto flotante de precisión simple. Se usa para almacenar números decimales. |
| `double`          | 8 bytes         | Aproximadamente -1.7E+308 a 1.7E+308 | Tipo de dato de punto flotante de doble precisión. Usado para almacenar números decimales con mayor precisión. |
| `char`            | 1 byte          | -128 a 127 (dependiendo del sistema)  | Tipo de dato para caracteres individuales. Almacena un solo carácter. |
| `bool`            | 1 byte          | `true` o `false`                     | Tipo de dato booleano. Solo puede almacenar valores de verdad (true) o falso (false). |
| `long`            | 4 u 8 bytes     | Depende de la arquitectura           | Tipo de dato entero largo. Almacena números enteros más grandes que `int`. |
| `long long`       | 8 bytes         | Depende de la arquitectura           | Tipo de dato entero largo de 64 bits. Usado para números enteros muy grandes. |
| `short`           | 2 bytes         | Depende de la arquitectura           | Tipo de dato entero corto. Usado para almacenar números enteros más pequeños. |
| `unsigned int`    | 4 bytes         | 0 a 4,294,967,295                    | Tipo de dato entero sin signo. Usado para almacenar solo números positivos. |
| `unsigned char`   | 1 byte          | 0 a 255                              | Tipo de dato de carácter sin signo. Almacena caracteres sin signo (valores de 0 a 255). |
| `unsigned long`   | 4 u 8 bytes     | 0 a 4,294,967,295 (depende de la arquitectura) | Tipo de dato entero largo sin signo. Almacena solo números positivos y grandes. |
