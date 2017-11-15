---
title: Air flow
summary: "Estimate heat transfer caused by ventilation, wind and stack effect"
permalink: heat_airflow.html
keywords: heat, transfer, buildings, ventilation
tags: [heat]
sidebar: sidebar_en
topnav: topnav_en
folder: en
---


## Video

How to predict heat transfer due to ventilation, caused by the wind or the stack effect. [PDF slides](/pdf/heat transfer 6 - aeraulics.pdf)

<iframe src="https://player.vimeo.com/video/242243089?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

## Formulas

A small opening with an area $$S$$ and a discharge coefficient $$C_d$$ separate two rooms at the pressures $$P_1$$ and $$P_2$$. The air flow rate $$Q_v$$ [m$$^3$$/s] through the opening can be estimated by:

$$ P_1 - P_2 = \frac{\rho Q_v^2}{2S^2C_d^2} $$

In case of wind, the total air pressure is the sum of the atmospheric pressure $$P_{atm}$$ and some dynamic pressure, which depends on a pressure coefficient $$C_p$$ and wind velocity $$V$$.

$$ P = P_{atm} + C_p \frac{1}{2} \rho V^2 $$

The mass density of air $$\rho$$ [kg/m$$^3$$] is roughly equal to this relation, where the temperature $$T$$ is in unit [K]:

$$\rho = \frac{353}{T}$$

<img src="images/thermique_tirage.png" style="width: 600px;">

The stack effect is caused by this relation between density and temperature. The two air volumes shown here have temperatures notes $$T_e$$ and $$T_i$$. The pressure difference between them is a function of the coordinate $$z$$:

$$ P_e(z) - P_i(z) = \left( P_e(0)-\rho_e \, g \, z\right) - \left( P_i(0)-\rho_i \, g \, z \right) = P_e(0)-P_i(0)-\rho_e \, g \, z \, \frac{T_i-T_e}{T_i}$$

The *neutral plane* is the coordinate $$z_n$$ at which this pressure difference is equal to zero:

$$z_n = \dfrac{P_e(0)-P_i(0)}{g(\rho_i-\rho_e)} $$

## Exercise

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a class="noCrossRef" href="#enonce" data-toggle="tab">Questioning</a></li>
    <li><a class="noCrossRef" href="#correction" data-toggle="tab">Solution</a></li>
</ul>

<div class="tab-content">

<div role="tabpanel" class="tab-pane active" id="enonce" markdown="1">

<img src="images/thermique_aeraulique.png" style="width: 500px;">

A door of height $$H=2$$m and width $$w=1$$m separates two rooms at temperatures $$T_1=15°C$$ and $$T_2=21°C$$.

Suppose (without proving it) that the air velocity at the interface is a function of the coordinate $z$$:

$$ V(z) = \sqrt{2\, \frac{P_1(z)-P_2(z)}{\rho}} $$

where $$\rho$$ is the mass density on the side from which air flows (which depends on whether the coordinate is above or below the neutral plane).

Integrate $$V(z)$$ over the height $$H$$ to find the total mass flow rate of air $$Q_m$$ [kg/s] through the door. Suppose the door is an infinite stack of small openings with a discharge coefficient $$C_d=0.4212$$.

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

Below the neutral plane, air flows from room 1 to room 2 with a total rate of:

$$Q_{m,12} = C_d \int_0^{z_n} \rho_1 \, V(z) \, w \, \mathrm{d}z $$

Above the neutral plane, air flows from room 2 to room 1 with a total rate of:

$$Q_{m,21} = C_d \int_{z_n}^{H} \rho_2 \, V(z) \, w \, \mathrm{d}z $$

The net air flow rate from 1 to 2 is $$Q_{m,12}-Q_{m,21}$$

</div>

</div>
