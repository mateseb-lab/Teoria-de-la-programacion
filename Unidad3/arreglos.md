---
# 🔢📚 Arreglos.
---
Un arreglo es una estructura de datos que se utiliza para guardar varios elementos que son del mismo tipo de dato dentro de espacios consecutivos de memoria. Esta organización logra mantener la información ordenada y accesible de forma eficiente [14].

Cada elemento del arreglo se identifica mediante una posición llamada índice, que generalmente comienza desde cero. Gracias a este sistema, es posible acceder, modificar o recorrer los datos de manera rápida, lo que resulta muy útil cuando se trabaja con grandes cantidades de información [14].

Los arreglos son fundamentales en la programación porque facilitan el almacenamiento masivo de datos bajo un mismo nombre de variable, evitando la necesidad de crear muchas variables individuales. Además, sirven como base para estructuras de datos más complejas, como matrices, listas y otros contenedores de información [14].

Estos arreglos son bastante utiles ya que permiten almacenar muchos datos al mismo tiempo lo que facilita la organizacion y eficiencia, pero su tamaño es fijo es decir que no puede aumenta ni reducir [14].

## ⚙️📚Tipos de arreglos
---

## ➖🔢➖🔢➖🔢Arreglo unidimensional:
Es el tipo más básico; almacena una lista de elementos en una sola fila, es decir se accede mediante un solo indice[14].

---
<p align="center">
<img width="432" height="117" alt="image" src="https://github.com/user-attachments/assets/1ab00b59-e898-4500-96cf-0a4fc933148d" />
</p>

---
## 🔲Arreglo bidimensional (matriz):
Representa datos en forma de tabla con filas y columnas, es decir de dos dimensiones por lo que para acceder a los elementos es necesario dos indices una para la fila otra para la columna[14].

---

<p align="center">
<img width="554" height="360" alt="image" src="https://github.com/user-attachments/assets/c5b3d21f-c700-4590-8b6b-70bc84742857" />
</p>

## 📦📦📦Arreglo Tridimensional:
Es una extensión de los anteriores y puede tener tres o más dimensiones. Se utilizan varios índices para acceder a los datos. Son útiles para representar información más compleja, como coordenadas en el espacio, por lo que en el caso de tres dimensiones se utilizaria tres indices; una para la fila, otra para la columna y la ultima para las capas[14].

---
<p align="center">
<img width="642" height="473" alt="image" src="https://github.com/user-attachments/assets/e485945f-d0f3-47a6-844e-de06f3020626" />
</p>

---
# ⚙️ Ejercicio de Arreglo Unidimensional🔍:
---
>“Desarrollar un programa que registre las temperaturas diarias de varias ciudades, calcule el promedio de temperatura de cada una y determine cuál ciudad presentó la temperatura más alta.”
```
//Sistema que registra la temperatura de varias ciudades para dar un promedio y analisar cual temperatura de Ciudad es mayor
#include <stdio.h>

int main(){
    int ciudadMayor;
    int CIUDADES = 3;
    int DIAS = 3;
    float promedio, suma;
    float listaTemp[DIAS];
    float sumaCiudades = 0;
    float mayoTemp = -999;

    for(int i = 1; i <= CIUDADES; i++){
        printf("CIUDAD %i\n", i);
        suma = 0;
        for(int j = 1; j<= DIAS; j++){
            printf("Ingrese la temperatura del DIA %i\n", j);
            scanf("%f", &listaTemp[j]);
            suma += listaTemp[j];
        }
        promedio = suma / DIAS;
        printf("EL promedio de la CIUDAD %i es: %.2f\n", i, promedio);
        
        if(promedio > mayoTemp){
            ciudadMayor = i;
        }
    }
    printf("La Ciudad con mayor temperatura es la ciudad: %i", ciudadMayor);
    
}
```
---
## Terminal

---
```
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> gcc ejercicio6.c -o ejercicio6
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> .\ejercicio6.exe
CIUDAD 1
Ingrese la temperatura del DIA 1
5.5
Ingrese la temperatura del DIA 2
5.5
Ingrese la temperatura del DIA 3
5.5
EL promedio de la CIUDAD 1 es: 5.50
CIUDAD 2
Ingrese la temperatura del DIA 1
5.5
Ingrese la temperatura del DIA 2
5.6
Ingrese la temperatura del DIA 3
6.7
EL promedio de la CIUDAD 2 es: 5.93
CIUDAD 3
Ingrese la temperatura del DIA 1
6.7
Ingrese la temperatura del DIA 2
6.7
Ingrese la temperatura del DIA 3
4.7
EL promedio de la CIUDAD 3 es: 6.03
La Ciudad con mayor temperatura es la ciudad: 3
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> 
```
# ⚙️ Ejercicio de Arreglo Bidimensional🔍:
>“Desarrollar un programa que reciba las calificaciones de varios estudiantes, calcule el promedio de cada uno y determine cuál estudiante obtuvo el promedio más alto.”
---

