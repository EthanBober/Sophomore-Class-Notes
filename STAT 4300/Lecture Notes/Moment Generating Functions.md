# Moment Generating Functions

- Chapter 6 of Textbook (some)

## Moments

> Definition: For any r.v. $X$ and any $n=1,2,3$ :
>
> - $n^{th}$ moment $m_n$: $\mathbb{E}[x^n]$ 
> - $n^{th}$ central moment $c_n$: $\mathbb{E}[\left(x-\mu\right)^n]$ 
> - $n^{th}$ standardized moment $s_n$: $\mathbb{E}[\left(\frac{x-\mu}{\sigma}\right)^n]$ 

- Example: $m_0=1$, $m_1 = \mu$, $E[x^2]$

- Example: $c_0 = 1, c_1=0, c_2= var[x]$

- You can interconvert from $m_n$ to $c_n$ via:

```math
\begin{align*}
c_2 = Var(x) = \mathbb{E}[(X-\mu)^2] = \mathbb{E}[X^2]-(\mathbb{E}[x])^2=m_2-m_1^2 \\
c_3 = \mathbb{E}[(X-\mu)^3] = \mathbb{E}[X^3-3X^2\mu+3X\mu^2-\mu^3] = m_3-3m_1m_2+3m_1^3-m_1^3
\end{align*}
```

- Main brunt of the simplification is via Linearity of Expectation

- Generally, to compute a moment

```math
\begin{align*}
m_n = \mathbb{E}[X^n]=\int_{-\infin}^{\infin}x^nf(x)
\end{align*}
```

- Or you can use the sum

## Moment Generation Function

- Rather than integrate or summate to find the moment, a useful tool is the *moment generating function*

> The MGF of a r.v X is $M_x(t)=E[e^{tx}] : t \in \real$  
>
> - The MGF exists if its finite for $t \in (-a,a)$ 

- Ex: MGF at t = 2 is $M_x(2)=E[e^{2x}]$

- Ex: MGF at t=0 is $M_x(0)=E[e^{0x}] = 1$ 

- Example: MGF of a Bernoulli Distribution

```math
\begin{align*}
M_x(t) &= \mathbb{E}[e^{tx}] = \sum_{k=0}^{k=1}e^{tx}*\mathbb{P}(X=k) \\ 
&= e^{t(1)}*(1-p)+e^{t*0}*p \\ 
&=pe^t+1-p
\end{align*}
```

- Example: MGF of Uniform

```math
\begin{align*}
M_u[e^{tu}] = \mathbb{E}[e^{tu}]&=\int_a^be^{tu}*\mathbb{P}(x=u)du \\
&= \int_a^be^{tu}*f(u)du \\
&=\frac{1}{b-a}\int_a^be^{tu}du \\
&= \frac{1}{b-a}\left(\frac{e^{tu}}{t}\right) \Big|^b_a \\
&= \frac{e^{bt}-e^{at}}{(b-a)t}
\end{align*}
```

- Example: MGF of Exponential

```math
X \sim \mathrm{Expo}[1]\\ 
\begin{align*}
M_x(t) = \mathbb{E}[e^{tX}] &= \int_{-\infin}^{\infin}e^{tx}f(x)\mathrm{d}x \\ 
&=\int_{0}^{\infin}e^{tx}e^{-x} \\ 
&=\int_{0}^{\infin}e^{(t-1)x}\\ 
&=\frac{e^{(t-1)x}-1}{t-1} \Big|^\infin_0\\ 
&=\frac{e^{(t-1)\infin}-1}{t-1}
\end{align*}
```

- If t > 0, the MGF will become infinity
  - Finite below zero
  - Hence:

```math
\begin{align*}
\begin{cases*}
\frac{1}{1-t} & t<0 \\
\infin & t>0
\end{cases*}
\end{align*}
```

- To go from MGF to moments

```math
\begin{align*}
\mathbb{E}[X] = M^{(n)}(0)
\end{align*}
```

- Or in other words take the derivative n times, plug in t = 0
- Example: For $X \sim \mathrm{Ber(p)}$ 

```math
\begin{align*}
\mathbb{E}[X'] = \frac{d}{dt}(pe^t+1-p)=pe^t=p
\end{align*}
```

- Example: For $X \sim \mathrm{Expo(1)}$ 

```math
\begin{align*}
\mathbb{E}[X'] &= \frac{d}{dt}(\frac{1}{1-t})\\ 
&=-1(1-t)^{-2}(-1)\big|_{x=0}\\ 
&=1
\end{align*}
```

- Why does the MGF work?

```math
\begin{align*}
\frac{d}{dt}M_x(t)\big|_{t=0}&=\frac{d}{dt}\mathbb{E}[e^{tx}]\big|_{t=0}\\
&=\mathbb{E}[\frac{d}{dt}e^{tx}]\big|_{t=0} \\
&= \mathbb{E}[Xe^{tx}]\big|_{t=0}\\ 
&= \mathbb{E}[x]
\end{align*}
```

