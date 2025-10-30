# [⬅️](../Unidad1/contenidosunidad1.md)Contenido de unidad 1
## 3. ⚙️Ejemplos algoritmos con estructuras lineales/secuenciales
---
### Durante la unidad 1 se practico en pseudocodigo(PSeInt) y el lenguaje de programacion C diferentes ejercicios con el proposito de desarrollar y practicar el manejo de algoritmos para resolver un problema determinado.
---
## 3.1 Ejemplos de algoritmos elaborado en el pseudocodigo PSeInt.
---
### Ejercicio ejemplo 1.
---
```
Algoritmo suma
	//Definicion de variables
	Definir numero1, numero2, resultado como Real
	//Datos de entrada
	Escribir "Ingrese numero1";
	Leer numero1;
	Escribir "Ingrese numero2";
	Leer numero2;
	//Proceso
	resultado = numero1 + numero2;
	//Datos de salida
	Escribir "Su suma es: ", resultado;
FinAlgoritmo
```
## [👉Diagrama de flujo](../Unidad1/diagramasflujo/Imagen1.md)
---
### Ejercicio ejemplo 2.
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
## [👉Diagrama de flujo](../Unidad1/diagramasflujo/Imagen2.md)
---
### Ejercicio ejemplo 3.
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
## [👉Diagrama de flujo](../Unidad1/diagramasflujo/Imagen3.md)
---
## 3.2 Ejemplos de algoritmos elaborado en el lenguaje de programacion C.
---
### Ejercicio ejemplo 1
```
#include <stdio.h>
#include <string.h>

int main(){
    //Definicion de variables
    int a, b, c;
    //Datos de entrada
    printf("Ingrese numero1:\n");
    scanf("%i", &a);

    printf("Ingrese el numero2:\n");
    scanf("%i", &b);
    //Proceso
    c = a + b;
    //Datos de salida
    printf("La suma es: %i", c);

return 0;
}
```
<img width="1083" height="165" alt="image" src="https://github.com/user-attachments/assets/266e5fd9-7f89-4cfe-9920-79414d53ce14" />

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
