>[!note]
>Definiamo una variabile aleatoria (VA) come una funzione:
>$$H:\Omega\to \mathbb{R}$$
>Per indicare le variabili aleatorie si usano lettere maiuscole, mentre si usano le lettere minuscole per indicare i valori numerici da loro assunte.
>
>I valori numerici delle variabili aleatorie prendono il nome di realizzazione.

La composizione di una variabile aleatoria con una funzione generica $f:\mathbb{R}\to\mathbb{R}$ è ancora una variabile aleatoria.

### Legge di probabilità
>[!note]
>Definiamo la legge di probabilità di una generica variabile aleatoria $X$ come: $$p_{X}(x)=\underbrace{P(\set{X=x})}_\text{abuso di notazione} =P(\set{\omega\in \Omega\quad\text{t.c.}\quad X(\omega)=x})$$

La legge della probabilità soddisfa sempre tutti gli assiomi delle probabilità, inoltre si ha che: $$\sum\limits_{x\in\mathbb{R}}p_{X}(x)=1$$
>[!tip] Funzione indicatrice
>Definiamo la funzione indicatrice $\mathbb{1}$ come:
>$$\mathbb{1}\set{A}=\begin{cases}
>1\quad&A\text{ è vero}\\
>0\quad&A\text{ è falso}
>\end{cases}$$
>Dove $A$ è un predicato qualsiasi. Questa è utile per indicare le leggi di probabilità con dominio non totale.

>[!tip] Legge di probabilità geometrica
>Definiamo una generica variabile aleatoria $X$ come geometrica se e solo se: $$X\sim\text{Geom}(a)\iff p_{X}(k)=(1-a)^{k-1}\cdot a\cdot \mathbb{1}\set{a\in[0,1]}$$

>[!tip] Legge di probabilità binomiale
>Definiamo una generica variabile aleatoria $X$ come binomiale se e solo se:
>$$X\sim\text{Bin}(n,p)\iff p_{X}(k)= \binom{n}{k}\cdot p^{k}\cdot(1-p)^{n-k}\cdot\mathbb{1}\set{k=0,\cdots,n}$$
>Dove $n$ è il numero di prove indipendenti, mentre $p$ è la probabilità di successo della singola prova.

Siano due eventi generici $A,B$, con $A=\set{X=x}$ e $B=\set{Y=y}$. Possiamo indicare: $$P(A|B)=p_{X|Y}(x|y)$$
Si ha inoltre che: $$P(\set{X=x}|B)=p_{X|B}(x)$$
### Valore atteso
>[!note]
>Definiamo il valore atteso di una legge di probabilità come:
>$$E[X]=\sum\limits_{x\in\mathbb{R}}x\cdot p_{X}(x)$$
>Questa è quindi la media pesata delle realizzazioni, dove i pesi sono le probabilità. Possiamo anche interpretare $E[X]$ come il baricentro della legge di probabilità.

>[!tip] Proprietà del valore atteso
>Sia $X$ una variabile aleatoria e $Y=g(X)$, con $g:\mathbb{R}\to\mathbb{R}$. Si ha che: $$E[Y]=E[g(X)]$$
>Questa è detta legge dello statistico inconsapevole.
>
>Si ha inoltre che se una generica $g(x)$ è lineare in $x$, allora: $$E[g(X)]=g(E[X])$$
>In caso $g(x)$ non sia lineare questa proprietà non è valida.

Siano due eventi generici $A,B$, con $A=\set{X=x}$ e $B=\set{Y=y}$. Possiamo dire che: $$E[X|B]=\sum\limits_{x\in\mathbb{R}}x\cdot p_{X|B}(x)$$
### Varianza
>[!note]
>Definiamo la varianza di una variabile aleatoria come:
>$$0\leq\text{Var}[X]=E\left[(X-E[X])^{2}\right]=E\left[X^{2}\right]-E[X]^{2}$$

>[!tip] Momenti della variabile aleatoria
>Definiamo il momento di ordine $n$ della variabile aleatoria $X$ come: $$E\left[X^{n}\right]$$
>Definiamo inoltre il momento centrato di ordine $n$ come: $$E\left[(X-E[X])^{n}\right]$$

Si ha che: $$\forall X\qquad \text{Var}[X]\geq0$$
Inoltre, in generale: $$\text{Var}[\alpha X+\beta]= \alpha^{2}\text{Var}[X]$$
>[!tip] Scarto quadratico medio
>Definiamo lo scarto quadratico medio di una generica variabile aleatoria $X$ come:
>$$\sigma_{X}=\sqrt{\text{Var}[X]}$$

### Legge della perdita di memoria
>[!note]
>Si ha che per $X$ variabile aleatoria geometrica discreta, vale:
>$$p_{X-t|X>t}(k)=p_{X}(k)\qquad \forall k,t\in\mathbb{N}$$

Come conseguenza diretta si ha che:
$$E[X-t|X>t]=E[X]\qquad\forall t\in\mathbb{N}$$
### Legge dell'aspettativa totale
>[!note]
>Siano $A_{1},\cdots,A_{n}$ partizioni di $\Omega$. Si ha che:
>$$E[X]=\sum\limits_{i=1}^{n}P(A_{i})\cdot E[X|A_{i}]$$
