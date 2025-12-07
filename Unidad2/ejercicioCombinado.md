
# 🛠️Ejercicio combinado estructura condicional y repetitiva.

Planteamiento del problema:
> Desarrollar un programa que pida una cantidad válida de números positivos, los lea y determine cuántos numeros positivos, negativos o ceros se escribieron. (y debe ser mayor que 0).
---
### Diagrama de flujo:
---
<img width="1146" height="691" alt="image" src="https://github.com/user-attachments/assets/738ef49b-f27d-47bd-87f4-d2b3c2df6302" />

---
### Codigo en lenguaje de programacion Java.
```
import java.util.Scanner;
public class ContarNumero{
    
    public static void main(String[] args){
        
        int ncant, n, positivos, negativos, ceros, contador;

        negativos = 0;
        positivos = 0;
        ceros = 0;

        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese la cantidad de numeros\n");
        ncant = entrada.nextInt();

        while(ncant <= 0){
            System.out.println("Error ingrese una cantidad de numeros validos\n");
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


# [⬅️](../Unidad2/contenidosUnidad2.md)Contenido de unidad 2
  
