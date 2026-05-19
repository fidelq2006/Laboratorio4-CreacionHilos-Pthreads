# Laboratorio 4: Creación de Hilos usando Pthreads

## Integrantes
- Fidel Quilumba
- Johan Sasnalema
- Jhon Tiupul
- Karely Bombòn 

## Asignatura
Sistemas Operativos

## Tema
Creación de hilos mediante la biblioteca pthread en lenguaje C.

---

# Objetivos

- Familiarizarse con las funciones pthread.
- Implementar programas multihilo.
- Analizar tiempos de ejecución.
- Comprender la sincronización entre hilos.

---

# Marco teórico

Los hilos (threads) son unidades de ejecución dentro de un proceso. Comparten memoria con otros hilos del mismo proceso, permitiendo ejecutar tareas simultáneamente con menor consumo de recursos que los procesos independientes.

La biblioteca POSIX Threads (pthread) proporciona funciones como:

- `pthread_create()` → Crear hilos
- `pthread_join()` → Esperar la finalización
- `pthread_exit()` → Finalizar hilos
- `pthread_mutex_lock()` → Sincronización

---

# Desarrollo

## Ejercicio 1: Hello World con hilos

### Descripción

Se desarrolló un programa utilizando dos hilos:

- Hilo 1 → imprime "Hello"
- Hilo 2 → imprime "world"

### Código

Subido en:

```txt
codigo/hilo_hello.c
```

### Compilación

```bash
gcc -pthread hilo_hello.c -o hello
./hello
```

### Resultado esperado

```txt
Hello world
```

### Evidencia


---

# Ejercicio 2: Paso de parámetros a los hilos

### Descripción

Se enviaron argumentos mediante punteros tipo `void*`, permitiendo que cada hilo reciba información distinta.

### Código

```txt
codigo/parametros.c
```

### Compilación

```bash
gcc -pthread parametros.c -o parametros
./parametros
```

### Resultado esperado

```txt
Hello     world
```

### Evidencia



---

# Ejercicio 3: Cálculo del tiempo de ejecución

### Descripción

Se calculó el tiempo necesario para crear múltiples hilos utilizando `gettimeofday()`.

### Código

```txt
codigo/tiempo.c
```

### Compilación

```bash
gcc -pthread tiempo.c -o tiempo
./tiempo
```

### Evidencia


---

# Ejercicios del informe

## Ejercicio extra 1:
### Crear 4 hilos con mensajes diferentes

Descripción:

Se implementaron cuatro hilos independientes donde cada uno imprime un mensaje específico.

Mensajes:

- Hilo 1:
- Hilo 2:
- Hilo 3:
- Hilo 4:

Código:

```txt
codigo/cuatro_hilos.c
```

Resultado:



---

## Ejercicio extra 2:
### Tiempo de ejecución para:

- 1 millón de hilos
- 2 millones de hilos
- 3 millones de hilos

Los resultados fueron registrados en microsegundos.

| Cantidad de hilos | Tiempo (µs) |
|-------------------|-------------|
| 1 millón | |
| 2 millones | |
| 3 millones | |

---

# Conclusiones

1. La programación con hilos permite ejecutar tareas concurrentes compartiendo memoria.

2. El uso de `pthread_join()` facilita la sincronización.

3. El tiempo de ejecución aumenta conforme incrementa la cantidad de hilos creados.

4. La creación masiva de hilos puede afectar el rendimiento del sistema.

---

# Referencias

- Documentación POSIX Threads
- GCC Compiler
- Guía de laboratorio proporcionada por la asignatura
