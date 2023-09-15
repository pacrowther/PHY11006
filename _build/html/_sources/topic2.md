# Topic 2: Heat and Heat Transfer

# Introduction

We said earlier that heat flows from a hotter body to a cooler body, but what is heat?
Heat is a form of energy. We have said that the temperature of a body is a measure of the average
kinetic energy of its component atoms, so to increase the temperature of a body we must add to this
kinetic energy. This is what we do when we supply heat, so heat must be another form of energy.
The science of thermodynamics, which we will study in this course, is largely the science of how heat,
work and the internal energy of a material are converted into each other so as to drive engines, initiate
chemical reactions, etc.

# Heat transfer mechanisms


How is heat transferred? There are three possible mechanisms: __convection__, __conduction__ and __radiation__.


## Convection

Convection is the transfer of heat by the net bulk motion of fluid (liquid or gas). Examples of heat
transfer by convection include boiling water in a kettle, weather systems and cooling fans. We can
divide convection systems into two categories: _natural_ convection and _forced_ convection.

Natural convection occurs when a heated fluid expands (thermal expansion). The expanded fluid is
less dense than the surrounding, cooler, fluid. The less dense fluid rises and the cooler, denser fluid
sinks. This results in a __cyclical convection__ current. An everyday example of this is in central heating
systems. The warm air rises above the radiator and the cold air (e.g. near a window) sinks, setting up
a convection current cycle.

Fluid __viscosity__, i.e. the resistance of the fluid to deformation, slows the fluid flow near solid surfaces,
resulting in a surface layer of more static fluid (e.g. air) that has an insulating effect. This is one reason
why wind gives _wind chill_ - it removes part or all of this static layer.
Forced convection occurs when the motion of hot or cold fluid is produced by external means, e.g. a
pump or fan. Forced convection can be a very efficient method of transferring heat, and has many
practical applications, e.g. fan oven, cooling fans in laptops, car engines, etc.

## Conduction

Conduction is the transfer of energy between atoms in a substance. Unlike convection, there is no
bulk motion; instead, collisions at the atomic scale cause the transfer of heat. The atoms of the higher-
temperature material have higher average kinetic energy, so collisions between them and the atoms
of the lower-temperature material tend to transfer energy from hotter to cooler, increasing the
velocity and kinetic energy of the cooler atoms and therefore their temperature.
Conductive heat flow is driven by temperature gradient: the greater the difference in average kinetic
energy, the more energy will be transferred in each collision. This is described by the __heat flow equation__,

```{math}
:label: eqn2.1
H = \frac{dQ}{dt} = -k A \frac{dT}{dx},
```

where $H$ is the heat current, i.e. the derivative of heat $Q$ with respect to time $t$, $A$ is the cross-sectional
area through which the heat flows and $k$ is the __thermal conductivity__ of the material. The negative
sign indicates that the direction of heat flow is from hot to cold. Since heat is a form of energy, $H$
(energy per unit time) is measured in watts; $k$ is measured in W/m/K.

Thermal conductivity is a property of the material, and depends on the efficiency with which its atoms
can transfer kinetic energy to their neighbours. Metals generally have high thermal conductivity,
because the free electrons that carry electrical current can also transfer kinetic energy. In non-metallic
crystals, kinetic energy is transferred by vibrations in the crystal lattice, and this can also be very efficient 
(diamond, for example, has an extremely high thermal conductivity). In contrast, gases have low
thermal conductivity, because collisions between gas atoms are uncommon - see {numref}`thermal-conductivities`.

```{margin} 
Table entries from Table 17.5 of University Physics with Modern Physics (Pearson), aside from glass and air
```

```{list-table} Thermal conductivities
:header-rows: 1
:name: thermal-conductivities
* - Substance 
  - $k$ (W m$^{-1}$ K$^{-1}$)
* - Aluminium 
  - 205.0
* - Copper
  - 385.0
* - Steel
  - 50.2
* - Glass
  - 0.96
* - Ice
  - 1.6
* - Air
  - 0.026
```

