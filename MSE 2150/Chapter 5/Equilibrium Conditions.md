# Equilibrium Conditions

## Contact Potential

- Consider two separate doped materials - p and n types

- Upon joining the two, the concentration gradient between holes and electrons in the two regions causes mobile charge carriers to diffuse into each other

  - Thus, holes from the p-side will diffuse to n and electrons from the n-side will diffuse to p

- However, this cannot happen indefinitely

  - Since the particles are charged, crossing over the junction leaves behind space charges
  - The space charges themselves are the uncompensated donor and acceptor atoms
  - The electrons leaving the n side leaves behind positive charge carriers $N_d^+$, and the holes leaving the p side leaves behind negative charge carriers $N_A^-$

  ![image-20250330182505069](C:\Users\Ethan Bober\AppData\Roaming\Typora\typora-user-images\image-20250330182505069.png)

![image-20250330183443883](C:\Users\Ethan Bober\AppData\Roaming\Typora\typora-user-images\image-20250330183443883.png)

- Thus, $\mathcal{E}$ - electric field will be pointing from positive to negative - or from the n-doped side to the p-doped side

- At equilibrium, no next charge flow can occur

  - In other words, the diffusion current and the drift current must cancel out to zero
  - In math terms:

  $$
  J_p (drift) + J_p(diff.) = 0 \\ J_n(drift) + J_n(diff.) =0
  $$

  - Therefore, the electric field builds up to the point where the net current is zero

  - This electric field exists in some region *W*, and there is some equilibrium potential difference across the junction $V_0$

    - This potential is otherwise known as a built-in potential, specifically a contact potential since it arises from the *contact* of the two doped materials
    - This electric field is dictated by:

    $$
    \mathcal{E} = - \frac{d\mathcal{V(x)}}{dx}
    $$

    - Note that the electric field is the negative of the change in potential difference
      - As the potential goes from positive to negative, that will be the direction of $\mathcal{E}$
    - The contact potential separates the bands by the amount $qV_0$ in order to ensure that the fermi levels match throughout the junction

![image-20250330184542042](C:\Users\Ethan Bober\AppData\Roaming\Typora\typora-user-images\image-20250330184542042.png)

- The quantitative relationship between $V_0$ and the doping concentrations between each sides can also be found:

  - Skipping the boring details:

  $$
  \begin{align*}
  J_p(x) &= q[\mu_p p(x) \mathcal{E}(x) - D_p \frac{dp(x)}{dx}] = 0
  \end{align*}
  $$

- Plug in Einstein relation and integrate over the right bounds to get:

$$
V_0 = \frac{kT}{q} * \ln (\frac{p_n}{p_p})
$$

- Assuming that the material has $N_a$ acceptors and $N_d$ donors, we can plug in to get
  $$
  V_0 = \frac{kT}{q} \ln\frac{N_a}{n_i^{2}/N_d} = \frac{kT}{q} \ln\frac{N_a N_d}{n_i^{2}}
  $$

- Rearranging the equation for the ratio of $p_p$ and $p_n$:
  $$
  \frac{p_p}{p_n} = \frac{n_n}{n_p} = e^{\frac{qV_0}{kT}}
  $$

- which can be useful for calculating I-V characteristics

> An equation that comes up often from previous chapters is
> $$
> \begin{align*}
> n_0 &= n_i e^{\frac{E_f - E_i}{kT}} \\ 
> E_f - E_i &= kT \ln\frac{n_0}{n_i} 
> \end{align*}
> $$
> The equivalent relationship holds for holes, and lets you find the distance from the intrinsic level to the fermi level for both sides of the junction

## Equilibrium Fermi Level

- At equilibrium, the fermi level is constant throughout the material
  - If it wasn't, the carriers in one region would migrate to the region with a lower fermi energy level - which wouldn't be equlibrium
- From this conclusion and some derivation I won't write :joy: but boils down to equating $p$ ratio to e equation you get:

$$
qV_0 = E_{vp} - E_{vn}
$$

- which means to say that the contact potential / strength of the electric fields is equal to the difference in the energies of the valence bands at equilibrium
  - This makes sense, as the fermi level MUST be equal at equilibrium, so the potential caused will lift the bands to accomplish this
  - Another way to look at this is that the "chemical potential" of the electrons must be equal - which is kinda what the fermi level is saying

