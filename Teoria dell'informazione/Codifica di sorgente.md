>[!note]
>È necessario rappresentare i risultati di un esperimento aleatorio con una stringa di bit, per farlo bisogna utilizzare delle codifiche.

>[!tip] Codeword prefix-free
>Per avere un codice disambiguo, ogni parola di codice non deve essere prefisso di altre parole di codice.

### Disuguaglianza di Kraft-McMillan
>[!note]
>È possibile trovare un codice prefix-free composto da $m$ codewords con lunghezze $l_{1},\cdots, l_{m}$ se e solo se: $$\sum\limits_{j=1}^{m}2^{-l_{j}}\leq 1$$

Da cui ricaviamo il seguente teorema: data una variabile aleatoria discreta $X$ con $m$ risultati possibili, per ogni codice prefix-free che assegna una codeword di $l_{j}\text{ bit}$ al risultato $X=x_{j}$ si ha: $$E[L]=\sum\limits_{j=1}^{n}l_{j}p_{X}(x_{j})\geq H(x)$$
In generale si ha che $l_{j}=\lceil i(x_{j})\rceil$ è quasi ottima.