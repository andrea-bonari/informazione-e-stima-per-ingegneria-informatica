Esistono diverse leggi che riguardano il caso in cui ci siano più variabili aleatorie nel caso discreto.

### Legge di probabilità congiunte
>[!note]
>Siano $X,Y$ due variabili aleatorie. Si ha che:
>$$P(\set{X=x}\cap\set{Y=y})=p_{X,Y}(x,y)$$

Si ha che:
$$p_{X,Y}(x,y)\geq0\qquad\forall(x,y)\in\mathbb{R}^{2}$$
Inoltre:
$$\sum\limits_{(x,y)\in\mathbb{R}^{2}}p_{X,Y}(x,y)=1$$
Si ha inoltre la proprietà di marginalizzazione:
$$p_{X}(x)=\sum\limits_{y\in\mathbb{R}}p_{X,Y}(x,y)\qquad\forall x\in\mathbb{R}$$
Questa è analoga anche per $Y$.

### Legge di probabilità condizionata
>[!note]
>Siano $X,Y$ due variabili aleatorie. Si ha che:
>$$p_{X|Y}(x|y)= \frac{p_{X,Y}(x,y)}{p_{Y}(y)}$$

### Variabili aleatorie indipendenti
>[!note]
>Si ha che due variabili aleatorie $X$ e $Y$ sono indipendenti se e solo se:
>$$X\perp Y\iff p_{X,Y}(x,y)=p_{X}(x)p_{Y}(y)\qquad \forall (x,y)\in\mathbb{R}$$

Questo caso è estendibile al caso $n$-esimo se:
$$p_{X_{1},\cdots,X_{n}}(x_{1},\cdots,x_{n})=p_{X_{1}}(x_{1})\cdots p_{X_{n}}(x_{n})\qquad \forall (x_{1},\cdots,x_{n})\in\mathbb{R}^{n}$$

>[!tip] Indipendenza condizionata
>Si ha che:
>$$\begin{align*}
X\perp Y\text{ condizionatamente ad }&A\iff\\ &p_{X,Y|A}(x,y)=p_{X|A}(x)\cdot p_{Y|A}(y)\quad \forall(x,y)
\end{align*}$$

### Valore atteso per variabili aleatorie multiple
>[!note]
>Definiamo la statistica congiunta di $X$ e $Y$ come: $$E[g(X,Y)]=\sum\limits_{x\in\mathbb{R}}\sum\limits_{y\in\mathbb{R}}g(x,y)\cdot p_{X,Y}(x,y)$$
>Inoltre, con $g(x,y)=x^{k}y^{i}$, definiamo il momento congiunto di $X$ e $Y$ come: $$E[X^{k}Y^{i}]$$

In generale $E[g(X,Y)]\neq g(E[X],E[Y])$, tuttavia ci sono eccezioni per combinazioni lineari, e per il caso: $$X\perp Y\implies E[X\cdot Y]=E[X]\cdot E[Y]$$
### Varianza per variabili aleatorie multiple
>[!note]
>Si ha che:
>$$\text{Var}[X+Y]=\text{Var}[X]+\text{Var}[Y]+2(E[XY]-E[X]E[Y])$$

Si ha il caso particolare:
$$X\perp Y\implies\text{Var}[X+Y]=\text{Var}[X]+\text{Var}[Y]$$

### Valore atteso e varianza di una variabile aleatoria binomiale
>[!note]
>Sia $X\sim\text{Bin}(n,p)$, con: $$\begin{align*}
>&X_{i}=\begin{cases}
>1\quad&\text{se successo nella prova }i\text{-esima} \\
>0\quad&\text{altrimenti}
>\end{cases}\qquad\forall i=1,\cdots,n\\
>&p_{X_{i}}(1)=p\qquad p_{X_{i}}(0)=1-p\qquad \forall i=1,\cdots,n
>\end{align*}$$
>Le $X_{i}$ sono tutte indipendenti e identicamente distribuite. In questo caso si ha:
>$$\begin{align*}
>E[X]&= n\cdot p\\
>\text{Var}[X]&= np(1-p)\quad\forall n\in\mathbb{N}\quad\forall p\in[0,1]
>\end{align*}$$
>Studiando la funzione della varianza si ha che $p= \frac{1}{2}$ è il massimo con varianza pari a $\frac{n}{4}$.

>[!tip] Variabili aleatorie di Bernoulli
>Definiamo una variabile aleatoria come di Bernoulli se:
>$$X_{i}\sim\text{Bern}(p)\iff E[X_{i}]=p=p_{X_{i}}(1)$$


