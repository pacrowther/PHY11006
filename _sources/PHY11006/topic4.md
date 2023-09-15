# Topic 4: The First Law of Thermodynamics

# Introduction

In general, a thermodynamic system is a collection of objects that is convenient to regard as a unit,
and that may have the potential to exchange energy with its surroundings (e.g. popcorn kernels
heated in a pot expand and does work as it exerts an upward force and moves the lid). Such a process,
in which there are changes in the state of a thermodynamic system is a thermodynamic process.
The first law of thermodynamics relates heat supplied, work done and internal energy. In fact, it is
simply a statement of energy conservation:

<div class="alert alert-block alert-info">
The total energy of an isolated system is constant
</div>

Here, an __isolated system__ is one which is not in any sort of contact with the outside world: it is not
exerting or subjected to any forces, it is not supplying or being supplied with heat or any other form
of energy. In this form, the law seems like a statement of the obvious. The first law is more useful if
we permit some contact with the outside world

<div class="alert alert-block alert-info">
The change in the internal energy of a system is equal to the heat supplied to
the system plus the work done on the system.
</div>

This can be expressed mathematically as

```{math}
:label: eqn4.1
\Delta U = Q + W.
```
where U is the change in internal energy, Q is the heat supplied to the system, and W is the work
done on the system. Note the sign conventions here: if the system actually radiates heat, Q < 0, and
if the system does work on its surroundings, W < 0.

# Heat and work

Both heat and work are forms of energy. Heat is the energy that flows between two systems in thermal contact with each other if they are not 
in thermal equilibrium, i.e. heat flow results from a difference in temperature. We have seen that the temperature of a body is related to 
the average kinetic energy of its constituent atoms, so we can comclude that _heat is energy transfer associated with random motion of 
atoms_. 

Work, on the other hand, is energy transfer associated with _directed_ motion, and in particular with the application of a force. In one 
dimension, we can write

$$
W = \int F dx.
$$

In the next section, we will see that we need to treat this integral with great care, because it is __path dependent__. Suppose I need to 
move a box from my office (E43) to Clive Tadhunter's office (E37), which is no the other side of the mid-corridor fire door. If I can simply 
move it the 10 m or so down the corridor, I will have done some amount of work $F \Delta x$ where $\Delta x$ in this case is 10 m. However, 
if the fire door is jammed shut because of some fault, and I have to talk down several  flights of stairs to the Hicks SE exit, up  
Hounsfield Road, into the main tntrance on D floor, up the stairs to E floor, and along the  corridor to E37, I will have done considerably 
more work to achive the same end result.

The same is true of heat: the amount of heat I need to suppply to raise the temperature of an object by a certain amount $\Delta T$ depends 
on the way that I do it, in other words the path that the temperature takes from $T$ to $T + \Delta T$. This patth dependence of heat and 
work turns out to be critical to practical applications of thermodynamics, as we shall see later in the course. The difference betwqeen the 
ordered motion of work and the disordered motion of heat is also very important, as we will see when we consider the Second Law and the 
concept of entropy.

## Some examples of work

In general, we have, for a force $F$ applied over a small displacement $\Delta x$, $\Delta W = F \Delta x$. (This is assuming that the force 
and the displacement are parallel; if they are not we need to write $\Delta W = {\textbf F} \cdot \Delta {\textbf x}$ where 
$\textbf{F}$ and $\Delta \textbf{x}$ are vectors). 

For gases, it is usually more useful to work in terms of presure: since $f = PA$ where $A$ is the area over which the pressure acts, the 
work done by pressure $P$ is $ PA \Delta x = P \Delta V$, whre $\Delta V$ is the change in the volume of the gas. Note that the work done 
__on__ the gas, which is what we usually for the First Law is equal to $- P \Delta V$.

Other forms of work include stretching a spring, where $\Delta W = f \Delta L$ where $f$ is the first applied to the spring and $\Delta L$ 
is the change in its length, expanding a liquid droplet ($\Delta W = \gamma \Delta A$ where $\gamma$ is the surface tension and $\Delta A$ 
is the change in aread), applying an electric field to a charged particle, and so on. In the rest of this course we sgall usually be using 
$-P \Delta V$, but it is important to remember that the First Law does not _only_ apply to expanding gases!

# Internal energy

