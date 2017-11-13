---
title: Thermal radiation
summary: "How to include heat input from the sun and radiative heat exchange between walls"
permalink: heat_radiation.html
keywords: heat, transfer, radiation, irradiance
tags: [thermique]
sidebar: sidebar_en
topnav: topnav_en
folder: en
---


## Solar radiation (shortwave)

[PDF slides](/pdf/heat transfer 4 - short wave radiation.pdf)

<iframe src="https://player.vimeo.com/video/242200967?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

The total heat $$\Phi_{SW}$$ brought by the sun to a surface $$S$$ with an absorption coefficient $$\alpha$$ is the sum of direct irradiance $$E_{dir}$$, diffuse irradiance $$E_{dif}$$ and reflected irradiance $$E_{ref}$$. Each of these variables can be calculated with a little trigonometry as functions of the angle of the wall and the position of the sun.

$$ \Phi_{SW} = \alpha . S . (E_{dir}+E_{dir}+E_{ref}) $$

The unit of $$\Phi_{SW}$$ is [W], and not [W/m$$^2$$], since irradiances have been multiplied by and area $$S$$.

## Longwave radiative heat exchange

[PDF slides](/pdf/heat transfer 5 - short wave radiation.pdf)

<iframe src="https://player.vimeo.com/video/242213846?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

View factors $$F_{ij}$$ are required to solve the radiative heat exchange between walls.

<table>
<tr>
<th> <img src="images/thermique GLO1.png" style="width: 450px;"> </th>
<th style="font-weight: normal">

In order for the system to be solvable, either the temperature or the net heat flux on each surface must be known. We can then solve it by using these two formulas:
<br>
<img src="images/thermique GLO2.png" style="width: 200px;">
<br>
This allows to either describe the system as an electrical circuit, or as a linear system of equations.

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

Consider this room:

<img src="images/thermique rayonnement exo.png" style="width: 250px;">

* The wall $$S_5$$ (on the left) is a window with a temperature of $$T_5 = 8°C$$.
* The surface $$S_0$$ is a radiator covering half the height of the wall on the right. Its temperature is $$T_0 = 60°C$$.
* All other surfaces have a temperature of $$T_0 = 20°C$$.

1. Calculate the radiative heat loss through the window, and the net heat flux given by the radiator.

2. Solve the problem again with these new conditions: the surface $$S_2$$ is adiabatic. Solve for its temperature $$T_2$$, and calculate the radiator heat flux again.

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

Correction à venir.

</div>

</div>
