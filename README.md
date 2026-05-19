En al articulo podrá encontrar el informe detallado del experimento con datos, gráficas, análisis y demás. También encontrará la descripción de los 4 bloques de código del proyecto y el archivo pny de este.

## Instalación de Python, Pygame y Jupyter Kernel en Visual Studio Code

Para ejecutar correctamente la simulación molecular del agua en Python, fue necesario instalar algunas herramientas adicionales en Visual Studio Code. Estas herramientas permiten ejecutar programas gráficos desarrollados con la librería Pygame.

### 1. Instalación de Python

Primero se instaló Python, que es el lenguaje de programación utilizado para desarrollar la simulación. Python permite ejecutar archivos con extensión `.py` y utilizar librerías científicas y gráficas.

Después de instalar Python, se verificó la instalación desde la terminal usando:

```bash
python --version
```

---

### 2. Instalación de Pygame

La simulación utiliza la librería Pygame para crear gráficos, animaciones y manejar eventos como movimiento del mouse y teclado.

La instalación se realizó desde la terminal de Visual Studio Code con el comando:

```bash
pip install pygame
```

Posteriormente se verificó que la instalación fuera correcta ejecutando:

```bash
pip show pygame
```

Pygame permite:

* Dibujar moléculas y enlaces.
* Crear ventanas gráficas.
* Actualizar animaciones en tiempo real.
* Detectar eventos del usuario.

---

### 3. Instalación de Jupyter y Jupyter Kernel

Inicialmente la simulación no se ejecutaba correctamente porque Visual Studio Code no tenía instalado el kernel de Jupyter. El kernel es el componente encargado de conectar Python con el entorno de ejecución de VS Code.

Para solucionarlo se instaló Jupyter usando:

```bash
pip install jupyter
```

Después de la instalación, Visual Studio Code detectó automáticamente el kernel de Python y permitió ejecutar correctamente el programa.

---

### 4. Instalación de extensiones en Visual Studio Code

También fue necesario instalar las extensiones oficiales de:

* Python
* Jupyter

Estas extensiones se instalaron desde la sección de extensiones de Visual Studio Code buscando:

* `Python`
* `Jupyter`

y presionando el botón **Install**.

---
## Instalación de IPyKernel en Visual Studio Code

`ipykernel` es un paquete de Python que permite conectar el intérprete de Python con Jupyter y Visual Studio Code. Gracias a este paquete, VS Code puede reconocer correctamente el entorno de Python y ejecutar notebooks o programas interactivos.

En este proyecto, la instalación de `ipykernel` ayudó a que Visual Studio Code detectara correctamente el entorno de ejecución y permitiera ejecutar la simulación sin errores.

### Pasos para instalar `ipykernel`

### 1. Abrir Visual Studio Code

Se abrió el programa Visual Studio Code.

---

### 2. Abrir una terminal

En la barra superior se seleccionó:

```text id="xbgg0o"
Terminal → Nueva terminal
```

Esto abrió una consola en la parte inferior de la ventana.

---

### 3. Ejecutar el comando de instalación

En la terminal se escribió el siguiente comando:

```bash id="4zn6tt"
pip install ipykernel
```

y luego se presionó Enter.

---

### 4. Verificar la instalación

Después de unos segundos, Python instaló automáticamente el paquete.
Para comprobar que la instalación fue correcta se pudo usar:

```bash id="7nygl5"
pip show ipykernel
```

Si aparece información del paquete, significa que la instalación fue exitosa.

---

### 5. Función de `ipykernel`

Este paquete permite:

* Conectar Python con Jupyter.
* Detectar el entorno de ejecución en Visual Studio Code.
* Ejecutar código interactivo.
* Evitar errores relacionados con kernels o entornos de Python.

En este proyecto, `ipykernel` permitió que la simulación molecular desarrollada con Pygame pudiera ejecutarse correctamente desde Visual Studio Code.

### 5. Ejecución del programa

Finalmente, la simulación se ejecutó desde la terminal de Visual Studio Code con:

```bash
python simulacion_molecular_agua.py
```

Al ejecutarse correctamente, se abrió una ventana gráfica interactiva que muestra el comportamiento molecular del agua en sus tres fases:

* sólido,
* líquido,
* y gaseoso.

El programa permite modificar la temperatura mediante un control deslizante y observar cómo cambian las moléculas y los enlaces de hidrógeno según el estado físico del agua.

# Ejecución del archivo requirements.txt e instalación de librerías

## 1. Crear el entorno virtual

En la terminal de Visual Studio Code escribir:

```bash
python -m venv venv
```

Esto crea una carpeta llamada:

```txt
venv
```

La carpeta contiene un entorno virtual independiente para el proyecto.

---

## 2. Activar el entorno virtual

