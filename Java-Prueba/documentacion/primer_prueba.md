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

- **Escribe un programa Java que implemente una clase `Rectángulo` con atributos `base` y `altura`, y métodos para calcular el área y el perímetro del rectángulo.**
   ```java
   public class Rectangulo {
       private double base;
       private double altura;
       
       public Rectangulo(double base, double altura) {
           this.base = base;
           this.altura = altura;
       }
       
       public double calcularArea() {
           return base * altura;
       }
       
       public double calcularPerimetro() {
           return 2 * (base + altura);
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `Empleado` con atributos `nombre`, `salario` y `departamento`, y métodos para obtener y establecer estos atributos.**
   ```java
   public class Empleado {
       private String nombre;
       private double salario;
       private String departamento;
       
       public Empleado(String nombre, double salario, String departamento) {
           this.nombre = nombre;
           this.salario = salario;
           this.departamento = departamento;
       }
       
       // Métodos para obtener y establecer atributos
       // (No se incluyen aquí por brevedad)
   }
   ```

- **Escribe un programa Java que implemente una clase `Lista` que pueda almacenar una lista de elementos genéricos y que incluya métodos para agregar, eliminar y buscar elementos en la lista.**
   ```java
   import java.util.ArrayList;
   import java.util.List;

   public class Lista<T> {
       private List<T> elementos;
       
       public Lista() {
           elementos = new ArrayList<>();
       }
       
       public void agregarElemento(T elemento) {
           elementos.add(elemento);
       }
       
       public void eliminarElemento(T elemento) {
           elementos.remove(elemento);
       }
       
       public boolean buscarElemento(T elemento) {
           return elementos.contains(elemento);
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `Calculadora` con métodos estáticos para realizar operaciones matemáticas básicas, como suma, resta, multiplicación y división.**
   ```java
   public class Calculadora {
       public static double sumar(double a, double b) {
           return a + b;
       }
       
       public static double restar(double a, double b) {
           return a - b;
       }
       
       public static double multiplicar(double a, double b) {
           return a * b;
       }
       
       public static double dividir(double a, double b) {
           if (b == 0) {
               throw new IllegalArgumentException("No se puede dividir por cero.");
           }
           return a / b;
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `Pila` (stack) que pueda almacenar una lista de elementos y que incluya métodos para agregar, eliminar y obtener elementos de la pila.**
   ```java
   import java.util.ArrayList;
   import java.util.List;

   public class Pila<T> {
       private List<T> elementos;
       
       public Pila() {
           elementos = new ArrayList<>();
       }
       
       public void apilar(T elemento) {
           elementos.add(elemento);
       }
       
       public T desapilar() {
           if (elementos.isEmpty()) {
               throw new IllegalStateException("La pila está vacía.");
           }
           return elementos.remove(elementos.size() - 1);
       }
       
       public T verTope() {
           if (elementos.isEmpty()) {
               throw new IllegalStateException("La pila está vacía.");
           }
           return elementos.get(elementos.size() - 1);
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `CuentaBancaria` con atributos `saldo` y `interes`, y métodos para depositar y retirar dinero, así como para calcular el interés ganado.**
   ```java
   public class CuentaBancaria {
       private double saldo;
       private double interes;
       
       public void depositar(double cantidad) {
           saldo += cantidad;
       }
       
       public void retirar(double cantidad) {
           if (cantidad > saldo) {
               throw new IllegalArgumentException("Saldo insuficiente.");
           }
           saldo -= cantidad;
       }
       
       public void calcularInteres() {
           double interesGanado = saldo * interes;
           saldo += interesGanado;
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `Vector` para realizar operaciones matemáticas vectoriales, como suma, resta, producto punto y producto cruz.**
   ```java
   public class Vector {
       private double x;
       private double y;
       
       public Vector(double x, double y) {
           this.x = x;
           this.y = y;
       }
       
       public Vector sumar(Vector otro) {
           return new Vector(this.x + otro.x, this.y + otro.y);
       }
       
       public Vector restar(Vector otro) {
           return new Vector(this.x - otro.x, this.y - otro.y);
       }
       
       public double productoPunto(Vector otro) {
           return (this.x * otro.x) + (this.y * otro.y);
       }
       
       public double productoCruz(Vector otro) {
           return (this.x * otro.y) - (this.y * otro.x);
       }
   }
   ```

- **Escribe un programa Java que implemente una clase `Matriz` para realizar operaciones matriciales, como suma, resta, multiplicación y transposición.**
   ```java
   public class Matriz {
       private int[][] datos;
       
       public Matriz(int[][] datos) {
           this.datos = datos;
       }
       
       // Métodos para realizar operaciones matriciales
       // (No se incluyen aquí por brevedad)
   }
   ```

- **Escribe un programa Java que implemente una clase `Registro` para almacenar información de estudiantes, con métodos para agregar, eliminar y buscar estudiantes por su número de identificación.**
   ```java
   import java.util.HashMap;
   import java.util.Map;

   public class RegistroEstudiantes {
       private Map<Integer, Estudiante> registro;
       
       public RegistroEstudiantes() {
           registro = new HashMap<>();
       }
       
       public void agregarEstudiante(Estudiante estudiante) {
           registro.put(estudiante.getId(), estudiante);
       }
       
       public void eliminarEstudiante(int id) {
           registro.remove(id);
       }
       
       public Estudiante buscarEstudiante(int id) {
           return registro.get(id);
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz `Figura` con un método `calcularArea()` y luego crea clases concretas para representar diferentes figuras geométricas que implementen esta interfaz.**
   ```java
   interface Figura {
       double calcularArea();
   }
   
   class Circulo implements Figura {
       private double radio;
       
       public Circulo(double radio) {
           this.radio = radio;
       }
       
       @Override
       public double calcularArea() {
           return Math.PI * radio * radio;
       }
   }
   
   class Cuadrado implements Figura {
       private double lado;
       
       public Cuadrado(double lado) {
           this.lado = lado;
       }
       
       @Override
       public double calcularArea() {
           return lado * lado;
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz funcional `Operacion` con un método `realizarOperacion(double a, double b)` y luego utilice expresiones lambda para definir diferentes operaciones matemáticas.**
   ```java
   interface Operacion {
       double realizarOperacion(double a, double b);
   }
   
   public class Calculadora {
       public static void main(String[] args) {
           Operacion suma = (a, b) -> a + b;
           Operacion resta = (a, b) -> a - b;
           Operacion multiplicacion = (a, b) -> a * b;
           Operacion division = (a, b) -> a / b;
           
           System.out.println("Suma: " + suma.realizarOperacion(5, 3));
           System.out.println("Resta: " + resta.realizarOperacion(5, 3));
           System.out.println("Multiplicación: " + multiplicacion.realizarOperacion(5, 3));
           System.out.println("División: " + division.realizarOperacion(5, 3));
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz `Animal` con un método `hacerSonido()` y luego crea clases concretas para diferentes tipos de animales que implementen esta interfaz.**
   ```java
   interface Animal {
       void hacerSonido();
   }
   
   class Perro implements Animal {
       @Override
       public void hacerSonido() {
           System.out.println("Guau");
       }
   }
   
   class Gato implements Animal {
       @Override
       public void hacerSonido() {
           System.out.println("Miau");
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz funcional `Transformador` con un método `transformar(String texto)` y luego utilice expresiones lambda para definir diferentes transformaciones de texto, como mayúsculas, minúsculas, etc.**
   ```java
   interface Transformador {
       String transformar(String texto);
   }
   
   public class Texto {
       public static void main(String[] args) {
           Transformador mayusculas = texto -> texto.toUpperCase();
           Transformador minusculas = texto -> texto.toLowerCase();
           Transformador reversa = texto -> new StringBuilder(texto).reverse().toString();
           
           System.out.println("Mayúsculas: " + mayusculas.transformar("hola"));
           System.out.println("Minúsculas: " + minusculas.transformar("HOLA"));
           System.out.println("Reversa: " + reversa.transformar("Hola Mundo"));
       }
   }
   ```

- **Escribe un programa Java que utilice el concepto de polimorfismo para imprimir sonidos de diferentes animales almacenados en un arreglo de la interfaz `Animal`.**
   ```java
   public class Main {
       public static void main(String[] args) {
           Animal[] animales = {new Perro(), new Gato()};
           for (Animal animal : animales) {
               animal.hacerSonido();
           }
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz funcional `Filtro` con un método `cumple(Object elemento)` y luego utilice expresiones lambda para filtrar elementos de una lista según ciertos criterios.**
   ```java
   import java.util.List;
   import java.util.ArrayList;

   interface Filtro {
       boolean cumple(Object elemento);
   }

   public class Filtrar {
       public static void main(String[] args) {
           List<String> nombres = new ArrayList<>();
           nombres.add("Juan");
           nombres.add("María");
           nombres.add("Carlos");
           nombres.add("Ana");

           Filtro filtro = nombre -> nombre.toString().startsWith("M");

           for (String nombre : nombres) {
               if (filtro.cumple(nombre)) {
                   System.out.println(nombre);
               }
           }
       }
   }
   ```

- **Escribe un programa Java que implemente una interfaz `Funcion` con un método `aplicar(int numero)` y luego utilice expresiones lambda para definir diferentes funciones matemáticas, como doble, triple, etc.**
   ```java
   interface Funcion {
       int aplicar(int numero);
   }

   public class Funciones {
       public static void main(String[] args) {
           Funcion doble = numero -> numero * 2;
           Funcion triple = numero -> numero * 3;

           System.out.println("El doble de 5 es: " + doble.aplicar(5));
           System.out.println("El triple de 5 es: " + triple.aplicar(5));
       }
   }
   ```

- **Escribe un programa Java que utilice el concepto de polimorfismo para calcular el área de diferentes figuras geométricas almacenadas en un arreglo de la interfaz `Figura`.**
   ```java
   public class Main {
       public static void main(String[] args) {
           Figura[] figuras = {new Circulo(5), new Cuadrado(4)};
           for (Figura figura : figuras) {
               System.out.println("Área: " + figura.calcularArea());
           }
       }
   }
   ```

- **Algoritmo de ordenación QuickSort:**
   ```java
   public class QuickSort {
       public static void quickSort(int[] array, int inicio, int fin) {
           if (inicio < fin) {
               int indiceParticion = particion(array, inicio, fin);
               quickSort(array, inicio, indiceParticion - 1);
               quickSort(array, indiceParticion + 1, fin);
           }
       }

       private static int particion(int[] array, int inicio, int fin) {
           int pivote = array[fin];
           int i = inicio - 1;
           for (int j = inicio; j < fin; j++) {
               if (array[j] <= pivote) {
                   i++;
                   int temp = array[i];
                   array[i] = array[j];
                   array[j] = temp;
               }
           }
           int temp = array[i + 1];
           array[i + 1] = array[fin];
           array[fin] = temp;
           return i + 1;
       }

       public static void main(String[] args) {
           int[] array = {5, 3, 7, 2, 8, 4};
           quickSort(array, 0, array.length - 1);
           System.out.println("Array ordenado: " + Arrays.toString(array));
       }
   }
   ```

- **Clase ThreadPool para administrar hilos:**
   ```java
   import java.util.concurrent.BlockingQueue;
   import java.util.concurrent.LinkedBlockingQueue;

   public class ThreadPool {
       private final int nThreads;
       private final WorkerThread[] threads;
       private final BlockingQueue<Runnable> queue;

       public ThreadPool(int nThreads) {
           this.nThreads = nThreads;
           queue = new LinkedBlockingQueue<>();
           threads = new WorkerThread[nThreads];

           for (int i = 0; i < nThreads; i++) {
               threads[i] = new WorkerThread();
               threads[i].start();
           }
       }

       public void submit(Runnable task) {
           synchronized (queue) {
               queue.add(task);
               queue.notify();
           }
       }

       private class WorkerThread extends Thread {
           public void run() {
               Runnable task;
               while (true) {
                   synchronized (queue) {
                       while (queue.isEmpty()) {
                           try {
                               queue.wait();
                           } catch (InterruptedException e) {
                               e.printStackTrace();
                           }
                       }
                       task = queue.poll();
                   }
                   try {
                       task.run();
                   } catch (RuntimeException e) {
                       e.printStackTrace();
                   }
               }
           }
       }

       public static void main(String[] args) {
           ThreadPool pool = new ThreadPool(5);
           for (int i = 0; i < 10; i++) {
               final int index = i;
               pool.submit(() -> System.out.println("Tarea " + index + " ejecutada por hilo " + Thread.currentThread().getName()));
           }
       }
   }
   ```

- **Algoritmo de Dijkstra para encontrar el camino más corto en un grafo dirigido:**
   ```java
   import java.util.*;

   public class Dijkstra {
       public static void dijkstra(int[][] grafo, int inicio) {
           int n = grafo.length;
           int[] distancias = new int[n];
           boolean[] visitados = new boolean[n];
           Arrays.fill(distancias, Integer.MAX_VALUE);
           distancias[inicio] = 0;

           for (int i = 0; i < n - 1; i++) {
               int minDistancia = Integer.MAX_VALUE;
               int minIndice = -1;
               for (int j = 0; j < n; j++) {
                   if (!visitados[j] && distancias[j] < minDistancia) {
                       minDistancia = distancias[j];
                       minIndice = j;
                   }
               }
               visitados[minIndice] = true;
               for (int j = 0; j < n; j++) {
                   if (!visitados[j] && grafo[minIndice][j] != 0 && distancias[minIndice] != Integer.MAX_VALUE && distancias[minIndice] + grafo[minIndice][j] < distancias[j]) {
                       distancias[j] = distancias[minIndice] + grafo[minIndice][j];
                   }
               }
           }

           System.out.println("Distancias mínimas desde el nodo " + inicio + ": ");
           for (int i = 0; i < n; i++) {
               System.out.println("Nodo " + i + ": " + distancias[i]);
           }
       }

       public static void main(String[] args) {
           int[][] grafo = {
                   {0, 4, 0, 0, 0, 0, 0, 8, 0},
                   {4, 0, 8, 0, 0, 0, 0, 11, 0},
                   {0, 8, 0, 7, 0, 4, 0, 0, 2},
                   {0, 0, 7, 0, 9, 14, 0, 0, 0},
                   {0, 0, 0, 9, 0, 10, 0, 0, 0},
                   {0, 0, 4, 0, 10, 0, 2, 0, 0},
                   {0, 0, 0, 14, 0, 2, 0, 1, 6},
                   {8, 11, 0, 0, 0, 0, 1, 0, 7},
                   {0, 0, 2, 0, 0, 0, 6, 7, 0}
           };
           dijkstra(grafo, 0);
       }
   }
   ```

- **Servidor TCP para admitir múltiples clientes concurrentes:**
   ```java
   import java.io.*;
   import java.net.*;

   public class TCPServer {
       public static void main(String[] args) {
           try (ServerSocket serverSocket = new ServerSocket(8888)) {
               System.out.println("Servidor TCP iniciado. Esperando conexiones...");

               while (true) {
                   Socket clientSocket = serverSocket.accept();
                   System.out.println("Cliente conectado desde " + clientSocket.getInetAddress());

                   ClientHandler clientHandler = new ClientHandler(clientSocket);
                   new Thread(clientHandler).start();
               }
           } catch (IOException e) {
               e.printStackTrace();
           }
       }
   }

   class ClientHandler implements Runnable {
       private final Socket clientSocket;

       public ClientHandler(Socket clientSocket) {
           this.clientSocket = clientSocket;
       }

       public void run() {
           try (BufferedReader in = new BufferedReader(new InputStreamReader(clientSocket.getInputStream()));
                PrintWriter out = new PrintWriter(clientSocket.getOutputStream(), true)) {

               String inputLine;
               while ((inputLine = in.readLine()) != null) {
                   System.out.println("Mensaje recibido del cliente: " + inputLine);
                   out.println("Mensaje recibido: " + inputLine);
               }
           } catch (IOException e) {
               e.printStackTrace();
           }
       }
   }
   ```

- **Búsqueda de patrones utilizando expresiones regulares:**
   ```java
   import java.util.regex.Matcher;
   import java.util.regex.Pattern;

   public class PatternMatching {
       public static void main(String[] args) {
           String texto = "Este es un texto de ejemplo con algunas coincidencias de patrones.";
           String patron = "coincidencias|texto";
           Pattern pattern = Pattern.compile(patron);
           Matcher matcher = pattern.matcher(texto);

           while (matcher.find()) {
               System.out.println("Coincidencia encontrada: " + matcher.group());
           }
       }
   }
   ```

- **Sistema de gestión de memoria virtual para simular la asignación y liberación de memoria:**
   ```java
   import java.util.*;

   public class MemoryManager {
       private final int totalMemory;
       private final int pageSize;
       private final BitSet memoryMap;

       public MemoryManager(int totalMemory, int pageSize) {
           this.totalMemory = totalMemory;
           this.pageSize = pageSize;
           this.memoryMap = new BitSet(totalMemory / pageSize);
       }

       public int allocate(int size) {
           int numPagesNeeded = (size + pageSize - 1) / pageSize;
           int startIndex = memoryMap.nextClearBit(0);
           if (startIndex == -1) {
               return -1; // No hay suficiente memoria disponible
           }
           if (startIndex + numPagesNeeded > memoryMap.size()) {
               return -1; // No hay suficiente memoria disponible
           }
           memoryMap.set(startIndex, startIndex + numPagesNeeded);
           return startIndex;
       }

       public void deallocate(int startIndex, int size) {
           int numPagesNeeded = (size + pageSize - 1) / pageSize;
           memoryMap.clear(startIndex, startIndex + numPagesNeeded);
       }

       public static void main(String[] args) {
           MemoryManager memoryManager = new MemoryManager(1024, 64);
           int allocatedIndex = memoryManager.allocate(128);
           if (allocatedIndex != -1) {
               System.out.println("Memoria asignada en el índice: " + allocatedIndex);
               memoryManager.deallocate(allocatedIndex, 128);
           } else {
               System.out.println("No se pudo asignar memoria.");
           }
       }
   }
   ```

- **Servidor HTTP básico para procesar solicitudes GET y POST:**
```java
import java.io.*;
import java.net.*;

public class SimpleHTTPServer {
    public static void main(String[] args) {
        int port = 8080;
        try (ServerSocket serverSocket = new ServerSocket(port)) {
            System.out.println("Servidor HTTP iniciado en el puerto " + port);
            while (true) {
                Socket clientSocket = serverSocket.accept();
                HttpRequestHandler requestHandler = new HttpRequestHandler(clientSocket);
                new Thread(requestHandler).start();
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

class HttpRequestHandler implements Runnable {
    private final Socket clientSocket;

    public HttpRequestHandler(Socket clientSocket) {
        this.clientSocket = clientSocket;
    }

    @Override
    public void run() {
        try (BufferedReader in = new BufferedReader(new InputStreamReader(clientSocket.getInputStream()));
             PrintWriter out = new PrintWriter(clientSocket.getOutputStream(), true)) {
            String requestLine = in.readLine();
            if (requestLine != null) {
                String[] requestParts = requestLine.split(" ");
                String method = requestParts[0];
                String path = requestParts[1];
                if ("GET".equals(method)) {
                    handleGetRequest(path, out);
                } else if ("POST".equals(method)) {
                    StringBuilder requestBody = new StringBuilder();
                    String line;
                    while ((line = in.readLine()) != null && !line.isEmpty()) {
                        requestBody.append(line).append("\r\n");
                    }
                    handlePostRequest(path, requestBody.toString(), out);
                }
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

    private void handleGetRequest(String path, PrintWriter out) throws IOException {
        String response = "";
        if ("/".equals(path)) {
            response = "HTTP/1.1 200 OK\r\nContent-Type: text/html\r\n\r\n";
            response += "<html><head><title>Simple HTTP Server</title></head><body>";
            response += "<h1>Welcome to Simple HTTP Server</h1>";
            response += "</body></html>";
        } else {
            response = "HTTP/1.1 404 Not Found\r\n\r\n";
        }
        out.println(response);
    }

    private void handlePostRequest(String path, String requestBody, PrintWriter out) throws IOException {
        String response = "HTTP/1.1 200 OK\r\nContent-Type: text/plain\r\n\r\n";
        response += "Received POST request with body:\r\n" + requestBody;
        out.println(response);
    }
}
```

- **Encriptación y desencriptación utilizando el cifrado AES:**
```java
import javax.crypto.*;
import javax.crypto.spec.SecretKeySpec;
import java.util.Base64;

public class AESEncryption {
    private static final String ALGORITHM = "AES";
    private static final String SECRET_KEY = "mysecretkey12345"; // Clave secreta de 16 bytes (128 bits)

    public static String encrypt(String plainText) throws Exception {
        SecretKey secretKey = new SecretKeySpec(SECRET_KEY.getBytes(), ALGORITHM);
        Cipher cipher = Cipher.getInstance(ALGORITHM);
        cipher.init(Cipher.ENCRYPT_MODE, secretKey);
        byte[] encryptedBytes = cipher.doFinal(plainText.getBytes());
        return Base64.getEncoder().encodeToString(encryptedBytes);
    }

    public static String decrypt(String encryptedText) throws Exception {
        SecretKey secretKey = new SecretKeySpec(SECRET_KEY.getBytes(), ALGORITHM);
        Cipher cipher = Cipher.getInstance(ALGORITHM);
        cipher.init(Cipher.DECRYPT_MODE, secretKey);
        byte[] decryptedBytes = cipher.doFinal(Base64.getDecoder().decode(encryptedText));
        return new String(decryptedBytes);
    }

    public static void main(String[] args) {
        try {
            String originalText = "Hola, mundo!";
            System.out.println("Texto original: " + originalText);

            String encryptedText = encrypt(originalText);
            System.out.println("Texto encriptado: " + encryptedText);

            String decryptedText = decrypt(encryptedText);
            System.out.println("Texto desencriptado: " + decryptedText);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

- **Ejemplo básico de una conexión con JDBC (Java Database Connectivity) para conectarte a una base de datos, ejecutar una consulta y recuperar resultados:**
```java
import java.sql.*;

public class JDBCExample {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/mydatabase";
        String username = "username";
        String password = "password";

        try (Connection connection = DriverManager.getConnection(url, username, password)) {
            System.out.println("Conexión exitosa a la base de datos");

            // Ejemplo de consulta
            String query = "SELECT * FROM users";
            try (Statement statement = connection.createStatement();
                 ResultSet resultSet = statement.executeQuery(query)) {
                while (resultSet.next()) {
                    int id = resultSet.getInt("id");
                    String name = resultSet.getString("name");
                    String email = resultSet.getString("email");
                    System.out.println("ID: " + id + ", Name: " + name + ", Email: " + email);
                }
            } catch (SQLException ex) {
                ex.printStackTrace();
            }
        } catch (SQLException ex) {
            ex.printStackTrace();
        }
    }
}
```

- **un ejemplo de cómo crear una interfaz funcional en Java y utilizarla en un método `main`:**

```java
@FunctionalInterface
interface MathOperation {
    int operate(int a, int b);
}

public class Main {
    public static void main(String[] args) {
        // Definición de una expresión lambda para la interfaz funcional MathOperation
        MathOperation addition = (a, b) -> a + b;

        // Uso de la expresión lambda en el método calculate
        System.out.println("Suma: " + calculate(10, 5, addition));

        // También se puede utilizar una expresión lambda directamente en el método calculate
        System.out.println("Resta: " + calculate(10, 5, (a, b) -> a - b));
    }

    // Método que toma una interfaz funcional como argumento
    public static int calculate(int a, int b, MathOperation mathOperation) {
        return mathOperation.operate(a, b);
    }
}
```
