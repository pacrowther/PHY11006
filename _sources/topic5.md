# Topic 5: Thermodynamic Processes

# Introduction

We have said that heat and work are path-dependent quantities: the amount of heat you need to
supply to a system, or the amount of work you need to do, to take it from state A to state B depends
on the path you take to get there. But what, in this context, do we mean by _path_?

Let's consider an ideal gas, with equation of state $PV = nRT$. (The same ideas will apply to any
system, but the variables we use to specify the system may be different.) For a fixed mass of gas, the
state of the gas is defined by any two of the variables ($P,V,T$), because we can always use the equation 
of state to find the third. So we can specify our initial and final states as points on a plot of $P$
against $V$. As the gas moves from state A to state B, it will pass through intermediate states, each of
which can also be specified as a point on the $PV$ plot. Therefore, any path between A and B is represented 
by a line joining A and B on the plot, and conversely any line joining A and B on the plot is a
possible - if not necessarily practical - way in which the gas could be taken from state A to state B by
supplying some combination of heat and work.

In general, these paths will not be analytically calculable - we'd have to model the system in a 
computer to work out exactly how to move the gas from state A to state B along some random wiggly path.
Therefore, we restrict our attention to those paths that lead to simple equations that we can solve.
This is, of course, what the 19th century developers of thermodynamics also did, since they had no
computers to do the calculations for them. Real applications of thermodynamics, e.g. real engines,
do not follow these simple paths, but it is often possible to construct an idealised version of the engine
that does, and this will give us some insight into how the engine performs. Later in the course we will
look at idealised versions of some typical engines, including steam engines, petrol engines and diesel
engines.

# Thermodynamic functions of state

To define the state of a system, we have to specify its properties. The properties that are useful for
this are the ones that do not depend on the prior history of the state: for example, we cannot use the
work done on a system to define its state, because the amount of work that has been done to put the
system into some state A depends on its history. Properties of a system that depend only on its current
state and not on its history are called __functions of state__. Examples of functions of state include 
pressure, temperature, volume, mass, density, magnetisation, electric charge, etc. Examples of variables
which are not functions of state include, as we have seen, history-dependent variables such as work
done and heat supplied, and also things that can change without changing the state, such as the kinetic
energy of one atom of a gas (the temperature depends on the average kinetic energy, not the kinetic
energy of one individual particle). The properties of a particular system may create relationships between 
functions of state, and these are called __equations of state__. The only equation of state we are
using in this course is the ideal gas law, but there are many others: for example, numerous modifications 
of the ideal gas law designed to make it a better representation of real gases (the best known
of these is the van der Waals equation of state, but there are many others), equations of state for
nuclear matter, used to model the behaviour of neutron stars in astrophysics, equations of state for
solid materials used to model their behaviour in the context of engineering or geology, and so on.


# Reversible and irreversible processes

If a system is left undisturbed for a long time, it will settle into equilibrium with its surroundings. In a system in equilibrium, all the 
functions of state have fixed, stable, well-defined values. If we slowly make an incremental change to one of the properties, say volume, 
the system will move from the original equilibrium to a new, very slightly different one. We can move it back to its original equilibrium by 
reversing the change, or we can continue to move it towards a new equilibrium in a different state. A slow process like this, where the 
system is never significantly out of thermal equilibrium, is called a __quasistatic process__.

In many cases, quasistatic processes are __reversible__: that is, if we reverse the direction of change, we can move the system back to its 
original state along the same path. This is not always true: for example, processes that involve friction are never reversible- there's no 
way that the heat you generated as you dragged that large box over the carpet can ever be collected together and reassembled into the work 
that was expended in doing the dragging, however slowly you did it.

Changes t=of state that involve _rapid_ changes to one or more functions of state are 
obviously not quasistatic, and in general are 
__irreversible__: for example: if you were to expand a volume of gas slowly by moving a piston, 
that would be reversible, but if you expand 
it rapidly by setting off an explosion, that would be irreversible. 
Most real thermodynamic processes are irreversible - you cannot refill 
your petrol tank by reversing the action of the engine. When we study the action of heat engines later in the course, we will use 
idealised paths on the $PV$ plot which _are_ quasistatic and reversible.

