# Convolution of Random Variables

Seien $X$ und $Y$ Zufallsgrößen mit gemeinsamer Dichte (Wahrscheinlichkeitsfunktion) $\mathrm{f}$ und $Z:=X+Y$.

### Diskrete Zufallsvariablen
Für $X$ und $Y$ diskret mit Träger in den natürlichen Zahlen gilt:
$$
P(Z=n)=\sum_{k=0}^{n} f(n-k, k)
$$

### Beispiel Diskrete Zufallsvariable
#### Aufgabe (Poissonverteilung)

$X$ und $Y$ seien unabhängig und Poisson-verteilt mit den Parametern $\lambda_{X}$ bzw. $\lambda_{Y}$.
(a) Bestimmen Sie die Verteilung von $X+Y$. Nutzen Sie dafür die Darstellung als Faltung.


Unter Verwendung der Darstellung als Faltung erhalten wir:
$$
\begin{aligned}
P(X+Y=n) &=\sum_{k=0}^{n} P(X=k, Y=n-k) \\
& \stackrel{\text { Uabh. }}{=} \sum_{k=0}^{n} P(X=k) P(Y=n-k) .
\end{aligned}
$$
Nun folgt für $n \notin \mathbb{N}_{0}$ (falls Poisson $f$ Wahrscheinlichkeit = 0) folgt
$$
P(X+Y=n)=\sum_{k=0}^{n} P(X=k) P(Y=n-k)=0 .
$$


Für $n \in \mathbb{N}_{0}$ 
$$
\begin{aligned}
P(X+Y=n) &=\sum_{k=0}^{n} e^{-\lambda_{X}} \frac{\lambda_{X}^{k}}{k !} e^{-\lambda_{Y}} \frac{\lambda_{Y}^{n-k}}{(n-k) !} \\
&=\frac{e^{-\left(\lambda_{X}+\lambda_{Y}\right)}}{n !} \sum_{k=0}^{n}\left(\begin{array}{l}
n \\
k
\end{array}\right) \lambda_{X}^{k} \lambda_{Y}^{n-k}
\end{aligned}
$$

$$                                              =\frac{e^{-\left(\lambda_{X}+\lambda_{Y}\right)}}{n !}\left(\lambda_{X}+\lambda_{Y}\right)^{n} \quad$$ 

(siehe binomischer Lehrsatz).
$X+Y$ ist daher Poisson-verteilt zum Parameter $\lambda_{X}+\lambda_{Y}$.

### Stetige Zufallsvariablen
Sind $X, Y$ stetig mit gemeinsamer Dichte $f$
$$
f_{Z}(z)=\int_{-\infty}^{\infty} f(z-s, s) d s
$$
Im Fall der Unabhängigkeit gilt:
$$
f_{Z}(z)=\int_{-\infty}^{\infty} f_{X}(z-s) f_{Y}(s) d s
$$
$f_{Z}$ heißt auch Faltung von $f_{X}$ und $f_{Y}$
$$
f_{Z}:=f_{X} * f_{Y}
$$

### Beispiel Diskrete Zufallsvariable
#### [Aufgabe](https://math.stackexchange.com/questions/1355980/sum-of-two-continuous-random-variables)

Consider two independent random variables $X$ and $Y$. 

Let
$$
f_{X}(x)=\left\{\begin{array}{ll}
1-x / 2, & \text { if } 0 \leq x \leq 2 \\
0, & \text { otherwise }
\end{array}\right.
$$

Let
$$
f_{Y}(y)=\left\{\begin{array}{ll}
2-2 y, & \text { if } 0 \leq y \leq 1 \\
0, & \text { otherwise }
\end{array}\right.
$$

Find the probability density function of $Z:= X+Y$.

**Consider the following cases:**

#### If 0 ≤ z ≤ 1 :

$$
\begin{aligned} f_{Z}(z) &=\int_{x=0}^{z} f_{X}(x) f_{Y}(z-x) d x \\ &=\int_{x=0}^{z}(1-x / 2)(2-2 y) d x \\ &=\left[2 x-2 z x+z x^{2} / 2+x^{2} / 2-x^{3} / 3\right]_{x=0}^{z} \\ &=2 z-\frac{3}{2} z^{2}+\frac{1}{6} z^{3} \end{aligned}
$$

#### If 1 < z ≤ 2 :

$$
\begin{aligned}
f_{Z}(z) &=\int_{x=z-1}^{z} f_{X}(x) f_{Y}(z-x) d x \\
&=\int_{x=z-1}^{z}(1-x / 2)(2-2 y) d x \\
&=\left[2 x-2 z x+z x^{2} / 2+x^{2} / 2-x^{3} / 3\right]_{x=z-1}^{z} \\
&=\frac{7}{6}-\frac{1}{2} z
\end{aligned}
$$

#### If 2 < z ≤ 3 :

$$
\begin{aligned}
f_{Z}(z) &=\int_{x=z-1}^{2} f_{X}(x) f_{Y}(z-x) d x \\
&=\int_{x=z-1}^{2}(1-x / 2)(2-2 y) d x \\
&=\left[2 x-2 z x+z x^{2} / 2+x^{2} / 2-x^{3} / 3\right]_{x=z-1}^{2} \\
&=\frac{9}{2}-\frac{9}{2} z+\frac{3}{2} z^{2}-\frac{1}{6} z^{3}
\end{aligned}
$$


### Intervallsgrenzen

**For $0 \leq z \leq 1:$**

Here, $x$ must be less than $z$ since $y$ can't be negative. So we must have $0<x<1$. 

**For $1<z \leq 2:$**

Again, $x$ must be less than $z$ since $y$ can't be negative. Also, since $y<1$, we must have $x$ at least $z-1$. Thus, $z-1<x<z$. 

**For $2<z \leq 3:$**

Again, since $y<1$, we must have $x$ at least $z-1$. Also, $x$ cannot exceed 2 so that instead of $z$ is the upper limit here. Thus, $z-1<x<2$. I

### Additional
More distributions and examples for continous convolution can be found **[here](https://stats.libretexts.org/Bookshelves/Probability_Theory/Book%3A_Introductory_Probability_(Grinstead_and_Snell)/07%3A_Sums_of_Random_Variables/7.02%3A_Sums_of_Continuous_Random_Variables)**

### Graphic Intuition


```python
%matplotlib
# Random Variables X and Y
x = randn(10000) + randint(0, 2, 10000) * 5
y = randn(10000) + randint(0, 2, 10000) * 5

fig, axes = plt.subplots(
    2, 2, sharex='col', sharey='row',
    gridspec_kw={'width_ratios': [1, 0.1], 'height_ratios': [0.1, 1]})

axes[1, 0].scatter(x, y, s=1)
axes[0, 0].hist(x, bins=200)
axes[1, 1].hist(y, bins=200, orientation='horizontal')

for z in linspace(-2, 8, num=6):
    # z = x + y  =>  y = z - x
    # which always has a slope of -1 for any fixed z.
    axes[1, 0].axline((z, z), slope=-1, c='orange')
```

    Using matplotlib backend: MacOSX


<img src="phoz.png">

### The orange lines are equal to the z-values.

#### Histogramm of $Z$


```python
%pylab

hist(x + y, bins=200)
plt.show()
```

    Using matplotlib backend: MacOSX
    Populating the interactive namespace from numpy and matplotlib


<img src="Figure_1.png">
