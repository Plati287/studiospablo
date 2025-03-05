# 📝 **Ejercicio: Contar Números Pares e Impares en un Rango**

## 📌 **Descripción del Problema**  
En este ejercicio, crearemos un programa en **Java** que permitirá al usuario ingresar un número entero positivo. A partir de este número, el programa realizará las siguientes acciones:  

1. **Solicitar al usuario** que ingrese un número entero positivo, que servirá como límite superior del rango.  
2. **Recorrer los números desde 1 hasta el número ingresado** por el usuario.  
3. **Contar cuántos números son pares y cuántos son impares** dentro de ese rango.  
4. **Mostrar el total de números pares e impares encontrados** en la consola.  

---

## 🎯 **Objetivos del Ejercicio**  
✔️ Practicar el uso de **bucles `for`** en Java.  
✔️ Aprender a **distinguir números pares e impares** usando el operador módulo (`%`).  
✔️ Reforzar el uso de **estructuras condicionales (`if-else`)**.  
✔️ Mejorar la interacción con el usuario a través de **entrada y salida de datos** con `Scanner`.  

---

## 📖 **Explicación del Funcionamiento**  
1. El programa **solicita un número entero positivo** al usuario.  
2. Utiliza un **bucle `for`** para recorrer todos los números **desde 1 hasta el número ingresado**.  
3. Dentro del bucle, se usa una **estructura `if-else`** para determinar si cada número es **par o impar**:  
   - Un número es **par** si su residuo al dividirlo entre `2` (`num % 2 == 0`) es igual a **0**.  
   - Un número es **impar** si su residuo al dividirlo entre `2` es diferente de **0**.  
4. Se cuentan los números pares e impares y se guardan en dos variables separadas.  
5. Al finalizar el recorrido, se muestra el total de **pares e impares** encontrados.  

---

## 📂 **Ejemplo de Entrada y Salida**  

### **Entrada:**  
```  
Ingrese un número entero positivo: 10  
```  

### **Salida esperada:**  
```  
Cantidad de números pares: 5  
Cantidad de números impares: 5  
```  

---

## 📚 **Notas Adicionales**  
- Si el usuario ingresa un **número negativo o cero**, el programa debería manejar la entrada para evitar errores.  
- Se podría mejorar el programa agregando validaciones para asegurarse de que el usuario ingrese solo números enteros positivos.  
- También se podría optimizar usando un **bucle `while`** en caso de querer validar la entrada antes de continuar con el conteo.  

---

Este ejercicio es ideal para reforzar el concepto de **bucles y condicionales** en Java 🚀.

import java.util.Scanner;

public class ContarParesImpares {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Pedir al usuario un número
        System.out.print("Ingrese un número entero positivo: ");
        int limite = scanner.nextInt();

        int pares = 0, impares = 0; // Contadores

        // Usar un bucle for para recorrer los números desde 1 hasta el límite
        for (int i = 1; i <= limite; i++) {
            if (i % 2 == 0) {
                pares++; // Si es par, incrementar contador de pares
            } else {
                impares++; // Si es impar, incrementar contador de impares
            }
        }

        // Mostrar resultados
        System.out.println("Cantidad de números pares: " + pares);
        System.out.println("Cantidad de números impares: " + impares);

        scanner.close();
    }
}
