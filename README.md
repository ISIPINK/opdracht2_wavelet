# opdracht2_wavelet

- uitschrijven van het bewijs van de equivalentie voor de admissibility condition (Eigenschap 7.2) via het stramien op de slides (leg elke stap uit)
- nagaan dat de indicatorfunctie op [0,1[ een MRA bepaalt (Voorbeeld 9.2)
- afleiden van de Haar wavelet via het Fourierdomein (Voorbeeld 9.15)

# Eigenschap 7.2

## Te Bewijzen

Admissibility condition:
$2\pi\int_{\mathbb{R}^{*}}{\frac{\left|{\widehat{\psi}}(a)\right|^{2}}{\left|a\right|}}da=:C_{\psi}<\infty$

$\forall \psi \in L^{2}, ||\psi|| =1 \text{ en } t \psi \in L^{1}: \text{Admissibility condition} \Leftrightarrow $

$$
\int_{-\infty}^{\infty}\psi(t)\,d t=0\qquad\mathrm{resp.}\qquad\widehat{\psi}(0)=0\ .
$$

## Bewijs ($\Rightarrow$)

$\psi \in L^{1}$ dit volgt uit Cauchy-Schwarz en $\psi \in L^{2} \text{ en } t \psi \in L^{1}$:

$$
\begin{aligned}
\int_{\mathbb{R}} |\psi| dt &\le \int_{\mathbb{R} \setminus [-1,1]} |\psi| dt + \int_{-1}^{1} |\psi| dt \\
                            &\le \int_{\mathbb{R} \setminus [-1,1]} |t| |\psi| dt +  \sqrt{\int_{-1}^{1} |1|^{2}dt  \int_{-1}^{1} |\psi|^{2} dt} \\
                            &\le \infty .
\end{aligned}
$$

Hierdoor is $\tilde{\psi}$ continu en ook $|\tilde{\psi}|^{2}$. Stel dat $|\tilde{\psi}(0)|^{2} >  0  $ neem een $\delta$ omgeving rond $0$ waar dat
$|\tilde{\psi}|^{2}$ enkel verschilt met $\varepsilon >0$ dan is $\forall \varepsilon>0,\forall t \in [-\delta,\delta]:|\tilde{\psi}(t)|^{2} \ge   |\tilde{\psi}(0)|^{2} - \varepsilon$.
Maar

$$
\begin{aligned}
\int_{\mathbb{R}^{*}} \frac{|\tilde{\psi}(a)|^{2}}{|a|} da &\ge \int_{-\delta}^{\delta} \frac{|\tilde{\psi}(0)|^{2} - \varepsilon}{|a|}da \\
&\ge \infty .
\end{aligned}
$$

wat een contradictie is waardoor $|\tilde{\psi}(0)|^{2} = 0 \Rightarrow \tilde{\psi}(0) = 0$

## Bewijs ($\Leftarrow$)

# Voorbeeld 9.2

# Voorbeeld 9.15
