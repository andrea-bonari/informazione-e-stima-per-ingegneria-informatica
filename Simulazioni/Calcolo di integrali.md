>[!note]
>È possibile calcolare un integrale difficile da valutare analiticamente o numericamente, usando una stima Monte Carlo dell'integrale:
>$$I=\int_{D}g(t)\text{ d}t=\int_{D}g(t)\frac{f_{X}(t)}{f_{X}(t)}\text{ d}t=E\left[\frac{g(X)}{f_{X}(x)}\right]$$
>Usando la media campionaria:
>$$\widehat{I}_{n}= \frac{1}{n}\sum\limits_{i=1}^{n}\frac{g(X_{i})}{f_{X}(x_{i})}\stackrel{P}{\to}E\left[\frac{g(X)}{f_{X}(x)}\right]=I$$
>Dove le $X_{i}\sim f_{X}$ sono le variabili aleatorie indipendenti e identicamente distribuite.