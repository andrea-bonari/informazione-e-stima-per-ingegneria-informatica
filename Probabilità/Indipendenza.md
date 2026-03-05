>[!note]
>Dati due generici eventi $A,B\in\Omega$. Si ha che $A$ e $B$ sono indipendenti se:
>$$A\perp B\iff P(A\cap B)=P(A)\cdot P(B)$$
>Intuitivamente questo significa che l'accadere di $A$ non porta informazione sull'accadere di $B$.

Una definizione più intuitiva potrebbe essere:
$$A\perp B\iff P(B|A)=P(B)$$
Tuttavia questa non gestisce casi limite come gli insiemi vuoti.

Si nota che:
$$A\cap B\neq\emptyset\implies A\not\perp B$$
### Indipendenza condizionata
>[!note]
>Siano dei generici eventi $A,B,C\in\Omega$, con $A\perp B$. Si ha che:
>$$A,B\text{ condizionatamente indipendenti per }C\iff P(A\cap B|C)=P(A|C)\cdot P(B|C)$$

Si noti che l'indipendenza non implica l'indipendenza condizionata, e l'indipendenza condizionata non implica l'indipendenza.

### Indipendenza totale
>[!note]
>Siano dei generici eventi $A_{1},\cdots,A_{n}\in\Omega$. Questi eventi si dicono indipendenti se e solo se:
>$$P(A_{i}\cap A_{j}\cap\cdots\cap A_{k})=P(A_{i})P(A_{j})\cdots P(A_{k})\qquad \forall \set{A_{i}, A_{j},\cdots, A_{k}}\subseteq\set{A_{1},A_{2},\cdots, A_{n}}$$
>Talvolta, questa condizione può essere troppo forte, e pertanto si adottano definizioni come l'indipendenza a $n$-uple, che limita la condizione a sottoinsiemi di cardinalità $n$.
>
>Un indipendenza totale implica l'indipendenza di tutte le indipendenze a $n$-uple.




