# Ejercicio 1: Pide números al usuario hasta que introduzca un 10

### Descripción:
Escribe un programa en Java que haga lo siguiente:

1. Pida al usuario que ingrese un número.
2. Luego, el programa debe comparar ese número con el número 10.
3. Si el número es menor que 10, debe imprimir: "[Número] es menor".
4. Si el número es mayor que 10, debe imprimir: "[Número] es mayor".
5. El programa debe seguir pidiendo números hasta que el usuario ingrese el número 10.
6. Cuando el número 10 sea ingresado, el programa debe imprimir "fin" y detenerse.

# Adivina el Número: Juego en Java

```java
import java.util.Scanner;

public class java {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numero_random = 34; // Número secreto
        int usuario = 0;

        System.out.println("Bienvenido al juego de adivina el número, debes de decir un número entre el 1 al 100");

        // Bucle para seguir pidiendo números hasta adivinar el correcto
        while(usuario != numero_random){
            System.out.println("Introduce un número");
            int intento = scanner.nextInt();

            if(intento > numero_random){
                System.out.println("El número es menor");
            } else if (intento < numero_random) {
                System.out.println("El número es mayor");
            }
            else{
                System.out.println("¡Adivinaste el número!");
                break; // Sale del bucle si el número es adivinado
            }
        }

        // Cierra el scanner al final del juego
        scanner.close();
    }
}

