## Vorgehensweise stetige Faltung mit unterschiedlichem Träger

#### 1. Definiere die obere und untere Grenze der Randverteiligen

$$
\quad \begin{array}{l}f_{X}(x)=\left\{\begin{array}{ll}p_{1} & a_{x} \leq x \leq b_{y} \\ 0 & \text { sonst }\end{array}\right. \\ f_{Y}(y)=\left\{\begin{array}{ll}p_{2} & a_{y} \leq y \leq b_{y} \\ 0 & \text { sonst }\end{array}\right.\end{array}
$$

$\begin{array}{ll}\text { Untere Grenze: } & a_{x}, a_{y} \\ \text { Obere Grenze: } & b_{x}, b_{y}\end{array}$ 

Teile $z$ in die Intervalle ein:

$\min \left\{a_{x}, a_{y}\right\} \leq z<\min \left\{b_{x}, b_{y}\right\}$

$\min \left\{b_{x}, b_{y}\right\} \leq z<\max \left\{b_{x}, b y\right\}$

$\max \left\{b_{x}, b y\right\} \leq z<b_{x}+b_{y}$

Nach diesen Fällen wird unterschieden.

#### Bestimmung der Intervallsgrenzen (pro Intervall)

$
\text { Pro Intervall falls s in } f_{y}(s) \text { und über s integriert wird }
$

$$
\begin{array}{l}
\int_{s=\max \left(z-b_{y}, a_{y}\right)}^{\min (z, b_{y})} f_{x}(z-s) f_{y}(s) d s
\end{array}
$$

### Aufgabenbeispiel

$$
\begin{array}{l}
f_{X}(x)=\left\{\begin{array}{cl}
\frac{1}{10} & 0 \leqslant x \leqslant 10 \\
0 & \text { sonst }
\end{array}\right. \\
f_{Y}(y)=\left\{\begin{array}{cc}
\frac{1}{20} & 0 \leqslant y \leqslant 20 \\
0 & \text { sonst }
\end{array}\right.
\end{array}
$$

$\begin{array}{ll}\text { Untere Grenze: } & a_{x}= 0, a_{y}= 0 \\ \text { Obere Grenze: } & b_{x}=10, b_{y}=20\end{array}$ 

Teile $z$ in die Intervalle ein:

$\min \left\{ a_{x}= 0, a_{y}= 0\right\}=0 \leq z<\min \left\{b_{x}=10, b_{y}=20\right\}=10$

$\min \left\{b_{x}=10, b_{y}=20\right\}=10 \leq z<\max \left\{b_{x}=10, b_{y}=20\right\}=20$

$\max \left\{b_{x}=10, b_{y}=20\right\}=20 \leq z<(b_{x}=10 + b_{y}=20)=30$

Nach diesen Fällen wird unterschieden.


**Falls $0 \leq z< 10$**

$$
\begin{array}{l}
\int_{s=\max \left(z-b_{y}, a_{y}\right)}^{\min (z, b)} f_{x}(z-s)  f_{y}(s) d s
\end{array}
$$

$
\begin{array}{l}
\int_{s=\max \left(z-20, 0\right)}^{\min (z, 20)} f_{x}(z-s), f_{y}(s) d s =
\int_{s=0}^{z} f_{x}(z-s), f_{y}(s) d s
\end{array}
$

**Falls $10 \leq z< 20$**

$$
\begin{array}{l}
\int_{s=\max \left(z-b_{y}, a_{y}\right)}^{\min (z, b)} f_{x}(z-s), f_{y}(s) d s
\end{array}
$$

$
\begin{array}{l}
\int_{s=\max \left(z-20, 0\right)}^{\min (z, 20)} f_{x}(z-s) f_{y}(s) d s =
\int_{s=0}^{z} f_{x}(z-s), f_{y}(s) d s
\end{array}
$

**Falls $20 \leq z< 30$**

$$
\begin{array}{l}
\int_{s=\max \left(z-b_{y}, a_{y}\right)}^{\min (z, b)} f_{x}(z-s), f_{y}(s) d s
\end{array}
$$

$
\begin{array}{l}
\int_{s=\max \left(z-20, 0\right)}^{\min (z, 20)} f_{x}(z-s) f_{y}(s) d s =
\int_{s=z-10}^{20} f_{x}(z-s), f_{y}(s) d s
\end{array}
$
