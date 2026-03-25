>[!note]
>Consideriamo, da una variable aleatoria $X:\Omega\to\mathbb{R}$, una funzione associata $f_{X}$ detta funzione di densità di probabilità (PDF). Possiamo dire che:
>$$P(a\leq X\leq b)=\int_{a}^{b}f_{X}(x)\text{ d}x$$
>Se le probabilità possono essere calcolate come integrali definiti di $f_{X}$, allora $X$ è una variabile aleatoria continua.

>[!tip] Funzione di densità
>Consideriamo $P(x\leq X\leq x+\delta)$, con $\delta>0$. Si ha che questa per definizione è: $$P(x\leq X\leq x+\delta)=\int_{x}^{x+\delta}f_{X}(t)\text{ d}t\approx \delta f_{X}(x)$$
>Calcoliamo quindi:
>$$\lim_{\delta\to 0}f_{X}(x)= \lim_{\delta\to0}\frac{P(x\leq X\leq x+\delta)}{\delta}=f_{X}(x)$$
>Che è la densità di probabilità per unità di lunghezza.

Si ha che:
$$\begin{align*}
f_{X}(x)&\geq 0\qquad\forall x\in\mathbb{R}\\
1=P(\Omega)&= P(X\in\mathbb{R})=\int_{-\infty}^{+\infty}f_{X}(x)\text{ d}x
\end{align*}$$

### Valore atteso e varianza
>[!note]
>Definiamo il valore atteso per variabili aleatorie continue come:
>$$E[X]=\int_{-\infty}^{+\infty}x\cdot f_{X}(x)\text{ d}x$$
>La definizione di varianza rimane analoga al caso discreto:
>$$\text{Var}[X]=E[X^{2}]-E[X]^{2}$$

>[!tip] Legge dello statistico inconsapevole
>Anche nel caso continuo vale la legge dello statistico inconsapevole:
>$$E[g(X)]=\int_{-\infty}^{+\infty}g(x)\cdot f_{X}(x)\text{ d}x$$

### Variabile aleatoria uniforme
>[!note]
>Si ha che $X$ è una variabile aleatoria uniforme se:
>$$X\sim u[a,b]\iff f_{X}(x)=\begin{cases}
>\frac{1}{b-a}\qquad&a\leq x\leq b \\
>0&\text{Altrimenti}
>\end{cases}$$
>Si ha che per variabili aleatorie uniformi:
>$$\begin{align*}
>E[X]&=  \frac{a+b}{2}\\
>\text{Var}[X]&= \frac{(b-a)^{2}}{12}
>\end{align*}$$

### Funzione cumulativa di probabilità
>[!note]
>Definiamo la funzione cumulativa di probabilità come: $$F_{X}(a)=P(X\leq x)=\int_{-\infty}^{x}f_{X}(t)\text{ d}t$$

Si ha che:
$$\begin{align*}
&0\leq F_{X}(x)\leq 1\qquad \forall x\in\mathbb{R}\\
&F_{X} \text{ strettamente non decrescente }\forall x\in\mathbb{R}\\
&\frac{\text{d}}{\text{d}x}F_{X}(x)= f_{X}(x)
\end{align*}$$

### Legge di probabilità Gaussiana
>[!note]
>Sia $X$ una variabile aleatoria continua. Diciamo che $X$ è Gaussiana se e solo se: $$X\sim\mathcal{N}(\mu_{x},\sigma_{x}^{2})\iff f_{X}(x)= \frac{1}{\sqrt{2\pi\sigma_{x}^{2}}}e^{-\frac{(x-\mu_{x})^{2}}{2\sigma_{x}^{2}}}$$
