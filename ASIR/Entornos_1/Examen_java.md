# Vamos a crear el contenido en un archivo .txt con los enunciados y soluciones de los ejercicios en Java
contenido = """
# Ejercicios de Programación en Java

Ejercicio 1: Imprimir Números del 1 al N

Descripción del Ejercicio:

Este ejercicio consiste en escribir un programa en Java que haga lo siguiente:

Pedir un número entero positivo: El programa debe solicitar al usuario que ingrese un número entero positivo. Esto significa que el número ingresado debe ser mayor que cero.

Recorrer los números: Después de recibir el número ingresado, el programa debe imprimir en consola todos los números desde 1 hasta el número que el usuario ingresó. Si el usuario ingresa, por ejemplo, el número 10, el programa debe imprimir todos los números desde el 1 hasta el 10, es decir, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.

Solución:


import java.util.Scanner;

public class Ejercicio1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce un número entero positivo: ");
        int numero = scanner.nextInt();

        for (int i = 1; i <= numero; i += 2) {
            System.out.print(i + " ");
        }
    }
}
Ejercicio 2: Sumar los N Primeros Números Pares
Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

Pedir un número entero positivo: El programa debe solicitar que el usuario ingrese un número entero positivo.
Sumar los N primeros números pares: El programa debe calcular la suma de los primeros N números pares. Por ejemplo, si N es 3, debe sumar: 2 + 4 + 6.
Solución:
import java.util.Scanner;

public class Ejercicio2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce un número entero positivo: ");
        int numero = scanner.nextInt();
        int suma = 0;
        int contador = 0;
        
        // Sumar los primeros N números pares
        for (int i = 2; contador < numero; i += 2) {
            suma += i;
            contador++;
        }
        
        System.out.println("La suma de los primeros " + numero + " números pares es: " + suma);
    }
}
Ejercicio 3: Imprimir los N Primeros Números Impares en Orden Descendente
Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

Pedir un número entero positivo: El programa debe solicitar que el usuario ingrese un número entero positivo.
Mostrar los primeros N números impares en orden descendente: El programa debe imprimir los primeros N números impares, pero de manera descendente. Por ejemplo, si N es 3, debe imprimir: 5, 3, 1.
Solución:
import java.util.Scanner;

public class Ejercicio3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce un número entero positivo: ");
        int numero = scanner.nextInt();
        int contador = 0;

        // Mostrar los primeros N números impares en orden descendente
        for (int i = numero * 2 - 1; contador < numero; i -= 2) {
            System.out.print(i + " ");
            contador++;
        }
    }
}
Ejercicio 4: Imprimir la Suma de los N Primeros Múltiplos de 3
Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

Pedir un número entero positivo N: El programa debe solicitar que el usuario ingrese un número entero positivo N.
Sumar los primeros N múltiplos de 3: El programa debe calcular la suma de los primeros N múltiplos de 3. Por ejemplo, si N es 4, los múltiplos serían: 3, 6, 9, 12, y su suma sería: 30.
Solución:
import java.util.Scanner;

public class Ejercicio4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce un número entero positivo: ");
        int numero = scanner.nextInt();
        int suma = 0;

        // Sumar los primeros N múltiplos de 3
        for (int i = 3; numero > 0; i += 3) {
            suma += i;
            numero--;
        }

        System.out.println("La suma de los primeros múltiplos de 3 es: " + suma);
    }
}
Ejercicio 5: Verificar si un Número es Primo
Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

Pedir un número entero positivo: El programa debe solicitar que el usuario ingrese un número entero positivo.
Verificar si el número es primo: El programa debe comprobar si el número ingresado es un número primo. Un número primo es aquel que solo es divisible por 1 y por sí mismo. El programa debe imprimir si el número es primo o no. Por ejemplo, si el número es 7, debe imprimir: El número 7 es primo.
Solución:
import java.util.Scanner;

public class Ejercicio5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introduce un número entero positivo: ");
        int numero = scanner.nextInt();
        boolean esPrimo = true;

        // Verificar si el número es primo
        for (int i = 2; i <= Math.sqrt(numero); i++) {
            if (numero % i == 0) {
                esPrimo = false;
                break;
            }
        }

        if (esPrimo && numero > 1) {
            System.out.println("El número " + numero + " es primo.");
        } else {
            System.out.println("El número " + numero + " no es primo.");
        }
    }
}
Ejercicio 6: Adivinar el Número con un Bucle While
Descripción del Ejercicio:
Escribe un programa en Java que haga lo siguiente:

Número predefinido: El programa debe tener un número predefinido en el código, el cual será el número que el usuario debe adivinar.
Adivinar el número: El programa debe solicitar al usuario que ingrese un número. Si el número ingresado es mayor, menor o igual al número correcto, el programa debe dar una pista (por ejemplo, "Es mayor", "Es menor", "¡Has acertado!").
Usar un bucle while: El programa debe seguir pidiendo números hasta que el usuario adivine correctamente el número predefinido.
Solución:
import java.util.Scanner;

public class Ejercicio6 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numeroCorrecto = 25;
        int intento;

        // Adivinar el número usando un bucle while
        do {
            System.out.print("Adivina el número: ");
            intento = scanner.nextInt();

            if (intento > numeroCorrecto) {
                System.out.println("Es menor.");
            } else if (intento < numeroCorrecto) {
                System.out.println("Es mayor.");
            } else {
                System.out.println("¡Has acertado!");
            }
        } while (intento != numeroCorrecto);
    }
}
