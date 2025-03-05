# Ejercicio 1: Pide números al usuario hasta que introduzca un 10

### Descripción:
Escribe un programa en Java que haga lo siguiente:

1. Pida al usuario que ingrese un número.
2. Luego, el programa debe comparar ese número con el número 10.
3. Si el número es menor que 10, debe imprimir: "[Número] es menor".
4. Si el número es mayor que 10, debe imprimir: "[Número] es mayor".
5. El programa debe seguir pidiendo números hasta que el usuario ingrese el número 10.
6. Cuando el número 10 sea ingresado, el programa debe imprimir "fin" y detenerse.

import java.util.Scanner;
public class java {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numero_random = 34;
        int usuario = 0;
        System.out.println("Bienvenido al juego de adivina el numero, debes de decir un numero entre el 1 al 100");
        while(usuario!=numero_random){
            System.out.println("introduce un numero");
            int intento = scanner.nextInt();
            if(intento > numero_random){
                System.out.println("El numero es menor");
            } else if (intento < numero_random) {
                System.out.println("El numero es mayor");

            }
            else{
                System.out.println("Adivinaste el numero");
                break;
            }
        } scanner.close();

    }
}
