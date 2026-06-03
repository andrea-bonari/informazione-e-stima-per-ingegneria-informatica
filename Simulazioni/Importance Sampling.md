>[!note]
>Nell'importance sampling si vuole far accadere l'evento $A$ con una probabilità maggiore per abbattere il numero di prove $n$. Consideriamo un esperimento aleatorio $X\sim p_{X}$ e un esperimento aleatorio ausiliario $Y\sim p_{Y}$: $$\begin{align*}
>p_{Y}(A)&= P(Y\in A)\qquad\text{Bernolli}\quad\mathbb{1}\set{y\in A}\\
>&= E[\mathbb{1}\set{y\in A}]
>\end{align*}$$
>Si ha che: $$p_{X}(A)=E[\mathbb{1}\set{x\in A}]=E\left[\mathbb{1}\set{y\in A}\frac{f_{X}(y)}{f_{Y}(y)} \right]\qquad f_{Y}(x)>0\quad \forall x$$

Nell'algoritmo importance sampling:
1. Genero $Y_{i}\sim f_{Y}\quad i=1,\cdots,n$ indipendenti e identicamente distribuite.
2. Calcolo $\widehat{p_{X}(a)}= \frac{1}{n}\sum\limits_{i=1}^{n}\mathbb{1}\set{y_{i}\in A}\frac{f_{X}(y_{i})}{f_{Y}(y_{i})}$.
Dove $f_{y}$ è scelta in modo che $p_{y}(A)>>p_{X}(a)$.

Si ha che la varianza dell'errore di stima è: $$\frac{1}{n}\left\{ E\left[\mathbb{1}\set{X\in A}\cdot \frac{f_{X}(y_{i})}{f_{Y}(y_{i})}\right]- p_{X}^{2}(A)\right\}$$
