# TrabajoEDP

## Índice
1) [Introducción](#1)
2) [Contexto histórico](#2)
3) [Clasificación de EDPs](#3)
4) [Casos particulares](#4)
5) [Ejercicios resueltos](#5)
    - [Ecuación de ondas](#6)
    - [Ecuación del calor](#7)
    - [Ecuación de Laplace](#8)

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
\frac{\partial ^2 u}{\partial t^2} = a^2\frac{\partial ^2 u}{\partial x^2}
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

### Ejemplo EDP de onda<a name="6"></a>
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
\frac{\partial u}{\partial t}(x,0) = 0  && \text{0&le;x&le;4}
\end{array}
\right.
$$

Y la siguiente condición inicial:

$$
\begin{align}
u(x,0) = 2sen(πx)
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
u(4,t) = X(4)T(t) = 0 \implies X(4) = 0\\
\frac{\partial u}{\partial t}(x,0) = X(x)T´(0) = 0 \implies T´(0) = 0
\end{aligned}
$$

Este paso nos asegura que la variable $x$ es la variable espacial, y por tanto aplicaremos el problema de Sturm-Liouville a su EDO para encontrar soluciones que satisfagan las condiciones de contorno (que no sean las triviales).

Buscamos una solución de la forma exponencial (EDO de coeficientes constantes) que es problema de Sturm-Liouville:

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
X(x) = C_{1}sen(x\sqrt{|\lambda|}) + C_{2}cos(x\sqrt{|\lambda|})
$$

Aplicamos las condiciones de contorno:

$$
\left\lbrace
\begin{aligned}
X(0) = C_{2} = 0\\
X(4) = C_{1}sen(4\sqrt{|\lambda|}) + C_{2}cos(4\sqrt{|\lambda|}) = 0 
\end{aligned}
\right. \implies C_{1}sen(4\sqrt{|\lambda|}) = 0 \implies sen(4\sqrt{|\lambda|}) = 0
$$

$$
\implies 4\sqrt{|\lambda|} = nπ \ ;\text{$n\in \mathbb{Z}$}
$$

$$
\begin{array}{ll}
\implies \lambda = -(n^2π^2)/16 && \text{$n = 1,2,3,...$}
\end{array}
$$

Obteniendo así n autofunciones solución de nuestra EDO. Estas autofuciones $X_{n}(x)$ forman una base ortogonal de un espacio vectorial de dimensión infinita, cuyo producto escalar se define como: 

$$
\begin{aligned}
⟨f, g⟩ = ∫_a^b f(x)g(x)w(x)dx
\end{aligned}
$$

Donde $w(x)$ es el peso y se calcula:

$$
w(x) = \frac{a_{2}}{a_{1}} w´(x)
$$

En nuestro caso:

$$
\begin{array}{ll}
w´(x) = 0 \implies w(x) = cte && \text{como por ejemplo: $w(x) = 1$}
\end{array}
$$

Para que la base de autofunciones sea lo más fácil de manejar posible, la normalizamos para que sea ortonormal.

$$
||X_{n}||^2 = ⟨X_{n}, X_{n}⟩ = ∫_0^4 X_{n}^2(x)dx = ∫_0^4 sen^2(\frac{nπx}{4})dx = ∫_0^4 \frac{1-cos(\frac{nπx}{2})}{2}dx = 
$$

$$
= \frac{x}{2} - \frac{sen(\frac{nπx}{2})}{4nπ}]_0^4 = 2 
$$

$$
\implies ||X_{n}|| = \sqrt{2}
$$

$$
φ_{n} = \frac{1}{\sqrt{2}} \sum_{n=1}^{\infty}sen(\frac{nπx}{4})
$$

Ahora, resolvemos la EDO que nos quedó por resolver:

$$
T´´= 9\lambda T
$$

Como sabemos el valor de $\lambda$ lo sustituimos:

$$
T´´= -\frac{9n^2π^2}{16}T
$$

La solución a esta EDO la podemos expresar como suma de senos y cosenos:

$$
T_{n}(t) = C_{1}sen(\frac{3nπt}{4}) + C_{2}cos(\frac{3nπt}{4})
$$

Aplicamos la ccondición de contorno:

$$
\frac{\partial u}{\partial t}(x,t) = \frac{3nπ}{4}[C_{1}cos(\frac{3nπx}{4}) -C_{2}sen(\frac{3nπx}{4})] \implies
$$

$$
\implies \frac{\partial u}{\partial t}(x,0) = C_{1}\frac{3nπ}{4}cos(0) = 0 \implies C_{1} = 0
$$

Entonces:

$$
T_{n}(t) = cos(\frac{3nπt}{4})
$$

Para tener una solución más general:

$$
T(t) = \sum_{n=1}^{\infty}cos(\frac{3nπt}{4})
$$

Por lo tanto la solución del problema quedaría así:

$$
u(x,t) = \frac{1}{\sqrt{2}}\sum_{n=1}^{\infty}C_{n}sen(\frac{nπx}{4})cos(\frac{3nπt}{4})
$$

Nos queda calcular los coeficientes $C_{n}$. Para ello usaremos las condiciones inciales:

$$
u(x,0) = \frac{1}{\sqrt{2}}\sum_{n=1}^{\infty}C_{n}sen(\frac{nπx}{4}) = 2sen(πx)
$$

$$
u(x,0) = \sum_{n=1}^{\infty}C_{n}\frac{1}{2\sqrt{2}}sen(\frac{nπx}{4}) = sen(πx)
$$

Es decir, lo podemos reescribir como:

$$
u(x,0) = \sum_{n=1}^{\infty}\frac{1}{2}C_{n}φ_{n}(x) = sen(πx)
$$

Si tomamos a $sen(πx)$ como un vector, los coeficientes $\frac{C_{n}}{2}$ son las coordenadas de dicho vector en la base ortonormal que forman las $φ_{n}(x)$. Entoces: 

$$
\frac{C_{n}}{2} = ⟨φ_{n}(x), sen(πx)⟩ = \frac{1}{\sqrt{2}}∫_{0}^{4}sen(\frac{nπx}{4})sen(πx)dx
$$

En este caso es suficiente comparar términos para obtener los coeficientes, ya que todos se anulan, menos en $n = 4$:

$$
C_{4} = 2
$$

Es decir, que la solución a nuestro problema es:

$$
u(x,t) = 2sen(\frac{nπx}{4})cos(\frac{3nπt}{4})
$$

Gráficamente la función obtenida representa la vibración de una cuerda a lo largo del tiempo, es decir, como va cambiando su forma a lo largo del tiempo aplicando las condiciones iniciales y de contorno del problema. Se vería así:

<p align="center">
    <img src="https://user-images.githubusercontent.com/91721764/236179258-cb7e51d4-3536-4dac-94c2-5b5ae24de233.gif" alt="Solución gráfica" width="300" height="300">


### Ejemplo EDP del calor<a name="7"></a>
Resolver la siguiente EDP:

$$
\frac{\partial u}{\partial t} = 4\frac{\partial^2 u}{\partial x^2}
$$

Con las condiciones de frontera siguientes:

$$
u(0,t) = u(2,t) = 0
$$

Y la siguiente condición inicial: 

$$
u(x,0) = x^2(2-x)
$$

Lo primero analizamos las variables: vemos que la variable espacial la representa la variable $x$ y la temporal la $t$. Lo verificaremos más adelante.

Aplicamos el método de separación de variables: buscamos una solución de la forma:

$$
u(x,t) = X(x)T(t)
$$

Calculamos las derivadas que necesitamos:

$$
\frac{\partial u}{\partial t} = XT´
\frac{\partial u}{\partial x} = X´T \implies \frac{\partial^2 u}{\partial x^2} = X´´T
$$

Y sustituimos en la EDP inicial:

$$
XT´= 4X´´T \implies \frac{T´}{4T} = \frac{X´´}{X} = \lambda
$$

Efectivamente vemos que este es un problema de separación de variables, y será la variable $x$ a la que le aplicaremos el Problema de Sturm-Liouville. Obteniendo dos EDOs:

$$
\left\lbrace
\begin{aligned}
X´´ = \lambda X\\
T´ = 4\lambda T
\end{aligned}
\right.
$$

Aplicamos las condiciones de contorno:

$$
\left\lbrace
\begin{aligned}
u(0,t) = X(0)T(t) = 0 \implies X(0) = 0\\
u(2,t) = X(2)T(t) = 0 \implies X(2) = 0
\end{aligned}
\right.
$$

Problema de Sturm-Liouville:

Buscamos soluciones a la EDO de coeficientes constantes, es decir:

$$
m^2 = \lambda \implies m = \pm \sqrt{\lambda}
$$

Dependiendo del valor de $\lambda$ podemos obtener 3 casos:

1) __Caso 1:__ $\lambda > 0$:
La solución sería una suma de funciones exponenciales:

$$
X(x) = C_{1}e^x\sqrt{\lambda} + C_{2}e^-x\sqrt{\lambda}
$$

Aplicamos las condiciones iniciales:

$$
\left\lbrace
\begin{aligned}
X(0) = C_{1} + C_{2} = 0\\
X(2) = C_{1}e^2\sqrt{\lambda} + C_{2}e^-2\sqrt{\lambda} = 0
\end{aligned}
\right.
$$

Para calcular los coeficientes $C_{1}$ y $C_{2}$ resolvemos el siguiente determinante:

$$
\begin{vmatrix}
1 & 1 \\
e^{2\sqrt{\lambda}} & e^{-2\sqrt{\lambda}}
\end{vmatrix} = e^{-2\sqrt{\lambda}} - e^{2\sqrt{\lambda}} = 0
$$

Operando:

$$
\frac{^{2\sqrt{\lambda}} - e^{-2\sqrt{\lambda}}}{2} = 0 \implies senh(2\sqrt{\lambda}) = 0 \implies \lambda = 0
$$

LLegando a una contradicción, es decir, que la única solución que hay para $\lambda > 0$ es la trivial.

$$
C_{1} = C_{2} = 0
$$

2) __Caso 2:__ $\lambda = 0$:
La solución es:

$$
X(x) = C_{1}x + C_{2}
$$

Aplicamos las condiciones iniciales:

$$
\left\lbrace
\begin{aligned}
X(0) = C_{2} = 0\\
X(2)V = 2C_{1} = 0
\end{aligned}
\right. \implies C_{1} = C_{2} = 0
$$

3) __Caso 3:__ $\lambda < 0$:
La solución es una suma de exponenciales que podemos expresar también como suma de senos y cosenos:

