# Topic 6: Heat Engines

# Introduction

As we saw in example 5.1, tracing out a closed cycle on a $PV$ plot can result in a partial conversion of
heat into work (only partial, because not all the heat supplied is converted: some is output as waste
heat). Macroscopic kinetic energy is energy associated with organized, coordinated motions of many
molecules, whereas heat transfer involves changes in energy of disordered molecular motion.
Conversion of mechanical energy into heat involves an increase of disorder. As a prelude to the second
law of thermodynamics we will consider two classes of device: __heat engines__ are partly
successful in converting heat into work. Refrigerators are partly successful in transporting
heat from cooler to hotter bodies.

A heat engine is any device that takes in heat $Q_H$, converts some of it into work $W$, and outputs the
rest as waste heat $Q_C$ . The engine contains a __working fluid__ that undergoes various processes (heating,
cooling, compression, expansion) in the course of the cycle. In the heat engines we shall consider in
this course, we will assume that the working fluid is an ideal gas and that all the processes involved
are quasistatic and reversible. In real engines, this is not true: many real engine cycles, such as the
steam engine, rely in part on a phase change (the working fluid of a steam engine is water, which
spends part of the cycle as liquid water, part as water vapour, and part as liquid and vapour in
equilibrium), which means that the working fluid cannot be modelled as an ideal gas, and of course all
real engines lose some energy to irreversible processes such as friction. However, a number of
common engines can be reasonably well modelled as a cycle of reversible processes applied to an
ideal gas as working fluid, and we shall look at some of these in this section.

# Thermal efficiency of a heat engine

The __thermal efficiency__ of a heat engine, usually denoted $\eta$, is the fraction of the input heat that is converted into work in one 
complete cycle

```{math}
:label: eqn6.1
\eta = \frac{|W|}{Q_{H}}.
```

Here I have written $|W|$, because our First Law definition of $W$ is the work done _on_ the system, and the porpose of a heat engine is to 
_do_ work, so we expect $W < 0$. Since the engine returns to its initial state at the end of each cycle, and we know that $U$ is a function 
of state, we must have $\Delta U = 0$ at the end end of a cycle, and therefore $\Delta Q = Q_{H} - |Q_{C}| = |W|$. Again we write $|Q_{C}|$ 
because we defined $Q_{C}$ above as the heat _given out_ by the system, whereas in our definition of the First 
Law Q$ us always heat _supplied_ to the system. Substituting this into Equation {eq}`eqn6.1` gives

```{math}
:label: eqn6.2
\eta = 1- \frac{|Q_{C}|}{Q_{H}}.
```

 Obviously the aim of engine designers is to maximise $\eta$. 

{numref}`fig6.0` shows the operation of a petrol engine. First a mixture of 
air and petrol vapour flows into a cylinder through an open intake value while the piston descends, increasing the volume of the cylinder 
from a minimum of $V$ (when the piston is all the way up) to a maximum of $rV$ (when it is all the way down). The quantity $r$ is called the 
__compression ratio__. At the end of this _intake stroke_, the intake value closes and the mixture is compressed to volume $V$ during the 
_compression stroke_. The mixture is then ignited nby the spark plug, and the heated gas expands back to volume $rV$, pushing on the piston 
and doing work; this is the _power stroke_. Finally the exhaust valve opens, and the combustion products are pushed out (during the _exhaust 
stroke_), leaving the cylinder ready for the next intake stroke.


```{figure} Images/6_engine.png
:name: fig6.0
:alt: Cycle of a four-stroke internal-combustion engine.
:align: center
:width: 100%
Cycle of an internal-combustion engine. Source: Fig 20.5 from University Physics with Modern Physics (Pearson)
```


# Some idealised heat engines

```{figure} Images/6_Otto.png
:name: fig6.1
:alt: Otto cycle
:align: center
:width: 70%
The Otto cycle. Source: [Wikipedia](http://en.wikipedia.org/wiki/Otto_cycle#/media/File:P-V_Otto_cycle.svg)
```

## The Otto cycle

The __Otto cycle__ is an idealised version of the petrol engine. As shown in {numref}`fig6.1`, the Otto cycle consists of six processes, but 
the first and last do not affect the work done or the efficiency, and can be neglected.

In the Otto cycle, heat is added at constant volume in step 2-3 (this represents the injection and ignition of the fuel) and rejected at 
constant volume in step 4-1 (when the exhaust valve is opened). Work is done adiabatically _on_ the gas in step 1-2 as the piston moves up 
from BDC (bottom dead centre) to TDC (top dead centre), and _by_ the gas as it forces the poston back out in step 3-4. Although we think of 
a petrol engine as being driven by petrol, the working fuild is actually air, or more precisely a mixture of air and combustion products: 
the petrol powers the engine by supplying the input heat in step 2-3.

