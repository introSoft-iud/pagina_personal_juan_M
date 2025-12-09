# Página Personal — Juan Macías


md signific markdown

¡Bienvenido a mi página personal! amarillo

Este espacio está dedicado a compartir mis proyectos, aprendizajes y reflexiones sobre programación, inteligencia artificial, ciencia de datos y otros temas que me apasionan.  

Aquí encontrarás ejemplos de código, entradas de blog, y recursos educativos que voy construyendo a lo largo de mi trabajo como profesor e investigador.

---

📚 *Temas principales*
- Python y desarrollo de software  
- Inteligencia Artificial y Machine Learning  
- Ciencia de datos y visualización  
- Educación y herramientas abiertas  

💬 Si deseas contactarme o colaborar, puedes hacerlo a través de mis redes o mediante GitHub.

## Últimas Entradas

* [Implementando la libreia turtle desde cero](./tareas/clase5.ipynb)

* *Interfase de usuario para la tortuga*

en esta entrega de mi blog vermos uhn totuga bajar escalas

<img width="318" height="528" alt="image" src="https://github.com/user-attachments/assets/9449da1a-57a4-48fe-8000-e7a450aae87e" />

este moviento se logra con las fuciones 

# iNTERFASE DE USUARIO

adelante(5)
abajo(3)

adelante(5)
abajo(3)

adelante(5)
abajo(3)
```



# Tarea Kevin


tortuga = "🐢"
espacios = 0 #string


def adelante(pasos_adelante):
    
      # Esta faespacioscil de ver que le falta a este print()
    global espacios
    print (espacios * " " + "-" * pasos_adelante, end='')
    #print("🐢")
    print()
    
    espacios = espacios + pasos_adelante
    #camino_abajo = espacios + "|\n"
    


def abajo(pasos_abajo):
    #global espacios
    for i in range (pasos_abajo):            
            print(" " * espacios + "|\n", end='')
    print(" " * espacios + "🐢")
```

En estas fuciones la variable `espacios` es una variable global que hace tales y pacuales

FIN


# Girar y dibujar usando solo `print()` e `input()`

A continuación presentamos una versión limpia y organizada del material, con explicaciones claras y código formateado correctamente.

---

## Ejemplo 1: Girar y avanzar según datos del usuario

Este programa pide dos distancias al usuario, avanza la primera en línea recta, gira 90° a la derecha y luego avanza la segunda, formando una figura en **L**.

```python
import turtle

t = turtle.Turtle()  # Crea una tortuga

# Pedir datos al usuario
distancia1 = int(input("¿Cuántos pasos avanza la tortuga inicialmente? "))
distancia2 = int(input("¿Cuántos pasos avanza la tortuga después de girar? "))

# Movimientos
t.forward(distancia1)   # Avanza la primera distancia
t.right(90)             # Gira 90° a la derecha
t.forward(distancia2)   # Avanza formando la L

turtle.done()           # Mantiene la ventana abierta
```
Tarea de Flor

# Girar y dibujar usando solo `print()` e `input()`

A continuación, presentamos una versión limpia y organizada del material, con explicaciones claras y código formateado correctamente.

---

## Crear la tortuga y moverla

```python
import turtle

t = turtle.Turtle()  # Crea la tortuga
pasos = int(input("¿Cuántos pasos avanza la tortuga? "))
t.forward(pasos)  # Avanza la cantidad de pasos
turtle.done()  # Mantiene la ventana abierta
```

### Explicación breve:

Este programa pide al usuario que ingrese cuántos pasos debe avanzar una tortuga. Al ingresar ese número, el programa simula el movimiento de la tortuga mostrando cómo llega a la nueva posición.

---

## Reto 2: Tortuga bajando

# iNTERFASE DE USUARIO

adelante(5)
abajo(3)

adelante(5)
abajo(3)

adelante(5)
abajo(3)### Explicación breve:

Este programa imprime una "v" por cada paso que la tortuga baja, representando el rastro vertical, y finalmente muestra la tortuga en la posición final.

---

## Reto 3: Tortuga gira

