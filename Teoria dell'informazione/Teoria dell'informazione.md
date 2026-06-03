>[!note]
>Definiamo l'auto-informazione di $A$ come: $$i(A)\widehat{\equiv}\log \frac{1}{p(A)}$$

È possibile scegliere la base del logaritmo a piacere:
- Base naturale: unità di misura $\text{nat}$, scelta fisica
- Base $2$: unità di misura $\text{bit}$, scelta informatica
- Base $10$: unità di misura $\text{Hartley}$

Si ha che:
$$i(A\cap B)=i(A)+i(B)$$

### Contenuto informativo di una variabile aleatoria discreta
>[!note]
>Consideriamo un'esperimento aleatorio il cui risultato è descritto da una variabile aleatoria $X$ discreta. Ad ogni evento associamo una probabilità e quindi un'auto informazione: $$i(\set{X=x})=i(x)\qquad\forall x\in\mathbb{R}$$
>Definiamo quindi la variabile aleatoria informazione: $$i(X)=\begin{cases}
>\log \frac{1}{p_{X}(x_{1})}\qquad&\text{Con probabilità }p_{X}(x_{1})\\\vdots&\vdots\\\log \frac{1}{p_{X}(x_{n})}&\text{Con probabilità }p_{X}(x_{n})
>\end{cases}$$
>Da cui possiamo definire l'informazione media, detta entropia, delle variabili aleatorie $X$: $$H(X)\widehat{\equiv}E[i(X)]=E\left[\log \frac{1}{p_{X}(x)} \right]=\sum\limits_{j=1}^{n}p_{X}(x_{j})\log \frac{1}{p_{X}(x_{j})}$$

Si ha che: $$H(Y)\geq0\qquad\forall Y$$
### Diseguaglianza di Jensen
>[!note]
>Dati $\lambda_{1},\cdots,\lambda_{m}$ tali che $\sum\limits_{i=1}^{m}\lambda_{i}=1$, con $\lambda_{i}\geq0\quad \forall i$, si ha che: $$\sum\limits_{i=1}^{m}\lambda_{i}\log x_{i}\leq \log\left(\sum\limits_{i=1}^{m}\lambda_{i}y_{i}\right)$$

Da questa disuguaglianza otteniamo che: $$H(Y)\leq \log(m)$$
In generale questa disuguaglianza vale per qualsiasi funzione concava (o convessa).