From Equation 6.2, the efficiency of the Otto engine is $\eta = 1 - \frac{T_4 - T_1}{T_3 - T_2}$, since the heat supplied at constant volume 
is $Q = C_{V} \Delta T$ and we assume that $C_{V}$ is the same in both steps (note that in a real  engine it won't be, since the working gas 
has a different chemical composition after ignition).

Since steps 1-2 and 3-4 are both adiabatic, we know from Equation {eq}`eqn5.5` that $T_{4} V_{1}^{\gamma -1} = T_{3} V_{2}^{\gamma - 1}$
and $T_{1} V_{1}^{\gamma -1} = T_{2} V_{2}^{\gamma - 1}$. Therefore we can write $T_{4} - T_{1} = T_{3} \left( 
\frac{V_{2}}{V_{1}}\right)^{\gamma-1}  - T_{2} \left (\frac{V_{2}}{V_{1}}\right)^{\gamma-1} = (T_{3} - T_{2} 
\left( \frac{V_{2}}{V_{1}} \right)^{\gamma-1}$, and hence we can simplify the efficiency to 

```{math}
:label: eqn6.3
\eta = 1 - \left( \frac{V_{2}}{V_{1}}\right)^{\gamma-1} = 1 - \frac{1}{r^{\gamma-1}},
```

where $r = V_{1} / V_{2}$ is the compression ratio. Therefore, to maximise the efficiency of a petrol engine, we should 
aim to maximise the compression ratio. This is limited by the fact that $T_{2} = T_{1} r^{\gamma-1}$: if we increae the compression ratio 
too much, the temperature inside the cylinder will increae to the point where the fuel ignites prematurely, before the spark. Typical 
compression ratios for petrol engines are around 10:1 (between 8:2 and 12:1).

## Diesel cycle

```{figure} Images/6_Diesel.png
:name: fig6.2
:alt: Diesel cycle
:align: center
:width: 70%
The Diesel cycle. Source: [Wikipedia](http://en.wikipedia.org/wiki/Diesel_cycle#/media/File:Diesel_cycle.svg)

```

The Diesel cycle, as its name suggests, is an idealised version of the diesel engine. The difference between the Diesel cycle and the Otto 
cycle is that the heating stage 2-3 takes place at constant pressure, rather than at constant volume as in the Otto cycle. The intake stroke 
(step 0-1) and exhaust stroke (step 4-0) shown in {numref}`fig6.1` do exist in the Diesel cycle, but have been omitted from 
{numref}`fig6.2`.

The thermal efficiency of a diesel engine is given by $\eta = 1 - \frac{C_{V} (T_{4} - T_{1})}{C_{P} (T_{3} - T_{2})}$. This is more 
complicated to work out than the petrol engine, because there are three volumes involved instead of two. We define the 
compression ratio $r = V_{1} / V_{2}$ as before, also also the __cut-off ratio__, $\alpha = V_{3} / V_{2}$. From the ideal gas law we deduce 
that it is also true that $\alpha = T_{3} / T_{2}$. 

From step 3-4 we deduce that $T_{4} V_{1}^{\gamma-1} = T_{3} V_{3}^{\gamma-1} = (\alpha T_{2}) (\alpha V_{2})^{\gamma-1} = \alpha^{\gamma} 
T_{2} V_{2}^{\gamma-1}.$ From step 1-2 we have $T_{1} V_{1}^{\gamma-1} = T_{2} V_{2}^{\gamma-1}$, so $T_{4} - T_{1} = \left( 
\frac{V_{2}}{V_{1}}\right)^{\gamma-1} (\alpha^{\gamma} - 1) T_{2} = \frac{\alpha^{\gamma} - 1}{r^{\gamma-1}} T_{2}$
and $T_{3} - T_{2} = (\alpha -1) T_{2}$; Hence

```{math}
:label: eqn6.4
\eta = 1 - \frac{C_{V}}{C_{P}} \frac{1}{r^{\gamma-1}} \frac{\alpha^{\gamma} - 1}{\alpha -1} = 1 - \frac{1}{r^{\gamma-1}} 
\frac{\alpha^{\gamma} - 1}{\gamma (\alpha - 1)}.
```

How does this compare with the efficiency of the Otto cycle? 

If we write $\beta = \alpha -1$ then $\alpha^{\gamma} = (1+\beta)^{\gamma} = 1 + \gamma \beta + \frac{1}{2} \gamma (\gamma - 1) \beta^{2} + \cdots > 1 + \gamma \beta,$
since both $\alpha$ and $\gamma$ are greater than 1. Therefore

$$
\frac{\alpha^{\gamma} - 1}{\gamma(\alpha - 1)} > \frac{\gamma \beta}{\gamma \beta} = 1,
$$

so for the same compression ratio, $r$, the Otto cycle has a higher efficiency than the Diesel cycle. However, in practice diesel engines 
can run at higher compression ratios than petrol engines (between 14:1 and 23:1, so roughly double a typical petrol engine compression 
ratio), and the factor $\frac{\alpha^{\gamma} - 1}{\gamma(\alpha-1)}$ is not very much greater than 1 (typical values of $\alpha$ seem to be 
around 2, which for a diatomic working gas with $\gamma$ = 7/5 gives 1.17), so a typical diesel engine is likely to be more efficient than a 
typical petrol engine.

The value of $\alpha$ is contrained by $T_{3}$, which is set by the temperature at which the fuel will ignite: unlike a petrol engine, 
diseel engines have no need for spark plugs since the full ignites spontaneously when it reaches the appopriate temperature. Since 
$T_{2}/T_{1} = r^{\gamma -1}$, we can express $\alpha$ in terms of the compression ratio, $T_{1}$ and $T{3}$ by

```{math}
:label: eqn6.5
\alpha = \frac{T_{3}}{T_{2}} = \frac{T_{3}}{T_{1}} \frac{T_{1}}{T_{2}} = \frac{1}{r^{\gamma -1}} \frac{T_{3}}{T_{1}}
```
As $T_{1}$ and $T_{3}$ are reasonably well defined, this means that the cut-off ratio is not really an independent parameter; if we know 
the flame temperature $T_{3}$ and the inlet temperature $T_{1}$, it is set by the compression ratio.

(topic6-carnot)=
# The Carnot cycle: the 'perfect' heat engine

The best possible cycle for a heat engine was proposed in 1824 by the French physicist Sadi Carnot (1796-1832). The __Carnot cycle__ is 
shown in {numref}`fig6.3`: it consists of two adiabatic steps and two isothermal steps. Heat is supplied in step 3-4 and rejected in step 
1-2: work 
is done in all four steps. Only two temperatures are involved: $T_{3} = T_{4} = T_{H}$ and $T_{1} = T_{2} = T_{C}$.

```{figure} Images/6_Carnot.png
:name: fig6.3
:alt: Carnot cycle
:align: center
:width: 70%
The Carnot cycle.
```

 Taking each step in turn:

1. Step 1-2, work done on system $W_{12} = n R T_{C} \ln (V_{1} / V_{2})$. As this step is isothermal $\Delta U = 0$ and so the system must 
output heat $|Q_{12}| = n R T_{C} \ln (V_{1} / V_{2})$.

2. Step 2-3: as this step is adiabatic, the heat supplied is zero, and from Equation {eq}`eqn5.7`, the work done is $W_{23} = 
\frac{1}{\gamma-1} (P_{3} V_{3} - P_{2} V_{2})  = n c_{V} (T_{H} - T_{C})$.

3. Step 3-4: work done _by_ system $|W_{34}| = n R T_{H} \ln (V_{4} / V_{3})$. Since $\Delta U = 0$, the system must take in heat $Q_{34} = 
n R T_{H} \ln (V_{4}/ V_{3})$.

4. Step 4-1: the work done _by_ the system is $|W_{41}| = n c_{V} (T_{H} - T_{C}).$ As the same temperatures are involved as in step 2-3 
these just cancel out so the net work done _by_ the system is $|W_{34}| - W_{12}$.

To simplify the resulting expression we use Equation {eq}`eqn5.5` to deduce $V_{2} T_{C}^{\gamma-1} = V_{3} T_{H}^{\gamma-1}$
and $V_{1} T_{C}^{\gamma-1} = V_{4} T_{H}^{\gamma-1}$. Therefore we conclude that $V_{1}/V_{2} = V_{4}/V_{3}$. Hence the net work done by 
the system is $|W| = n R (T_{H} - T_{C}) \ln (V_{4}/V_{3})$, and the heat supplied is $Q_{H} = Q_{34} = n R T_{H} \ln (V_{4}/V_{3})$.
From Equation {eq}`eqn6.1` the efficiency of the Carnot cycle is

```{math}
:label: eqn6.6
\eta = 1 - \frac{T_{C}}{T_{H}}.
```

The Carnot cycle is not an idealised version of a real engine - in practical terms it is _extremely_ difficult to supply heat without 
raising the temperature of your working fluid. It was deliberately desgined as a theoretical construct to demonstrate maximium efficiency.
We shall see in the next section that the Second Law of Thermodynamics can be used to demonstraet that it is impossible for any engine, real 
or idealized, to be more dfficient than a Carnot engine.

Equation {eq}`eqn6.6` can be used to define the __thermodynamic temperature__, because although we used the ideal gas law to derive it, it 
is in fact  indepdent of the working substance of the cycle. Therefore, if a Carnot cycle takes in heat $Q_{H}$ and rejects heat $|Q_{C}|$, 
we can define the __Kelvin temperature__

```{math}
:label: eqn6.7
\frac{T_{C}}{T_{H}} = \frac{|Q_{C}|}{Q_{H}}.
```

Since the Carnot cycle is purely theoretical and does not correspond to any real device, this is not a very useful definition in practical 
terms, but it is closely connected to the definition of temperature in terms of entropy, which _is_ useful.

# Refrigerators and heat pumps

A heat engine takes in heat from a hot reservoir, converts some of it to mechanical work and rejects the rest to a cold reservoir. Our 
idealised cycles all use reversible processes, so we should be able to run them in reverse. In reverse, the working fuild takes in heat from 
a cold reservoir, some work is done on it, and the resulting (greater) heat is expelled into a hot reservoir. The net effect of doing work 
on the system is to move heat from the cold reservoir to the hot reservoir - in orther words, it's a refrigerator. (A heat pump is 
thermodynamically equivalent to a refrigerator, but it has a different purpose: the aim of a refrigerator is to cool the cool reservoir; 
i.e. 
the interior of the fridge, whereas the aim of a heat pump is to heat the hot reservoir, i.e. the interior of the building). 

