>[!note]
>Consideriamo delle variabili aleatorie $A_{k}$, con una densità di probabilità $f_{A_{k}}$ associata a ciascuna di loro. Sia una successione di variabili aleatorie $\set{A_{k}}_{k}$, e sia $a$ un numero positivo. Si ha che $\set{A_{k}}$ converge in probabilità ad $a$ se: $$\lim_{k\to+\infty}P( |A_{k}-a|>\varepsilon)=0\qquad \forall \varepsilon>0$$
>Questa è rappresentabile con: $$A_{k}\stackrel{P}{\to} a$$
>Questa è detta convergenza debole.

La convergenza è detta debole perché: $$\set{Y_{k}}\stackrel{P}{\to} a\centernot\implies E[Y_{n}]\to a$$
### Diseguaglianza di Markov
>[!note]
>Sia $X\geq0$ una variabile aleatoria, si ha che, fissato $a>0$:
>$$\begin{align*}
>E[X]&= \sum\limits_{x}x\cdot p_{X}(x)\\
&= \sum\limits_{x<a}x\cdot p_{X}(x)+\sum\limits_{x\geq a}x\cdot p_{X}(x)\\
&\geq\sum\limits_{x\geq a}x \cdot p_{X}(x)\\
&\geq a\sum\limits_{x\geq a}p_{X}(X)=a\cdot P(X\geq a)
>\end{align*}$$

>[!tip] Disuguaglianza di Chelyshev
>Dato il risultato precedente, consideriamo la disequazione: $$(X-E[X])^{2}\geq0$$
>Da questa si ottiene il risultato: $$P\left((X-E[X])^{2}\geq a\right)\leq \frac{\text{Var}[X]}{a}\qquad \forall a>0$$
>Possiamo anche dire: $$\text{Var}[x]\geq \varepsilon^{2}P(|X-E[X]|\geq \varepsilon)\qquad\forall\varepsilon\geq0$$
>Inoltre, per $\varepsilon=k\sigma_{X}$: $$\frac{1}{k^{2}}\geq P\left(\left| \frac{X-E[X]}{\sigma_{X}} \right|\geq k\right)\iff 1- \frac{1}{k^{2}}\leq P\left(\left| \frac{X-E[X]}{\sigma_{X}}\right|\leq k\right)$$

### Media campionaria
>[!note]
>Siano $X_{1},\cdots,X_{n}$ delle variabili aleatorie indipendenti identicamente distribuite. Sia inoltre $X\sim X_{i}$. Definiamo la media campionaria come la variabile aleatoria: $$M_{n}= \frac{X_{1}+\cdots X_{n}}{n}$$
>Si ha che: $$\begin{align*}
>E[M_{n}]&=E[X]\\
>\text{Var}[M_{n}]&= \frac{1}{n}\text{Var}[X]
>\end{align*}$$

Si ha che: $$\begin{align*}
&\lim_{n\to\infty}\text{Var}[M_{n}]=0\\
&\set{M_{n}}_{n}\stackrel{P}{\to}E[X]\quad\text{Legge debole dei grandi numeri}
\end{align*}$$
