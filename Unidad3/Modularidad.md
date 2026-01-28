---
# 💡 Modularidad.
---
La modularidad en el ambito de computacion y programacion significa dividir un problema grande en modulos o partes independientes mucho mas pequeños para resolver el problema mayor. 
Por lo tanto cada modulo tiene una funcion especifica y autonoma, por lo que es mas eficiente y simplificado, logrando resolver una parte del problema sin tener en cuenta los demas modulos.

Este sistema de modularida ofrece varias ventajas, especialmente en el desarrollo de software, permitiendo un mejor manejo y organizacion, asi logrando una reutilizacion del codigo y mantenimiento eficiente, ademas de ser muy util
cuando se trabaja un problema a solucionar en equipo.

---
<p align="center">
<img width="850" height="625" alt="image" src="https://github.com/user-attachments/assets/ac17fd04-0c3f-4e78-8390-77ab099fafad" />
</p>

---

La modularidad en la programación consiste en dividir un programa en pequeñas piezas individuales llamadas módulos.Cada módulo tiene su propio trabajo específico dentro del sistema.Esto hace que el código teh sea más fácil de entender y ajustar sin arruinar todo el asunto

Los pasos para aplicar la modularidad consisten en:

- Identificar y expresar el problema mayor a resolver.
- Analizar el problema y dividirlo en sub problemas(modulos) que sean de menor complejidad, donde cada uno resuelva una parte del problema central.
- Establecer cómo se comunicarán los módulos entre sí (parámetros de funciones, métodos, entradas y salidas).
- Programar cada modulo.
- Un modulo no debe depender del funcionamiento de otro, sino del resultado que proporciona.
- Validar que cada modulo funcione correctamente independientemente.
- Finalmente unir todos lo modulos para resolver el problema mayor propuesto.

funciones
Funciones con envío de parámetros

---
# ⚙️ Ejercicio de Modularidad por pase de parametro por Valor🔍:
Planteamiento del problema:
>Crear un programa que simule el sistema de una cuenta de banco (Ver saldo de la cuenta, depositar, retirar y salir) divido por modulos.
---

```
//Programa que simula la gestion de una cuenta bancaria de estado de depositar y retirar
#include <stdio.h>
#include <stdlib.h>
float operacionDepositar(int a, float b), operacionRetirar(int a, float b);
void operacionesCuenta();

int main(){
    operacionesCuenta();    
    return 0;
}
//Pedir tipo de operacion que ejecutara
void operacionesCuenta(){
    float saldo = 100;
    int i = 1;
    while(i > 0){
    int operacion, opDepositar, opRetirar;
    printf("ESTA EN SU CUENTA DE BANCO, seleccione el tipo de operacion que desea realizar:\n 1.Consular Saldo\n 2.Depositar Dinero\n 3.Retirar Dinero\n 4.Salir\n");
    scanf("%i", &operacion);
    while(operacion < 1 || operacion > 4){
        printf("Ingrese una opcion valida:\n");
        scanf("%i", &operacion);
    }
    switch(operacion){
        case 1:
        printf("Su saldo disponible es de: %.2f\n", saldo);
        break;
        case 2:
        printf("Ingrese la cantidad que desea depositar a la cuenta de banco:\n 1. 10$\n 2. 20$\n 3. 40$\n 4. 80$\n 5. 100$\n");
        scanf("%i", &opDepositar);
        while(opDepositar< 1 || opDepositar > 5){  
            printf("Ingrese una opcion valida:\n");
            scanf("%i", &opDepositar);
        }
        printf("El saldo actual es de: %.2f\n", operacionDepositar(opDepositar, saldo));
        saldo = operacionDepositar(opDepositar, saldo);
        break;
        case 3:
        printf("Ingrese la cantidad que desea retirar a la cuenta de banco:\n 1. 10$\n 2. 20$\n 3. 40$\n 4. 80$\n 5. 100$\n");
        scanf("%i", &opRetirar);
        while(opRetirar < 1 || opRetirar > 5){  
            printf("Ingrese una opcion valida:\n");
            scanf("%i", &opRetirar);
        }
        printf("El saldo de la cuenta es de: %.2f\n", operacionRetirar(opRetirar, saldo));
        saldo = operacionRetirar(opRetirar, saldo);
        break;
        case 4:
        i = 0;
        break;
    }
    }
}
//Operacion de depositar al saldo
float operacionDepositar(int a, float b){
    float cuentaBanco;
    switch(a){
        case 1:
        cuentaBanco = b + 10;
        break;
        case 2:
        cuentaBanco = b + 20;
        break;
        case 3:
        cuentaBanco = b + 40;
        break;
        case 4:
        cuentaBanco = b + 80;
        break;
        case 5:
        cuentaBanco = b + 100;
        break;
    }
    return(cuentaBanco);
}
//Operacion de retirar al saldo
float operacionRetirar(int a, float b){
    float cuentaBanco;
    switch(a){
        case 1:
        if(b < 10){
            printf("Saldo insuficiente:\n");
            return b;
        }
        cuentaBanco = b - 10;
        break;
        case 2:
        if(b < 20){
            printf("Saldo insuficiente:\n");
            return b;
        }
        cuentaBanco = b - 20;
        break;
        case 3:
        if(b < 40){
            printf("Saldo insuficiente:\n");
            return b;
        }
        cuentaBanco = b - 40;
        break;
        case 4:
        if(b < 80){
            printf("Saldo insuficiente:\n");
            return b;
        }
        cuentaBanco = b - 80;
        break;
        case 5:
        if(b < 100){
            printf("Saldo insuficiente:\n");
            return b;
        }
        cuentaBanco = b - 100;
        break;
    }
    return(cuentaBanco);
}

```
---
## Terminal:
---
```
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> gcc ejercicio4.c -o ejercicio4
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> .\ejercicio4.exe
ESTA EN SU CUENTA DE BANCO, seleccione el tipo de operacion que desea realizar:
 1.Consular Saldo
 2.Depositar Dinero
 3.Retirar Dinero
 4.Salir
1
Su saldo disponible es de: 100.00
ESTA EN SU CUENTA DE BANCO, seleccione el tipo de operacion que desea realizar:
 1.Consular Saldo
 2.Depositar Dinero
 3.Retirar Dinero
 4.Salir
2
Ingrese la cantidad que desea depositar a la cuenta de banco:
 1. 10$
 2. 20$
 3. 40$
 4. 80$
 5. 100$
2
El saldo actual es de: 120.00
ESTA EN SU CUENTA DE BANCO, seleccione el tipo de operacion que desea realizar:
 1.Consular Saldo
 2.Depositar Dinero
 3.Retirar Dinero
 4.Salir
4
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c>
```
---