`````{admonition} Example 2.1
:class: dropdown

````{tab-set}
```{tab-item} Question
Window glass has a thermal conductivity of 0.96 W/m/K. If the inside temperature is 25$^{\circ}$ C and the
outside temperature is 10$^{\circ}$ C, what is the rate of heat loss through a 1.00 m$^2$ window made of 2.5 mm
thick glass? How is this modified if the window is made of a double-glazed unit consisting of two panes
of 2.5 mm thick glass separated by a 5 mm air gap (the thermal conductivity of air is 0.026 W/m/K?
```

```{tab-item} Solution
The first part is straightforward. We assume that the temperature decreases linearly through the
glass, so $dT/dx = \Delta T/ dx = -15/0.0025 = -6000$ K/m. Therefore $H = 1.00 \times 0.96 \times 60$ = 5800 W 
(rounding to two significant figures to match the precision of the input variables).

For the second part, we have three distinct regions of heat flow: the inner pane, the outer pane and the air gap. 
We know the temperature of the inner face of the inner pane and the outer face of the outer pane, but we do not know the other two 
temperatures. If we call the four temperature $T_1$, $T_2$, $T_3$ and $T_4$ (working from the inside out, so that $T_1 = 25^{\circ}$ C and 
$T_4 = 10^{\circ}$ C) we have $H_{12} = - k_{g} A \frac{T_{2} - T_{1}}{x_g}; H_{23} = - k_{a} A \frac{T_{3} - T_{2}}{x_a}; H_{34} = - k_{g} 
A \frac{T_{4} - T_{3}}{x_{g}}$ where $k_g, x_g$ are the conductivity and thickness of the glass, and $k_a, x_a$ of the air.

If the system has reached a steady state, we must have $H_{12} = H_{23} = H_{34}$, otherwise the air in the gap is either heating up or 
cooling down. Therefore $k_{g} \frac{(T_{2} - T_{1})}{x_{g}} = k_{a} \frac{(T_{3} - T_{2})}{x_{a}} = k_{g} \frac{(T_{4} - T_{3})}{x_{g}}$.
From the first and last terms of this, it is obvious that $T_{2} - T_{1} = T_{4} - T_{3}$. From the first two terms, 
$T_{3} - T_{2} = \frac{k_{g} x_{a}}{k_{a} x_{g}} (T_{2} - T_{1}) = 73.8 (T_{2} - T_{1}).$ Therefore
$T_{4} - T_{1} = (T_{4} - T_{3}) + (T_{3} - T_{2}) + (T_{2} - T_{1}) = 75.8 (T_{2} - T_{1})$. It follows that 
$T_{2} - T_{1} = -15/75.8 = -0.198$ K. We put this in our equation for heat flow to get 
$H = -0.96 \times 1.00 \times \frac{-0.198}{0.0025}$ = 76 W.

Double glazing is a very effective means of reducing heat loss!
```
````
`````

## Radiation

Any object at a temperature above absolute zero will emit electromagnetic radiation. This can come
from many sources: charged particles emit electromagnetic radiation when they are accelerated (and
if two atoms collide and change their velocities, they have undergone acceleration), electrons move
to lower energy states, molecules move to lower rotational or vibrational states, etc. If the material
is dense enough, the photons produced by these various processes will randomise their energies by
collisions until they reach a state where the photon energy distribution is independent of the material
composition and is determined purely by the temperature of the body. In the ideal case, this is known
as __blackbody__ radiation or __thermal__ radiation and the power emitted is

```{math}
:label: eqn2.2
H_{\rm BB} = \frac{dQ}{dt} = A \sigma T^{4}
```


where $A$ is the surface area of the emitting body and $\sigma$ is a constant known as Stefan's constant (or
the Stefan-Boltzmann constant); in SI units $\sigma = 5.670 \times 10^{-8}$ W/m$^2$/K$^4$.

Real bodies are less efficient emitters of electromagnetic radiation than the ideal blackbody (which is
defined as an object that is 100% efficient at emitting or absorbing radiation). This is described by the
emissivity $\epsilon$, which is a number between 0 and 1: a body with emissivity $\epsilon$ will radiate power

```{math}
:label: eqn2.3
H = A \epsilon \sigma T^{4}
```

The emissivity is a property of the material and of the nature of the surface: for example, highly
polished stainless steel has an emissivity of 0.075, but rough, weathered stainless steel has an
emissivity of 0.85. Generally, shiny, polished surfaces have very low emissivity and rough, dark
surfaces have high emissivity.

```{margin}
Values cited from the [Engineering Toolbox](https://www.engineeringtoolbox.com/emissivity-coefficients-d_447.html)
```

Since electromagnetic radiation can propagate in a vacuum, radiative heat transfer differs from convective 
and conductive heat transfer in not requiring the two bodies to be in physical contact - for
example, the Sun can heat the Earth by radiative heat transfer.

Thermal radiation has a continuous spectrum extending over the whole wavelength range, but the
wavelength of peak emission depends on the temperature according to __Wien's law__,

```{math}
:label: eqn2.4
\lambda_{\rm max} T = 2.989 \times 10^{-3} {\rm m K}.
```

At temperatures near room temperature, ~300 K, emission peaks around 10 $\mu$m, in the infrared part
of the spectrum. This is why cameras operating at infrared wavelengths are known as thermal cameras 
and can be used to measure temperature. It is worth noting that thermal cameras translate to
temperature using Equation {eq}`eqn2.2`, and therefore will not give accurate readings when pointed at shiny
surfaces with low emissivities.

# Heat capacity

Supplying heat to an object will, in general, raise its temperature. But what is the relationship between
the amount of heat supplied and the change in temperature? This is quantified by the heat capacity
of the object, $C$:

