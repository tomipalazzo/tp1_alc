---
marp: true
footer: 'Analisis Avanzado'
paginate: true


title: "Un pequeño vistazo a **GRAFOS**"
author: "Ariel Salgado"

---

# Espacios Métricos
<br/><br/>

## Palazzo Tomas Alejandro 
### Analisis Avanzado - FCEN - UBA


---
<style>

.divteo {
   padding-left: 10px;
   border: red 5px solid;
   border-radius: 15px;
}
.h1teo{
   font-size: 45px;
   color: red;
}
.pteo{
   padding-left: 25px;
}
</style>


<script type="text/x-mathjax-config">
  MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});
</script>


![bg right:26%](#ff')


## <span style="color:purple;">Definición</span>
Sea $E$ un conjunto. Una función $d : E × E → \R$ se llama una métrica o una distancia sobre $E$ si se cumple:

1. **Separa Puntos**: $d(x,y)=0 \iff x=y$ 
1. **Simetria**: $d(x,y)=d(y,x)$
1. **Desigualdad Triangular**: $d(x,y) \leq d(x,z) + d(z,y)$  

Al par $(E,d)$ lo llamaremos *espacio métrico*

---
# $\R^n$ y sus distancias mas naturales

Sean $x = (x_1,...,x_n), y=(y_1,...,y_n)$ elementos de $\R^n$  
Definimos la a <span style="color:red;">distancia euclidea</span> como

$$d_2(x,y) = \left( \sum_{i=1}^n (x_i - y_i)^2 \right)^{1/2} = ||x-y||_2$$

La <span style="color:red;">distancia 1</span> como 
$$d_1(x,y) = \sum_{i=1}^n |x_i - y_i|  = ||x-y||_1$$

La <span style="color:red;">distancia infinito</span> como 
$$d_\infty(x,y)= \sup_{i=1...n} |x_i-y_i| = ||x-y||_\infty$$

---

# Distancias entre funciones continuas
Dado un intervalo cerrado $[a,b]\subset \R$, llamamos $C([a,b])$ al conjunto de todas las funciones $f:[a,b] \rightarrow \R$ continuas

La metrica *natural* de este conjunto es:
$$d_\infty(x,y)= \sup_{a \leq t \leq b} |x(t)-y(t)|$$

Otra métrica en $C([a,b])$ es la siguiente:
$$d_1(x,y) = \int_a^b |x(t)-y(t)| dt.$$

---

$d_\infty(x,y)$            |  $d_1(x,y)$
:-------------------------:|:-------------------------:
![](funciones_continuas.png)  |  ![](funciones_continuas.png)

---

# Métrica Discreta
## <span style="color:purple;">Definición</span>
Sea $E$ un conjunto cualquiera. Definimos la <span style="color:red;">Métrica Discreta</span> como:
$$\delta(x,y)=\left\{ \begin{array}{lcc}
             0 &   si  & x = y \\
             \\ 1 &  si  & x \neq y
             \end{array}
   \right.
$$



---

Veamos que $\delta(x,y)$ es una distancia:
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>


---

Veamos que $\delta(x,y)$ es una distancia:
<br/><br/>

$\delta(x,y)=\left\{ \begin{array}{lcc}
             0 &   si  & x = y \\
             \\ 1 &  si  & x \neq y
             \end{array}
   \right.
$

<br/><br/>
<br/><br/>

---

# Topología de espacios métricos

Teniendo en cuenta que $(E,d)$ es un espacio métrico

## <span style="color:purple;">Definición</span>

Dados $x \in E$ y $r > 0$, la <span style="color:red;">bola abierta de centro $x$ y radio $r$ es el conjunto</span>

$$B(x,r) = \{ y \in E: d(x, y) < r\}$$

Dados $x \in E$ y $r > 0$, la <span style="color:red;">bola cerrada de centro $x$ y radio $r$ es el conjunto</span>

$$B(x,r) = \{ y \in E: d(x, y)\leq r\}$$

---


# Bolas abiertas en $\R^2$




<p align="right" class='left'>
  <img width="600" height="500" src="bolas_r2.png" />
</p>



---

## <span style="color:purple;">Definición</span>
Sea $A\subset E$. Decimos que $x$ es un <span style="color:red;">punto interior</span> de $A$ si existe algún $r>0$ tal que $B(x,r)\subset A$
## <span style="color:purple;">Definición</span>
Sea $A\subset E$. El <span style="color:red;">interior de $A$</span> es el conjunto de todos los puntos interiores de $A$, y lo notamos $A^\circ$

---
## <span style="color:purple;">Definición</span>
Un conjunto $G \subset E$ se dice <span style="color:red;">abierto</span> si cada punto de $G$ es un punto interior de $G$ (análogamente, si $G=G^\circ$)
## <span style="color:purple;">Observación</span>
Un conjunto $G \subset E$ es abierto $\iff$ para todo $x \in G$ existe algún $r>0$ tal que $B(x,r) \subset G$  

---

---


<div class='divteo'>
<h1 class='h1teo'>Teorema</h1>

<p class=pteo> La unión de cualquier familia o colección de conjuntos
abiertos es abierta. 
La intersección de finitos conjuntos abiertos es abierta.

</p>


</div>

<br/><br/>
<br/><br/>
<br/><br/>



---



---

## <span style="color:purple;">Definición</span>

Decimos que $x$ es un <span style="color:red;"> *punto de adherencia*</span> del conjunto $A \subset E$ si para todo $r>0, A\cap B(x,r) \neq \empty$

Es equivalente decir que para todo $r>0$, existe $a \in A$, tal que $a \in B(x,r)$.

## <span style="color:purple;">Definición</span>

La <span style="color:red;">clausura</span> de $A \in E$ es el conjunto $\bar{A}$ formado por todos los puntos (de $E$) de adherencia del conjunto $A$

---

## <span style="color:purple;">Definición</span>
Un conjunto $F \subset E$ es <span style="color:red;">cerrado</span> si cada punto de $F$ es un punto de adherencia de $F$ (análogamente, si $F = \bar{F}$)

<div class='divteo'>
<h1 class='h1teo'>Teorema</h1>

$A$ es cerrado $\iff A^c$ es abierto 

</div>
<br/><br/>
<br/><br/>


---



---

<div class='divteo'>
<h1 class='h1teo'>Teorema</h1>

* La intersección de cualquier familia o colección de conjuntos
cerrados es cerrada.

* La unión de finitos conjuntos cerrados es cerrada.
</div>




<br/><br/>
<br/><br/>

---


---

## <span style="color:purple;">Definición</span>

Un conjunto $V \subset E$ se llama un entorno de $x$ si existe un
conjunto abierto $G$ tal que $x \in G \subset V$.

## <span style="color:purple;">Observación</span>

El conjunto $V$ es un entorno de $x \iff x \in V^\circ$

---

## <span style="color:purple;">Definición</span>
Decimos que $x \in E$ es un <span style="color:red;">punto de acumulación </span> de A si para
todo $r > 0$, el conjunto $A \cap B(x,r)$ es infinito.



**Equivalentemente**, $x \in E$ es punto de acumulación de A si
cada entorno de x contiene un punto de A distinto de x.

<br/><br/>
<br/><br/>
<br/><br/>


---


---

## <span style="color:purple;">Definición</span>
El conjunto de puntos de acumulación de $A \subset E$ se denomina
conjunto derivado de $A$,

$$A'=\{x \in E: x \text{ es un punto de acumulación de } A\}$$
<br/><br/>
<br/><br/>
**ejemplos**

---

<div class='divteo'>
<h1 class='h1teo'>Teorema</h1>

Sea $A \subset E$. Entonces, $\bar{A} = A \cup A'$ 

</div>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>

---

# Punto Frontera
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>

---

# Punto Frontera


## <span style="color:purple;">Definición</span>

Dado $A \subset E$, decimos que $x$ es un punto de la <span style="color:red;">frontera </span> de $A$ si para todo $r>0$, se cumple

$$B(x,r) \cap A \neq \empty \text{  }\text{ y } \text{  }B(x,r) \cap A^c \neq \empty$$
 

 Al conjunto de puntos frontera lo llamamos $\partial A$
<br/><br/>
<br/><br/>

---

<div class='divteo'>
<h1 class='h1teo'>Proposición</h1>

Sea $A \subset E$. Entonces, $\bar{A} = A \cup \partial A$ 

</div>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>


---

---

# Sucesiones en Espacios Metricos

## <span style="color:purple;">Definición</span>

Decimos que una sucesión $(x_n)_n\in E$ converge a $x \in E$ si dado cualquier $\varepsilon > 0$ existe $n_0 \in \N$ tal que $d(x, x_n) < \varepsilon$ para todo $n \geq n_0$


---
# Sucesiones en Espacios Metricos

## <span style="color:purple;">Definición</span>

Decimos que una sucesión $(x_n)_n\in E$ converge a $x \in E$ si dado cualquier $\varepsilon > 0$ existe $n_0 \in \N$ tal que $d(x, x_n) < \varepsilon$ para todo $n \geq n_0$

<div class='divteo'>

### <span style="color:purple;">Notaciones</span>

 $$ \lim_{x\to\infty}  x_n = x$$
 $$x_n \xrightarrow[n \to \infty]{} x$$
</div>


---