Given that the laws of physics are reversible, it may seem surprising that so many real-world processes are not Later inn the course we will 
explore this using the concept of __entropy__, and next year you will study the 
microscopic-level interpretation of entropy as part of 
statistical mechanics.

# The differential form of the First Law

In order to calculate the heat supplied and work done along a particular path on the $PV$ plot, 
we will use the differential form of the First 
Law. For an infinitesimal change $dU$ we have

```{math}
:label: eqn5.1
dU = \bar{d}Q + \bar{d}W
```

The symbol $\bar{d}$ indicates an __inexact differential__. For an __exact differential__ such as $dU$ we can write 
$\int_{x_{1}}^{x_{2}} dU = U(x_{2}) - U(x_{1})$, regardless of exactly how we do the integral. This is the same thing as saying that $U$ is 
a function of state. On the other hand, $Q$ and $W$ are not functions of state, so the result of doing such an integral over $\bar{d}Q$ or 
$\bar{d}W$ would depend on the path we took from $x_{1}$ to $x_{2}$.

In order to _do_ an integral over $\bar{d}Q$ or $\bar{d}W$, we need to express it in terms of variables that _are_ functions of state. For 
example, if we can write $\bar{d}W = -P dV$, and we can use an equation of state to relate $P$ to $V$ along a particular path, then we can 
calculate $W$ along the path, because both $P$ and $V$ are functions of state, so the integral 
is well-defined.

# Processes  with a constant function of state

One way to simplify our calculations is to consider processes where one of the relevant functions of state is held constant throughout the 
process. When we are using an ideal gas as our working fluid, the relevant functions of state are _pressure, temperature_ and _volume_.

## Isobaric processes

__Isobaric processes__ take place at constant __pressure__ (the word derives from the Greek for equal weight). On a $PV$ plot, an isobaric 
process is a horizontal line. Because the pressure is constant, calculating the work done in an isobaric process is simple

```{math}
:label: eqn5.2
W = -\int_{V_{i}}^{V_{f}} P dV = - P (V_{f} - V_{i}),
```

where $V_{i}$ and $V_{f}$ are the initial and final volumes respectively. Also by definition, $Q = C_{P} (T_{f} - T_{i})$, where $C_{P}$ is 
the heat capacity of the working fluid at constant pressure, The initial and final temperatures $T_{i}$ and $T_{f}$ can be calculated 
using 
the equation of state.

