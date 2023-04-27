# TrabajoEDP

## Índice
1) [Introducción](#1)
2) [Contexto histórico](#2)
3) [Clasificación de EDPs](#3)
4) [Casos particulares](#4)
5) [Ejercicios resueltos](#5)

---

## 1. Introducción<a name="1"></a>
En este trabajo de profundización se abarcarán los siguientes temas: la clasificación de ecuaciones en derivadas parciales, así como un ejemplo resuelto de cada una de ellas, con la evaluación correspondiente para cada solución con su gráfica. 

---

## 2. Contexto histórico<a name="2"></a>
Una de los primeros descubrimientos y aportaciones más importantes sobre las ecuaciones de ondas se remonta al siglo XVIII (año 1750 aprox.), cuando el matemático francés  Jean le Rond d'Alembert empezó a trabajar sobre la teoría de vibraciones y de ondas sobre una cuerda tensa. D´Alambret desarrolló una ecuación de ondas para replicar la propagación de las ondas en una cuerda infinita y uniforme.

En el siglo XIX el matemático Augustin Louis Cauchy continuó al desarrollo de las ecuaciones de ondas haciendo grandes aportaciones. Formuló el llamado problema de Cauchy, que consiste en dar una solución que satisfaga la ecuación de ondas, dadas unas condiciones de frontera y condiciones iniciales. Este problema es importante porque ofrece la obtención de unas soluciones más exactas, y lo más importante, en situaciones más generales que las de D´Alambert.

Las EDP de ondas se convirtieron en una herramienta fundamental en la física. Los físicos implementaron dichas ecuaciones para modelar la propagación de ondas electromagnéticas, acústicas y gravitartorias. También se implementaron en el ámbito de la ingeniería para diseñar y optimizar sistemas como antenas, sensores acústicos o dispositivos de comunicación.

En la actualidad se sigue investigando las ecuaciones de ondas en matemáticas y física, y se han desarrollado técnicas más sofisticadas para el cálculo de soluciones, así como comprender mejor su naturaleza. Además, pese a que a muchos les parezca imposible, se han encontrado aplicaciones de las ecuaciones de ondas en otros campos como la medicina (como por ejemplo en la ecografía), la geofísica y la oceanografía, entre otros.

---

## 3. Clasificación de las EDPs<a name="3"></a>

### Ecuación general de las EDPs de segundo orden
Consideremos la siguiente expresión como la ecuación general de las ecuaciones en derivadas parciales:

$$
\begin{aligned}
A(x,y)\frac{\partial^2 u}{\partial x^2} + 2B(x,y)\frac{\partial^2 u}{\partial x \partial y} + C(x,y)\frac{\partial^2 u}{\partial y^2} + a(x,y)\frac{\partial u}{\partial x} + b(x,y)\frac{\partial u}{\partial y} + c(x,y)u(x,y) = f(x,y)
\end{aligned}
$$

Donde la función u(x,y) es la función solución que cumple la iguialdad.

### Clasificación de las EDPs de segundo orden
Una vez presentada la ecuación general de las ecuaciones en derivadas parciales de segundo orden, ya podemos realizar la clasificación de las mismas:
* __Hiperbólicas__: $&Delta; = B^2 -AC > 0$
* __Parabólicas__: $&Delta; = B^2 -AC = 0$
* __Elípticas__: $&Delta; = B^2 -AC < 0$

---
    
## 4. Casos particulares<a name="4"></a>
En este trabajo nos limitaremos a estudiar estos casos particulares de las EDPs de segundo orden.

#### 1. Ecuaciones hiperbólicas (ecuaciones de onda)
Este tipo de ecuaciones representan los fenómenos oscilatorios de diferenete naturaleza como pueden ser: vibraciones de cuerdas o membranas, oscilaciones acústicas de un gas en tubos u oscilaciones electromagnéticas.

La ecuación más simple de las ecuaciones de vibraciones de la cuerda, ecuación ondulatoria unidimensional. En este tipo hay ecuaciones más complejas en las que intervienen fuerzas externas, vibraciones forzadas.

Las ecuaciones de onda más sencillas tienen la siguiente forma:

$$
\begin{aligned}
\frac{\partial ^2}{\partial t^2} = a^2\frac{\partial ^2}{\partial x^2}
\end{aligned}
$$

En este caso la constante $a^2$ representa el cociente siguiente: $\frac{T}{&rho;}$, donde T es la tensión de la cuerda y $&rho;$ es la densidad lineal de la cuerda.

#### 2. Ecuaciones parabólicas (ecuaciones del calor)
Estas ecuaciones representan la conductividad térmica a lo largo de una varilla. La ecuación más simple es la siguiente:

$$
\begin{aligned}
\frac{\partial u}{\partial t} = a^2\frac{\partial u^2}{\partial x^2}
\end{aligned}
$$

En este caso la constante $a^2$ representa el cociente siguiente: $\frac{K}{c&rho;}$, donde la $K$ es el coeficiente de conductividad térmica, la $c$ es el calor específico y $&rho;$ represenata la densidad del medio.

#### 3. Ecuaciones elípticas (ecuaciones de Laplace)
Los procesos a ciclo fijo, cuando la función que buscamos no depende del tiempo, se determinan por las ecuaciones de tipo elíptico, la más común es la ecuación de Laplace, y tienen esta forma:

$$
\begin{aligned}
&Delta;u = \frac{\partial u^2}{\partial x^2} + \frac{\partial u^2}{\partial y^2} = 0
\end{aligned}
$$

## 5. Ejercicios resueltos<a name="5"></a>
Para la resolución de los tres ejercicios utilizaremos el Método de Separación de Variables o también conocido como el Método de Fourier.

Veremos que todos los ejercicioes se resuelven de una manera muy similar, sin embargo los resultados obtenidos nos proporcionarán información muy diferente.

### Ejemplo EDP de onda
Resolver la siguiente EDP:

$$
\begin{aligned}
\frac{\partial u^2}{\partial t^2} = 9\frac{\partial u^2}{\partial x^2}
\end{aligned}
$$

Con las siguientes condiciones de contorno o frontera:

$$
u(x,0) = 2sin(πx)
$$

Y estas condiciones iniciales:

$$
\frac{\partial u}{\partial t}(x,0) = 0 ; 0&le;x&le;4
$$















