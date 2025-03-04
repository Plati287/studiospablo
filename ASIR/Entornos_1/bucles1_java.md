
# Ejemplos de Bucles en Java: `for` y `while`

## Ejemplo con `for`: Contar del 1 al 5

```java
public class EjemploFor {
    public static void main(String[] args) {
        // Usamos un bucle 'for' para contar del 1 al 5
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);  // Imprime el valor de 'i'
        }
    }
}
```

## Ejemplo de Bucle en Java: `while`

### Ejemplo con `while`: Contar del 1 al 5

```java
public class EjemploWhile {
    public static void main(String[] args) {
        // Usamos un bucle 'while' para contar del 1 al 5
        int i = 1;
        while (i <= 5) {
            System.out.println(i);  // Imprime el valor de 'i'
            i++;  // Incrementa 'i' en cada iteración
        }
    }
}
```

---

# Ejercicios Básicos de Java: Bucle `while` y `for`

## Ejercicios con `while` (Súper básicos)

1. **Contar del 1 al 5**  
   Escribe un programa que imprima los números del 1 al 5 utilizando un bucle `while`.

```java
public class ContarDel1Al5 {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println(i);
            i++;
        }
    }
}
```

2. **Sumar los números del 1 al 10**  
   Escribe un programa que sume los números del 1 al 10 utilizando un bucle `while`.

```java
public class SumarDel1Al10 {
    public static void main(String[] args) {
        int suma = 0;
        int i = 1;
        while (i <= 10) {
            suma += i;
            i++;
        }
        System.out.println("La suma de los números del 1 al 10 es: " + suma);
    }
}
```

3. **Mostrar los primeros 3 múltiplos de 2**  
   Escribe un programa que imprima los primeros tres múltiplos de 2 utilizando un bucle `while`.

```java
public class MultiplosDe2 {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 3) {
            System.out.println(2 * i);
            i++;
        }
    }
}
```

4. **Pedir un número y contar hasta él**  
   Escribe un programa que pida al usuario un número y cuente desde el 1 hasta ese número utilizando un bucle `while`.

```java
import java.util.Scanner;

public class ContarHastaNumero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Introduce un número: ");
        int num = scanner.nextInt();
        
        int i = 1;
        while (i <= num) {
            System.out.println(i);
            i++;
        }
    }
}
```

5. **Pedir números hasta que el usuario escriba 0**  
   Escribe un programa que pida al usuario números repetidamente hasta que introduzca el número 0 utilizando un bucle `while`.

```java
import java.util.Scanner;

public class PedirNumerosHastaCero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numero;
        
        do {
            System.out.print("Introduce un número (0 para salir): ");
            numero = scanner.nextInt();
        } while (numero != 0);
        
        System.out.println("Has introducido el 0, programa terminado.");
    }
}
```

---

## Ejercicios con `for` (Súper básicos)

1. **Contar del 1 al 5 con `for`**  
   Escribe un programa que imprima los números del 1 al 5 utilizando un bucle `for`.

```java
public class ContarDel1Al5For {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

2. **Sumar los números del 1 al 10 con `for`**  
   Escribe un programa que sume los números del 1 al 10 utilizando un bucle `for`.

```java
public class SumarDel1Al10For {
    public static void main(String[] args) {
        int suma = 0;
        for (int i = 1; i <= 10; i++) {
            suma += i;
        }
        System.out.println("La suma de los números del 1 al 10 es: " + suma);
    }
}
```

3. **Mostrar los primeros 3 múltiplos de 3**  
   Escribe un programa que imprima los primeros tres múltiplos de 3 utilizando un bucle `for`.

```java
public class MultiplosDe3 {
    public static void main(String[] args) {
        for (int i = 1; i <= 3; i++) {
            System.out.println(3 * i);
        }
    }
}
```

4. **Mostrar los números pares del 2 al 10**  
   Escribe un programa que imprima los números pares entre el 2 y el 10 utilizando un bucle `for`.

```java
public class NumerosPares {
    public static void main(String[] args) {
        for (int i = 2; i <= 10; i += 2) {
            System.out.println(i);
        }
    }
}
```

5. **Contar hacia atrás del 5 al 1**  
   Escribe un programa que cuente hacia atrás desde el 5 hasta el 1 utilizando un bucle `for`.

```java
public class ContarHaciaAtras {
    public static void main(String[] args) {
        for (int i = 5; i >= 1; i--) {
            System.out.println(i);
        }
    }
}
```