```{math}
:label: eqn2.5
Q = C \Delta T = mc \Delta T
```

where $Q$ is the heat supplied, $\Delta T$ is the resulting temperature change, $m$ is the mass of the object and
$c$ is the specific heat capacity. The SI units of $C$ are J/K, and of $c$, J/kg/K.
When dealing with gases, it is often useful to define the molar heat capacity, measured in J/mol/K
confusingly, this is also usually denoted $c$, so if you have a problem involving the heat capacity of a gas, make sure that you
know whether you are dealing with specific heat capacity or molar heat capacity.
The heat capacity at constant pressure, $C_P$, differs from the heat capacity at constant volume, $C_V$. This
difference is not generally important for solids and liquids, but is very significant for gases. The specific
heat capacity of a given material is also usually dependent on temperature; we will explore this later
in the course.

```{margin} 
Table entries from Section 19.2 of AQA Physics A level textbook (Oxford) plus ice.
```

```{list-table} Specific heat capacities
:header-rows: 1
:name: heat-capacities
* - Substance 
  - $c$ (J kg$^{-1}$ K$^{-1}$)
* - Aluminium 
  - 900
* - Copper
  - 390
* - Ice
  - 2100
* - Water
  - 4190
```


# Latent Heat

Supplying heat to an object does not always raise its temperature. Sometimes the energy will cause
the material to undergo a phase transition, such as melting, vaporisation, or ionisation. For example,
supplying heat to a mixture of ice and water at 0$^{\circ}$ C will not, initially, increase the temperature: instead,
it will cause the ice to melt. Only when all the ice has melted will the temperature of the water start
to increase (this is why we add ice to drinks to keep them cool). The heat required to cause a phase
transition is called the latent heat, is measured in J/kg, and is given by

```{math}
:label: eqn2.6
Q = mL
```

where $L$ is the (specific) latent heat and $m$ is the mass of material. The latent heat required to melt a
solid is called the latent heat of fusion ($L_{\rm f}$); that required to vaporise a liquid is the latent heat of vaporisation ($L_{\rm v}$. 
When a vapour condenses into a liquid, or a liquid freezes into a solid, the latent heat is released
back into the environment. This feature is commonly used in refrigeration systems, where the refrigerant 
enters the area to be cooled as a liquid, absorbs heat by evaporating into a vapour, and is subsequently 
condensed back into a liquid to release the waste heat.

Like specific heat capacity, latent heat is temperature-dependent. In particular, latent heat of vaporisation 
decreases with increasing temperature and will reach zero at the critical point of the material,
at which point the difference between the liquid and gas phases essentially disappears.


```{margin} 
Table entries from Table 17.4 of University Physics with Modern Physics (Pearson)
```

```{list-table} Latent heats of Fusion ($L_{f}$) and Vaporization ($L_{v}$) at 1 atmospheric pressure
:header-rows: 1
:name: latent-heat
* - Substance 
  - Melting point (K)
  - $L_{f}$ (J kg$^{-1}$)
  - Boiling point (K)
  - $L_{v}$ (J kg$^{-1}$)
* - Mercury 
  - 234
  - $11.8 \times 10^{3}$
  - 630 
  - $272 \times 10^{3}$
* - Water 
  - 273.15
  - $334 \times 10^{3}$
  - 373.15
  - $2256 \times 10^{3}$
* - Silver
  - 1233.95
  - $88.3 \times 10^{3}$
  - 2466
  - $2336 \times 10^{3}$
```


`````{admonition} Example 2.2
:class: dropdown

````{tab-set}
```{tab-item} Question
The half-litre bottle of water you carelessly left standing in the sunshine has reached a temperature of 35$^{\circ}$ C. You
decide to cool it to a more refreshing 10$^{\circ}$ C by adding ice cubes from your freezer. If each ice cube has a mass of 20 g and your 
freezer 
has a temperature of -18$^{\circ}$ C, how many ice cubes do you need to add?

(the specific heat capacity of liquid water is 4.2 kJ/K/kg, the specific heat capacity of ice is 2.1 kJ/K/kg and 
the latent heat of fusion of ice is 334 kJ/kg. The density of water is 1000 kg/m$^3$.)
```

```{tab-item} Solution
The heat loss by the water is $m c \Delta T = 0.50 \times 4.2 \times 25$ = 52.5 kJ. This is 
supplied to a mass $M$ of ice. The ice has to 
warm from -18$^{\circ}$ C to 0$^{\circ}$ C then melt, then warm as liquid water to 10$^{\circ}$ C. The total heat required is therefore $M 
\times (18 \times 2.1 + 334 + 4.2 \times 10) = 413.8 M$ kJ. If we equate this to the heat supplied by the water, we  find $M = 52.5/413.8 = 
0.127$ kg. 

Six ice cubes won't quite do it, so you need to add seven.
```
````
`````

