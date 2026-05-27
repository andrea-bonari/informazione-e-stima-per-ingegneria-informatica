>[!note]
>Siano $X_{i}$ variabili aleatorie indipendenti e identicamente distribuite con $\text{Var}[X_{i}]<\infty$ e siano: $$Z_{n}=\frac{X_{1}+X_{2}+\cdots+X_{n}-nE[X_{1}]}{\sqrt{n\text{Var}[X_{i}]}}\qquad Z\sim\mathcal{N}(0,1)$$
>Allora si ha che: $$F_{Z_{n}}(c)\stackrel{n\to\infty}{\to} F_{z}(c)=\Phi(c)\qquad\forall c\in\mathbb{R}$$
>Questo è detto Teorema fondamentale del limite (CLT).

Questo teorema vale per qualsiasi legge di probabilità di $X_{i}$, e si può usare per fare calcoli approssimati: $$F_{Z_{n}}\to F_{z}\implies Z_{n}\approx \mathcal{N}(0,1)\qquad\text{per }n\text{ sufficientemente grandi}$$
Consideriamo inoltre che: $$Z_{n}= \frac{S_{n}-n\mu}{\sqrt{n\sigma^{2}}}\implies S_{n}\approx\mathcal{N}\left(n\mu, n\sigma^{2}\right)$$
>[!tip] Problema del sondaggista
>Applichiamo il CLT al problema del sondaggista. Sia $f$ la frazione di persone che soddisfa un evento $A$. Il sondaggista seleziona un campione di $n$ persone a caso. Per la $i$-esima persona estratta poniamo il quesito e registriamo la risposta:
>$$X_{i}=\begin{cases}
>1\qquad&\text{Se }A\text{ è verificato per la persona }i\text{-esima} \\
>0&\text{Altrimenti}
>\end{cases}$$
>Con $X_{i}\sim\text{Bern}(f)$ e $X_{i}$ indipendenti ed identicamente distribuite. L'obiettivo del sondaggista è stimare con alta probabilità (ad esempio $95\%$) la stima di $f$ che cade in un intorno piccolo di $f$ (ad esempio $1\%$). Quindi: $$P(|M_{n}-f|\leq\underbrace{0.01}_\text{Accuratezza})\geq \underbrace{0.95}_{\text{Livello fiduciario}}$$
>
>Per prima cosa standardizziamo l'evento: $$\begin{align*}
>0.01&\leq |M_{n}-f|= \left| \frac{S_{n}}{n}- f\right|= \left|\frac{S_n-\overbrace{nf}^{E[S_{n}]}}{n}\right|\\
>&\implies\underbrace{\left|\frac{S_{n}-nf}{\sqrt{n}\sigma}\right|}_{Z_{n}}\geq \frac{0.01\sqrt{n}}{\sigma}\\
>&\implies P\left(|Z_{n}|\geq \frac{0.01\sqrt{n}}{\sigma}\right)
>\end{align*}$$
>Siccome $\sigma^{2}=f(1-f)\leq \frac{1}{4}$: $$\begin{align*}
P\left(|Z_{n}|\geq \frac{0.01\sqrt{n}}{\sigma}\right)&\leq P(|Z_{n}|\geq 0.02\sqrt{n})\\
&\approx P(|Z|\geq 0.02\sqrt{n})\qquad Z\sim\mathcal{N}(0,1)\\
&= 2(1-\Phi(0.02\sqrt{n}))\leq0.05\\
&\implies \Phi(0.02\sqrt{n})\geq0.0975\\
&\implies0.02\sqrt{n}\approx \Phi^{-1}(0.975)=1.96\\
&\implies n\geq \left(\frac{1.96}{0.02}\right)^{2} =9604
\end{align*}$$
>