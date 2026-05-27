>[!note]
>Consideriamo una quantità da stimare $\theta$, e la interpretiamo con variabile aleatoria $\Theta=f_{\theta}$ conosciuta a priori. A questo punto tramite uno strumento di misura osserviamo $X=f_{X|\Theta}$. Infine tramite uno stimatore otterremo $\widehat{\Theta}(X)$.
>
>Se $\theta$ è discreta potremo testare la sua ipotesi per ottenere $\Theta\in\set{0,1}$. Avendo poi conoscenza a priori di $\Theta$ potremo dire che: $$\begin{cases}
>p_{\Theta}(0)=p\\p_{\Theta}(1)=1-p
>\end{cases}$$
>Calcolando poi la legge a posteriori di $\Theta$ dato $X$, per la regola di Bayes: $$p_{\Theta|X}(\theta|x)= \frac{f_{X|\Theta}(x|\theta)p_{\Theta}(\theta)}{f_{X}(x)}$$
>Da cui possiamo calcolare: $$p_{\Theta|X}(0|x)\qquad p_{\Theta|X}=1-p_{\Theta}(0|x)$$
>Per $\Theta$ continua possiamo dire che: $$f_{\Theta|X}(\theta|x)= \frac{f_{X|\Theta}(x|\theta)f_{\Theta}(\theta)}{f_{X}(x)}$$
>Con: $$f_{X}(x)=\int f_{X|\Theta}(x|\theta')f_{\Theta}(\theta')\text{ d}\theta'$$
>![[Pasted image 20260527181649.png|center]]

Data una generica variabile aleatoria o variabile $a$, da adesso in poi utilizzeremo $\widehat{a}$ per indicare le sue stime.

>[!tip] Stima classica
>Consideriamo una quantità da stimare $\theta$ non osservabile direttamente. Tramite uno strumento di misura osserviamo una variabile aleatoria $X=x$, misurata da una funzione $f_{X}(x,\theta)$. Una volta fatto passeremo da uno stimatore, che ci restituirà una variabile aleatoria $\widehat{\Theta}(X)$.
>![[Pasted image 20260527175045.png|center]]

### Stimatore Massimo a posteriori (MAP)
>[!note]
>Per $\theta$ discreta, il risultato dopo aver applicato Bayes è: $$p_{\Theta|X}(\theta|x)$$
>Decidiamo per l'ipotesi con la massima probabilità a posteriori: $$\widehat{\Theta}_\text{MAP}(x)= \arg\max_{\theta}p_{\Theta|X}(\theta|x)$$
>Nel caso continuo, dopo aver applicato Bayes ottengo: $$f_{\Theta|X}(\theta|x)$$
>E possiamo dire che: $$\widehat{\Theta}_\text{MAP}(x)=\arg\max_{\theta}f_{\Theta|X}(\theta|x)$$

Questa stima MAP minimizza la probabilità di errore di stima a posteriori, quindi: $$P\left(\Theta\neq \widehat{\Theta}_\text{MAP}(X)|X=x\right)\leq P\left(\Theta\neq \widehat{\Theta}(X)|X=x\right)\qquad \forall x\forall \widehat{\theta}$$
Per la legge delle probabilità totali: $$P\left(\Theta\neq \widehat{\Theta}_\text{MAP}(X)\right)\leq P\left(\Theta\neq \widehat{\Theta}(X)\right)\qquad \forall \widehat{\theta}$$

### Stimatore ai minimi errori quadratici medi (LMS)
>[!note]
>L'obiettivo di questo stimatore è minimizzare l'errore quadratico medio: $$E\left[\left(\Theta-\widehat{\Theta}\right)^{2}\right]=h(\underbrace{c}_{\widehat{\Theta}})$$
>Si ha che: $$\frac{\text{d}}{\text{d}t}h(c)= \frac{\text{d}}{\text{d}t}\left(E\left[\Theta^{2}\right]-2cE[\Theta]+c^{2} \right)=0$$
>Da cui ricaviamo: $$c=E[\Theta]=\widehat{\Theta}_\text{LMS}$$
>Da questo risultato ricaviamo che: $$h(c=E[\Theta])=\text{Var}[\theta]=\text{MMSE}$$
>Dove $\text{MMSE}$ è il l'errore quadrato minimo medio.

>[!tip] Stima LMS di $\Theta$ basata sull'osservazione $X$
>Avendo due variabili aleatorie $\Theta$ e $X$, osserviamo $X=x$. In questo modo la LMS cambia: $$h(c)=E\left[(\theta-c(x))^{2}|X=x\right]$$
>Da cui: $$c(x)=E[\Theta|X=x]=\widehat{\Theta}_\text{LMS}(x)$$
>Il minimo errore quadratico medio è: $$E\left[\left(\Theta-\widehat{\Theta}_\text{LMS}(X)\right)^{2}\right]=E[\text{Var}[\Theta|X]]\leq\text{Var}[\Theta]$$
>

Si ha che: $$E\left[\left(\Theta-\widehat{\Theta}_{\text{LMS}}(x)\right)^{2}|X=x\right]\leq E\left[\left(\Theta - g(x)\right)^{2}|X=x\right]\qquad\forall x\forall g$$
Dove $g$ è uno stimatore qualsiasi. Di conseguenza: $$E\left[\left(\Theta-\widehat{\Theta}_{\text{LMS}}(X)\right)^{2}\right]\leq E\left[\left(\Theta - g(X)\right)^{2}\right]\qquad\forall g$$
Definiamo l'errore di stima come: $$\stackrel{\sim}{\Theta}=\widehat{\Theta}_\text{LMS}-\Theta$$
Si ha che: $$\begin{align*}
&E[\stackrel{\sim}{\Theta}]=0\\&E[\stackrel{\sim}{\Theta}\cdot h(X)]=0\\&\text{Cov}\left[\stackrel{\sim}{\Theta},\widehat{\Theta}_\text{LMS}\right]=0\implies \rho\left[\stackrel{\sim}{\Theta},\widehat{\Theta}_\text{LMS}\right]\\&\text{Var}\left[\stackrel{\sim}{\Theta}\right]=E[\text{Var}[\Theta|X]]
\end{align*}$$