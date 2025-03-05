# Updating the exam content to remove the factorial problem and make the random number static

exam_markdown_content_4_exercises = """
# Examen de Java: Bucles `for` y `while`

## Instrucciones:
1. Responde los ejercicios de acuerdo a las indicaciones.
2. El examen se compone de ejercicios prácticos de programación en Java.
3. Cada ejercicio tiene una puntuación asignada.
4. El examen tiene una puntuación total de 10 puntos.
5. Recuerda que debes realizar todos los ejercicios de manera correcta.

---

## Puntuación:

- Ejercicio 1: Adivina el Número (5 puntos)
- Ejercicio 2: Contar números pares e impares (4 puntos)
- Ejercicio 3: Sumar los Números Impares del 1 al 100 (0.5 puntos)
- Ejercicio 4: Imprimir los Primeros 10 Números Naturales (0.5 puntos)


---

## Ejercicios

### Ejercicio 1: Adivina el Número (5 puntos)

Escribe un programa en Java que haga lo siguiente:
1. Usa un número secreto entre 1 y 100 (por ejemplo, puedes usar el número 50).
2. Pide al usuario que adivine el número.
3. Mientras el usuario no adivine, el programa debe seguir pidiendo números y dar pistas (mayor o menor).
4. Cuando el usuario adivine, mostrar un mensaje de éxito y terminar el programa.

### Ejercicio 2: Contar Números Pares e Impares (4 puntos)

Escribe un programa en Java que realice lo siguiente:
1. Solicite al usuario que ingrese un número entero positivo, que servirá como límite superior del rango.
2. Recorra los números desde 1 hasta el número ingresado por el usuario.
3. Contará cuántos números son pares y cuántos son impares dentro de ese rango.
4. Finalmente, mostrará el total de números pares e impares encontrados en la consola.

### Ejercicio 3: Sumar los Números Impares del 1 al 100 (0.5 puntos)

Escribe un programa que sume todos los números impares entre 1 y 100 utilizando un bucle `while`.

### Ejercicio 4: Imprimir los Primeros 10 Números Naturales (0.5 puntos)

Escribe un programa que imprima los primeros 10 números naturales (del 1 al 10) utilizando un bucle `for`.
"""


# Soluciones Examen de Java: Bucles `for` y `while`

## Ejercicio 1: Adivina el Número (5 puntos)

### Solución:
 Ejercicio 1: Adivina el Número (5 puntos)

```java
import java.util.Scanner;
public class AdivinaNumero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numeroSecreto = 50; // Número secreto entre 1 y 100
        int intento = 0;

        System.out.println("Adivina el número entre 1 y 100:");

        while (intento != numeroSecreto) {
            intento = scanner.nextInt();

            if (intento < numeroSecreto) {
                System.out.println("El número es mayor. Intenta de nuevo.");
            } else if (intento > numeroSecreto) {
                System.out.println("El número es menor. Intenta de nuevo.");
            } else {
                System.out.println("¡Correcto! Has adivinado el número.");
            }
        }
    }
}
Ejercicio 2: Contar Números Pares e Impares (4 puntos)
import java.util.Scanner;

public class ContarParesImpares {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int pares = 0;
        int impares = 0;

        System.out.println("Dime un número:");
        int numero = scanner.nextInt();

        for (int i = 1; i <= numero; i++) {
            if (i % 2 == 0) {
                pares++;
            } else {
                impares++;
            }
        }

        System.out.println("Hay " + pares + " números pares.");
        System.out.println("Hay " + impares + " números impares.");
    }
}
Ejercicio 3: Sumar los Números Impares del 1 al 100 (0.5 puntos)

public class SumarImpares {
    public static void main(String[] args) {
        int suma = 0;

        for (int i = 1; i <= 100; i++) {
            if (i % 2 != 0) {
                suma += i;
            }
        }

        System.out.println("La suma de los números impares entre 1 y 100 es: " + suma);
    }
}