# ⚙️ Ejercicio de Modularidad por pase de parametro por Referencia🔍:
>Crear un programa que simule el sistema de una cuenta de banco (Ver saldo de la cuenta, depositar, retirar y salir) divido por modulos.
---

```
#include <stdio.h>
#include <stdlib.h>

void operacionDepositar(int a, float *saldo);
void operacionRetirar(int a, float *saldo);
void operacionesCuenta();

int main(){
    operacionesCuenta();    
    return 0;
}

//Pedir tipo de operacion que ejecutara
void operacionesCuenta(){
    float saldo = 100;
    int i = 1;

    while(i > 0){
        int operacion, opDepositar, opRetirar;

        printf("\nESTA EN SU CUENTA DE BANCO\n");
        printf("1. Consultar Saldo\n2. Depositar Dinero\n3. Retirar Dinero\n4. Salir\n");
        scanf("%i", &operacion);

        while(operacion < 1 || operacion > 4){
            printf("Ingrese una opcion valida:\n");
            scanf("%i", &operacion);
        }

        switch(operacion){
            case 1:
                printf("Su saldo disponible es de: %.2f\n", saldo);
                break;

            case 2:
                printf("Ingrese la cantidad que desea depositar:\n");
                printf("1. 10$\n2. 20$\n3. 40$\n4. 80$\n5. 100$\n");
                scanf("%i", &opDepositar);

                while(opDepositar < 1 || opDepositar > 5){
                    printf("Ingrese una opcion valida:\n");
                    scanf("%i", &opDepositar);
                }

                operacionDepositar(opDepositar, &saldo);
                printf("El saldo actual es de: %.2f\n", saldo);
                break;

            case 3:
                printf("Ingrese la cantidad que desea retirar:\n");
                printf("1. 10$\n2. 20$\n3. 40$\n4. 80$\n5. 100$\n");
                scanf("%i", &opRetirar);

                while(opRetirar < 1 || opRetirar > 5){
                    printf("Ingrese una opcion valida:\n");
                    scanf("%i", &opRetirar);
                }

                operacionRetirar(opRetirar, &saldo);
                printf("El saldo actual es de: %.2f\n", saldo);
                break;

            case 4:
                i = 0;
                break;
        }
    }
}

//Operacion de depositar al saldo (Por referencia)
void operacionDepositar(int a, float *saldo){
    switch(a){
        case 1:
          *saldo += 10;
          break;
        case 2:
          *saldo += 20;
          break;
        case 3:
          *saldo += 40;
          break;
        case 4:
          *saldo += 80;
          break;
        case 5:
          *saldo += 100;
          break;
    }
}

//Operacion de retirar al saldo (por referencia)
void operacionRetirar(int a, float *saldo){
    switch(a){
        case 1:
            if(*saldo < 10){
            printf("Saldo insuficiente\n");
            return; }
            *saldo -= 10;
            break;
        case 2:
            if(*saldo < 20){
            printf("Saldo insuficiente\n");
            return; }
            *saldo -= 20;
            break;
        case 3:
            if(*saldo < 40){
            printf("Saldo insuficiente\n");
            return; }
            *saldo -= 40;
            break;
        case 4:
            if(*saldo < 80){
            printf("Saldo insuficiente\n");
            return; }
            *saldo -= 80;
            break;
        case 5:
            if(*saldo < 100){
            printf("Saldo insuficiente\n");
            return; }
            *saldo -= 100;
            break;
    }
}

```
---
## Terminal:
---
```
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> gcc ejercicio5.c -o ejercicio5
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> .\ejercicio5.exe

ESTA EN SU CUENTA DE BANCO
1. Consultar Saldo
2. Depositar Dinero
3. Retirar Dinero
4. Salir
1
Su saldo disponible es de: 100.00

ESTA EN SU CUENTA DE BANCO
1. Consultar Saldo
2. Depositar Dinero
3. Retirar Dinero
4. Salir
3
Ingrese la cantidad que desea retirar:
1. 10$
2. 20$
3. 40$
4. 80$
5. 100$
5
El saldo actual es de: 0.00

ESTA EN SU CUENTA DE BANCO
1. Consultar Saldo
2. Depositar Dinero
3. Retirar Dinero
4. Salir
3
Ingrese la cantidad que desea retirar:
1. 10$
2. 20$
3. 40$
4. 80$
5. 100$
2
Saldo insuficiente
El saldo actual es de: 0.00

ESTA EN SU CUENTA DE BANCO
1. Consultar Saldo
2. Depositar Dinero
3. Retirar Dinero
4. Salir
4
PS C:\Users\Admin\lenguaje_c\calculoasignatura.c> 
```

# [⬅️](../Unidad2/contenidosUnidad2.md)Contenidos de unidad 2

