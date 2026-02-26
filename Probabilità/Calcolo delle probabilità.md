>[!note]
>Definiamo $P(A)$ come la probabilità di un generico evento $A\subseteq \Omega$. Si hanno i seguenti assiomi:
>$$\begin{align*}
>P(A)&\geq0\\
>P(\Omega)&=1\\
>P(A\cup B)&=P(A)+P(B)\qquad A\cap B\neq\emptyset
>\end{align*}$$

Da questi assiomi si ricavano proprietà come $P(A)\leq1$, $P(\emptyset)=0$.

>[!tip] Unione di una infinità di eventi disgiunti
>Si ha che:
>$$P\left(\bigcup_{i=1}^{\infty} A_{i}\right)= \sum\limits_{i=1}^{\infty} P(A_{i})\qquad A_{i}\cap A_{j}\neq\emptyset\quad i\neq j$$

### Spazio campionario 
>[!note]
>Definiamo lo spazio campionario $\Omega$ come l'insieme di tutti i possibili risultati dell'esperimento aleatorio.
>
>Ogni elemento di $\Omega$ è detto elemento elementare.
>
>Si ha che $\Omega$ ha le seguenti proprietà:
>- Mutua esclusività degli eventi elementari
>- Esaustività dei risultati
>  
>È insensato assegnare probabilità a singoli eventi elementari, tuttavia ha senso assegnarle a sottoinsiemi di $\Omega$.

>[!tip] $\sigma$-algebra
>Si dice $\sigma$-algebra di $\Omega$ una famiglia di sottoinsiemi di $\Omega$, detta $\mathcal{F}$ tale che:
>$$\begin{align*}
>&\Omega\in \mathcal{F}\\
>A\in\mathcal{F}\implies& A^{C}=\Omega\smallsetminus A\in \mathcal{F}\\
>A_{i}\in\mathcal{F}\quad\forall i\in\mathbb{N}\implies& \bigcup_{i=1}^{\infty}A_{i}\in\mathcal{F}\text{ è infinita numerabile di insiemi}
>\end{align*}$$
>Una $\sigma$-algebra di $\Omega$ è quindi l'insieme dei suoi sottoinsiemi misurabili.
>

Si ha che $(\Omega,\mathcal{F})$ è uno spazio numerabile.

Un evento è quindi un sottoinsieme misurabile dello spazio campionario $\Omega$, ed è pertanto un sottoinsieme della $\sigma$-algebra. Si usa per la loro notazione le lettere maiuscole.

### Teorema delle probabilità totali
>[!note]
>Siano $A_{1},\cdots,A_{n}$ degli eventi. Si ha che:
>$$\begin{align*}
>P\left(\bigcup_{i=1}^{n}A_{i}\right)&= \sum\limits_{i=1}^{n}P(A_{i})+\cdots\\
>&\space+(-1)^{r+1}\sum\limits_{i_{1}<\cdots<i_{r}}P(A_{i_{1}}\cap\cdots\cap A_{i_{r}})+\cdots\\
>&\space+(-1)^{n+1}\sum\limits_{i_{1}<\cdots i_{n}}P(A_{i_{1}}\cap\cdots \cap A_{i_{n}})
>\end{align*}$$
>In caso $A_{1},\cdots, A_{n}$ siano disgiunti allora la formula si semplifica in:
>$$P\left(\bigcup_{i=1}^{n}A_{i}\right)=\sum\limits_{i=1}^{n}P(A_{i})$$

Si ha quindi che la probabilità è proporzionale all'area della regione $A$: $$P(A)= \frac{\text{area}(A)}{\text{area}(\Omega)}\quad \forall A\in\mathcal{F}(\Omega)$$

>[!tip] Forma discreta
>Sia $\omega$ un evento elementare di $\Omega$, allora: $$P(\omega) = \frac{1}{|\Omega|}\qquad\forall \omega\in\Omega$$
>
>Si ha che data una legge di probabilità uniforme discreta, e dato un evento $A$:
>$$P(A)=\frac{\#\text{ casi favorevoli ad }A}{\#\text{ casi totali}}= \frac{|A|}{|\Omega|}$$