$$
X(x) = C_{1}sen(\sqrt{|\lambda|}x) + C_{2}cos(\sqrt{|\lambda|}x)
$$

Aplicamos las condiciones iniciales: 

$$
\left\lbrace
\begin{aligned}
X(0) = C_{2} = 0\\
X(2) = C_{1}sen(2\sqrt{|\lambda|}) = 0
\end{aligned}
\right. 
$$

$$
\begin{array}{ll}
\implies sen(2\sqrt{|\lambda|}) = 0 \implies 2\sqrt{|\lambda|} = nπ && \text{$n \in \mathbb{Z}$}
\end{array}
$$

$$
\begin{array}{ll}
\implies \lambda = -\frac{n^2π^2}{4} && \text{$n=1,2,3,...$}
\end{array}
$$

Por lo tanto obtenemos que:

$$
X_{n} = sen(\frac{nπx}{2})
$$

Donde cada autofunción $X_{n}$ forman una base ortogonal de un espacio vectorial de dimensión infinita donde el producto vectorial es: 

$$
\begin{aligned}
⟨f, g⟩ = ∫_a^b f(x)g(x)w(x)dx
\end{aligned}
$$

Donde $w(x)$ es el peso y se calcula:

$$
w(x) = \frac{a_{2}}{a_{1}} w´(x)
$$

