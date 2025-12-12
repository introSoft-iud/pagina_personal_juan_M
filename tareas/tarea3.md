# Encapsulación de la tortuga

En esta entrada de mi blog veremos cómo encapsular el comportamiento de la tortuga creada en la tarea 2. Exploraremos primero una **encapsulación funcional** y luego una **encapsulación mediante programación orientada a objetos**.

```python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

```python
# Reto 1
# Simula el comportamiento de la tortuga usando solo print() e input()

print("Simulación de tortuga:")

# Posición inicial
posicion = 0
print("La tortuga está en la posición:", posicion)

# Avanzar
input("Presiona ENTER para avanzar 50 unidades...")

# Dibujar rastro con '-' y flecha al final
pasos = 50
print("-" * (pasos - 1) + "→")

# Actualizar posición
posicion += pasos

# Mostrar nueva posición
print("La tortuga avanzó", pasos, "unidades.")
print("La nueva posición es:", posicion)
```

```
Simulación de tortuga:
La tortuga está en la posición: 0
-------------------------------------------------→
La tortuga avanzó 50 unidades.
La nueva posición es: 50
```

![Simulación reto 1](https://github.com/user-attachments/assets/6e41bef4-fe32-40b0-b63f-bf98af9915c7)

```python
# Reto 2
# Simula la tortuga bajando usando solo print() e input()

print("Simulación de tortuga bajando:")

pasos = 10  # Cantidad de pasos hacia abajo
input("Presiona ENTER para que la tortuga comience a bajar...")

for _ in range(pasos):
    print("|")

print("↓")  # Flecha al final
```

```
Simulación de tortuga bajando:
|
|
|
|
|
|
|
|
|
|
↓
```

![Simulación reto 2](https://github.com/user-attachments/assets/02a8e9eb-a664-469a-9b00-57e7a5e61de5)

```python
# Reto 3
# Tortuga avanzando hacia adelante y luego hacia abajo

print("Simulación de tortuga:\n")

# Tramo horizontal
input("Presiona ENTER para avanzar 50 unidades hacia la derecha...")
print("-" * 49 + "→")

# Tramo vertical hacia abajo
input("Presiona ENTER para avanzar 10 líneas hacia abajo...")
for _ in range(9):
    print(" " * 49 + "|")
print(" " * 49 + "↓")

print("\nLa tortuga ha terminado su recorrido.")
```

```
Simulación de tortuga:

-------------------------------------------------→
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 ↓

La tortuga ha terminado su recorrido.
```

![Simulación reto 3](https://github.com/user-attachments/assets/4ab9a96b-ffc9-4913-90e8-f795f2c8c21e)

```python
# Reto 4
# Girar y dibujar usando solo print() e input()

print("Simulación de tortuga dibujando escalones\n")

# Escalón 1
print("Escalón 1:")
input("ENTER para avanzar 5...")
print("----→")

input("ENTER para bajar 2...")
print("    |")
print("    ↓")

# Escalón 2
print("\nEscalón 2:")
input("ENTER para avanzar 5...")
print("---------→")

input("ENTER para bajar 2...")
print("         |")
print("         ↓")

# Escalón 3
print("\nEscalón 3:")
input("ENTER para avanzar 5...")
print("--------------→")

input("ENTER para bajar 2...")
print("              |")
print("              ↓")

print("\nDibujo terminado.")
```

```
Simulación de tortuga dibujando escalones

Escalón 1:
----→
    |
    ↓

Escalón 2:
---------→
         |
         ↓

Escalón 3:
--------------→
              |
              ↓

Dibujo terminado.
```

![Simulación reto 4](https://github.com/user-attachments/assets/ead55273-0f9f-4552-88ef-407f62bdc2ec)


[Haz clic aquí para ver la versión funcional](https://github.com/introSoft-iud/mini_geom_project_new)  
[Haz clic aquí para ver la versión orientada a objetos](ruta/a/version-poo.md)
