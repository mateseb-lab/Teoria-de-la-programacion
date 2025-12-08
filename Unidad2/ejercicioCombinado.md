
# 🛠️Ejercicio combinado: estructura condicional y repetitiva.

### Planteamiento del problema:
> Desarrollar un programa que pida una cantidad válida de números positivos, los lea y determine cuántos numeros positivos, negativos o ceros se escribieron. (y debe ser mayor que 0).
---
### Diagrama de flujo:
<img width="1146" height="691" alt="image" src="https://github.com/user-attachments/assets/738ef49b-f27d-47bd-87f4-d2b3c2df6302" />

---
### Código en lenguaje de programación Java:
---
```
import java.util.Scanner;
public class ContarNumero{
    
    public static void main(String[] args){
        
        int ncant, n, positivos, negativos, ceros, contador;

        negativos = 0;
        positivos = 0;
        ceros = 0;

        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese cantidad de n:\n");
        ncant = entrada.nextInt();

        while(ncant <= 0){
            System.out.println("Error ingrese otra vez:\n");
            ncant = entrada.nextInt();
        }

        for(contador = 1; contador <= ncant ;contador++){

            System.out.println("Ingrese numeros:\n");
            n = entrada.nextInt();

            if(n > 0){
                positivos++;
            }else if(n < 0){
                negativos++;
            }else{
                ceros++;
            }
        }

        entrada.close();

        System.out.printf("Los numeros positivos que ingreso son: %d\n", positivos);
        System.out.printf("Los numeros negativos que ingreso son: %d\n", negativos);
        System.out.printf("Los numeros ceros que ingreso son: %d\n", ceros);
    }

    @Override
    public String toString() {
        return "ContarNumero []";
    }

}
```
### Terminal
---
```
PS C:\Users\Admin\lenguaje_java\ejercicioportafol.md>  & 'D:\java\jdk-21\bin\java.exe' '-XX:+ShowCodeDetailsInExceptionMessages' '-cp' 'C:\Users\Admin\AppData\Roaming\Code\User\workspaceStorage\911d8a6dda0acae9c4f436dfbd78ba83\redhat.java\jdt_ws\ejercicioportafol.md_408231d7\bin' 'ContarNumero'
Ingrese cantidad de n:

-4
Error ingrese otra vez:

-5
Error ingrese otra vez:

4
Ingrese numeros:

4
Ingrese numeros:

0
Ingrese numeros:

-4
Ingrese numeros:

4
Los numeros positivos que ingreso son: 2
Los numeros negativos que ingreso son: 1
Los numeros ceros que ingreso son: 1
PS C:\Users\Admin\lenguaje_java\ejercicioportafol.md>
```
---
## Verificación ❓📝:
---
### Pruebas de Escritorio:
---
### Caso 1:

| **Entrada** |      | **Proceso**                      |             |             |             |            |            |        | **Salida** (final)  |
|-------------|------|----------------------------------|-------------|-------------|-------------|------------|------------|--------|---------------------|
| **ncant**   | **n**| i = 1; i <= ncant; i++           | ¿n > 0?     | ¿n < 0?     | ¿n == 0?    | positivos++| negativos++| ceros++|                     |
| 0           | -    | -                                | -           | -           | -           | -          | -          | -      |                     |
| 3           | 12   | 1                                | sí          | no          | no          | 1          | 0          | 0      |                     |
| 3           | 0    | 2                                | no          | no          | sí          | 1          | 0          | 1      |                     |
| 3           | -9   | 3                                | no          | sí          | no          | 1          | 1          | 1      |                     |
| **Total**   |      |                                  |             |             |             | **1**      | **1**      | **1**  | **1 / 1 / 1**       |


### Caso 2:

| **Entrada** |      | **Proceso**                      |             |             |             |            |            |        | **Salida** (final)  |
|-------------|------|----------------------------------|-------------|-------------|-------------|------------|------------|--------|---------------------|
| **ncant**   | **n**| i = 1; i <= ncant; i++           | ¿n > 0?     | ¿n < 0?     | ¿n == 0?    | positivos++| negativos++| ceros++|                     |
| **4**       | 7    | 1                                | sí          | no          | no          | 1          | 0          | 0      |                     |
| **4**       | -2   | 2                                | no          | sí          | no          | 1          | 1          | 0      |                     |
| **4**       | 0    | 3                                | no          | no          | sí          | 1          | 1          | 1      |                     |
| **4**       | -8   | 4                                | no          | sí          | no          | 1          | 2          | 1      |                     |
| **Total**   |      |                                  |             |             |             | **1**      | **2**      | **1**  | **1 / 2 / 1**       |

### Caso 3:

| **Entrada** |      | **Proceso**                      |             |             |             |            |            |        | **Salida** (final)  |
|-------------|------|----------------------------------|-------------|-------------|-------------|------------|------------|--------|---------------------|
| **ncant**   | **n**| i = 1; i <= ncant; i++           | ¿n > 0?     | ¿n < 0?     | ¿n == 0?    | positivos++| negativos++| ceros++|                     |
| **4**       | 15   | 1                                | sí          | no          | no          | 1          | 0          | 0      |                     |
| **4**       | 0    | 2                                | no          | no          | sí          | 1          | 0          | 1      |                     |
| **4**       | -3   | 3                                | no          | sí          | no          | 1          | 1          | 1      |                     |
| **4**       | 8    | 4                                | sí          | no          | no          | 2          | 1          | 1      |                     |
| **Total**   |      |                                  |             |             |             | **2**      | **1**      | **1**  | **2 / 1 / 1**       |


# [⬅️](../Unidad2/contenidosUnidad2.md)Contenidos de unidad 2
  
