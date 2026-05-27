>[!note]
>Definiamo un processo di Bernoulli come una sequenza di variabili aleatorie indipendenti e identicamente distribuite:
>$$\left\{\begin{matrix}X_{1},\space X_{2},\space \cdots\\X_{i}\sim\text{Bern}(p)\\X_{i}\text{ indipendenti e identicamente distribuite}\end{matrix}\right\}\iff \text{BP}(p)$$
>I processi di Bernoulli servono a modellizzare una sequenza di successi o insuccessi.

### Numero di successi in $n$ istanti temporali
>[!note]
>Definiamo $S$ come il numero di successi in $n$ prove, allora: $$\begin{align*}
>S&= \sum\limits_{i=1}^{n}X_{i}\qquad S\sim\text{Bin}(n,p)\\
>p_{S}(k)&= \begin{cases}
>\binom{n}{k}p^{k}(1-p)^{n-k}\qquad &k=0,1\cdots,n\\0&\text{altrimenti}
>\end{cases}
>\end{align*}$$

### Tempo di primo arrivo
>[!note]
>Definiamo il tempo di primo arrivo $T_{1}$ come il numero di prove fino al primo successo: $$\begin{align*}
>&T_{1}\sim\text{Geom}(p)\qquad p_{T_{1}}(t)=\begin{cases}
>(1-p)^{t-1}p\qquad&t=1,2,\cdots\\0&\text{Altrimenti}
>\end{cases}\\
>&E[T_{1}]= \frac{1}{p}\qquad \text{Var}[T_{1}]= \frac{1-p}{p^{2}} 
>\end{align*}$$
>Inoltre $T_{1}$ gode di perdita di memoria.

### Tempo di interarrivo
>[!note]
>Definiamo $T_{i}$ come i tempi di inter-arrivo, dove $T_{i}\sim\text{Geom}(p)$ indipendenti e identicamente distribuiti. Definiamo il tempo al $k$-esimo arrivo $Y_{k}$ come: $$Y_{k}=T_{1}+T_{2}+\cdots+T_{k}$$
>Si ha che: $$P(Y_{k}=t)= \begin{cases}
>\binom{t-1}{k-1}p^{k}(1-p)^{t-k}\qquad& t\geq k\\0&\text{Altrimenti}\end{cases}$$
>Con: $$E[Y_{k}]= \frac{k}{p}\qquad \text{Var}[Y_{k}]= k \frac{1-p}{p^{2}}$$
>In questo caso si dice: $$Y_{k}\sim\text{Pascal-k}(p)$$

### Splitting di un processo di Bernoulli
>[!note]
>È possibile dividere un processo di Bernoulli $X_{i}$ in più processi $Y_{i}$ e $Z_{i}$. Per farlo, si ha che: $$\begin{align*}
>X_{i}&= 0\implies Y_{i}=Z_{i}=0\\
>X_{i}&= 1\implies \begin{cases}
>Y_{i}=1,Z_{i}=0\quad\text{con probabilità }0.5\\Y_{i}=0,Z_{i}=1\quad\text{altrimenti}
>\end{cases}
>\end{align*}$$
>Si ha che le $Y_{i}$ sono di Bernoulli, e che per $i\neq j$ si ha $Y_{i}\perp Y_{j}$ (analoghi sono questi ragionamenti per $Z$). Inoltre: $$Y\sim\text{BP}(p\cdot q)\qquad Z\sim\text{BP}(p\cdot(1-q))$$
>Infine si ha che: $$Y\centernot\perp Z$$

### Merging di un processo di Bernoulli
>[!note]
>È possibile unire due processi di Bernoulli indipendenti $Y_{i},\text{BP}(p)$ e $Z_{i},\text{BP}(q)$ in un processo di Bernoulli $X_{i}$, si ha che: $$X_{i}=Y_{i}\oplus Z_{i}$$
>Si ha che le $X_{i}$ sono di Bernoulli, e che per $i\neq j$ si ha $X_{i}\perp X_{j}$. Si ha inoltre che: $$X\sim\text{BP}(p+q-p\cdot q)$$