The internal energy of a system is the total energy of its constituent particles. This includes the translational, rotational and 
vibrational energy that we considered in Section {ref}`topic3-heat-capacity`, and also the 
potential energy due to forces between atoms, which we neglected in the 
ideal gas but which are obviously important in liquids and solids.

Unlike heat and work, internal energy is a __function of state__: it is determined only be the current propoerties of the system, not by 
its history. If I take a system that is in state A (say, a gas with a specified $P, T$ and $V$) and by supplying heat and/or by doing work I 
take it to state B, the change in its internal energy _is not path dependent_: whatever combination of heat and work I applied, in whatever 
order, the change in the internal energy will be the same.

`````{admonition} Example 4.1
:class: dropdown

````{tab-set}
```{tab-item}  Question
One mole of a monatomic ideal gas, say argon, is enclosed in a contained which has one movable wall, so that the gas remains at the same 
pressure as the outside environment. (Neglect any frictional forces). The gas is heated at a constant pressure by an amount $\Delta T$.

* What is the work done on the gas?

* What is the change in the internal energy of the gas?

* What is the heat supplied to the gas?

* What is the relation between the molar heat capacity at constant pressure, $c_{P}$, and the molar heat at constant volume, $c_{V}$?
```

```{tab-item} Solution
If the gas is heated at constant pressure, then since $PV = RT$ (for one mole), tjhe colume must change. The amount of work doen _by_ the 
gas is $P \Delta V = R \Delta T$, so the amount of work done _on_ the gas is $-R \Delta T$. From Equation {eq}`eqn3.5`, we know that the 
change in the internal energy of the gas is $\Delta U = \frac{3}{2} N_{A} k_{B} \Delta T = \frac{3}{2} R \Delta T$. (As this is a monatomic 
ideal gas, its internal energy is just the kinetic energy of its atoms: there is no rotational or vibrational degrees of freedom to worry 
about).

Therefore from the First Law we have $Q - \Delta U - W = \frac{3}{2} R \Delta T - (- R \Delta T) = \frac{5}{2} R \Delta T$. 
But by definition we know $Q = c_{P} \Delta T$ where $c_{P}$ is the molar heat capacity at constant pressure, and at constant volume
we know that $\Delta U = Q = c_{V} \Delta T$ since no work is done. Therefore as we have previously deduced (Equation {eq}`eqn3.7`) 
$c_{V} = \frac{3}{2} R$ and so $c_{P} = \frac{5}{2} R = c_{V} + R$. Note that although a more complicated gas, such as isobutane from 
Example 3.2, would have a larger value of $c_{V}$, it would still be true that $c_{P} = c_{V} + R$, since the work done by the gas 
poressure would be the same (provided that the gas could be trated as an ideal gas).
```
````
`````

# Cyclic process

A process that eventually returns a system to its initial staret is called a cyclic process. For such a process, the final state is the same 
as the initial state, so the total internal energy change most be zero. If a net quantity of work $W$ is done on the system, an equal amount 
of work must have flowed into the system as heat $Q$.

Every day your body (a thermodynamic system) goes through a cyclic process. Heat is added by metabolizing food, and your body does work in 
breating, walking and other activiies. If you return to the same state at the end of the day, the net change in your internal energy is 
zero i.e. $\Delta U = 0$ so $Q = -W$.

`````{admonition} Example 4.2
:class: dropdown

````{tab-set}
```{tab-item}  Question
One gram of water (1 cm$^{3}$) becomes 1671 cm$^{3}$ of steam when boiled at a constant pressure of 1 atm (101 kPa). Compute (i) the work 
done vaporizing the water and (ii) its increase in internal energy. (Note the heat of vaporization at this pressure is $L_{V} = 2.26 \times 
10^{6}$ J/kg
```

```{tab-item} Solution
The water does work $P (V_{2} - V_{1}) = 1.67 \times 10^{2}$ J so the work done on the water is $W = - 1.67 \times 10^{2}$ J. From Eqn 
{eq}`eqn2.6` $Q = m L_{V} = 2.26 \times 10^{3}$ J.The first law of thermodynamics holds for thermodynamic processes of all kinds,
$\Delta U = Q + W  = 2.09 \times 10^{3}$ J. Over 90% of the heat remains in the system as an increase in internal energy, with the remainder 
leaving the system as it expands from liquid to vapour.
```
````
`````

