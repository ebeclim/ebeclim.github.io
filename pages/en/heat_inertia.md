---
title: Thermal inertia
summary: "How to estimate dynamic effects in a more or less simplified way"
permalink: heat_inertia.html
keywords: heat, transfer, inertia, transient
tags: [heat]
sidebar: sidebar_en
topnav: topnav_en
folder: en
---

## Video

Explanation of thermal inertia and the differences between internal and external insulation

Explication de l'inertie thermique et de la différence entre une isolation par l'intérieur ou par l'extérieur. [PDF slides](/pdf/heat transfer 3 - inertia.pdf)

<iframe src="https://player.vimeo.com/video/242072875?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

## Formulas

Heat stored in a building component is defined by the difference between its temperature $$T_i$$ and a reference temperature $$T_0$$. In a wall of thickness $$e_i$$, mass density $$\rho_i$$ and heat capacity $$c_{p,i}$$, it can be estimated in the unit [J/m$$^2$$] as:

$$Q_i = \rho_i . e_i . c_{p,i} (T_i-T_0) $$

The total inertia of an $$n$$-layered wall is the sum of these accumulated energies over all layers:

$$Q = \sum_{i=1}^n Q_i = \sum_{i=1}^n \rho_i . e_i . c_{p,i} (T_i-T_0) $$

{% include warning.html content="Always check for units! It's very easy to get them wrong but it's also easy to make sure they're right." %}

<table>
<tr>
<th> <img src="images/thermique transitoire.png" style="width: 250px;"> </th>
<th style="font-weight: normal">
In a transient state, we can calculate the evolution of temperatures in time as a function of R and C values of a building component. These values depend on the discretization size and material properties. In the example shown here, the following equation is to be solved:

$$ C \dfrac{\partial T}{\partial t} = \frac{1}{R} (T_1-T) + \frac{1}{R} (T_2-T) $$

</th>
</tr>
</table>

## Exercise

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a class="noCrossRef" href="#enonce" data-toggle="tab">Questioning</a></li>
    <li><a class="noCrossRef" href="#correction" data-toggle="tab">Solution</a></li>
</ul>

<div class="tab-content">

<div role="tabpanel" class="tab-pane active" id="enonce" markdown="1">

Consider a wall made of three layers:

| Layer 1 (concrete) | Layer 2 (insulatin) | Layer 3 (finishing) |
|-------|--------|---------|
| $$e_c=15$$ cm | $$e_i=4$$ cm | $$e_f=1,5$$ cm |
| $$\lambda_c=1,5$$ W/m.K | $$\lambda_i=0,04$$ W/m.K | $$\lambda_f=1,5$$ W/m.K |
| $$c_c=920$$ J/kg.K | $$c_i=920$$ J/kg.K | $$c_f=920$$ J/kg.K |
| $$\rho_c=2700$$ kg/m$$^3$$ | $$\rho_i=75$$ kg/m$$^3$$ | $$\rho_f=2700$$ kg/m$$^3$$ |

The outdoor temperature is $$T_e=-5°C$$ and the indoor temperature is $$T_i=20°C$$. The outdoor heat transfer coefficient is $$h_e=16,7$$ W/m$$^2$$.K and the indoor one is $$h_i=9,1$$ W/m$$^2$$.K

**1. Internal insulation**

Suppose an internal insulation.

* Calculate the thermal resistance of each layer and the heat flux $$\varphi$$ through the wall.
* Calculate the temperature distribution across the wall and the average temperature of each material.
* Calculate the total stored heat and estimate the heat inertia.

**2. External insulation**

Answer the same questions as above in the case of an external insulation

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

La correction sera bientôt affichée. En attendant venez en cours.

</div>

</div>
