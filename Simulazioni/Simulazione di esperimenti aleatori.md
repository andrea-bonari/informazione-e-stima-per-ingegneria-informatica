>[!note]
>Dato un evento $A$ e un esperimento aleatorio è possibile ripetere l'esperimento aleatorio tante volte (in maniera indipendente), e per ogni prova registrare una variabile aleatoria $X_{i}$: $$X_{i}=\begin{cases}
>1\qquad &A\text{ si verifica nella prova }i\\0&\text{Altrimenti}
>\end{cases}\qquad X_{i}\sim\text{Bern}(P(A))$$
>Con $X_{i}$ indipendenti e identicamente distribuite. Costruendo la loro media campionaria $M_{n}$: $$M_{n}=\frac{\#\text{ casi favorevoli ad }A}{\#\text{ casi totali}}$$
>Per la legge debole dei grandi numeri, la media campionaria è una buona stima di $P(A)$: $$M_{n}\stackrel{P}{\to}E[M_{n}]=P(A)$$

>[!tip] Controllo dell'errore di stima
>In modo analogo al problema del sondaggista, abbiamo un livello fiduciario dove vogliamo cadere con grande probabilità: $$P(|M_{n}-P(A)|<\varepsilon)>0.95$$
>Inoltre vogliamo avere un errore quadratico medio di stima piccolo: $$\text{MSE}_{n}=E\left[(M_{n}-P(A))^{2}\right]=\text{Var}[M_{n}]= \frac{P(A)(1-P(A))}{n}\leq \frac{1}{4n}$$
>Calcoliamo quindi l'errore relativo di stima: $$\frac{\sqrt{\text{MSE}_{n}}}{P(A)}=\sqrt{\frac{1-P(A)}{n\cdot P(A)}}\stackrel{!}{\leq}\varepsilon$$
>E quindi: $$n\geq \frac{1}{\varepsilon^{2}}\frac{1-P(A)}{P(A)}$$
>Per $P(A)\to1$, un $n$ piccolo è sufficiente, tuttavia per $P(A)\to0$ $n$ deve essere molto grande, quindi stimare la probabilità di eventi rari è dispendioso.

### Generatore di numeri casuali
>[!note]
>Per simulare è necessario generare numeri casuali. Per farlo utilizziamo dei sistemi caotici, cioè sistemi che data una condizione iniziale (detta seed), ci fornisce in uscita una sequenza di bit pseudo-casuali.
>

>[!tip] Generazione di variabili aleatorie uniformi
>Avendo a disposizione una sequenza pseudo-casuale di bit $0$ e $1$, è possibile generare numeri casuali $X\sim\mu[0,1]$.
>
>È possibile generare realizzazioni $x$ da $x\sim f_{x}$ con $f_{x}$ data. Per farlo processiamo l'output del generatore di variabili aleatorie uniformi con una funzione $g(u)$.
>
>Sia la funzione $g(u)$ monotona crescente, allora la funzione: $$F_{X}(x)=g^{-1}(x)\qquad\text{se }0<g^{-1}(x)<1$$
>Siccome $F_{X}(x)$ è non decrescente, possiamo anche dire che: $$F_{X}^{-1}(u)=g(u)\qquad\forall u\in[0,1]$$

### Metodo di acceptance-rejection
>[!note]
>Supponiamo di voler generare campioni $X\sim f_{X}$, scegliamo un valore $m$ tale che: $$m\geq\max_{x}f_{X}(x)$$
>Scegliamo casualmente dei punti nella regione rettangolare $[0,a]\times[0,m]$, tenendo solo i punti che cadono sotto $f_{X}$ (acceptance).

>[!tip] Algoritmo di acceptance-rejection
>1. Genero $U\sim\mu[0,a]$
>2. Genero $U'\sim\mu[0,m]$, con $U'\perp U$
>3. Accetto e pongo $X=U$ se $m\cdot u'\leq f_{X}(U)$, altrimenti torno ad $1$.

Si trova un valore $m$ tale che: $$m f_{Y}(x)\geq f_{X}(x)\qquad\forall x\in\mathbb{R}$$
1. Si genera un $Y\sim f_{Y}$ e $U'=\mu[0,1]$ con $Y\perp U'$
2. Accettiamo e poniamo $X=Y$ se $mf_{Y}(y)\cdot U'\leq f_{X}(y)$, altrimenti torno ad $1$.

È provabile che mediamente si genera $1$ campione valido di $X$ ogni $m$ cicli, di conseguenza l'efficienza dell'algoritmo di acceptance-rejection è $\frac{1}{m}$.
### Algoritmo di Box-Muller
>[!note]
>L'algoritmo di Box-Muller è un algoritmo di generazione casuale con efficienza $100\%$. Consideriamo di generare campioni da un vettore di variabili aleatorie Gaussiane standard indipendenti: $$\overrightarrow{X}=(X_{1},\cdots,X_{n})^{T}$$
>Definiamo: $$\overrightarrow{\mu}=E\left[\overrightarrow{X}\right]=\vec{0}$$
>Introduciamo una matrice di covarianza $\Sigma$: $$\begin{align*}
>\Sigma&= [\text{Cov}[X_{i},X_{j}]]_{i,j}\\&= \begin{pmatrix}\text{Cov}[X_{1},X_{1}]&\cdots&\text{Cov}[X_{1},X_{n}]\\\vdots&\ddots&\vdots\\\text{Cov}[X_{n},X_{i}]&\cdots&\text{Cov}[X_{n},X_{n}]\end{pmatrix}\\&= E\left[\left(\overrightarrow{X}-\overrightarrow{\mu}\right)\left(\overrightarrow{X}-\overrightarrow{\mu}\right)\right]
>\end{align*}$$
>Per le variabili aleatorie Gaussiane standard $\Sigma=I_{n}$ perché le $X_{i}$ sono indipendenti e identicamente distribuite.
>
>Per generare un campione:
>1. Genero le $Z_{i}\sim\mathcal{N}(0,1)$ per $i=1,\cdots,n$ in maniera indipendente.
>2. Pongo $\overrightarrow{X}=A\cdot \overrightarrow{Z}+\overrightarrow{b}$, e si determinano $A$ e $\overrightarrow{b}$ in modo che $E\left[\overrightarrow{X}\right]=\overrightarrow{\mu}$ e $\text{Cov}\left[\overrightarrow{X},\overrightarrow{X}\right]=\Sigma$, da cui ricaviamo $\overrightarrow{\mu}=\overrightarrow{b}$ e $A\cdot A^{T}=\Sigma$.

La fattorizzazione $M=V\cdot V^{T}$ è detta fattorizzazione di Cholesky:
$$V=\text{Cholesky}(M)$$
### Campionare da distribuzioni discrete
>[!note]
>Per campionare da distribuzioni discrete si può riadattare il metodo della cumulata inversa:
>$$X=\begin{cases}
>x_{1} \qquad&0<U<P_{X}(x_{1}) \\
>\vdots&\vdots\\x_{j}&P_{X}(x_{j-1})<U<F_{X}(x_{j}) \\
>\vdots&\vdots\\x_{n}&P_{X}(x_{n-1})<U<1
>\end{cases}$$

Quindi come algoritmo possiamo seguire:
1. Genero $U\sim\mu[0,1]$
2. Assegno $X$ come indicato sopra