Donde $w(x)$ es:

$$
w´(x) = 0 \implies w(x) = cte = 1
$$

Normalizamos la base de autofunciones dividiendo por su norma:

$$
||X_{n}(x)||^2 = ⟨X_{n}, X_{n}⟩ = ∫_0^2 sen^2(\frac{nπx}{2})dx = ∫_0^2 \frac{1-cos(nπx)}{2}dx = \frac{x}{2} + \frac{sen(nπx)}{2nπ}]_0^2
$$

$$
||X_{n}(x)||^2 = ⟨X_{n}, X_{n}⟩ = 1 \implies ||X_{n}(x)|| = 1
$$

Nuestra base ortonormal de autofunciones es:

$$
φ_{n} = sen(\frac{nπx}{2})
$$

Resolvemos la otra EDO de coeficientes constantes:

$$
T´ = 4\lambda T
$$

$$
m = 4\lambda \implies m = -n^2π^2
$$

Luego la solución a esta EDO es:

$$
T(t) = C_{1}e^{-n^2π^2t}
$$

Entonces la solución a nuestra EDP es:

$$
u_{n}(x,t) = C_{n}sen(\frac{nπx}{2})e^{-n^2π^2t}
$$

Para tener una solución más general:

$$
u(x,t) = \sum_{n=1}^{\infty}C_{n}sen(\frac{nπx}{2})e^{-n^2π^2t}
$$

Solo nos queda calcular los coeficientes $C_{n}$ y que la función resultante cumpla nuestra condición inicial:

$$
\begin{aligned}
u(x,0) = \sum_{n=1}^{\infty}C_{n}sen(\frac{nπx}{2}) = x^2(2-x)\\
u(x,0) = \sum_{n=1}^{\infty}C_{n}φ_{n} = \vec{v}
\end{aligned}
$$

Analizando esta igualdad vemos que los coeficientes $C_{n}$ son las coordenadas del vector $\vec{v}$ en la base $φ_{n}$, es decir:

$$
C_{n} = ⟨φ_{n}, x^2(2-x)⟩ = ∫_0^2 sen(\frac{nπx}{2})x^2(2-x)dx
$$

Aplicando tres veces integración por partes obtenemos que:

$$
C_{n} = \frac{-32}{n^3π^3}[2(-1)^n + 1]
$$

Finalmente tenemos que la solución a nuestro problema es la siguiente:

$$
u(x,t) = \sum_{n=1}^{\infty}\frac{-32}{n^3π^3}[2(-1)^n + 1]sen(\frac{nπx}{2})e^{-n^2π^2t}
$$

Gráficamente la solución se representa de la siguiente manera:

<p align="center">
<img width="694" alt="Captura de pantalla 2023-05-06 a las 23 43 14" src="https://user-images.githubusercontent.com/91721764/236861272-6c031f50-8088-45a8-9637-c4a6525953a2.png" alt="Solución gráfica" width="300" height="300">





