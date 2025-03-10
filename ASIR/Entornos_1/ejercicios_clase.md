# Ejercicio 1: Pide Números al Usuario Hasta Que Introduzca un 10

### Descripción:
Escribe un programa en Java que haga lo siguiente:

1. **Pedir al usuario un número**: El programa debe solicitar que el usuario ingrese un número.
2. **Comparar el número con el 10**:
   - Si el número es **menor que 10**, debe imprimir: 
     - "[Número] es menor".
   - Si el número es **mayor que 10**, debe imprimir: 
     - "[Número] es mayor".
3. **Seguir pidiendo números**: El programa debe seguir pidiendo números hasta que el usuario ingrese el número 10.
4. **Terminar al ingresar el 10**: Cuando el usuario ingrese el número 10, el programa debe imprimir "fin" y finalizar.

---

# Adivina el Número: Juego en Java

### Descripción:
Este es un juego en Java donde el programa selecciona un número aleatorio, y el usuario debe adivinarlo. El programa le indicará si el número es mayor o menor que el número secreto. El objetivo es adivinar el número en la menor cantidad de intentos posibles.

### Instrucciones:
1. **Generar un número secreto**: En este caso, el número secreto es **34**.
2. **Solicitar un número al usuario**: El programa pedirá al usuario que ingrese un número.
3. **Comparar el intento del usuario**: 
   - Si el intento es **mayor** que el número secreto, el programa mostrará el mensaje: "El número es menor".
   - Si el intento es **menor** que el número secreto, el programa mostrará el mensaje: "El número es mayor".
4. **Cuando el número sea adivinado**: El programa mostrará el mensaje: "¡Adivinaste el número!" y terminará.

import java.util.Scanner;

public class AdivinaElNumero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numero_random = 34; // Número secreto
        int usuario = 0;

        System.out.println("Bienvenido al juego de adivina el número, debes decir un número entre el 1 y 100.");

        // Bucle para seguir pidiendo números hasta adivinar el correcto
        while (usuario != numero_random) {
            System.out.println("Introduce un número:");
            int intento = scanner.nextInt();

            if (intento > numero_random) {
                System.out.println("El número es menor.");
            } else if (intento < numero_random) {
                System.out.println("El número es mayor.");
            } else {
                System.out.println("¡Adivinaste el número!");
                break; // Sale del bucle si el número es adivinado
            }
        }

        // Cierra el scanner al final del juego
        scanner.close();
    }
}


# Ejercicio: Mostrar los Números Pares Hasta un Número

### Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

1. **Pedir un número entero positivo**: El programa debe solicitar que el usuario ingrese un número entero positivo.
2. **Recorrer los números**: El programa debe recorrer los números desde 1 hasta el número ingresado por el usuario.
3. **Mostrar los números pares**: El programa debe imprimir en la consola todos los números pares dentro de ese rango.
   - Si el número ingresado es, por ejemplo, **15**, el programa debe imprimir los números pares hasta 15.


# Ejercicio 2: Mostrar los Números Pares Hasta un Número

### Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

1. **Pedir un número entero positivo**: El programa debe solicitar que el usuario ingrese un número entero positivo.
2. **Recorrer los números**: El programa debe recorrer los números desde 1 hasta el número ingresado por el usuario.
3. **Mostrar los números pares**: El programa debe imprimir en la consola todos los números pares dentro de ese rango.
   - Si el número ingresado es, por ejemplo, **15**, el programa debe imprimir los números pares hasta 15.

---

### Solución:

A continuación se presenta una posible solución en Java para este ejercicio:


import java.util.Scanner;

public class Java {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Introduce un número:");
        int numero = scanner.nextInt();
        
        // Bucle para recorrer los números desde 1 hasta el número ingresado
        for (int i = 1; i <= numero; i++) {
            if (i % 2 == 0) {  // Si el número es par
                System.out.println(i);  // Imprime cada número par en una nueva línea
            }
        }

        scanner.close();
    }
}