En PowerShell escribir:

```bash
.\venv\Scripts\Activate
```

Si se activa correctamente, la terminal mostrará algo parecido a:

```txt
(venv) PS C:\Users\rojas\Downloads>
```

---

## 3. Generar automáticamente el archivo requirements.txt

Con el entorno virtual activado y las librerías ya instaladas, escribir:

```bash
pip freeze > requirements.txt
```

Este comando:

* obtiene todas las librerías instaladas,
* guarda sus versiones,
* y crea automáticamente el archivo:

```txt
requirements.txt
```

---

## 4. Verificar que el archivo fue creado

Escribir en la terminal:

```bash
dir
```

Debe aparecer:

```txt
requirements.txt
```

---

## 5. Instalar las librerías desde requirements.txt

Para instalar automáticamente todas las librerías guardadas en el archivo, ejecutar:

```bash
pip install -r requirements.txt
```

El comando leerá el archivo e instalará todas las dependencias necesarias del proyecto.

---

## 6. Ejemplo de contenido generado por pip freeze

El archivo puede contener líneas como:

```txt
numpy==2.3.1
matplotlib==3.10.3
pygame==2.6.1
ipykernel==7.2.0
```

Cada línea representa una librería y su versión exacta instalada en el entorno virtual.


# 6. Activar el entorno virtual

En Windows escribir:

```bash id="0r8x5u"
venv\Scripts\activate
```

Luego presionar ENTER.

Si funciona correctamente aparecerá algo similar a:

```txt id="u7w0q4"
(venv) PS C:\Users\rojas\Downloads>
```

Esto significa que el entorno virtual ya está activo.

---

# 7. Instalar las librerías automáticamente

Con el entorno virtual activado escribir:

```bash id="b5g0s6"
pip install -r requirements.txt
```

Luego presionar ENTER.

Python comenzará a descargar e instalar:

* NumPy
* Matplotlib
* Pandas
* SciPy
* Pygame

---

# 8. Verificar que las librerías fueron instaladas

Escribir:

```bash id="2s8t7j"
pip list
```

La terminal mostrará todas las librerías instaladas dentro del entorno virtual.

---

# 9. Ejecutar el programa

Finalmente ejecutar el archivo Python mediante:

```bash id="z9j6x3"
python simulacion_molecular_agua.py
```

Si todo fue instalado correctamente, el programa abrirá la simulación molecular del agua sin errores.

---

# Explicación

El archivo `requirements.txt` sirve para guardar todas las librerías necesarias del proyecto. Esto permite instalar automáticamente todas las dependencias con un solo comando y facilita compartir el proyecto con otros usuarios o ejecutarlo en diferentes computadores sin problemas de compatibilidad.

ENTORNO VIRTUAL

# Creación de un entorno virtual en Visual Studio Code

## 1. Instalación de Python

Primero se debe descargar e instalar Python 3.11 desde la página oficial:

[Python Official Website](https://www.python.org/downloads/?utm_source=chatgpt.com)

Durante la instalación es importante activar la opción:

```txt id="4yrm7s"
Add Python to PATH
```

Esto permite ejecutar Python desde la terminal de Windows.

---

# 2. Abrir la carpeta del proyecto en Visual Studio Code

En Visual Studio Code se debe abrir la carpeta donde se encuentra el proyecto:

```txt id="u9m0wr"
Archivo → Abrir carpeta
```

Luego se selecciona la carpeta correspondiente.

---

# 3. Abrir la terminal

Dentro de Visual Studio Code abrir:

```txt id="3q0g5m"
Terminal → Nuevo terminal
```

---

# 4. Crear el entorno virtual

En la terminal se escribe:

```bash id="k4i4vk"
python -m venv venv
```

Este comando crea una carpeta llamada:

```txt id="h3w6a7"
venv
```

La carpeta contiene una instalación independiente de Python para el proyecto.

---

# 5. Activar el entorno virtual

En Windows se activa escribiendo:

```bash id="h8c0mg"
venv\Scripts\activate
```

Si el entorno virtual se activó correctamente, aparecerá algo similar a:

```txt id="f0ev8i"
(venv) PS C:\Users\...
```

Esto indica que el entorno virtual ya está funcionando.

---

# 6. Crear el archivo requirements.txt

En Visual Studio Code crear un archivo llamado:

```txt id="4j8a8s"
requirements.txt
```

Dentro del archivo escribir:

```txt id="ot7c5f"
numpy
matplotlib
pandas
scipy
pygame
```

Guardar el archivo con:

```txt id="0p1vrn"
Ctrl + S
```

---

# 7. Instalar las librerías necesarias

Con el entorno virtual activado, escribir en la terminal:

```bash id="0skwwu"
pip install -r requirements.txt
```

Este comando instala automáticamente todas las librerías necesarias para ejecutar el proyecto.

También es posible instalarlas manualmente mediante:

```bash id="ynj6g7"
pip install numpy matplotlib pandas scipy pygame
```

---

# 8. Verificar instalación

Para comprobar que las librerías fueron instaladas correctamente se puede usar:

```bash id="rq9ahk"
pip list
```

La terminal mostrará la lista de paquetes instalados dentro del entorno virtual.

---

# 9. Ejecutar el programa

Finalmente, para ejecutar el proyecto se utiliza:

```bash id="lx3r4s"
python simulacion_molecular_agua.py
```

El entorno virtual garantiza que el proyecto funcione correctamente utilizando las versiones adecuadas de Python y sus librerías, evitando incompatibilidades entre diferentes programas instalados en el sistema.

Estas son las indicaciones para que corra el ultimo bloque codigo que usa pygame:

# INSTALAR PYGAME EN VISUAL STUDIO CODE — PASO A PASO

## 1. Instalar Python

Entrar a:

https://www.python.org/downloads/

Descargar:

* Python 3.12

IMPORTANTE:

Durante la instalación marcar:

[✓] Add Python to PATH

Luego:

Install Now

---

## 2. Instalar Visual Studio Code

Descargar desde:

https://code.visualstudio.com/

Instalar normalmente.

---

## 3. Abrir Visual Studio Code

Abrir VS Code.

---

## 4. Instalar extensión de Python

En VS Code:

Ctrl + Shift + X

Buscar:

Python

Instalar la extensión oficial de Microsoft.

---

## 5. Crear carpeta del proyecto

Crear una carpeta llamada:

SimulacionAgua

---

## 6. Abrir carpeta en VS Code

File → Open Folder

Seleccionar:

SimulacionAgua

---

## 7. Crear archivo Python

Crear archivo:

simulacion.py

Pegar el código.

---

## 8. Abrir terminal

En VS Code:

Terminal → New Terminal

---

## 9. Instalar pygame

En la terminal escribir:

pip install pygame

Si falla:

python -m pip install pygame

---

## 10. Verificar instalación

En terminal escribir:

python

Luego:

import pygame

Si no aparece error, funciona.

Salir con:

exit()

---

## 11. Ejecutar la simulación

En terminal escribir:

python simulacion.py

---

# PRUEBA RÁPIDA

Copiar este código en simulacion.py:

```python
import pygame

pygame.init()

screen = pygame.display.set_mode((400,300))

running = True

while running:

    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    screen.fill((30,30,30))

    pygame.display.flip()

pygame.quit()
```

Ejecutar:

python simulacion.py

Si aparece una ventana negra, pygame funciona correctamente.
BLOUQE 1 DEL CODIGO
****# Bloque 1 — Cálculo del calor latente de fusión del hielo con análisis estadístico

Este bloque de código tiene como objetivo calcular experimentalmente el calor latente de fusión del hielo utilizando datos obtenidos en laboratorio. Además, realiza un análisis estadístico de los resultados para evaluar la precisión del experimento y comparar el valor experimental con el valor teórico reportado en la literatura.

Inicialmente, el programa importa tres bibliotecas fundamentales de Python: pandas, NumPy y SciPy. La biblioteca pandas se utiliza para organizar y manipular los datos experimentales mediante estructuras tipo tabla conocidas como DataFrame. NumPy permite efectuar cálculos numéricos de manera eficiente utilizando arreglos y operaciones matemáticas vectorizadas. Finalmente, SciPy proporciona herramientas estadísticas avanzadas, especialmente útiles para calcular el error estándar y el intervalo de confianza de las mediciones.

Posteriormente, se construye una tabla de datos llamada datos utilizando un DataFrame de pandas. En esta tabla se almacenan las mediciones experimentales obtenidas durante el laboratorio. Cada fila corresponde a una medición distinta y cada columna representa una magnitud física específica: la masa del hielo, la masa del agua, la masa del calorímetro, la temperatura inicial y la temperatura final. Todas las masas se expresan en kilogramos y las temperaturas en grados Celsius.

Después de definir los datos experimentales, el programa establece las constantes físicas necesarias para los cálculos. Se define el calor específico del agua con un valor de 4186 J/(kg·°C) y el calor específico del calorímetro con un valor de 900 J/(kg·°C). Estas constantes permiten calcular la cantidad de energía transferida durante el proceso térmico.

A continuación, el código define las incertidumbres instrumentales asociadas a las mediciones. La incertidumbre de masa se establece como Δm = 5×10⁻⁶ kg, mientras que la incertidumbre de temperatura se fija en ΔT = 0.05 °C. Estas incertidumbres representan la precisión de los instrumentos utilizados en el experimento y son importantes para evaluar la confiabilidad de los resultados obtenidos.

El programa muestra luego las incertidumbres y las mediciones experimentales utilizando estructuras repetitivas. Mediante un ciclo for y la función iterrows() de pandas, el código recorre cada fila del DataFrame e imprime cada medición junto con su respectiva incertidumbre. Esto permite visualizar claramente todos los datos experimentales antes de realizar los cálculos físicos.

Posteriormente, el código procede al cálculo del calor latente de fusión del hielo para cada medición experimental. Para ello, se utiliza la ecuación derivada del principio de conservación de la energía en calorimetría:

L_f = \frac{(Mc_{agua}+M_{cal}c_{cal})(T_i-T_f)-m_h c_{agua}T_f}{m_h}

En esta expresión:

* $M$ representa la masa del agua.
* $c_{agua}$ es el calor específico del agua.
* $M_{cal}$ corresponde a la masa del calorímetro.
* $c_{cal}$ es el calor específico del calorímetro.
* $T_i$ es la temperatura inicial.
* $T_f$ es la temperatura final.
* $m_h$ representa la masa del hielo.
* $L_f$ corresponde al calor latente de fusión del hielo.

El código extrae individualmente cada variable física desde el DataFrame y sustituye los valores numéricos dentro de la ecuación. Luego calcula el numerador de la expresión, que representa la energía total cedida por el agua y el calorímetro menos la energía absorbida por el hielo al calentarse hasta la temperatura final. Finalmente, divide este resultado entre la masa del hielo para obtener el valor experimental del calor latente de fusión.

Cada resultado calculado se almacena en una lista llamada Lf. Una vez finalizadas todas las mediciones, la lista se convierte en un arreglo NumPy para facilitar el análisis estadístico posterior.

El siguiente paso consiste en calcular el promedio experimental de los valores obtenidos. Para ello, el programa utiliza la función mean() de NumPy, obteniendo así un único valor representativo del calor latente de fusión medido experimentalmente.

Después, el código realiza un análisis estadístico completo de las mediciones. Primero calcula la desviación estándar muestral utilizando la función std() con el parámetro ddof=1. Esta magnitud permite evaluar qué tan dispersos se encuentran los resultados respecto al promedio.

Posteriormente, se calcula el error estándar utilizando la función sem() de SciPy. El error estándar mide la precisión del promedio experimental y disminuye a medida que aumenta la cantidad de mediciones realizadas.

Luego se determina el intervalo de confianza al 95% utilizando la distribución t de Student mediante la función stats.t.interval(). Este intervalo proporciona un rango dentro del cual probablemente se encuentra el verdadero valor experimental del calor latente de fusión.

El código también calcula el porcentaje de error respecto al valor teórico aceptado para el calor latente de fusión del hielo, cuyo valor es:

L_{teo}=3.348\times10^5\ \text{J/kg}

El porcentaje de error se calcula mediante la ecuación:

%\ error = \left|\frac{L_{prom}-L_{teo}}{L_{teo}}\right|\times100

Este cálculo permite comparar cuantitativamente el valor experimental con el valor teórico y evaluar la calidad del procedimiento experimental realizado.

Finalmente, el programa imprime una interpretación física de los resultados obtenidos. En esta sección se concluye que, si el porcentaje de error es relativamente pequeño, el experimento puede considerarse exitoso y consistente con la teoría. También se mencionan posibles fuentes de error experimental, tales como pérdidas de calor hacia el ambiente, limitaciones instrumentales y transferencia térmica imperfecta.

En conjunto, este bloque de código no solo automatiza los cálculos físicos y estadísticos del experimento, sino que además permite organizar los resultados, analizarlos rigurosamente y obtener conclusiones cuantitativas sobre la validez del procedimiento experimental realizado.
****
# Bloque 2 — Generación de gráficas experimentales mediante programación orientada a objetos

Este bloque de código tiene como objetivo generar diferentes representaciones gráficas de los datos experimentales obtenidos durante el cálculo del calor latente de fusión del hielo. Para ello, se emplean herramientas de visualización de datos junto con principios de programación orientada a objetos, permitiendo organizar el código de manera más estructurada, reutilizable y eficiente.

Inicialmente, el programa importa las bibliotecas necesarias para realizar los cálculos y las gráficas. La biblioteca NumPy se utiliza para manejar arreglos numéricos y facilitar operaciones matemáticas sobre los datos experimentales. Por otra parte, matplotlib.pyplot permite construir gráficos científicos de manera sencilla y visualmente clara. Finalmente, desde el módulo abc se importan las herramientas ABC y abstractmethod, utilizadas para crear clases abstractas.

Posteriormente, se define una clase abstracta llamada GraficaBase. Esta clase funciona como una plantilla general para todas las gráficas que se crearán posteriormente. Su propósito principal es reunir las características comunes que compartirán todas las representaciones gráficas del programa.

Dentro del constructor **init** de la clase GraficaBase se almacenan tres atributos fundamentales: el título de la gráfica, la etiqueta del eje horizontal y la etiqueta del eje vertical. Estos parámetros permiten personalizar cada figura según los datos que se deseen representar.

Además, esta clase contiene el método configurar_grafica(), encargado de aplicar configuraciones generales a cualquier gráfica. En este método se asigna el título, los nombres de los ejes y se activa una cuadrícula para facilitar la lectura de los datos experimentales.

La clase también incluye el método abstracto graficar(). Al ser un método abstracto, no contiene implementación directa, sino que obliga a que cada clase hija desarrolle su propia forma de generar la gráfica correspondiente. Esto constituye una aplicación del polimorfismo dentro de la programación orientada a objetos.

Después de definir la clase base, el programa crea una clase hija denominada GraficaDispersion, la cual hereda las propiedades de GraficaBase. Esta clase se utiliza para construir gráficas de dispersión, también conocidas como scatter plots.

En el constructor de GraficaDispersion se reciben los valores del eje x y del eje y, además de los parámetros heredados de la clase base. Los datos son convertidos a arreglos NumPy para facilitar su manipulación numérica.

Dentro del método graficar() se crea una nueva figura utilizando:

\text{Figura de tamaño }(6,4)

Luego, los puntos experimentales se representan mediante la función scatter(), que permite visualizar la relación entre dos variables físicas experimentales. Finalmente, se llama al método configurar_grafica() heredado de la clase base y se muestra la gráfica utilizando show().

Posteriormente, el programa define otra clase hija llamada GraficaLinea. Esta clase también hereda de GraficaBase y se utiliza para representar gráficos de dispersión acompañados de una línea de referencia horizontal.

Además de almacenar los datos experimentales, esta clase recibe un parámetro adicional llamado linea, el cual representa el valor de referencia que se desea comparar con las mediciones experimentales.

En el método graficar() se representan primero los datos mediante scatter() y posteriormente se dibuja una línea horizontal utilizando plot(). Esta línea sirve como referencia visual para comparar los resultados experimentales con un valor teórico o promedio.

Luego se crea la clase GraficaBarras, destinada a representar diagramas de barras. Esta clase también hereda de GraficaBase y almacena etiquetas categóricas junto con los valores numéricos asociados a cada barra.

En su método graficar() se utiliza la función bar() de matplotlib para representar visualmente las diferencias entre distintas mediciones o porcentajes de error.

Una vez definidas las clases, el programa introduce los datos experimentales que serán utilizados en las gráficas. Entre estos datos se encuentran las temperaturas iniciales y finales, las masas de hielo, los valores experimentales del calor latente, el valor teórico y los porcentajes de error de cada medición.

Posteriormente, el código genera cinco gráficas distintas utilizando objetos creados a partir de las clases previamente definidas.

La primera gráfica representa la relación entre la temperatura inicial y el calor latente de fusión. Para ello, se utiliza un objeto de la clase GraficaLinea. En esta gráfica se incluyen los puntos experimentales y una línea horizontal cercana al valor teórico del calor latente, permitiendo observar qué tan próximos se encuentran los resultados obtenidos respecto al valor esperado.

La segunda gráfica corresponde a una gráfica de dispersión entre la masa del hielo y el calor latente calculado. Esta representación permite analizar si existe alguna relación entre la cantidad de hielo utilizada y el valor experimental obtenido del calor latente.

La tercera gráfica es un diagrama de barras que compara el valor teórico del calor latente con cada una de las mediciones experimentales y con el promedio obtenido. Esta gráfica resulta útil para visualizar rápidamente la diferencia entre los resultados experimentales y el valor aceptado teóricamente.

La cuarta gráfica representa el porcentaje de error asociado a cada medición experimental mediante un gráfico de barras. Esto permite identificar cuál medición presentó mayor desviación respecto al valor teórico.

Finalmente, la quinta gráfica corresponde a una gráfica de dispersión entre la temperatura final y la masa de hielo utilizada en cada experimento. Esta representación ayuda a estudiar posibles relaciones entre ambas variables físicas.

Desde el punto de vista computacional, este bloque de código constituye un ejemplo de aplicación de programación orientada a objetos en el análisis experimental de datos físicos. El uso de herencia y clases abstractas permite reutilizar código, evitar redundancias y organizar mejor las funciones de graficación.

Además, el empleo de matplotlib facilita la interpretación visual de los resultados experimentales, permitiendo comparar tendencias, detectar posibles anomalías y evaluar la calidad de las mediciones realizadas.

En conjunto, este bloque complementa el análisis numérico desarrollado anteriormente, proporcionando herramientas visuales fundamentales para interpretar experimentalmente el comportamiento del calor latente de fusión del hielo y la precisión de las mediciones efectuadas en laboratorio.
# Bloque 3 — Curva de calentamiento del agua

Este bloque de código tiene como objetivo representar gráficamente la curva de calentamiento del agua utilizando la biblioteca matplotlib. La gráfica muestra cómo varía la temperatura del sistema en función de la energía térmica suministrada, permitiendo visualizar tanto las regiones de calentamiento como los cambios de fase del agua.

Inicialmente, el programa importa las bibliotecas necesarias. Se utiliza matplotlib.pyplot para construir y personalizar la gráfica, mientras que NumPy se importa para facilitar operaciones numéricas y manejo de datos.

Posteriormente, se definen los datos experimentales utilizados para construir la curva de calentamiento. El arreglo x representa la energía térmica suministrada al sistema, expresada en joules, mientras que el arreglo y contiene las temperaturas correspondientes en grados Celsius.

Los puntos definidos representan distintas etapas físicas del proceso térmico del agua:

* Desde A hasta B el hielo aumenta su temperatura desde −30 °C hasta 0 °C.
* Desde B hasta C ocurre la fusión del hielo a temperatura constante.
* Desde C hasta D el agua líquida incrementa su temperatura desde 0 °C hasta 100 °C.
* Desde D hasta E ocurre la vaporización del agua a temperatura constante.
* Finalmente, después de E el vapor continúa aumentando su temperatura.

El código crea luego una figura mediante:

\text{Tamaño de figura }(12,6)

Esto establece un área amplia de visualización que facilita la lectura de las regiones y etiquetas presentes en la gráfica.

Posteriormente, el programa colorea distintas regiones de la gráfica utilizando la función axvspan(). Estas regiones permiten distinguir visualmente cada estado físico y los procesos de cambio de fase.

La región comprendida entre 150 J y 396.7 J se colorea de azul claro y representa la coexistencia de hielo y agua durante el proceso de fusión. En esta etapa, la energía suministrada no aumenta la temperatura, sino que se utiliza para romper parcialmente los enlaces intermoleculares del sólido.

La región entre 396.7 J y 815.7 J se colorea de verde claro y corresponde al calentamiento del agua líquida. En esta etapa, el incremento de energía produce un aumento progresivo de la temperatura.

Posteriormente, la región entre 815.7 J y 3076 J se colorea de naranja claro y representa el proceso de vaporización, donde el agua líquida y el vapor coexisten simultáneamente. Durante esta transición, la temperatura permanece constante mientras la energía absorbida se emplea en vencer las fuerzas intermoleculares.

Después de definir las regiones coloreadas, el código construye la curva principal utilizando la función plot(). Esta línea representa la evolución de la temperatura conforme aumenta la energía térmica suministrada al sistema.

La gráfica incluye además puntos experimentales identificados mediante las letras A, B, C, D y E. Estos puntos se representan con scatter() y corresponden a las etapas más importantes del proceso térmico.

Cada punto es etiquetado utilizando la función text(), permitiendo identificar claramente las transiciones físicas del sistema. Las etiquetas se desplazan ligeramente respecto a los puntos para evitar superposición visual y mejorar la legibilidad de la figura.

Posteriormente, el código dibuja líneas verticales punteadas mediante axvline(). Estas líneas sirven como referencias visuales que delimitan los cambios de fase y las regiones de calentamiento presentes en la curva.

El programa también incorpora textos descriptivos dentro de la gráfica para identificar cada región física:

* Hielo
* Hielo + agua
* Agua
* Agua + vapor
* Vapor

Estas anotaciones ayudan a interpretar físicamente cada segmento de la curva y facilitan la comprensión del comportamiento térmico del agua.

Luego se configuran los ejes de la gráfica. El eje horizontal representa la energía térmica suministrada al sistema, expresada en joules, mientras que el eje vertical representa la temperatura en grados Celsius.

También se establecen límites personalizados para ambos ejes mediante xlim() y ylim(). Esto permite centrar adecuadamente la información y mejorar la presentación visual de la gráfica.

Posteriormente, el programa personaliza las marcas de los ejes mediante xticks() y yticks(). Las marcas seleccionadas corresponden específicamente a los puntos de transición más relevantes del sistema, facilitando la interpretación cuantitativa de la gráfica.

El código activa además una cuadrícula tenue utilizando grid(alpha=0.3). La cuadrícula permite visualizar con mayor precisión la posición relativa de los puntos y regiones dentro de la gráfica.

Finalmente, se agrega una leyenda descriptiva en la parte inferior de la figura mediante figtext(). Esta descripción actúa como pie de figura y explica que la gráfica representa la curva de calentamiento del agua y sus cambios de fase, indicando además la referencia bibliográfica utilizada.

Desde el punto de vista físico, esta gráfica constituye una representación fundamental de la termodinámica del agua. Permite observar claramente que durante los cambios de fase la temperatura permanece constante a pesar de que el sistema continúa absorbiendo energía térmica.

Esto ocurre porque la energía suministrada se emplea en modificar la estructura molecular del sistema, rompiendo enlaces intermoleculares en lugar de incrementar la energía cinética promedio de las moléculas.

En conjunto, este bloque de código permite construir una representación visual clara y detallada del comportamiento térmico del agua, integrando conceptos de calor específico, calor latente y cambios de fase mediante herramientas de programación científica en Python.
# Bloque 4 — Simulación molecular del agua y cambios de fase usando tkinter

Este bloque de código tiene como objetivo construir una simulación interactiva del comportamiento molecular del agua durante sus cambios de fase utilizando programación gráfica en Python. La simulación representa visualmente el movimiento de las moléculas de agua en estado sólido, líquido y gaseoso, permitiendo observar cómo cambia la movilidad molecular conforme varía la temperatura del sistema.

El programa utiliza la biblioteca tkinter, la cual forma parte de la librería estándar de Python y permite crear interfaces gráficas de usuario sin necesidad de instalar paquetes adicionales. También se importan las bibliotecas math y random. La biblioteca math se emplea para realizar operaciones matemáticas y trigonométricas relacionadas con el movimiento molecular, mientras que random introduce variaciones aleatorias en las velocidades y orientaciones de las moléculas para simular el comportamiento térmico natural.

Inicialmente, el código define una sección de configuración general donde se establecen las dimensiones de la ventana principal y del área de simulación. Variables como WIDTH y HEIGHT controlan el tamaño total de la interfaz gráfica, mientras que SIM_X, SIM_Y, SIM_W y SIM_H delimitan la región donde se dibujarán las moléculas.

También se define el número de columnas y filas de moléculas mediante:

\text{COLS}=6,\quad \text{ROWS}=4

Esto determina la cantidad inicial de moléculas presentes en la simulación.

Además, el programa establece la velocidad de actualización de la animación mediante:

FPS_{MS}=16

Este valor corresponde aproximadamente a 60 cuadros por segundo, lo que permite una animación fluida del movimiento molecular.

Posteriormente, el código define múltiples diccionarios de colores utilizados para representar visualmente cada estado físico del agua. Por ejemplo, el oxígeno adopta colores distintos dependiendo de la fase:

* Verde para el hielo.
* Azul para el agua líquida.
* Naranja para el vapor.

Asimismo, se definen colores para los átomos de hidrógeno, enlaces intermoleculares, fondos degradados y elementos decorativos de la interfaz.

Luego se construye el diccionario PHASE_DATA, el cual almacena toda la información asociada a cada fase del agua. Para cada estado físico se incluyen:

* Nombre de la fase.
* Etiqueta visual.
* Nivel de movilidad molecular.
* Distancia promedio entre moléculas.
* Energía cinética relativa.
* Descripción física detallada.

Este diccionario funciona como una base de datos que permite actualizar automáticamente la interfaz cuando cambia la temperatura.

Después se definen funciones auxiliares importantes. Las funciones hex_to_rgb() y rgb_to_hex() permiten convertir colores entre formato hexadecimal y formato RGB. Esto es necesario para generar los degradados de color utilizados en el fondo de la simulación.

Posteriormente se define la función get_phase(), encargada de determinar el estado físico del agua según la temperatura actual del sistema. La lógica implementada establece:

T<0\rightarrow \text{sólido} \quad ; \quad 0\leq T<100\rightarrow \text{líquido} \quad ; \quad T\geq100\rightarrow \text{gas}

Esta función resulta fundamental porque controla el comportamiento dinámico de toda la simulación.

Luego se define la clase Molecule, encargada de representar individualmente cada molécula de agua. Cada objeto de esta clase almacena:

* Posición base.
* Posición actual.
* Velocidades horizontales y verticales.
* Ángulo de rotación molecular.
* Velocidad angular.
* Fila y columna dentro de la estructura molecular.

En el constructor **init**() se asignan valores iniciales aleatorios a las velocidades y orientaciones moleculares. Esto evita que todas las moléculas se comporten exactamente igual y hace la simulación más realista.

La función más importante de esta clase es update(), la cual actualiza continuamente el movimiento de cada molécula según la fase física y la temperatura del sistema.

Cuando el agua se encuentra en estado sólido, las moléculas presentan:

* poca agitación térmica,
* fuerte atracción intermolecular,
* movimiento principalmente vibracional.

Esto se implementa utilizando pequeños valores de vibración aleatoria llamados jitter, junto con una fuerza de atracción alta y un amortiguamiento considerable.

En estado líquido, las moléculas poseen mayor libertad de movimiento. Por ello, el código incrementa la agitación térmica y reduce la fuerza de atracción intermolecular. Esto permite que las moléculas fluyan y se desplacen parcialmente dentro del recipiente.

En estado gaseoso, la energía cinética es mucho mayor. El programa aumenta significativamente la velocidad aleatoria y elimina prácticamente la atracción entre moléculas. Como resultado, las partículas se dispersan libremente dentro del área de simulación.

El código también implementa colisiones con los bordes de la región de simulación. Cuando una molécula alcanza un límite, su velocidad cambia de dirección simulando un rebote elástico parcial.

Posteriormente se define la clase principal App, encargada de administrar toda la interfaz gráfica y la simulación completa.

En el constructor **init**() se crea la ventana principal utilizando tkinter. También se construye un lienzo gráfico o Canvas, donde serán dibujadas todas las moléculas, textos y elementos visuales de la simulación.

Dentro de esta clase se inicializan variables relacionadas con la temperatura y el control del slider interactivo. El usuario puede modificar la temperatura arrastrando el control deslizante, lo que produce cambios inmediatos en el comportamiento molecular.

La función _init_molecules() genera todas las moléculas iniciales organizándolas en una red similar a la estructura del hielo. Las posiciones se calculan utilizando separaciones horizontales y verticales uniformes.

La función _build_static() construye todos los elementos estáticos de la interfaz gráfica, incluyendo:

* fondo principal,
* títulos,
* barra de temperatura,
* leyendas,
* tarjetas informativas,
* regiones descriptivas.

Posteriormente, la función _build_dynamic() crea los elementos dinámicos que cambiarán continuamente durante la simulación, como:

* indicador de temperatura,
* color del slider,
* nombre de la fase,
* textos descriptivos,
* valores físicos asociados.

La función _update_ui() actualiza automáticamente todos los componentes visuales cuando cambia la temperatura. Dependiendo de la fase física actual, el programa modifica:

* colores,
* textos,
* descripciones,
* indicadores visuales,
* información termodinámica.

Una de las funciones más importantes es _draw_sim(), encargada de dibujar toda la simulación molecular.

Primero se genera un fondo con degradado de color dependiendo del estado físico. Luego se dibujan los enlaces de hidrógeno entre moléculas cercanas mediante líneas punteadas.

El programa calcula la distancia entre moléculas utilizando:

genui{"math_block_widget_always_prefetch_v2":{"content":"d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}"}}

Si la distancia es menor que un valor umbral, se dibuja un enlace de hidrógeno entre ambas moléculas.

Posteriormente, el código representa gráficamente cada molécula de agua utilizando:

* un átomo de oxígeno central,
* dos átomos de hidrógeno,
* enlaces covalentes,
* rotación molecular.

La orientación de los hidrógenos se calcula mediante funciones trigonométricas utilizando ángulos moleculares.

El programa también incorpora eventos interactivos del mouse. Las funciones _on_press(), _on_drag() y _on_release() permiten controlar el slider de temperatura mediante arrastre del cursor.

Finalmente, la función _animate() constituye el núcleo de la simulación. Esta función se ejecuta continuamente utilizando:

\text{root.after}(FPS_{MS},\ \text{animate})

En cada iteración se actualizan las posiciones moleculares, se recalculan los enlaces y se redibuja toda la interfaz gráfica, generando así una animación continua y dinámica.

Desde el punto de vista físico, esta simulación representa de forma cualitativa el comportamiento microscópico del agua durante sus cambios de fase. Aunque no constituye una simulación molecular exacta basada en dinámica molecular real, reproduce correctamente varios fenómenos físicos importantes:

* vibración molecular en sólidos,
* movilidad parcial en líquidos,
* dispersión molecular en gases,
* enlaces de hidrógeno,
* incremento de energía cinética con la temperatura.

En conjunto, este bloque integra conceptos de física, termodinámica, química molecular, programación orientada a objetos, animación computacional e interfaces gráficas, permitiendo construir una herramienta educativa interactiva para visualizar el comportamiento molecular del agua durante sus cambios de fase.

CÓMO INSTALAR PANDAS
PASO 1 — Abrir la terminal en Visual Studio Code

Terminal → New Terminal
PASO 2 — Verificar Python

Escribe esto y presiona ENTER:

python --version

Si no funciona escribe:

py --version
PASO 3 — Instalar pandas

Escribe esto y presiona ENTER:

pip install pandas

Si aparece error escribe:

python -m pip install pandas

o también:

py -m pip install pandas

IMPORTANTE:
sys NO se instala.

Solo se usa así dentro del código:

import sys





