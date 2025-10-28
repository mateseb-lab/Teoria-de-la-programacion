# [⬅️](../Introduccion/contenidos.md)Contenido de unidad 1
## 3. ⚙️Ejemplos algoritmos con estructuras lineales/secuenciales
---
### Durante la unidad 1 se practico en pseudocodigo(PSeInt) y el lenguaje de programacion C diferentes ejercicios con el proposito de desarrollar y practicar el manejo de algoritmos para resolver un problema determinado.
---
## 3.1 Ejemplos de algoritmos elaborado en el pseudocodigo PSeInt.
---
### Ejercicios elaborados en clase 1.
```
Algoritmo operacion
	//Definicion de variables//
	Definir A, B como Entero
	//Proceso//
	A = 2
	B = 5
	resultado = 4/A*3/6 + 6 /A/1/B^A/4*A
	//Datos de salida//
	Escribir resultado
FinAlgoritmo
```
## [Diagrama de flujo](../../Unidad1/diagramasflujo/Imagen1.md)
### Ejercicio elaborados en clase 2.
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
<img width="1141" height="712" alt="image" src="https://github.com/user-attachments/assets/a5a93b65-5f11-4b40-8ab3-38c2f4a0c8f8" />

---
### Ejercicio elaborado en clase 3.
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
<img width="1142" height="715" alt="image" src="https://github.com/user-attachments/assets/1fc6ef26-0ec0-440c-be46-8433cb9f28b2" />

---
### Ejercicio elaborado en clase 4.
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
<img width="1142" height="706" alt="image" src="https://github.com/user-attachments/assets/35ef68c0-d8db-4fc6-89cb-3bd094de98dd" />

---
### Ejercicio elaborado en clase 5
---
```
Algoritmo Ejercicio_Promedio
	// Definicion de variables//
	Definir nota1, nota2, nota3, PROM30, PROM40, Prom Como Real;
	// Entrada de datos//
	Escribir "Intrduzca la nota de unidad 1";
	Leer nota1;
	Escribir "Introduzca la nota de unidad 2";
	Leer nota2;
	Escribir "Introduzca la nota de unidad 3";
	Leer nota3;
	PROM30 = (30/100);
	PROM40 = (40/100);
	// Proceso//
	OP1 = nota1*PROM30;
	OP2 = nota2*PROM30;
	OP3 = nota3*PROM40;
	Prom = OP1+OP2+OP3;
	// Datos de Salida//
	Escribir "Su promedio es de: ",Prom;
FinAlgoritmo
```
<img width="1151" height="714" alt="image" src="https://github.com/user-attachments/assets/43a6a96f-6fe1-4bf6-9872-93894cc8e841" />

---
### Ejercicio ejemplo algoritmo 6
```
Algoritmo presupuesto
	//Definicion de variables//
	Definir alto,ancho, operacion, operacion2 Como Real;
	//Datos de entrada//
	Escribir "Ingrese alto xfavor";
	Leer alto;
	
	Escribir "Ingrese ancho xfavor";
	Leer ancho;
	
	Escribir "Cuanto cobra por m2";
	Leer m2;
	//Proceso//
	Operacion = alto*ancho;
	Operacion2 = Operacion*m2;
	//Datos de salida//
	Escribir "Su presupuesto es ", Operacion2;
FinAlgoritmo
```
<img width="1146" height="715" alt="image" src="https://github.com/user-attachments/assets/f5350b4d-03bb-494c-b41c-4bbebabeff6f" />

---
## 3.2 Ejemplos de algoritmos elaborado en el lenguaje de programacion C.
---
### Ejercicio ejemplo 1
```
#include <stdio.h>

int main(){
    printf("Hola mundo");
    
    return 0;
}
```
<img width="1101" height="154" alt="image" src="https://github.com/user-attachments/assets/7c167f14-8c31-46c7-8eab-2be66bc6de90" />

---
### Ejercicio ejemplo 2
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    //Opcion 1, lista de caracteres (arreglo)
   /* char nombresCompletos[20];
    printf("Ingrese sus nombres completos:\n");
    scanf("%[^\n]", nombresCompletos);
    getchar();
    printf("Sus nombres completos ingresados son: %s", nombresCompletos);
    */

    //Opcion 2 puntero al inicio de una cadena
    char * nombresCompletos = malloc(100 * sizeof(char)); //reservar memoria
    printf("Ingrese sus nombres completos:\n");
    scanf("%[^\n]s ", nombresCompletos);
    printf("Sus nombres completos ingresados son: %s", nombresCompletos);
    
    //Opcion 3, solo lectura
    /*char *nombresCompletos = "Mateo Pucha";
    printf("Ingrese sus nombres completos:\n");
    scanf("%[^\n]", nombresCompletos);
    getchar();
    printf("Sus nombres completos ingresados son: %s\n", nombresCompletos);*/

    return 0;
}
```
<img width="1101" height="154" alt="image" src="https://github.com/user-attachments/assets/44f93e93-646d-44f5-a3b3-b3363dc75732" />


---
### Ejercicio ejemplo 3
```
#include <stdio.h>
#include <string.h>

int main(){
    int a, b, c;
    printf("Ingrese numero1:\n");
    scanf("%i", &a);

    printf("Ingrese el numero2:\n");
    scanf("%i", &b);

    c = a + b;

    printf("La suma es: %i", c);

return 0;
}
```
<img width="1083" height="165" alt="image" src="https://github.com/user-attachments/assets/266e5fd9-7f89-4cfe-9920-79414d53ce14" />

---
## Ejercicio ejemplo 4
```
#include <stdio.h>
#include <stdlib.h>

int main(){

    int numero1, doble, triple;
    printf("Ingrese el valor del numero:\n");
    scanf("%i",&numero1);

    doble = numero1 * 2;
    triple = numero1 * 3;

    printf("El valor del doble de su numero es:%i\n", doble);
    printf("El valor del triple de su numero es:%i\n", triple);

    return 0;
}
```
<img width="1081" height="160" alt="image" src="https://github.com/user-attachments/assets/ac382720-1f2b-45b3-b569-336f6ec27252" />

---
### Ejercicio ejemplo 5
```
#include <stdio.h>
#include <stdlib.h>

int main(){
    float a, vf, vi, t;
    printf("Ingrese el valor de la velocidad inicial(m/s):\n");
    scanf("%f", &vi);

    printf("Ingrese el valor de la velocidad final(m/s):\n");
    scanf("%f", &vf);

    printf("Ingrese el instante de tiempo(segundos):\n");
    scanf("%f", &t);

    a = (vf - vi) / t;

    printf("El valor de la aceleracion es: %f\n", a);

    return 0;
}
```
<img width="1078" height="179" alt="image" src="https://github.com/user-attachments/assets/5a2fb68c-0dbd-4447-a309-3a6d263db5f3" />

---
### Ejercicio ejemplo 6
```
#include <stdio.h>
#include <stdlib.h>

int main(){
    float metros, km, cm, mm;
    printf("Ingrese su valor en metros:\n");
    scanf("%f", &metros);

    km = metros / 1000;
    cm = metros * 100;
    mm = metros * 1000;

    printf("el valor en kilometros es:%f\n", km);
    printf("el valor en centimetros es:%f\n", cm);
    printf("el valor en milimetros es:%f\n", mm);

    return 0;
}
```
<img width="1081" height="191" alt="image" src="https://github.com/user-attachments/assets/58c8a40e-05d6-46c4-9ed5-185ffb996d1f" />



















