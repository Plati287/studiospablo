Ejercicio: Adivina el Número
Escribe un programa en Java que:

Genere un número secreto aleatorio entre 1 y 100.
Pida al usuario que adivine el número.
Mientras el usuario no adivine, el programa debe seguir pidiendo números y dar pistas (mayor o menor).
Cuando el usuario adivine, mostrar un mensaje de éxito y terminar el programa.

import java.util.Scanner;

public class AdivinaElNumero {
    public static void main(String[] args) {
        // Crear un objeto Scanner para leer la entrada del usuario
        Scanner scanner = new Scanner(System.in);

        // Definir el número secreto que el usuario debe adivinar (puedes cambiarlo manualmente aquí)
        int numeroSecreto = 42;  // Cambia este número por el que quieras

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
