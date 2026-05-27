>[!note]
>Un processo di Poisson può essere vista come l'estensione a tempo continuo di un processo di Bernoulli. Questo è definito come: $$\text{PP}(\lambda)$$

Un processo di Poisson ha omogeneità temporale, nello specifico l'intensità degli arrivi è costante nel tempo: $$P(k\text{ arrivi in un intervallo di tempo }\tau)=P(k,\tau)=\text{costante}$$
Siano $N_{t_{1}}$ il numero di arrivi in $t_{1}$ e $N_{t_{2}}$ il numero di arrivi in $t_{2}$, si ha che: $$N_{t_{1}}\perp N_{t_{2}}\iff t_{1}\cap t_{2}=\emptyset$$
Inoltre il numero di arrivi in un intervallo di tempo infinitesimo deve essere nullo. Se la funzione di probabilità degli arrivi è: $$P(k,\delta)=\begin{cases}
1- \lambda\delta+o(\delta)\quad&k=0\\\lambda\delta+o(\delta)&k=1\\o(\delta)&k>1
\end{cases}$$
Possiamo dire che: $$E[\text{numero di arrivi in un tempo }\delta]=\lambda\delta+o(\delta)$$
E quindi: $$\lim_{\delta\to 0}\frac{E[\text{numero di arrivi in un tempo }\delta]}{\delta}=\lambda$$
### Distribuzione del numero di arrivi in un intervallo di tempo
>[!note]
>Siano $N_{[0,\tau]}$ il numero di arrivi in un intervallo $[0,\tau]$. Si ha che: $$P(N_[0,\tau]=k)=\begin{cases}
>\frac{(\lambda\tau)^{k}}{k!}e^{-\lambda t}\quad&k=0,1,2,\cdots\\0&\text{Altrimenti}
>\end{cases}$$
>Da questa ricaviamo la legge di Poisson: $$N_{[0,\tau]}\sim\text{Poisson}(\lambda\cdot \tau)$$

La legge di Poisson ha la caratteristica di avere: $$\sum\limits_{k=0}^{\infty} \frac{(\lambda\tau)^{k}}{k!}e^{-\lambda t}=1$$
Inoltre si ha: $$E[N_{[0,\tau]}]=\lambda \tau\qquad\text{Var}[N_{[0,\tau]}]=\lambda \tau$$
### Distribuzione del tempo al $k$-esimo arrivo
>[!note]
>Sia $Y_{k}$ il tempo trascorso al $k$-esimo arrivo di un processo di Poisson. $Y_{k}$ è una variabile aleatoria continua. Possiamo dire che: $$\begin{align*}
>f_{Y_{k}}(t)&= \lim_{\delta\to0}\frac{P(t<Y_{k}<t+\delta)}{\delta}=\lim_{\delta\to0} \frac{(\lambda t)^{k-1}\cdot(\lambda\delta+o(\delta))\cdot e^{-\lambda t}}{\delta(k-1)!}\\
>&= \begin{cases}
>\frac{\lambda (\lambda t)^{k-1}e^{-\lambda t}}{(k-1)!}\qquad &t\geq0,k\geq 1\\0&\text{altrimenti}
>\end{cases}
>\end{align*}$$
>In questo caso si dice che: $$Y_{k}\sim\text{Erlang-k}(\lambda)$$
>Si ha che: $$E[Y_{k}]= \frac{k}{\lambda}\qquad \text{Var}[Y_{k}]= \frac{k}{\lambda^{2}}$$

Si ha che: $$Y_{1}\sim\text{Erlang-1}(\lambda)\sim\text{Exp}(\lambda)$$
Inoltre in generale si ha che: $$Y_{k}=T_{1}+T_{2}+\cdots+T_{k}\sim\text{Erlang-k}(\lambda)$$
Con $T_{i}$ variabili indipendenti e identicamente distribuite e $T_{i}\sim\text{Exp}(\lambda)$.

### Somma di due variabili aleatorie di Poisson indipendenti
>[!note]
>Consideriamo un processo di Poisson $\text{PP}(\lambda)$. Si ha che su questo la somma di due variabili aleatorie indipendenti di Poisson è una variabile aleatoria di Poisson con parametro somma dei parametri di partenza: $$N_{[0,k]}=\underbrace{N_{[0,a]}}_{\sim\text{Poisson}(a\lambda)}+\underbrace{N_{[a,k]}}_{\sim\text{Poisson}((k-a)\lambda)}\sim\text{Poisson}(k\lambda)$$

### Merging di processi di Poisson indipendenti
>[!note]
>Siano due processi di Poisson $\text{PP}(\lambda_{1})$ e $\text{PP}(\lambda_{2})$. Siano $N_{u,\delta}$ il numero di arrivi nel processo di Poisson unito, allora: $$P(N_{u,\delta}=k)=\begin{cases}
>1-(\lambda_{1}+\lambda_{2})\delta\qquad&k=0\\(\lambda_{1}+\lambda_{2})&k=1\\o(\delta)&k>1
>\end{cases}$$
>Il processo di Poisson risultate sarà $$\text{PP}(\lambda_{1}+\lambda_{2})$$

### Splitting di processi di Poisson
>[!note]
>È possibile dividere un processo di Poisson $\text{PP}(\lambda)$ in più processi. Per farlo, si ha che: $$\begin{align*}
>X_{i}&= 0\implies Y_{i}=Z_{i}=0\\
>X_{i}&= 1\implies \begin{cases}
>Y_{i}=1,Z_{i}=0\quad\text{con probabilità }p\\Y_{i}=0,Z_{i}=1\quad\text{altrimenti}
>\end{cases}
>\end{align*}$$
>Si ha che i processi risultanti avranno omogeneità temporale, cioè l'intensità degli arrivi è indipendente dal tempo: $$\text{PP}(p\lambda)\quad\text{e}\quad\text{PP}((1-p)\lambda)$$

### Incidenza casuale per processi di Poisson
>[!note]
>Consideriamo un processo di Poisson, e lo osserviamo a partire da un tempo casuale. La distribuzione della lunghezza dell'intervallo di tempo che trascorre tra $2$ arrivi consecutivi a cavallo dell'istante di tempo scelto è: $$W\sim\text{Erlang-2}(\lambda)$$

### Approssimazione Poissoniana della Binomiale
>[!note]
>Sotto l'ipotesi di avere $n\cdot p$ costante, possiamo approssimare: $$\text{Bin}\left(n, \frac{1}{n}\right)\approx \text{Poisson}(\underbrace{\lambda \tau}_{n\cdot p})$$
>Inoltre, per $n\cdot p\stackrel{n\to\infty}{\to}\infty$: $$\text{Bin}\left(n, \frac{1}{n}\right)\approx \mathcal{N}$$
