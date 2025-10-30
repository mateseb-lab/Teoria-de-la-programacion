## 3. ⚙️Ejemplos algoritmos con estructuras lineales/secuenciales
---
### Durante la unidad 1 se practico en pseudocodigo(PSeInt) y el lenguaje de programacion C diferentes ejercicios con el proposito de desarrollar y practicar el manejo de algoritmos para resolver un problema determinado.
### Un algoritmo de tipo lineal, o también secuencial, se caracteriza por seguir una ejecuccion recta en la ejecución de sus instrucciones. Estas se van realizando una después de otra, sin desviaciones ni tomas de decisión, desde el principio hasta el fin. Cada acción se apoya en la ejecucion anterior, completándose una única vez, trazando así un flujo continuo hasta alcanzar la solución.
---
## 3.1 Ejemplos de algoritmos elaborado en el pseudocodigo PSeInt.
---
### Ejercicio ejemplo 1.
>En el siguiente ejercicio se elaboró un algoritmo que pueda resolver operaciones matemáticas para realizar la conversión de datos medidos en metros a kilómetros, centímetros y milímetros.
---
```
Algoritmo equivalencia
	// Definicion de variables//
	Definir metros, km, cm, mm como Real;
	//Datos de entrada
	Escribir "Ingrese su valor en metros: ";
	Leer metros;
	//Proceso
	km = metros / 1000;
    cm = metros * 100;
    mm = metros * 1000;
	//Datos de salida
	Escribir "Su valor en km es: ", km;
	Escribir "Su valor en cm es:", cm;
	Escribir "Su valor en mm es:", mm;
FinAlgoritmo
```
## [➡️Diagrama de flujo](../Unidad1/diagramasflujo/Imagen1.md)
## [➡️Prueba de Escritorio](../Unidad1/pruebasEscritorio/prueba1.md)
---
### Ejercicio ejemplo 2.
>El algoritmo, mediante la fórmula de área, utiliza los datos de la base y la altura que son pedidas para realizar la operación dividida entre dos de la fórmula para después calcular el resultado de área.
---
```
Algoritmo operacionArea
	//Definir variables
	Definir base, altura, area como Real;
	//Datos de entrada
	Escribir "Ingrese la base:";
	Leer base;
	Escribir "Ingrese la altura:";
	Leer altura;
	//Proceso 
	area = (base*altura)/2;
	//Datos de salida
	Escribir "Su area es de: ", area;
FinAlgoritmo
```
## [➡️Diagrama de flujo](../Unidad1/diagramasflujo/Imagen2.md)
## [➡️Prueba de Escritorio](../Unidad1/pruebasEscritorio/prueba2.md)
---
### Ejercicio ejemplo 3.
>El algoritmo presentado realiza el cálculo de fórmulas para encontrar la longitud y el área, utilizando el valor PI y el dato de área pedida para llegar al resultado final.
---
```
Algoritmo longitudArea
	//Definicion de variables//
	Definir radio, Op1, Op2 como Real;
	//Datos de entrada
	Escribir "Ingrese radio: ";
	Leer radio;
	//Proceso//
	Op1 = 2*PI*radio;
	OP2 = PI*radio^2;
	//Datos de salida//
	Escribir "Su Longitud es: ",Op1,"Su Area es: ",Op2;
FinAlgoritmo
```
## [➡️Diagrama de flujo](../Unidad1/diagramasflujo/Imagen3.md)
## [➡️Prueba de Escritorio](../Unidad1/pruebasEscritorio/prueba3.md)
---
## 3.2 Ejemplos de algoritmos elaborado en el lenguaje de programacion C.
---
### Ejercicio ejemplo 1
```
#include <stdio.h>
#include <stdlib.h>

int main(){
    //Definicion de variables
    float metros, km, cm, mm;
    //Datos de entrada
    printf("Ingrese su valor en metros:\n");
    scanf("%f", &metros);
    //Proceso
    km = metros / 1000;
    cm = metros * 100;
    mm = metros * 1000;
    //Datos de salida
    printf("el valor en kilometros es:%f\n", km);
    printf("el valor en centimetros es:%f\n", cm);
    printf("el valor en milimetros es:%f\n", mm);

    return 0;
}
```
<img width="1081" height="165" alt="image" src="https://github.com/user-attachments/assets/aa620bf6-8a40-40d8-94f8-ba195ffd1ae7" />

---
### Ejercicio ejemplo 2
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    //Definicion de variables
    float base, altura, area;
    //Datos de entrada
    printf("Ingrese la base:\n");
    scanf("%f", &base);

    printf("Ingrese la altura:\n");
    scanf("%f", &altura);
    //Proceso
    area = (base * altura)/ 2;
    //Datos de salida
    printf("Su area es de:%f", area);

    return 0;
}
```
<img width="1081" height="165" alt="image" src="https://github.com/user-attachments/assets/af54ed0a-4bad-4e47-97da-1f45f1d300ce" />



---
## Ejercicio ejemplo 3
```
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main() {
    //Definicion de variables
    float radio, longitud, area;
    //Datos de entrada
    printf("Escriba el valor del radio:\n");
    scanf("%f", &radio);
    //Proceso
    longitud = 2*M_PI*radio;
    area = M_PI*pow(radio, 2);
    //Datos de salida
    printf("El valor de la longitud es:%f\n", longitud);
    printf("El valor del area es:%f\n", area);

    return 0;
}
```
<img width="981" height="165" alt="image" src="https://github.com/user-attachments/assets/c5b8110c-0778-4472-ba3f-ad2e69713568" />

---
# [⬅️](../Unidad1/contenidosunidad1.md)Contenido de unidad 1
