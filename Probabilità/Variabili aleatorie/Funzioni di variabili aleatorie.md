>[!note]
>Sia $X$ una variabile aleatoria con legge di probabilità $f_{X}$. Sia inoltre $Y=g(X)=aX+b$, con $a,b$ constanti note e $a\neq0$.
>In generale, si ha che: $$f_{Y}(y)=f_{X}\left( \frac{y-b}{a}\right)\cdot \frac{1}{|a|}\qquad \forall a\in\mathbb{R}\smallsetminus\set{0}\quad\forall b$$

>[!tip] Metodo diretto
>Sia $Y=g(X)$, con $g$ funzione nota, deterministica e strettamente monotona. Siano inoltre due eventi $\set{x\leq X\leq x+\delta_{X}}$ e $\set{y\leq Y\leq g(x+\delta_{X})}$. Espandendo il secondo evento con Taylor possiamo dire che:
>$$\set{g(x)\leq Y\leq g(x+\delta_{X})}\approx\set{g(x)\leq Y\leq g(x)+\underbrace{\delta_{X}\cdot \left|\frac{\text{d}}{\text{dx}}g(x)\right|}_{\delta_{Y}} }$$
>Possiamo quindi dire che: $$P(x\leq X\leq x+\delta_{X})\approx P(g(x)\leq Y\leq g(x)+\delta_{Y})$$
>E di conseguenza: $$\delta_{X}f_{X}(x)\approx \delta_{Y}f_{Y}(g(x))$$
>Quindi: $$f_{Y}(g(x))= \frac{f_{X}(x)}{\left|\frac{\text{d}}{\text{d}x}g(x)\right|}$$
>Ricordando che $g$ è strettamente monotona, si ha che $x=g^{-1}(y)$, e quindi: $$f_{Y}(y)= \frac{f_{X}(g^{-1}(y))}{\left|\frac{\text{d}g}{\text{d}x}g^{-1}(y)\right|}$$

### Legge della somma di variabili aleatorie
>[!note]
>Siano $X,Y$ due variabili aleatorie discrete, con $X\perp Y$. Sia inoltre $W=X+Y$. Si ha che: $$P_{W}(w)=\sum\limits_{x}p_{X}(x)p_{Y}(w-y)$$
>Questa è detta somma di convoluzione.
>Nel caso $X,Y$ siano variabili aleatorie continue indipendenti, si ha che: $$f_{W}(w)=\int_{-\infty}^{+\infty}f_{X}(x)f_{Y}(w-x)\text{ d}x$$
>Questo è detto integrale di convoluzione.

>[!tip] Calcolo della somma di convoluzione per via grafica
>In primis, si sovrappone graficamente le 2 leggi di probabilità. Si "ribalta" poi una delle due leggi, e si trasla di $w$ posizioni (verso destra se $w>0$, verso sinistra altrimenti) la legge "ribaltata". Infine si moltiplica e sommano le probabilità.

Si ha che la convoluzione di due variabili aleatorie indipendenti uniformi con stesso supporto $a$, si la funzione risultante avrà forma triangolare con vertici $(0,0)$, $\left(a, \frac{1}{a}\right)$ e $(2a,0)$.

### Legge congiunta di due variabili aleatorie Gaussiane indipendenti
>[!note]
>Sia $X\sim\mathcal{N}(\mu_{x},\sigma_{x}^{2})\perp Y\sim\mathcal{N}(\mu_{x},\sigma_{x}^{2})$, e quindi: $$f_{X,Y}(x,y)=f_{X}(x)\cdot f_{Y}(y)= \frac{1}{\sqrt{2\pi\sigma_{x}^{2}}}e^{-\frac{(x-\mu_{x})^{2}}{2\sigma_{x}^{2}}}\cdot \frac{1}{\sqrt{2\pi\sigma_{y}^{2}}}e^{-\frac{(y-\mu_{y})^{2}}{2\sigma_{y}^{2}}}\qquad (x,y)\in\mathbb{R}^{2}$$
>Che è una campana tridimensionale centrata in $(\mu_{x},\mu_{y})$.

