# Ejercicio: Adivina el Número

Escribe un programa en **Java** que haga lo siguiente:

1. Genere un número secreto aleatorio entre 1 y 100.
2. Pida al usuario que adivine el número.
3. Mientras el usuario no adivine, el programa debe seguir pidiendo números y dar pistas (mayor o menor).
4. Cuando el usuario adivine, mostrar un mensaje de éxito y terminar el programa.

## Ejemplo de solución en Java

```java
import java.util.Scanner;

public class AdivinaElNumero {
    public static void main(String[] args) {
        // Crear un objeto Scanner para leer la entrada del usuario
        Scanner scanner = new Scanner(System.in);

        // Generar un número aleatorio entre 1 y 100
        int numeroSecreto = (int) (Math.random() * 100) + 1;

        // Variable para almacenar la suposición del usuario
        int intento = 0;

        // Pedir al usuario que adivine el número
        System.out.println("¡Bienvenido al juego Adivina el Número!");
        System.out.println("Estoy pensando en un número entre 1 y 100.");
        
        // Continuar pidiendo intentos hasta que el usuario adivine el número
        while (intento != numeroSecreto) {
            System.out.print("Introduce tu suposición: ");
            intento = scanner.nextInt();

            if (intento < numeroSecreto) {
                System.out.println("¡El número es mayor!");
            } else if (intento > numeroSecreto) {
                System.out.println("¡El número es menor!");
            } else {
                System.out.println("¡Felicidades! Has adivinado el número.");
            }
        }

        // Cerrar el escáner al final
        scanner.close();
    }
}
