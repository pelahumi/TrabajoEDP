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
\left\lbrace
\begin{array}{ll}
u(0,t) = u(4,t) = 0 && \text{t&ge;0}\\
u(x,0) = 2sen(πx)
\end{array}
\right.
$$

Y la siguiente condición inicial:

$$
\begin{align}
\frac{\partial u}{\partial t}(x,0) = 0  && \text{0&le;x&le;4}
\end{align}
$$

Analizando las condiciones de contorno podemos llegar a la conclusión de que la variable $x$ es la variable espacial y representa la longitud de la cuerda. Por otro lado, vemos que la variable $t$ corresponde a la variable temporal representando así el tiempo. Cabe destacar que este análisis previo debería de hacerse siempre, puesto que las variables no se tienen por que llamar $x$ para la variable espacial y $t$ para la temporal, aunque lo más común es que sí que se utilice dicha notación.

Como mencionamos al principio del epígrafe, usaremos el Método de Separación de Variables (MSV) o Método de Fourier para resolver estas ecuaciones. Dicho método consiste en buscar una solución de la forma:

$$
u(x,t) = X(x)T(t)
$$

Una vez propuesta nuestra solución, sustituimos los valores correspondientes en la ecuación inicial:

$$
\begin{aligned}
\frac{\partial u}{\partial x} = X´T \implies \frac{\partial u^2}{\partial x^2} = X´´T\\
\frac{\partial u}{\partial t} = XT´ \implies \frac{\partial u^2}{\partial t^2} = XT´´
\end{aligned}
$$

Sustituyendo en la ecuación inicial:

$$
XT´´ = 9X´´T
$$

Como podemos ver, esta ecuación si que es de variables separadas, ya que podemos separarlas en los dos miembros de la ecuación de la siguiente forma:

$$
\frac{T´´}{9T} = \frac{X´´}{X}
$$

La ecuación reusltante solo puede ser resulta por una constante:

$$
\frac{T´´}{9T} = \frac{X´´}{X} = \lambda
$$

Al igualar cada miembro de la ecuación a la constante obtenemos un sistema de dos ecuaciones diferenciales ordinarias (EDOs):

$$
\left\lbrace
\begin{aligned}
X´´ = \lambda X\\
T´´= 9\lambda T
\end{aligned}
\right.
$$

Aplicamos las condiciones de contorno obtenemos:

$$
\begin{aligned}
u(0,t) = X(0)T(t) = 0 \implies X(0) = 0\\
u(4,t) = X(4)T(t) = 0 \implies X(4) = 0
\end{aligned}
$$

Este paso nos asegura que la variable $x$ es la variable espacial, y por tanto aplicaremos el problema de Sturm-Liouville a su EDO para encontrar soluciones que satisfagan las condiciones de contorno (que no sean las triviales).

Buscamos una solución de la forma exponencial (EDO de coeficientes constantes):

$$
m^2 = \lambda \implies m = \pm \sqrt{\lambda}
$$

Evaluando los diferentes valores que puede tomar $\lambda$ nos podemos encontrar 3 casos:

1) __Caso 1:__ $\lambda > 0$:

Si $\lambda$ es un número positivo, la solución nos quedaría una exponencial de la siguiente forma:
        
$$
\begin{aligned}
u(x,t) = C1e^{x\sqrt{\lambda}} + C2e^{-x\sqrt{\lambda}}
\end{aligned}
$$

Aplicando los resultados que obtuvimos con las condiciones de contorno:

$$
\left\lbrace
\begin{aligned}
X(0) = C1e^{0\sqrt{\lambda}} + C2e^{-0\sqrt{\lambda}} = C1 + C2 = 0\\
X(4) = u(x,t) = C1e^{4\sqrt{\lambda}} + C2e^{-4\sqrt{\lambda}} = 0
\end{aligned}
\right.
$$

Para resolver el sistema basta con calcular el siguiente determinante:

$$
\begin{vmatrix}
1 & 1 \\
e^{4\sqrt{\lambda}} & e^{-4\sqrt{\lambda}}
\end{vmatrix} = e^{-4\sqrt{\lambda}} - e^{4\sqrt{\lambda}} = 0
$$

Haciendo una serie de operaciones obtenemos que:

$$
e^{4\sqrt{\lambda}} - e^{-4\sqrt{\lambda}} = 0 \implies (e^{4\sqrt{\lambda}} - e^{-4\sqrt{\lambda}})/2 = 0 \implies sinh(4\sqrt{\lambda}) = 0 \iff \lambda = 0
$$

LLegamos a una contradicción, ya que teniamos como hipótesis que $\lambda < 0$ y para que exista una solución distinta de la trivial $\lambda = 0$.

2) __Caso 2:__ $\lambda = 0$:

En esta caso la solución sería la siguiente: 

$$
X(x) = C1x + C2
$$

Aplicamos las condiciones de contorno:

$$
\left\lbrace
\begin{aligned}
X(0) = C2 = 0\\
X(4) = 4C1 + C2 = 0
\end{aligned}
\right. \implies C1 = C2 = 0
$$

Obtenemos la solución trivial.

3) __Caso 3:__ $\lambda < 0$:

Resolviendo la EDO de coeficientes constantes:

$$
m = \pm \sqrt{-\lambda} = \pm i\sqrt{|\lambda|}
$$

La solución de la EDO es una exponencial, pero la podemos expresar como suma de senos y cosenos:

$$
X(x) = C1sen(x\sqrt{|\lambda|}) + C2cos(x\sqrt{|\lambda|})
$$

Aplicamos las condiciones de contorno:

$$
\left\lbrace
\begin{aligned}
X(0) = C2 = 0\\
X(4) = C1sen(4\sqrt{|\lambda|}) + C2cos(4\sqrt{|\lambda|}) = 0 
\end{aligned}
\right. \implies C1sen(4\sqrt{|\lambda|}) = 0 \implies sen(4\sqrt{|\lambda|}) = 0 \implies 4\sqrt{|\lambda|} = nπ \ ;\text{$n\in \mathbb{Z}$}
$$

$$
\begin{array}{ll}
\implies \lambda = -(n^2π^2)/16 && \text{$n = 1,2,3,...$}
\end{array}
$$



