- **¿Qué es Java y cuál es su propósito principal en la programación?**
   - **Respuesta:** Java es un lenguaje de programación de alto nivel y orientado a objetos. Su propósito principal es proporcionar una plataforma independiente donde el código escrito una vez pueda ejecutarse en cualquier dispositivo o sistema operativo que tenga una máquina virtual Java (JVM) instalada.

- **Describe la diferencia entre una clase y un objeto en Java.**
   - **Respuesta:** Una clase en Java es un plano o una plantilla para crear objetos. Define los atributos y comportamientos comunes a un tipo de objeto. Un objeto, por otro lado, es una instancia de una clase. Representa una entidad del mundo real y tiene un estado (atributos) y comportamiento (métodos).

- **¿Cuál es la diferencia entre una interfaz y una clase abstracta en Java? ¿Cuándo usarías una sobre la otra?**
   - **Respuesta:** Una interfaz en Java define un conjunto de métodos que una clase debe implementar, pero no proporciona ninguna implementación de esos métodos. Una clase abstracta, por otro lado, puede contener tanto métodos abstractos como métodos concretos. Se utiliza una interfaz cuando se quiere garantizar un contrato común entre varias clases sin importar su jerarquía de herencia, mientras que una clase abstracta se utiliza cuando se quiere proporcionar una implementación parcial de una clase y permitir la herencia de otras clases.

- **Explica el concepto de herencia en Java y proporciona un ejemplo.**
   - **Respuesta:** La herencia en Java es un mecanismo que permite a una clase heredar atributos y métodos de otra clase. La clase que hereda se llama subclase o clase derivada, y la clase de la que se hereda se llama superclase o clase base. Por ejemplo:
     ```java
     // Superclase
     class Animal {
         void hacerSonido() {
             System.out.println("Haciendo sonido genérico");
         }
     }
     
     // Subclase
     class Perro extends Animal {
         void hacerSonido() {
             System.out.println("Ladrando");
         }
     }
     ```

- **¿Qué es el polimorfismo en Java y cómo se implementa?**
   - **Respuesta:** El polimorfismo en Java se refiere a la capacidad de una variable, objeto o método para tomar diferentes formas. Se implementa a través del sobrescribir (override) de métodos en clases derivadas y el enlace dinámico. Por ejemplo, una referencia de tipo de una superclase puede apuntar a un objeto de una subclase, y al llamar a un método sobre esa referencia, se ejecutará el método de la subclase si ha sido sobrescrito.

- **Escribe un programa Java que imprima "¡Hola, mundo!" en la consola.**
   ```java
   public class HelloWorld {
       public static void main(String[] args) {
           System.out.println("¡Hola, mundo!");
       }
   }
   ```

- **Escribe un programa Java que sume dos números enteros y muestre el resultado.**
   ```java
   public class Suma {
       public static void main(String[] args) {
           int num1 = 5;
           int num2 = 7;
           int suma = num1 + num2;
           System.out.println("La suma es: " + suma);
       }
   }
   ```

- **Escribe un programa Java que determine si un número es par o impar.**
   ```java
   public class ParImpar {
       public static void main(String[] args) {
           int numero = 7;
           if (numero % 2 == 0) {
               System.out.println("El número es par.");
           } else {
               System.out.println("El número es impar.");
           }
       }
   }
   ```

- **Escribe un programa Java que imprima los números del 1 al 10 en una línea.**
   ```java
   public class Numeros {
       public static void main(String[] args) {
           for (int i = 1; i <= 10; i++) {
               System.out.print(i + " ");
           }
       }
   }
   ```

- **Escribe un programa Java que encuentre el máximo de tres números enteros dados.**
    ```java
    public class Maximo {
        public static void main(String[] args) {
            int num1 = 10;
            int num2 = 5;
            int num3 = 8;
            
            int maximo = num1;
            if (num2 > maximo) {
                maximo = num2;
            }
            if (num3 > maximo) {
                maximo = num3;
            }
            System.out.println("El máximo es: " + maximo);
        }
    }
    ```

- **Escribe un programa Java que calcule el área de un círculo con un radio dado.**
   ```java
   import java.util.Scanner;

   public class AreaCirculo {
       public static void main(String[] args) {
           Scanner input = new Scanner(System.in);
           System.out.print("Ingrese el radio del círculo: ");
           double radio = input.nextDouble();
           double area = Math.PI * Math.pow(radio, 2);
           System.out.println("El área del círculo es: " + area);
       }
   }
   ```

- **Escribe un programa Java que solicite al usuario su nombre y luego imprima un saludo personalizado.**
   ```java
   import java.util.Scanner;

   public class SaludoPersonalizado {
       public static void main(String[] args) {
           Scanner input = new Scanner(System.in);
           System.out.print("Ingrese su nombre: ");
           String nombre = input.nextLine();
           System.out.println("¡Hola, " + nombre + "!");
       }
   }
   ```

- **Escribe un programa Java que sume los números del 1 al 100 e imprima el resultado.**
   ```java
   public class SumaNumeros {
       public static void main(String[] args) {
           int suma = 0;
           for (int i = 1; i <= 100; i++) {
               suma += i;
           }
           System.out.println("La suma de los números del 1 al 100 es: " + suma);
       }
   }
   ```

- **Escribe un programa Java que determine si un número dado es primo o no.**
   ```java
   import java.util.Scanner;

   public class NumeroPrimo {
       public static void main(String[] args) {
           Scanner input = new Scanner(System.in);
           System.out.print("Ingrese un número entero positivo: ");
           int numero = input.nextInt();
           boolean esPrimo = true;
           for (int i = 2; i <= Math.sqrt(numero); i++) {
               if (numero % i == 0) {
                   esPrimo = false;
                   break;
               }
           }
           if (esPrimo && numero > 1) {
               System.out.println(numero + " es un número primo.");
           } else {
               System.out.println(numero + " no es un número primo.");
           }
       }
   }
   ```

- **Escribe un programa Java que convierta grados Celsius a Fahrenheit.**
    ```java
    import java.util.Scanner;

    public class CelsiusToFahrenheit {
        public static void main(String[] args) {
            Scanner input = new Scanner(System.in);
            System.out.print("Ingrese la temperatura en grados Celsius: ");
            double celsius = input.nextDouble();
            double fahrenheit = (celsius * 9/5) + 32;
            System.out.println("La temperatura en grados Fahrenheit es: " + fahrenheit);
        }
    }
    ```

