---
#  Estructuras Condicionales.
---
Las estructuras condicionales comparan una variable con uno o más valores, de modo que se pueda determinar un curso de acción dentro del programa en función de los resultados obtenidos. Es importante señalar que la comparación puede hacerse con otra variable o con una constante, según se requiera. Las simples y las múltiples son los dos tipos fundamentales [10].

## 1️⃣ Estructura Condicional simple if.
---
Las estructuras condicionales simples permiten que se tomen decisiones en el interior de un algoritmo. Se incorpora en una estructura selectiva una expresión lógica, la cual se utiliza como condición para determinar el camino que se tomará dentro del programa. Si la condición (expresión lógica) es verdadera, se llevarán a cabo todas las instrucciones que estén dentro del bloque de la estructura condicional simple. Si la expresión lógica es falsa, en cambio ninguna de estas instrucciones se ejecutara [10].


<img width="640" height="301" alt="image" src="https://github.com/user-attachments/assets/97c23cb7-9bde-4b28-9244-3e7ec1324750" />

---
<img width="686" height="359" alt="image" src="https://github.com/user-attachments/assets/f15fb0c2-3809-42fd-becc-bbce461a72f6" />

---

## 2️⃣ Estructura Condicional doble if-else
---
Las estructuras condicionales dobles hacen posible la elección entre dos posibilidades o alternativas, dependiendo de si una condición específica se cumple o no. Por lo tanto, las estructuras condicionales dobles ofrecen dos rutas distintas que el flujo de ejecución del programa podría seguir. Si la expresión a evaluar es verdadera, el programa tomará una rama; si es falsa, tomará otra [10].

<img width="566" height="423" alt="image" src="https://github.com/user-attachments/assets/ca695dd8-b31c-4401-9a57-72eb72568fbd" />

<img width="533" height="342" alt="image" src="https://github.com/user-attachments/assets/bc88d183-a1eb-449f-b24a-57ba84647050" />

---

## 3️⃣ Estructura Condicional multiple switch.
---
La estructura de decisión múltiple evaluará una expresión que puede adoptar n valores diferentes. 1, 2, 3, 4, ..., n. Dependiendo del valor que se escoja de estos en la condición, se ejecutará uno de los n acciones, o, de manera equivalente, el algoritmo seguirá un camino específico entre los n posibles [3].

La condición se representará únicamente en la estructura condicional múltiple mediante una expresión aritmética (o a través de una variable numérica) que es diferente de las condicionales anteriores, donde el resultado de las condicionales solo puede ser verdadero o falso [3].

<img width="540" height="347" alt="image" src="https://github.com/user-attachments/assets/52ab8d50-6324-4d69-a757-12f8f94ee2fa" />

<img width="868" height="333" alt="image" src="https://github.com/user-attachments/assets/0313b489-664c-45ed-8a1f-d914df5bd8cf" />

---
## ⚙️ Ejercicios de Estructuras Condicionales en lenguaje C:
Planteamineto del problema:
>Dado como dato el sueldo de un trabajador, considera un aumento del 45% si su sueldo es inferior a 800, de lo contrario realiza un descuento del 10%. Finalmente mostrar el sueldo con el aumento o el descuento efectuado.
---
## 1️⃣ Estructura Condicional simple else:
```
#include <stdio.h>

int main(){

    int sueldo, SUELDOLIMIT, aumento, suma, descuento, resta;

    SUELDOLIMIT = 800;

    printf("Ingrese sueldo:\n");
    scanf("%i", &sueldo);

    if(sueldo < SUELDOLIMIT){

        aumento = sueldo * 0.45;
        suma = sueldo + aumento;
        printf("Su aumento del 45 por ciento con el sueldo es de: \n%i", suma);
    }

    if(sueldo >= SUELDOLIMIT){

        descuento = sueldo * 0.10;
        resta = sueldo - descuento;
        printf("Su descuento del 10 por ciento con el sueldo es de: \n%i", resta);
    }

    return 0;
}
```
---
## 2️⃣ Estructura Condicional doble if-else.
```

```

# [⬅️](../Unidad2/contenidosUnidad2.md)Contenido de unidad 2
