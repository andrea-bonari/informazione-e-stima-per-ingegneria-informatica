>[!note]
>Siano $A$ e $B$ due eventi generici. Definiamo la probabilità condizionata di $A$ dato $B$, $P(A|B)$ come la probabilità che avvenga l'evento $A$ data la certezza che $B$ si verifichi:
>$$P(\underbrace{A}_{\text{Evento di interesse}}|\underbrace{B}_{\text{Evento condizionante}})= \frac{P(A\cap B)}{P(B)}$$
>Questa è valida se e solo se $P(B)>0$, e quindi $B\neq\emptyset$.

Nel caso $P(A|B)$, è come se $B$ diventasse il nuovo spazio campionario, e pertanto le probabilità possono essere interpretate come una rinormalizzazione delle probabilità iniziali, tendendo comunque validi gli assiomi fondamentali:
$$P(A\cap B|C)=P(A|C)+P(B|C)$$

Alcuni risultati notevoli sono:
$$\begin{align*}
P(A|A)&= 1\quad &\forall A\neq\emptyset\in \Omega\\
P(A|\Omega)&= P(A)\quad&\forall A\neq\emptyset\in \Omega\\
P(A|B)&=0\quad &\forall A,B\neq\emptyset\in\Omega&\quad A\cap B=\emptyset
\end{align*}$$

Inoltre, si ha che:
$$P(A)\cdot P(B|A)=P(B)\cdot P(A|B)$$

>[!tip] Definizione alternativa
>Si ha che: $$P(A\cap B)= P(B|A)\cdot P(A)= P(A|B)\cdot P(B)$$
>Questa è valida anche per $P(A)=0$ o $P(B)=0$.

### Regola moltiplicativa
>[!note]
>Siano $A_{1},\cdots,A_{n}$ eventi generici. Si ha che:
>$$P\left(\bigcap_{i=1}^{n}A_{i} \right)=P(A_{1}) P(A_{2}|A_{1})P(A_{3}|A_{1}\cap A_{2}) \cdots P(A_{n}|A_{1}\cap\cdots\cap A_{n-1})$$

### Teorema delle probabilità totali
>[!note]
>Siano $A_{1},\cdots, A_{n}$ partizioni di $\Omega$. Si ha che:
>$$P(B)=\sum\limits_{i=1}^{n} P(A_{i})\cdot P(B|A_{i})$$

>[!tip] Partizioni
>Si definiscono $A_{1},\cdots,A_{n}$ partizioni di $\Omega$ se e solo se:
>$$\bigcup_{i=1}^{n}A_{i}=\Omega\qquad A_{i}\cap A_{j}=\emptyset\quad i\neq j$$

### Regola di Bayes
>[!note]
>Si ha che:
>$$P(A_{i}|B)=\frac{P(B|A_{i})P(A_{i})}{\sum\limits_{j=1}^{n}P(B|A_{j})P(A_{j})}$$
>Questa regola è importante per risolvere problemi di inferenza, e quindi conoscendo le probabilità degli scenari, e le probabilità di causa effetto, vogliamo calcolare la probabilità che sia stato lo scenario $i$-esimo a causare l'effetto $B$.