```python
import turtle

t = turtle.Turtle()  # Crea una tortuga
distancia1 = int(input("¿Cuántos pasos avanza la tortuga inicialmente? "))
distancia2 = int(input("¿Cuántos pasos avanza la tortuga después de girar? "))

t.forward(distancia1)  # La tortuga avanza la distancia inicial
t.right(90)  # Gira 90 grados a la derecha
t.forward(distancia2)  # Avanza la segunda distancia formando una 'L'
turtle.done()  # Mantiene la ventana abierta
```

### Explicación breve:

El usuario ingresa primero cuántos pasos avanza la tortuga en línea recta. Luego, la tortuga gira 90 grados a la derecha y avanza otra distancia determinada por el usuario. Esto genera en la pantalla gráfica una trayectoria en forma de "L", mostrando la posición final de la tortuga.

---

## Reto 4: Encapsula los comportamientos anteriores usando funciones

```python
import turtle

t = turtle.Turtle()
t.speed(1)  # Opcional, para ver mejor

def adelante(n, paso=20, espacio=5):
    for _ in range(n):
        t.pendown()
        t.forward(paso)
        t.penup()
        t.forward(espacio)

def abajo(n, paso=20, espacio=5):
    t.right(90)
    for _ in range(n):
        t.pendown()
        t.forward(paso)
        t.penup()
        t.forward(espacio)
    t.left(90)

# Pedir datos al usuario
pasos_derecha = int(input("¿Cuántas rayitas hacia la derecha? "))
pasos_abajo = int(input("¿Cuántas rayitas hacia abajo? "))

# Dibujar con los datos del usuario
adelante(pasos_derecha)
abajo(pasos_abajo)

turtle.done()
```

### Explicación breve:

Creamos funciones:

- `adelante(t, n)`: mueve la tortuga \( t \) \( n \) unidades hacia adelante, que en la orientación inicial es a la derecha.
- `abajo(t, n)`: gira la tortuga 90° a la derecha (queda mirando hacia abajo), avanza \( n \) unidades, y luego gira 90° a la izquierda para volver a mirar a la derecha.

Pedimos datos al usuario:

- Primero cuántos pasos quiere a la derecha.
- Luego cuántos pasos quiere hacia abajo.

Dibujamos la **L**:

- Llamamos `adelante(t, pasos_derecha)`: se dibuja el tramo horizontal.
- Llamamos `abajo(t, pasos_abajo)`: se dibuja el tramo vertical.

Juntos forman la **L**, pero ahora usando funciones reutilizables.

---

## Reto 5: La tortuga baja las escalas

```python
import turtle

t = turtle.Turtle()
t.speed(1)

def adelante(n, paso=20, espacio=5):
    # Avanza en segmentos horizontales separados
    for _ in range(n):
        t.pendown()
        t.forward(paso)
        t.penup()
        t.forward(espacio)

def abajo(n, paso=20, espacio=5):
    # Baja en segmentos verticales separados
    t.right(90)
    for _ in range(n):
        t.pendown()
        t.forward(paso)
        t.penup()
        t.forward(espacio)
    t.left(90)

num_escalones = int(input("¿Cuántos escalones? "))

for i in range(1, num_escalones + 1):
    print(f"# Escalón {i}")
    pasos_derecha = int(input(f"Escalón {i}: ¿cuántos pasos hacia la derecha? "))
    adelante(pasos_derecha)
    pasos_abajo = int(input(f"Escalón {i}: ¿cuántos pasos hacia abajo? "))
    abajo(pasos_abajo)

turtle.done()
```

### Explicación breve:

Un escalón = un tramo hacia la derecha + un tramo hacia abajo.

- `adelante(n)`: dibuja \( n \) pequeños segmentos horizontales separados (simulan los pasos hacia la derecha).
- `abajo(n)`: gira la tortuga hacia abajo, dibuja \( n \) pequeños segmentos separados verticales y luego la vuelve a orientar hacia la derecha.

Esto lo logré con ayuda de inteligencia artificial, ya que me falta aprender más acerca del tema. Muchas gracias.




---
