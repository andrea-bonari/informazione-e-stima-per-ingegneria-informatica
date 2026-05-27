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

