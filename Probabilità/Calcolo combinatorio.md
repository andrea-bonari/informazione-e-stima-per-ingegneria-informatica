>[!note]
>Il calcolo combinatorio è la branca della matematica orientata all'ottenimento del numero di casi distinti che si possono presentare in un esperimento aleatorio, oppure il numero di elementi che compongono un insieme.

Spezziamo un esperimento aleatorio in un spazio campionario discreto in $r$ stadi di scelta, con $n_{i}$ numero di scelte nello stadio $i$-esimo. Si ha che:
$$\#\text{ totale di scelte}=\prod_{i=1}^{r}n_{i}$$
### Numero di sottoinsiemi
>[!note]
>Si ha che il numero totale di sottoinsiemi un insieme $A$ è:
>$$\#\text{totale di sottoinsiemi}=\prod_{i=1}^{r=|A|}n_{i}=2^{|A|}$$

### Permutazioni
>[!note]
>Sia $A$ un insieme con $n$ elementi distinti. Si ha che il suo numero di permutazioni (modi in cui si possono ordinare gli elementi di $A$) è:
>$$n!$$

### Combinazioni
>[!note]
>Sia $A$ un insieme con $n$ elementi distinti. Si ha che il numero di combinazioni dei suoi elementi (numero di sottoinsiemi non ordinati con $k$ elementi distinti) è:
>$$\binom{n}{k}= \frac{n!}{(n-k)!\cdot k!}$$
>Questo è definito come coefficiente binomiale.

>[!tip] Proprietà del coefficiente binomiale
>Si ha che:
>$$\sum\limits_{k=0}^{n}\binom{n}{k}=2^{n}$$

>[!tip] Disposizioni
>Definiamo il numero di sequenze ordinate di $k$ elementi presi da un insieme di $n$ elementi distinti come: $$\binom{n}{k}\cdot k!= \frac{n!}{(n-k)!}$$

### Probabilità binomiale
>[!note]
>Siano $n$ diverse prove indipendenti con una probabilità di successo binaria fissa nella singola prova $P(\text{successo})=p$. Si ha che: 
>$$P(\text{Particolari sequenze con }k\text{ positivi e }n-k\text{ negativi})=p^{k}(1-p)^{n-k}\binom{n}{k}$$

### Probabilità multinomiale
>[!note]
>Consideriamo il caso in cui si hanno $r$ casi di scelta.
>Si ha che: $$n=n_{1}+n_{2}+\cdots+n_{r}$$
>Dove $n_{i}$ sono quindi partizioni di $n$.
>Si ha che il numero totale di partizioni creabili è:
>$$\binom{n}{n_{1},\cdots,n_{r}}=\frac{n!}{n_{1}!\cdots n_{r}!}$$