Isobaric processes are common in real life: if you heat something in an open container, the process is isobaric (but not, in general, either 
quasistatic or reversible - you can't un-cook something by refrigerating it!).

## Isothermal process

__Isothermal processes__ take place at constant __temperature__. For an ideal gas, since $PV = 
nRT$, an isothermal process on a $PV$ plot 
is a curve with $P \propto 1/V$. Since the internal energy of an ideal gas is determined by its temperature, $U$ does not change during an 
isothermal process, so $Q = -W$.

The work done during an isothermal process can be calculated by using $P = nRT/V$. Assuming a 
fixed mass of gas, $n$, $R$ and $T$ are all 
constant, so

```{math}
:label: eqn5.3
W = -\int_{V_{i}}^{V_{f}} P dV = - nRT \int_{V_{i}}^{V_{f}} \frac{dV}{V} = - nRT \ln \frac{V_{f}}{V_{i}}.
```

## Isochoric processes

__Isochoric processes__ take place at constant __volume__ (because the word isochoric, which comes from the Greek for equal space, is not 
common and is not obviously connected to volume, the work isovolumic is often used instead). An 
isochoric process is a vertical line on a 
$PV$ plot. Since the work done by a gas is $P \Delta V$ and $\Delta V = 0$, no work is done by the gas during an isochoric process, so 
$\Delta U = Q$. By definition, $Q = C_{V} (T_{f} - T_{i})$, where $C_{V}$ is the heat capacity of the working fluid at constant volume. 

`````{admonition} Example 5.1a
:class: dropdown

````{tab-set}
```{tab-item} Question
Suppose we take one mole of a monatomic ideal gas at pressure $P_1$ and volume $V_1$, and heat it at constant pressure until it reaches 
volume $V_{2}$. We then heat it at constant volume until it reaches pressure $P_2$. What are (i) the heat supplied; (ii) the work done; 
(iii) the change in internal energy?
```

```{tab-item} Solution
Let's label the four states A, B, C and D, where A is ($P_1, V_1$), B is ($P_1, V_2$), C is ($P_2, V_2)$ and D is ($P_2, V_1)$.

From the ideal gas law, $PV = nRT$, we see that $T_{A} = P_1 V_1 / R$, 
$T_{B} = P_1 V_2 /R$, $T_{C} = P_2 V_2 /R$ and $T_{D} = P_2 V_1 /R$. 
Since we have one mole of a monatomic ideal gas, the heat capacity at constant pressure is $C_{P} = \frac{5}{2} R$ and the heat capacity at 
constant volume is  $C_{V} = \frac{3}{2} R$.

The heat supplied going from A to B is $Q_{AB} = C_{P} (T_{B} - T_{A}) = \frac{5}{2} P_1 (V_2 - V_1).$ From B to C the heat supplied is 
$Q_{BC} = C_{V} (T_{C} - T_{B}) = \frac{3}{2} V_2 (P_2 - P_1).$ Therefore the total heat supplied is 

$$Q_{ABC} = \frac{5}{2} P_1 V_2 - 
\frac{5}{2} P_1 V_1 + \frac{3}{2} P_2 V_2 - \frac{3}{2} P_1 V_2 = \frac{3}{2} P_2 V_2 - \frac{5}{2} P_1 V_1 + P_1 V_2.
$$

There is no work done in the isochoric process from B to C, so the total work done _on_ the gas is just
$W_{AB} = - P \Delta V = P_1 (V_1 - V_2).$ The change in internal energy is $\Delta U = Q+ W = \frac{3}{2} (P_2 V_2 - P_1 V_1).$
```
````
`````

`````{admonition} Example 5.1b
:class: dropdown

````{tab-set}
```{tab-item} Question
If instead we first heat the gas at constant volume until it reaches pressure $P_{2}$ and then heat it at constant pressure until it 
reaches 
volume $V_{2}$, what are the heat supplied, work down and change in internal energy?
```

```{tab-item} Solution
If we start with the isochoric step $Q_{AD} = C_{V} (T_{D} - T_{A}) = \frac{3}{2} V_{1} (P_2 - P_1)$. Then the isobaric step gives
$Q_{DC} = C_{P} (T_{C} - T_{D}) = \frac{5}{2} P_{2} (V_2 - V_1).$ The total heat supplied is 

$$
Q_{ADC} = \frac{3}{2} P_2 V_1 - \frac{3}{2} P_1 V_1 + \frac{5}{2} P_2 V_2 - \frac{5}{2} P_2 V_1 = \frac{5}{2} P_2 V_2 - \frac{3}{2} P_1 V_1 
- P_2 V_1.
$$

There is no work done from A to D, to the total work done on the gas is $W_{DC} = - P \Delta V = P_2 (V_1 - V_2).$ The change in internal 
energy is $\Delta U = Q + W = \frac{3}{2} (P_2 V_2 - P_1 V_1).$

Note that the change in internal energy is the same in both cases, as it should be because internal energy is a function of state. However, 
the heat supplied and the work done both differ. If we were to combined this as a cycle ADCBA, running the first path in reverse, the net 
work done on the gas would be $(P_2 - P_1) (V_1 - V_2)$, i.e. the gas 
would _do_ net work $(P_2 - P_1)(V_2 - V_1)$ on its surroundings since 
$V_2 > V_1$. This is the basis on which __heat engines__ work: They convert heat to work by tracing out a closed cycle on the $PV$ plot.

Also note that since $PV = RT$ for one mole of gas, we can write $\Delta U = \frac{3}{2} R (T_{C} - T_{A}) = C_{V} \Delta T.$
This is what we should expect: we saw above that for an isochoric process $\Delta U = Q = C_{V} \Delta T$, and as $U$ and $T$ are
both functions of state, it must therefore always be true that $\Delta U = C_{V} \Delta T$.
 ```
````
`````

# Adiabatic processes

Isobaric, isochoric and isothermal processes are three of the simple paths we will use to construct idealised heat engines. The forth path 
is slightly different: instead of constraining one of the functions of state, we constrain one of the variables of the First Law, namely 
$Q$. An __adiabatic process__ is a reversible process in which there is no heat flow, i.e. Q$ = 0$ and $dU = \bar{d}W$. Note that an 
adiabatic process is _not_ isothermal: the internal energy of the working fluid does change but it changes because work is done, not 
because heat is supplied.

If the working fluid is $n$ moles of an ideal gas, we know that $dU = n c_{V} dT$, where $c_{V}$ is the molar heat capacity, and $\bar{d} W 
= - P dV$. Since $PV = nRT$, we can write 

$$
n c_{V} dT = - \frac{nRT}{V} dV,
$$ 

and separating variables gives 

$$
c_{V} \frac{dT}{T} = -R \frac{dV}{V}.
$$

We can now integrate this from $V_{i}$ to $V_{f}$ (corresponding to $T_{i}$ to $T_{f}$) to get 
$c_{V} \ln (T_{f}/T_{i}) = - 
R \ln (V_{f}/V_{i})$. Taking antilogs of this gives $T_{f}^{c_{V}} V_{f}^{R} = T_{i}^{c_{V}} 
V_{i}^{R}$.

Since we usually work in terms of $P$ and $V$ it is useful to eliminate $T (= PV/nR$). This gives

$$
P_{f}^{c_{V}} V_{f}^{c_{V}+R} = P_{i}^{c_{V}} V_{i}^{c_{V}+R}.
$$

But we know that $c_{P} = c_{V} + R$  (see Example 4.1), so we can write this as

$$
P_{f}^{c_{V}} V_{f}^{c_{P}} = P_{i}^{c_{V}} V_{i}^{c_{P}}.
$$

If we define the __adiabatic index__ $\gamma = c_{P}/c_{V}$, we can take 
the 
$c_{v}$-th root of this to obtain

```{math}
:label: eqn5.4
PV^{\gamma} = {\rm constant}.
```

using this and $PV = nRT$, we also have

```{math}
:label: eqn5.5
TV^{\gamma-1} = {\rm constant}.
```

and

```{math}
:label: eqn5.6
PT^{\gamma/(1-\gamma)} = {\rm constant}.
```

(not, of course, numerically the same constants!).

This allows us to determine the work done along an adiabatic path. If we know the initial pressure and volume, we can calculate $P_{i} 
V_{i}^{\gamma} = K$, say. Then

$$
W = - \int_{V_{i}}^{V_{f}} P dV = - K \int_{V_{i}}^{V_{j}} V^{-\gamma} dV = - \frac{K}{1-\gamma} 
[ V^{1-\gamma}]_{V_{i}}^{V_{f}} = 
\frac{K}{\gamma -1} \left( V_{f}^{1-\gamma} - V_{i}^{1-\gamma} \right).
$$

But since $P V^{\gamma}$ is constant, $K = P_{f} V_{f}^{\gamma}$ we can 
simplify this to

```{math}
:label: eqn5.7
W = \frac{1}{\gamma -1} (P_f V_f - P_i V_i).
```

Note that, because $Q = 0$, this must be equal to the change in internal energy $\Delta U = n c_{V} (T_f - T_i).$ This is easily verified 
using the ideal gas law. 


```{margin} Table entries from Table 19.1 of University Physics with Modern Physics (Pearson)
```

```{list-table} Molar Heat Capacities of Gases at Low Pressure
:header-rows: 1
:name: ratio-of-heat-capacities
* - Gas 
  - $c_{V}$ (J mol$^{-1}$ K$^{-1}$)
  - $c_{P}$ (J mol$^{-1}$ K$^{-1}$)
  - $\gamma = c_{p}/c_{v}$ 
* - He
  - 12.47
  - 20.78
  - 1.67
* - Ar
  - 12.47
  - 20.78
  - 1.67
* - H$_{2}$
  - 20.42
  - 28.74
  - 1.41
* - N$_{2}$
  - 20.76
  - 29.07 
  - 1.40
* - O$_{2}$
  - 20.85
  - 29.17
  - 1.40
* - CO
  - 20.85
  - 29.16
  - 1.40
* - CO$_{2}$
  - 28.46
  - 36.94
  - 1.30
* - SO$_{2}$
  - 31.39
  - 40.37
  - 1.29
```


Measured values of $c_{P}$ and $c_{V}$ are presented in {numref}`ratio-of-heat-capacities` for real gases at low pressures, together with 
the ratio of their heat capacities, $\gamma$. An ideal monatomic gas has $c_{V} = \frac{3}{2} R$ and $c_{P} = \frac{5}{2} R$ so $\gamma$ = 
5/3, in agreement with empirical results for helium and argon. For most diatomic gases at room temperature $c_{V} = \frac{5}{2} R$ and
$c_{P} = \frac{7}{2} R$ so $\gamma$ = 7/5, again in excellent agreement with empirical values for N$_{2}$, O$_{2}$, CO.

`````{admonition} Example 5.2
:class: dropdown

````{tab-set}
```{tab-item} Question
One mole of nitrogen, initially at a pressure of 101 kPa and a temperature of 25$^{\circ}$ C, is adiabatically compressed to half its 
original  volume. What are its final pressure and temperature? How much work has been done? 

(Nitrogen gas is a diatomic molecule, and at room  temperature it has $\gamma$ = 7/5.)
```

```{tab-item} Solution
Since the final volume is half the initial volume, $P_{f}  = P_{i} V_{i}^{\gamma} / V_{f}^{\gamma} = 2^{\gamma} P_{i}$ = 267 kPa.

Likewise, using Equation {eq}`eqn5.5`, $T_{f} = T_{i} V_{i}^{\gamma -1}/V_{f}^{\gamma -1} = 2^{\gamma -1} T_{i}$ = 393 K = 120$^{\circ}$ C.

The initial volume is $V_{i}  n R T_{i} / P_i} = 1 \times 8.31 \times 298 / 101000$ = 0.0245 m$^{3}$ so that the work done is $W = 
\frac{5}{2} \left( (267000/2) - 101000 \right) \times 0.0245$ = 1.99 kJ.
```
````
`````

In real life, adiabatic processes are often _fast_ processes: no heat is transferred because the system does not have time to reach 
equilibrium. However, when we do calculations in this course, we shall assume that adiabatic processes take place slowly and reversibly 
within a container that is completely insulated from its surroundings, so that no heat flows in or out.

`````{admonition} Example 5.3
:class: dropdown

````{tab-set}
```{tab-item} Question
A typical bedroom contains about 2500 moles of air. Find the change in the internal energy of this much air when it is cooled from 
35.0$^{\circ}$ C 
to 26.0$^{\circ}$ C at a constant pressure of 1.0 atm. Treat the air as an ideal diatomic gas 
with $\gamma$ = 7/5.
```

```{tab-item} Solution
$$
c_{V}  = \frac{R}{\gamma - 1} = 20.79 {\rm K/mol/K}
$$
so $dU = n c_{V} dT = (2500) (20.78) (26.0 - 35.0) = -4.68 \times 10^{5}$ J. To cool 2500 moles of air by 9 degrees, an air conditioner 
needs to extract this much energy and transfer it to the air outside.
```
````
`````

