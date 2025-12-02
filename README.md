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
```python
# iNTERFASE DE USUARIO

adelante(5)
abajo(3)

adelante(5)
abajo(3)

adelante(5)
abajo(3)
```

La implementacion de estas funciones es 

``` python

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






---