Studiandone le curve di livello, e quindi imponendo: $$f_{X,Y}(x,y)\stackrel{!}{=}z$$
Otteniamo degli ellissoidi, e nel caso $\sigma_{x}^{2}=\sigma_{y}^{2}$ otteniamo delle circonferenze.

### Somma di due variabili aleatorie Gaussiane indipendenti
>[!note]
>Siano $X\sim \mathcal{N}(0,\sigma_{x}^{2})\perp Y\sim\mathcal{N}(0,\sigma_{y}^{2})$ due variabili aleatorie indipendenti, e $W=X+Y$. Abbiamo che: 
>$$\begin{align*}
>f_{W}(w)&= \int_{-\infty}^{+\infty}f_{X}(x)f_{Y}(w-x)\text{ d}x\\
>&= \int_{-\infty}^{+\infty} \frac{1}{\sqrt{2\pi\sigma_{x}^{2}}}e^{\frac{- x^{2}}{2\sigma_{x}^{2}}} \cdot \frac{1}{\sqrt{2\pi\sigma_{x}^{2}}}e^\frac{- (w-x)^{2}}{2\sigma_{y}^{2}}\text{ d}x\\
>&= \frac{1}{\sqrt{2\pi(\sigma_{x}^{2}+\sigma_{y}^{2})}}e^{\frac{- x^{2}}{2(\sigma_{x}^{2}+\sigma_{y}^{2})}} \qquad\forall w\in\mathbb{R}
>\end{align*}$$
>Abbiamo nello specifico che:
>$$E[W]=0\qquad \text{Var}[W]=\sigma_{x}^{2}+\sigma_{y}^{2}$$

In generale, si ha che la somma di due variabili aleatorie Gaussiane è Gaussiana.

### Covarianza
>[!note]
>Siano $X$ e $Y$ due variabili aleatorie. Definiamo la loro covarianza come:
>$$\text{Cov}[X,Y]=E[(X-E[X])\cdot (Y-E[Y])]=E[XY]-E[X]E[Y]$$

Si ha che $\text{Cov}[X,X]=\text{Var}[X]$. Inoltre per $X\perp Y$, si ha che: $\text{Cov}[X,Y]=0$.

>[!tip] Coefficiente di correlazione lineare
>Definiamo il coefficiente di correlazione lineare come: $$\rho[X,Y]= \frac{\text{Cov}[X,Y]}{\sigma_{X}\sigma_{Y}}= E\left[\frac{(X-E[X])}{\sigma_{X}}, \frac{(Y-E[Y])}{\sigma_{Y}}\right]$$
>Si ha che $|\rho[X,Y]|\leq1$, in particolare se $|\rho[X,Y]|=1$ allora $Y=aX+b\quad a,b\in\mathbb{R}$. Inoltre: $$X\perp Y\implies \rho[X,Y]=0$$

### Varianza della somma di variabili aleatorie
>[!note]
>Siano $X_{i}$ delle variabili aleatorie. Introducendo $\stackrel{\sim}{X_{i}}=X_{i}-E[X_{i}]$, possiamo dire che:
>$$\begin{align*}
>\text{Var}\left[\sum\limits_{i=1}^{n}X_{i}\right]&= \text{Var}\left[\sum\limits_{i=1}^{n}\stackrel{\sim}{X_{i}}\right]\\
>&= E\left[\left(\sum\limits_{i=1}^{n}\stackrel{\sim}{X_{i}}\right)^{2}\right]\\
>&= E\left[\sum\limits_{i=1}^{n}\stackrel{\sim}{X_{i}^{2}}+\sum\limits{i\neq j}\stackrel{\sim}{X_{i}}\stackrel{\sim}{X_{j}}\right]\\
>&= \sum\limits_{i=1}^{n}E[\stackrel{\sim}{X_{i}^{2}}]+\sum\limits_{i\neq j}E[\stackrel{\sim}{X_{i}}\stackrel{\sim}{X_{j}}]\\
>&= \sum\limits_{i=1}^{n}\text{Var}[X_{i}]+\sum\limits_{i\neq j}\text{Cov}[X_{i},X_{j}]\\
>\end{align*}$$

### Somma di un numero casuale di variabili aleatorie
>[!note]