Real internal comustion engines are not reversible, because the heating stage (step 2-3 in the Otto and Diesel cycles) is achieved by 
igniting the fuel, which is not a reversible procedure. External combustion engines, such as the Stirling and Rankine cycles, are much more 
promising. Domestic fridges use a reverse Rankine cycle, as shown schematically in {numref}`fig6.4`.


```{figure} Images/6_fridge.png
:name: fig6.4
:alt: Schematic diagram of a heat pump or refrigerator
:align: center
Schematic diagram of a heat pump or refrigerator. Source: 
[Wikipedia](http://en.wikipedia.org/wiki/Refrigerator#/media/File:Refrigerator-cycle.svg)

```

In {numref}`fig6.4` hot vapour enters the condenser (1), where it is condensed into a liquid, releasing heat. The resulting high-pressure 
liquid 
flows through an expansion valve (2), which caused a drop i pressure and temperature. The cold, low pressure fiuid (a mixture of liquid and 
vapour) then passes through the evaporator (3) where it is converted to a vapoour, taking in heat from its surroundings. It then passes to 
the compressor (4) where it is pumped up to a high pressure (with a consequent increase in temperature) to return to the initial stage.

The equivalent of efficiency for a refrigerator or heat pump is called the __coefficient of performance__. This is defined broadly as the 
ratio of the desired outout to the work done, which means that it is different for refrigerators and heat pumps. For a refrigerator the 
desired output is the removal of heat from the cold reservoir, so the coefficient of performance is 

