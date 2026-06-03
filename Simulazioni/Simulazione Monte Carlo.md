>[!note]
>Sia $g(x)$ una qualsiasi funzione di $X$, è possibile stimare la statistica: $$E[g(X)]=\int_{\mathbb{R}}f_{X}(x)g(x)\text{ d}x$$
>È possibile usare la media campionaria per stimarla, se le $X_{i}\sim f_{X}$ sono indipendenti e identicamente distribuite: $$\frac{1}{n}\sum\limits_{i=1}^{n}g(X_{i})=\widehat{G}_{n}\stackrel{P}{\to}E[g(X)]$$

Quindi, nell'algoritmo Monte Carlo:
1. Genero $X_{i}\sim f_{X}\quad i=1,\cdots,n$ in maniera indipendente
2. Calcolo $\widehat{G}_{n}$

Si ha che $\widehat{G}_{n}$ è la stima Monte Carlo di $E[g(X)]$.

In generale l'errore relativo di stima è: $$\sqrt{\frac{\text{Var}\left[\widehat{G}_{n}\right]}{E[X]^{2}}}$$