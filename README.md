# opdracht2_wavelet

- uitschrijven van het bewijs van de equivalentie voor de admissibility condition (Eigenschap 7.2) via het stramien op de slides (leg elke stap uit)
- nagaan dat de indicatorfunctie op [0,1[ een MRA bepaalt (Voorbeeld 9.2)
- afleiden van de Haar wavelet via het Fourierdomein (Voorbeeld 9.15)

# Eigenschap 7.2

## Te Bewijzen

Admissibility condition:

$$
2\pi\int_{\mathbb{R}^{*}}{\frac{\left|{\widehat{\psi}}(a)\right|^{2}}{\left|a\right|}}da=:C_{\psi}<\infty
.
$$

$\forall \psi \in L^{2}, ||\psi|| =1 \text{ en } t \psi \in L^{1}: \text{Admissibility condition} \Leftrightarrow $

$$
\int_{-\infty}^{\infty}\psi(t)\,d t=0\qquad\mathrm{resp.}\qquad\widehat{\psi}(0)=0\ .
$$

## Bewijs

Door dat $t \psi \in L^{1}$ is $\widehat{\psi}$ continu afleidbaar (Lemma 2.17).
De middelwaarden stelling geeft: $\forall |z|\le 1,\exists |c(z)|\le 1 :$

$$
\begin{aligned}
  \widehat{\psi}(z) &= \widehat{\psi}(0)+\widehat{\psi}'(c) z \Rightarrow \\
  |\widehat{\psi}(z)|  &\ge  |\widehat{\psi}(0)| - |\widehat{\psi}'(c(z)) | |z| \\
  |\widehat{\psi}(z)|  &\le  |\widehat{\psi}(0)| + |\widehat{\psi}'(c(z)) | |z|
.
\end{aligned}
$$

Opmerking omdat $\widehat{\psi}'$ continu is op een compact interval is het ook eindig en is $|\widehat{\psi}'(c(z)) |$ ook eindig.

### Bewijs ($\Rightarrow$)

$$
\begin{aligned}
\infty &> 2 \pi \int_{\mathbb{R}^{*}} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da \\
&> 2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(0)|^{2} - 2 |a| |\widehat{\psi}'(c(a))||\widehat{\psi}(0)| + |a|^{2} |\widehat{\psi}'(c(a))|^{2}   }{|a|} da.
\end{aligned}
$$

De $2$ laatste termen zijn eindig dus irrelevant voor de ongelijkheid:

$$
\begin{aligned}
\infty &> \int_{-1}^{1} \frac{|\widehat{\psi}(0)|^{2}}{|a|} da \Leftrightarrow \\
\widehat{\psi}(0) &=0
.
\end{aligned}
$$

### Bewijs ($\Leftarrow$)

Krijg dit niet juist gerenderd in github, ik gebruik hier de andere ongelijkheid en de veronderstelling.

Stel dat $\widehat{\psi}(0) =0$.

$$
\begin{aligned}
& 2\pi \int_{\mathbb{R}^{*}} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da \\
&\le 2 \pi \int_{\mathbb{R}^{*} \setminus [-1,1]} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da\\
&\le 2 \pi \int_{\mathbb{R}^{*} \setminus [-1,1]} |\widehat{\psi}(a)|^{2} da +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da \\
&\le 2 \pi \int_{\mathbb{R}^{*} } |\widehat{\psi}(a)|^{2} da +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da\\
&\le 2 \pi \int_{\mathbb{R}^{*} } |\psi(a)|^{2} da +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da\\
&\le \text{eindig} +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}(a)|^{2} }{|a|} da\\
&\le \text{eindig} +2 \pi \int_{-1}^{1} \frac{|\widehat{\psi}'(c(a))|^{2} |a|^{2}  }{|a|} da\\
&\le \text{eindig} +2 \pi \int_{-1}^{1} |\widehat{\psi}'(c(a))|^{2} |a| da\\
&\le \text{eindig} + \text{eindig} \\
&< \infty.
\end{aligned}
$$

# Voorbeeld 9.2

(b) en (c) volgen bijna direct uit de definitie, bij (c) is ONB triviaal. <br>
De inclusies volgt uit de schalingsvergelijking (Stelling 9.4), $h_{0}=h_{1} = \frac{1}{\sqrt{2}}$. <br>
Volledigheid en separatie kunnen bewezen worden zoals in (Stelling 9.8) ze volgen er ook uit: <br>

$|\phi(t)| \le \frac{2}{1 + t^{2}} $, $|\int \phi(t)dt | = 1 $.

# Voorbeeld 9.15

$$
\begin{aligned}
& \int_{0}^{0.5} e^{itz} dt - \int_{0.5}^{1} e^{itz} dt   \\
&=\frac{1}{iz} \left( 2 e^{\frac{iz}{2}} - 1 - e^{iz} \right) \\
&=\frac{e^{\frac{iz}{2}}}{iz} \left( 2  - e^{\frac{-iz}{2}} - e^{\frac{iz}{2}} \right) \\
&=\frac{e^{\frac{iz}{2}}}{iz} \left( 2  - 2 \cos\left( \frac{z}{2}\right) \right) \\
&=\frac{4 e^{\frac{iz}{2}}}{iz} \sin^{2}\left(\frac{z}{4}\right)
.
\end{aligned}
$$