```{math}
:label: eqn6.8
COP_{R} = \frac{Q_{C}}{W}
```
whereas for a heat pump the desired output is the supply of heat to the hot reservoir, so

```{math}
:label: eqn6.9
COP_{HP} = \frac{|Q_{H}|}{W}
```
From the first law, $W = |Q_{H}| - Q_{C}$, giving

```{math}
:label: eqn6.10
COP_{R} = \frac{Q_{C}}{|Q_{H}| - Q_{C}} \\
COP_{HP} = \frac{|Q_{H}|}{|Q_{H}| - Q_{C}}.
```

If the refrigerator cycle were an ideal cycle with thermal efficiency $\eta= 1 - T_{C}/T_{H}$ the coefficients of performance would be 

```{math}
:label: eqn6.11
COP_{R} = \frac{T_{C}}{T_{H} - T_{C}} \\
COP_{HP} = \frac{T_{H}}{T_{H} - T_{C}}.
```
Notice that these are typically greater than one. For example, if your kitchen has a temperature of 25$^{\circ}$ C and you want your fridge 
to be at 
4$^{\circ}$ C, the ideal coefficient of performance would be 277/21 = 13.2; conversely if your kitchen is heated to 25$^{\circ}$ C nby a 
heat pump 
operating 
between the house and outside aire with a temperature of 4$^{\circ}$ C the ideal coefficient of performance would be 298/21 = 14.2. These 
values 
represent the maximum theoretically achievable, and in the real world coefficients of performance will be substantially less than this, 
especially for heat pumps since one should take into account the power required to circulate the heat around the house e.g. by pumping hot 
water through the radiator system, However, even real coefficients fo performance are significantly greater than unity.
