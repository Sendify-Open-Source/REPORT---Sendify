# Fundamentos de Java para Principiantes

## Resumen del Curso
Curso introductorio para aprender los **fundamentos de la programación con Java**, con énfasis en conceptos básicos de **programación orientada a objetos (POO)**. No requiere descargas: todo se hace en el **navegador**, usando editores de código en línea.

- **Duración total:** ~60 minutos (5 lecciones × ~10 min aprox)
- **Público objetivo:** Estudiantes de 12–17 años, **sin experiencia previa** en programación
- **Prerrequisitos:** Ninguno
- **Herramientas necesarias:** Navegador (Chrome, Firefox, Safari, Edge)
- **📂 Repositorio de código fuente:** [_Repositorio_](https://github.com/java-fundamentals-course-Sendify)

---

## Secuencia de la lección

### Lección 1: Introducción a la programación y Java + Sintaxis básica (≈10–12 min)
- **Descripción:** Presenta qué es programar, por qué se utiliza Java y cómo luce un programa mínimo. Se introducen las bases de la sintaxis: declaración de variables, tipos de datos comunes (`int`, `double`, `boolean`, `String`, `char`) y el uso de operadores y expresiones para realizar cálculos simples.
- **Enlace:** [_Ver Contenido_](https://youtu.be/07itrzLZKrQ)
- **Consejos clave:**
  - Piensa en **programar** como dar **instrucciones paso a paso** a la computadora (como una receta).
  - Java es un lenguaje muy usado en la vida real (apps, juegos, sistemas grandes) y es una excelente base para aprender POO.
  - Recuerda la forma general: `tipo nombre = valor;` (por ejemplo, `int edad = 15;`).
  - Usa `System.out.println(...)` para mostrar resultados y combina texto con variables usando `+`.
  - Distingue entre **asignar** (`=`) y **comparar** (`==`); y entiende los operadores básicos: aritméticos (`+ - * / %`), relacionales (`> < >= <= == !=`) y lógicos (`&& || !`).

---

### Lección 2: Estructuras de control y métodos (≈10–12 min)
- **Descripción:** Introduce las estructuras de control más usadas: sentencias `if-else` para tomar decisiones y bucles (`for`, `while`) para repetir acciones. Además, se presentan los **métodos** (funciones) como forma de reutilizar código, junto con parámetros y valores de retorno.
- **Enlace:** [_Ver Contenido_](https://youtu.be/Cvyaw_p3ugQ)
- **Consejos clave:**
  - Usa `if` / `else` para ejecutar bloques de código solo cuando una condición se cumple, por ejemplo:  
    `if (edad >= 18) { ... } else { ... }`.
  - Aplica bucles `for` cuando sabes cuántas veces repetir y `while` cuando se repite mientras una condición sea verdadera.
  - Piensa en un **método** como una “acción” o “verbo”: por ejemplo, `calcularPromedio`, `mostrarMensaje`.
  - Declara métodos estáticos simples para practicar:  
    `public static int sumar(int a, int b) { return a + b; }`.
  - Evita escribir código duplicado: extrae lógica repetida en métodos reutilizables.

---

### Lección 3: Entrada/Salida básica e introducción a la POO (≈10–12 min)
- **Descripción:** Muestra cómo leer datos desde la consola usando `Scanner` y cómo mostrar resultados al usuario. Luego introduce la idea de **clases** y **objetos**: se crea una clase sencilla con atributos y métodos (por ejemplo, una clase `Estudiante` con nombre y edad).
- **Enlace:** [_Ver Contenido_](https://youtu.be/rAiP1Qx2G-g)
- **Consejos clave:**
  - Usa `Scanner` para leer entradas:  
    ```java
    Scanner sc = new Scanner(System.in);
    int edad = sc.nextInt();
    String nombre = sc.nextLine();
    ```
  - Diferencia entre **tipo primitivo** (`int`, `double`, `boolean`) y **tipo referencia** como `String` o tus propias clases.
  - Piensa en una **clase** como el “molde” y en los **objetos** como “instancias” creadas a partir de ese molde.
  - Define atributos dentro de la clase (por ejemplo, `String nombre; int edad;`) y métodos que describan comportamientos simples (como `presentarse()`).
  - Usa constructores para inicializar objetos:  
    `public Estudiante(String nombre, int edad) { this.nombre = nombre; this.edad = edad; }`.

---

### Lección 4: POO básica y estructuras de datos simples (≈10–12 min)
- **Descripción:** Profundiza en los fundamentos de POO con **encapsulación** (uso de `private` y getters/setters) y **creación de múltiples objetos**. Se integran **arrays** y/o manejo de **cadenas** con objetos, por ejemplo, una lista de estudiantes almacenada en un arreglo.
- **Enlace:** [_Ver Contenido_](https://www.youtube.com/watch?v=GE3UkzCddXE)
- **Consejos clave:**
  - Encapsula los datos marcando los atributos como `private` y exponiendo solo lo necesario con métodos `get` y `set`.
  - Encapsulación ≈ **proteger datos** internos de la clase y controlar cómo se modifican.
  - Usa arrays para manejar colecciones sencillas de datos, por ejemplo:  
    `Estudiante[] grupo = new Estudiante[3];`.
  - Practica recorrer un array con un bucle `for` para mostrar información de todos los objetos creados.
  - Cuando trabajes con `String`, recuerda que representa texto y tiene métodos útiles (como `length()`, `toUpperCase()`, etc.) que pueden combinarse con objetos.

---

### Lección 5: Programa POO básico + mejores prácticas (≈12–15 min)
- **Descripción:** Integra todo en un programa sencillo basado en POO, como un **registro de “Estudiante”** o un **juego de adivinanzas** con clases. Se repasan las **mejores prácticas** y los **errores comunes** que suelen cometer los principiantes.
- **Enlace:** [_Ver Contenido_](https://www.youtube.com/watch?v=gOi_coaKv6s&list=PLyeEfgjLet3t4Cdlm3RKH5L_hQA4syNlT)
- **Consejos clave:**
  - Empieza definiendo bien tu modelo: por ejemplo, una clase `Estudiante` con atributos (`nombre`, `edad`, `nota`) y métodos (`calcularEstado`, `presentarse`).
  - Mantén el código organizado: una clase por archivo, nombres claros para clases, métodos y variables.
  - Evita mezclar demasiada lógica en `main`; usa métodos y clases para separar responsabilidades.
  - No te asustes por los errores de compilación: lee el mensaje con calma y revisa primero paréntesis, llaves y punto y coma.
  - Para seguir aprendiendo, practica pequeños cambios sobre tu programa: agregar un nuevo atributo, un nuevo método o una nueva condición.

---

## Recursos Adicionales

- **Códigos usados completos:** [_Repositorio de Java_](https://github.com/java-fundamentals-course-Sendify)
- **Proyecto final en línea (POO básica):** _[Proyecto Final](https://replit.com/@flow11051/FInalJava)_
- **Enlaces extra / lecturas sugeridas:**

  - _[Historia de Java](https://www.youtube.com/watch?v=E8weQyNVWug)_

  - _[Importancia de Java](https://www.youtube.com/watch?v=mksMlTrV8QA)_

---

## Todas las actividades prácticas

- **Actividades de todas las lecciones:** _[Ver actividades](https://replit.com/@coleflows/Actividades-JAVA)_

---

## 👥 Elaboración

**Universidad Peruana de Ciencias Aplicadas**  
Carrera de Ingeniería de Software  
Período **202520** — Curso **1ASI0729 Desarrollo de Aplicaciones Open Source**  

**Nombre del equipo:** Sendify  
**Líder del equipo:** Eduardo Cossar  
**Integrantes:** Joan Aguirre, Renzo Retuerto, Rafael Tasayco, Juan Diego Esquirva  
**Fecha de entrega:**  14/11/2025

