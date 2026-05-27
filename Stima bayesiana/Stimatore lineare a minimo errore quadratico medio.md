>[!note]
>Consideriamo $\Theta$ come una variabile aleatoria continua. È possibile costruire una stima lineare in $X$ di $\Theta$: $$\widehat{\Theta}_\text{LIN}(X)=aX+b$$
>Per farlo bisogna trovare $a^{*}$ e $b^{*}$ in modo da minimizzare l'errore quadratico medio di stima: $$\begin{cases}
>a^{*}= \frac{\text{Cov}[X,\Theta]}{\text{Var}[X]} \\
>b^{*}= E[\Theta]-a^{*}\cdot E[X]
>\end{cases}$$
>E di conseguenza: $$\widehat{\Theta}_\text{LIN}(X)=E[\Theta]+ \frac{\text{Cov}[X,\Theta]}{\text{Var}[X]}\cdot(X-E[X])$$

Si ha che per trovare lo stimatore LMS devo solo valutare statistiche del primo ordine $E[\Theta]$ e $E[X]$, e del secondo ordine $\text{Cov}[X,\Theta]$ e $\text{Var}[X]$.

La formula precedente può essere riscritta come: $$\frac{\widehat{\Theta}_{\text{LIN}}-E[\Theta]}{\sigma_{TH}}=\rho[X,\Theta]\cdot \frac{X-E[X]}{\sigma_{X}}$$

>[!tip] Stima LMS lineare con più osservazioni
>Imponiamo di trovare una stima lineare nelle $X_{i}$, si ha: $$\widehat{\Theta}_\text{LIN}= a_{1}X_{1}+\cdots +a_{n}X_{n}+b\qquad\text{minimizzando } E\left[\left(\Theta-\widehat{\Theta}_\text{LIN} \right)^{2}\right]$$
>In modo analogo a prima, è possibile dimostrare che i coefficienti ottimi si calcolano da statistiche del primo e del secondo ordine di $\Theta$ e di $X_{1}$.

