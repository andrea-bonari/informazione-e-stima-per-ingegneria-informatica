>[!note]
>Sia $X$ una variabile aleatoria con legge di probabilità: $f_{X}$. Sia inoltre $Y=g(X)=aX+b$, con $a,b$ constanti note e $a\neq0$.
>In generale, si ha che: $$f_{Y}(y)=f_{X}\left( \frac{y-b}{a}\right)\cdot \frac{1}{|a|}\qquad \forall a\in\mathbb{R}\smallsetminus\set{0}\quad\forall b$$

>[!tip] Metodo diretto
>Sia $Y=g(X)$, con $g$ funzione nota, deterministica e strettamente monotona. Siano inoltre due eventi $\set{x\leq X\leq x+\delta_{X}}$ e $\set{y\leq Y\leq g(x+\delta_{X})}$. Espandendo il secondo evento con Taylor possiamo dire che:
>$$\set{g(x)\leq Y\leq g(x+\delta_{X})}\approx\set{g(x)\leq Y\leq g(x)+\underbrace{\delta_{X}\cdot \left|\frac{\text{d}}{\text{dx}}g(x)\right|}_{\delta_{Y}} }$$
>Possiamo quindi dire che: $$P(x\leq X\leq x+\delta_{X})\approx P(g(x)\leq Y\leq g(x)+\delta_{Y})$$
>E di conseguenza: $$\delta_{X}f_{X}(x)\approx \delta_{Y}f_{Y}(g(x))$$
>Quindi: $$f_{Y}(g(x))= \frac{f_{X}(x)}{\left|\frac{\text{d}}{\text{d}x}g(x)\right|}$$
>Ricordando che $g$ è strettamente monotona, si ha che $x=g^{-1}(y)$, e quindi: $$f_{Y}(y)= \frac{f_{X}(g^{-1}(y))}{\left|\frac{\text{d}g}{\text{d}x}g^{-1}(y)\right|}$$

