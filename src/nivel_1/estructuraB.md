# Estructura Básica de un programa y Compilación

## Estructura Básica
En C++ es esencial seguir una estructura específica para que el compilador pueda reconocer el programa. En Programación Competitiva, no se requieren clases o estructuras complejas, ya que todo inicia desde la función _**main**_. Por lo que la estructura básica incluye:

1. **Directivas del Procesador:** Estas instrucciones permiten _"incluir"_ funciones y/o símbolos de otro(s) archivo(s) para poder hacer uso de ellos. Por ahora, utilizaremos la _"librería"_ [iostream](https://learn.microsoft.com/es-es/cpp/standard-library/iostream?view=msvc-170) para leer e imprimir en la consola.
    ```C++
    #include <iostream>
    ```

2. **Función Principal:** Es el punto de partida del programa. La función **_int main()_** devuelve un número entero que indica el estatus de la ejecución (0: éxito, 1: error), pero de esto último no tenemos que preocuparnos.
    ```C++
    int main() {
        return 0;
    }
    ```

3. **Espacio de nombres:** Los **_namespace_** se pueden ver como contenedores de funciones y símbolos que están asociadas a ese namespace. Por defecto se accede a ellos usando su nombre seguido de **_::_** (ejemplo: `std::`). Sin embargo esto es redundante y consume mucho tiempo de escritura, por lo que podemos _"configurar"_ que se estará usando ese _**namespace**_ y así solamente escribir el nombre de la función y/o símbolo.
    ```C++
    using namespace std;
    ```
    Comparativa entre usar y no usar _**using namespace**_:
    - **Sin _using namespace_**:
        ```C++
        #include <iostream>

        int main() {
            int a, b;
            std::cin >> a >> b;
            std::cout << (a + b) << "\n";

            return 0;
        }
        ```
    - **Con _using namespace_**:
        ```C++
        #include <iostream>
        using namespace std;

        int main() {
            int a, b;
            cin >> a >> b;
            cout << (a + b) << "\n";

            return 0;
        }
        ```

## Compilación de un archivo de C++

### Intalación de un Compilador
Un compilador es un programa que traduce el código fuente a un lenguaje ejecutable por la computadora. Existen varios compiladores para C++. Si no tienes uno, sigue alguno de los siguientes tutoriales de instalación:
- [Linux](https://code.visualstudio.com/docs/cpp/config-linux#_ensure-gcc-is-installed)
- [Windows](https://code.visualstudio.com/docs/cpp/config-mingw#_installing-the-mingww64-toolchain)
- [macOS](https://code.visualstudio.com/docs/cpp/config-clang-mac#_ensure-clang-is-installed)

### Compilación y Ejecución
Una vez instalado el compilador, crea un archivo con extensión **.cpp** y agrega todo el código dentro de este.
```C++
#include <iostream>
using namespace std;

int main() {
    cout << "Hola Mundo!";

    return 0;
}
```

Para compilar el archivo, abre la consola y navega hasta la carpeta donde se encuentre el archivo. Luego, usa el siguiente comando (usaremos **g++** para este ejemplo):

```
g++ <nombre_del_archivo>.cpp -o <nombre_del_ejecutable>
```

Finalmente, ejecuta el archivo generado:

**Linux/macOS**
```
./<nombre_del_ejecutable>
```

**Windows**
```
<nombre_del_ejecutable>.exe
```
