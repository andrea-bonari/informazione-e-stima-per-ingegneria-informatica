Esistono diverse leggi che riguardano il caso in cui ci siano più variabili aleatorie nel caso continuo.

### Densità di probabilità congiunta
>[!note]
>Siano $X$ e $Y$ due variabili aleatorie continue. Queste sono congiuntamente continue se e solo se:
>$$P((x,y)\in S)=\iint_{(x,y)\in S}f_{X,Y}(x,y)\text{ d}x \text{ d}y$$
>Con: $$\begin{align*}
>&f_{X,Y}(x,y)\geq0\qquad \forall (x,y)\in\mathbb{R}^{2}\\
>&\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}f_{X,Y}(x,y)\text{ d}x \text{ d}y=1
>\end{align*}$$
>Cioè che la probabilità è il volume sotteso alla superficie descritta da $f_{X,Y}$ nel dominio $S$.

### Valore atteso
>[!note]
>Si ha che:
>$$E[g(X,Y,)]=\iint_{(x,y)\in\mathbb{R}^{2}}g(x,y)\cdot f_{X,Y}(x,y)\text{ d}x \text{ d}y$$

### Legge marginale di probabilità
>[!note]
>Definiamo la densità marginale di $X$ rispetto a $f_{X,Y}$ come:
>$$f_{Y}(y)=\int_{-\infty}^{+\infty}f_{X,Y}(x,y)\text{ d}y$$
>La densità marginale di $Y$ rispetto a $f_{X,Y}$ è analoga.

### Indipendenza tra 2 variabili aleatorie continue
>[!note]
>Siano $X$ e $Y$ due variabili aleatorie continue. Queste sono dette indipendenti se e solo se: $$X\perp Y\iff f_{X,Y}(x,y)= f_{X}(x)\cdot f_{Y}(y)\qquad \forall (x,y)\in\mathbb{R}^{2}$$

### Densità di probabilità condizionata
>[!note]
>Si ha che: $$f_{Y|X}(y|x)= \frac{f_{X,Y}(x,y)}{f_{X}(x)}= \frac{f_{X,Y}(x,y)}{\int_{\mathbb{R}}f_{X,Y}(x,t)\text{ d}t}$$

### Regola di Bayes continua
>[!note]
>Siano $X$ e $Y$ due variabili aleatorie continue. Si ha che: $$f_{X|Y}(x,y)= \frac{f_{Y|X}(y|x)f_{X}(x)}{f_{Y}(y)}$$

Questa regola vale anche se si combinano variabili aleatorie discrete o continue.
