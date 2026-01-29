# APE 2:
---
```
#include <stdio.h>
#include <stdlib.h>
void calcularValorTotal(int a);
void calcularValorCliente(float *a);


int main(){
  int clientes;
  printf("Ingrese el numero de clientes:\n");
  scanf("%i", &clientes);
  while(clientes <= 0){
    printf("Ingrese un numero valido de clientes:\n");
    scanf("%i", &clientes);
  }
  calcularValorTotal(clientes);
  return 0;
}

void calcularValorTotal(int a){
  float n;
  n = 0;
  for(int i = 1; i <= a; i++){
    printf("CLIENTE %i\n ---------------------------------------\n", i);
    calcularValorCliente(&n);
  }
  printf("El valor total recaudado es de: %.2f", n);
}

void calcularValorCliente(float *a){
  float horas, total;
  int consola;
  total = 0;
  printf("Ingrese el numero de horas:\n");
  scanf("%f", &horas);
  while(horas <= 0){
    printf("Ingrese un numero valido de horas:\n");
    scanf("%f", &horas);
  }
  printf("Ingrese el tipo de consola:\n 1.PlayStation\n 2.Xbox\n 3.Nintendo\n");
  scanf("%i", &consola);
  while(consola <= 0){
    printf("Seleccione una opcion valida:\n");
    scanf("%i", &consola);
  }
  if(consola == 1){
    total = horas * 2.5;
  }else if(consola == 2){
    total = horas * 2;
  }else{
    total = horas * 1.5;
  }
  printf("El valor a pagar por el cliente es de: %.2f\n", total);

  *a += total;
}

```
