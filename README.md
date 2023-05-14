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
Los orígenes de las EDP se remontan a los siglos XVII y XVIII, cuando los matemáticos empezaron a trabajar en el cálculo de variaciones y en la formulación de leyes físicas en términos matemáticos.

Uno de los primeros avances significativos en la teoría de las EDP fue realizado por el matemático francés Jean le Rond d'Alembert, quien en 1747 publicó un artículo que establecía la ecuación de onda para describir la propagación de ondas en una cuerda tensa. Más tarde, en la segunda mitad del siglo XIX, el matemático francés Joseph Fourier introdujo la transformada de Fourier, una técnica poderosa para resolver ecuaciones diferenciales parciales.

En el siglo XX, las EDP se convirtieron en un área activa de investigación en matemáticas aplicadas y se utilizaron ampliamente en la física y la ingeniería. Las ecuaciones diferenciales parciales han sido fundamentales para entender fenómenos como la propagación de ondas sísmicas, el flujo de fluidos, la difusión de calor y la dinámica de los campos electromagnéticos. La investigación en EDP continúa siendo un área de gran interés en la actualidad, y las nuevas técnicas y herramientas matemáticas han permitido la formulación y resolución de ecuaciones cada vez más complejas.

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
φ_{n}(x) = sen(\frac{nπx}{2})
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
<img width="694" alt="Captura de pantalla 2023-05-06 a las 23 43 14" src="https://user-images.githubusercontent.com/91721764/236861272-6c031f50-8088-45a8-9637-c4a6525953a2.png" alt="Solución gráfica">

 
### Ejemplo EDP de Laplace<a name="8"></a>

Resolver la siguiente EDP:
    
$$
\frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0
$$

Con las siguientes condiciones:

$$
\left\lbrace
\begin{aligned}
u(x,0) = u(x,π) = 0\\
u(0,y) = u(π,y) = y
\end{aligned}
\right.
$$

Lo primero es comprobar si es un problema de separación de variables, para ello buscamos soluciones de la forma:

$$
u(x,y) = X(x)Y(y)
$$

Calculamos las derivadas, sustituimos en la ecuación original y vemos si las dos variables $x$ e $y$ se pueden separar una a cada lado de la ecuación.
	
$$
\left\lbrace
\begin{aligned}
\frac{\partial u}{\partial x} = X´Y \implies \frac{\partial^2 u}{\partial x^2} = X´´Y\\
\frac{\partial u}{\partial y} = XY´ \implies \frac{\partial^2 u}{\partial y^2} = XY´´\\
\end{aligned}
\right.
$$

Sustituyendo:
	
$$
X´´Y + XY´´= 0 \implies X´´Y = -XY´´ \implies \frac{X´´}{X} = -\frac{Y´´}{Y} = \lambda
$$

Sí es un problema de separación de variables, y tenemos el siguiente sistema de EDOs:
	
$$
\left\lbrace
\begin{aligned}
X´´= \lambda X\\
Y´´= -\lambda Y
\end{aligned}
\right.
$$

Aplicando las condiciones:
	
$$
\left\lbrace
\begin{aligned}
u(x,0) = X(x)Y(0) = 0 \implies Y(0) = 0\\
u(x,π) = X(x)Y(π) = 0 \implies Y(π) = 0
\end{aligned}
\right.
$$
	
Esto nos determina que el problema de Sturm-Liouville hay que aplicarlo a la variable $y$:	

Problema de Sturm-Liouville:

Tenemos una EDO de coeficientes constantes, por lo que buscamos soluciones exponenciales:

$$
m^2 = -\lambda \implies m = \pm\sqrt{-\lambda}
$$	

1) __Caso 1:__ $-\lambda = 0$:

La solución es trivial:

$$	
Y(y) = C_{1}y + C_{2}
$$

Aplicamos las condiciones de frontera:
	
$$
\left\lbrace
\begin{aligned}
Y(0) = C_{2} = 0\\
Y(π) = πC_{1} = 0
\end{aligned}
\right. \implies C_{1} = C_{2} = 0
$$

2) __Caso 2:__ $-\lambda > 0$:

La solución es una suma de fuciones hiperbólicas:
														
$$														 
Y(y) = C_{1}cosh(\sqrt{|\lambda|}x) + C_{2}senh(\sqrt{|\lambda|}x)													
$$
														 
Aplicando las condiciones de contorno:
	
$$
\left\lbrace
\begin{aligned}														 
Y(0) = C_{1}cosh(0) = 0 \implies C_{1} = 0\\
Y(π) = C_{2}senh(\sqrt{|\lambda|}π) = 0  \lambda = 0
\end{aligned}
\right. \implies C_{1} = C_{2} = 0
$$
	
3) __Caso 3:__ $-\lambda < 0$:

Nos queda:

$$
\begin{array}{ll}
Y´´= -\lambda Y && \text{$\lambda > 0$}
\end{array}
$$

Entonces, la solución es una suma de senos y cosenos:
  
$$
Y(y) = C_{1}sen(\sqrt{\lambda}x) + C_{2}cos(\sqrt{\lambda}x)  
$$

Aplicamos las condiciones de contorno:
  