```
#include <stdio.h>
#include <stdlib.h>

int main(){
    int ESTUDIANTES = 5;
    int CALIFICACIONES = 4, mayorCalificacion;
    float matriz[ESTUDIANTES][CALIFICACIONES], promedio;
    float mayorprom = -999;

    //Ingresar la nota de cada estudiante
    for(int i = 1; i <= ESTUDIANTES; i++){
        printf("ESTUDIANTE %i\n", i);
        float suma = 0;
        for(int j = 1; j <= CALIFICACIONES; j++){
            printf("Ingrese la nota %i\n", j);
            scanf("%f", &matriz[i][j]);
            while(matriz[i][j] < 0 || matriz[i][j] > 10){
                printf("Ingrese una nota valida:\n");
                scanf("%f", &matriz[i][j]);
            }
            suma += matriz[i][j];
        }
        promedio = suma / CALIFICACIONES;
        //Valida estudiante con mayor promedio
        if(promedio > mayorprom){
            mayorCalificacion = i;
        }
        printf("El promedio del estudiante %i es: %.2f\n", i, promedio);
    }
    printf("El estudiante con mayor promedio es: %i", mayorCalificacion);
    }
```

---
## Terminal:
---
```
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> gcc ejercicio7.c -o ejercicio7
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> .\ejercicio7.exe
ESTUDIANTE 1
Ingrese la nota 1
5
Ingrese la nota 2
5
Ingrese la nota 3
5
Ingrese la nota 4
5
El promedio del estudiante 1 es: 5.00
ESTUDIANTE 2
Ingrese la nota 1
5
Ingrese la nota 2
5
Ingrese la nota 3
5
Ingrese la nota 4
5
El promedio del estudiante 2 es: 5.00
ESTUDIANTE 3
Ingrese la nota 1
5
Ingrese la nota 2
5
Ingrese la nota 3
6
Ingrese la nota 4
6
El promedio del estudiante 3 es: 5.50
ESTUDIANTE 4
Ingrese la nota 1
6
Ingrese la nota 2
6
Ingrese la nota 3
7
Ingrese la nota 4
7
El promedio del estudiante 4 es: 6.50
ESTUDIANTE 5
Ingrese la nota 1
-8
Ingrese una nota valida:
9
Ingrese la nota 2
8
Ingrese la nota 3
-2
Ingrese una nota valida:
44
Ingrese una nota valida:
4
Ingrese la nota 4
5
El promedio del estudiante 5 es: 6.50
El estudiante con mayor promedio es: 5
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c>  
```
---
# ⚙️ Ejercicio de Arreglo Tridimensional🔍:
---
>"Crear un programa que utilice un arreglo tridimensional para almacenar datos numéricos, permitiendo al usuario ingresar los valores y posteriormente mostrarlos organizados por capas, filas y columnas."
```
#include <stdio.h>

int main() {
    int arreglo[2][2][3];
    int i, j, k;

    // Ingreso de datos
    printf("Ingresa los valores del arreglo Tridimensional (2x2x3):\n");

    for (i = 0; i < 2; i++) {            // Capas
        printf("\n--- Capa %d ---\n", i);
        for (j = 0; j < 2; j++) {        // Filas
            for (k = 0; k < 3; k++) {    // Columnas
                printf("Elemento [%d][%d][%d]: ", i, j, k);
                scanf("%d", &arreglo[i][j][k]);
            }
        }
    }

    // Mostrar datos
    printf("\nValores almacenados en el arreglo Tridimensional:\n");

    for (i = 0; i < 2; i++) {
        printf("\n--- Capa %d ---\n", i);
        for (j = 0; j < 2; j++) {
            for (k = 0; k < 3; k++) {
                printf("%d ", arreglo[i][j][k]);
            }
            printf("\n");
        }
    }

    return 0;
}
```
## Terminal:
---
```
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> gcc ejercicio8.c -o ejercicio8
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> .\ejercicio8.exe
Ingresa los valores del arreglo Tridimensional (2x2x3):

--- Capa 0 ---
Elemento [0][0][0]: 1
Elemento [0][0][1]: 2
Elemento [0][0][2]: 3
Elemento [0][1][0]: 1
Elemento [0][1][1]: 2
Elemento [0][1][2]: 3

--- Capa 1 ---
Elemento [1][0][0]: 4
Elemento [1][0][1]: 5
Elemento [1][0][2]: 6
Elemento [1][1][0]: 7
Elemento [1][1][1]: 8
Elemento [1][1][2]: 9

Valores almacenados en el arreglo Tridimensional:

--- Capa 0 ---
1 2 3
1 2 3 

--- Capa 1 ---
4 5 6
7 8 9
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c>
```
# [⬅️](../Unidad3/contenidosUnidad3.md)Contenidos de unidad 3
