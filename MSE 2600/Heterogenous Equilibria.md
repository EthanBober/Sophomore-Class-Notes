# Metal-Metal Oxide Reaction Equilibria

- For the reaction:

```math
\mathrm{Ni(s) + \frac{1}{2}O_2(g) = NiO(s)} 
```

- In the right direction, Ni is getting oxidized
- In the left, NiO is getting reduced
- In this situation, there are three possible cases emerge
  - Right Side Stable -> Pure NiO
  - Left Side Stable -> Pure Ni
  - Equilibrium -> Pure Ni + Pure NiO
- Note that in all three reaction, $O_2$ is always present; In the second case, its pressure would be lower 
- At equilibrium

```math
\Delta G =0: \mu_T\mathrm{Ni(s)} +\frac{1}{2}\mu_T\mathrm{O_2(g)} = \mu_T\mathrm{NiO(s)}
```

- For $O_2$ gas:

```math
\mu_T\mathrm{O_2}(g) = \mu \degree + RT \ln(\mathrm{O_2})
```

- Solids at equilibrium remain the same, as **solids cannot adjust there free energy with pressure*

- Therefor at equilibrium

```math
\begin{align*}
\Delta G \degree &= -RT \ln \left(\frac{1}{(\mathrm{pO_2})^{1/2}}\right) \\ &=RT \ln (pO_2)^{1/2} 
\end{align*}
```

> - In the equation, the log rule allows us to remove the negative by flipping the fraction, making the equation easier to handle in the process

- At a given T, the reaction is ONLY at equilibrium at one volume of $pO_2$ 
- If $PO_2 > PO_{2}:eq$, NiO is stable, *Ni cannot be present*
- If $PO_2 < PO_2:eq$, Ni is stable, *NiO cannot be present*
  - Basically, unless $O_2$ is consumed, the $\Delta G$ is stuck where it is as condensed phases cannot adjust there relative stability 
- Example: Calculate the equilibrium $pO_2$ at 1000K for the Ni/NiO reaction:

```math
\text{Ni(s) + } \frac{1}{2}\text{O}_2(g) = \text{NiO(s)}: \quad \Delta G^\circ = -244{,}550 + 98.5T
```

- Put in terms of one mole of $O_2$ so $pO_2$ can be directly found instead of having $\frac{1}{2}$ exponential

```math
2\text{Ni(s)} + \text{O}_2(g) &= 2\text{NiO(s)}: \quad \Delta G^\circ = -489{,}100 + 197T \\

```

- At eq.

```math
\quad \Delta G^\circ = -RT \ln\left(\frac{1}{p\text{O}_2}\right) = RT \ln p\text{O}_2
```

- So at 1000K,

```math
\Delta G^\circ = -489{,}100 + (1000)(197) = (8.314)(1000) \ln p\text{O}_2
```

- This yields a final answer of $pO_2$ = $5.52E10^{-16}$ 

# Ellingham Diagrams