$$
\left\lbrace
\begin{aligned}			
Y(0) = C_{2} = 0\\
Y(π) = C_{1}sen(\sqrt{\lambda}π) = 0
\end{aligned}
\right.
$$

$$
\begin{array}{ll}
\sqrt{\lambda}π = nπ && \text{$n \in \mathbb{Z}$}
\end{array}
$$
  
$$
\begin{array}{ll}
\implies \lambda = n^2 && \text{$n=1,2,3...$}
\end{array}
$$

Luego la solución es:

$$
Y_{n}(y) = sen(ny)
$$

Obteniendo así n autofunciones que forman una base ortogonal de un espacio vectorial infinito dimensional, cuyo producto escalar viene definido por:

$$
\begin{aligned}
⟨f, g⟩ = ∫_a^b f(y)g(y)w(y)dy
\end{aligned}
$$

Donde el peso $w(y)$ es:

$$
w´(y) = 0 \implies w(y) = cte \implies w(y) = 1
$$

Normalizamos la base:

$$
||Y_{n}||^2 = ⟨Y_{n}, Y_{n}⟩ = ∫_0^π sen^2(ny)dy = ∫_0^π \frac{1 - cos(2ny)}{2}dy = \frac{y}{2} - \frac{sen(2ny)}{4n}]_0^π
$$

$$
\implies ||Y_{n}||^2 = \frac{π}{2} \implies ||Y_{n}|| = \sqrt{\frac{π}{2}}
$$

Luego:
$$
φ_{n}(y) = \sqrt{\frac{π}{2}}sen(ny)

Resolvemos la otra EDO:

$$
X´´= \lambda X \implies X´´= n^2X
$$

Entonces:

$$
X(x) = C_{1}senh(nx) + C_{2}cosh(nx)
$$

De momento lo dejaremos así.

Agrupando el producto de ambas soluciónes obtenemos la solución $u(x,y)$:

$$
u_{n}(x,y) = \sqrt{\frac{π}{2}}sen(ny)[A_{n}senh(nx) + B_{n}cosh(nx)]
$$

Entonces:

$$
u(x,y) = \sum_{n=0}^{\infty}\sqrt{\frac{π}{2}}sen(ny)[A_{n}senh(nx) + B_{n}cosh(nx)]
$$

Aplicando las condiciones iniciales:

$$
u(0,y) = \sum_{n=0}^{\infty}B_{n}\sqrt{\frac{π}{2}}sen(ny) = y
$$

Que no es más que el producto escalar de $y$ con $φ_{n}(y)$ donde $B_{n}$ son las coordenadas de $y$ en la base formada por $φ_{n}(y)$:

$$
B_{n} = ∫_0^π \sqrt{\frac{π}{2}}sen(ny)ydy 
$$

Resolviendo por partes obtenemos que:

$$
B_{n} = -\frac{π}{n}cos(nπ) = \frac{π(-1)^{n+1}}{n}
$$

Aplicamos la otra condición inicial:

$$
u(π,y) = \sum_{n=0}^{\infty}\sqrt{\frac{π}{2}}sen(ny)[A_{n}senh(nπ) + B_{n}cosh(nπ)] = y
$$

Tomando:

$$
C_{n} = [A_{n}senh(nπ) + B_{n}cosh(nπ)]
$$

Tenemos otra vez:

$$
u(π,y) = \sum_{n=0}^{\infty}C_{n}\sqrt{\frac{π}{2}}sen(ny) = y
$$

Que es el mismo producto escalar de antes, pero con $C_{n}$ de coordenadas:

$$
C_{n} = \frac{π(-1)^{n+1}}{n}
$$

Entonces:

$$
\frac{π(-1)^{n+1}}{n} = [A_{n}senh(nπ) + \frac{π(-1)^{n+1}}{n}cosh(nπ)]
$$

Despejando obtenemos que:

$$
A_{n} = \frac{π(-1)^{n+1}[1-cosh(nπ)]}{nsenh(nπ)}
$$

Por último solo falata sustituir $A_{n}$ y $B_{n}$:

$$
u(x,y) = \sum_{n=0}^{\infty}\sqrt{\frac{π}{2}}sen(ny)[\frac{π(-1)^{n+1}[1-cosh(nπ)]}{nsenh(nπ)}senh(nx) + \frac{π(-1)^{n+1}}{n}cosh(nx)]
$$

La ecuación de Laplace describe la distribución estacionaria de temperatura, presión, voltaje u otro fenómeno físico en un medio sin fuentes ni sumideros. Una forma común de visualizar la solución de la ecuación de Laplace es a través de un gráfico tridimensional de la función solución. Veamos como se vería dicho gráfico:

<p align="center">
<img width="654" alt="Captura de pantalla 2023-05-13 a las 19 31 39" src="https://github.com/pelahumi/TrabajoEDP/assets/91721764/02356d16-ac53-4f9f-b5d4-37b4cda3a318">

Podemos observar que las condiciones de contorno forman un cuadrado donde se produce la variación de la solución. Visto en movimiento:

<p align="center">
![Solucion grafica](https://github.com/pelahumi/TrabajoEDP/assets/91721764/605775d1-203c-44c1-bd9a-b181a22a8e52)



