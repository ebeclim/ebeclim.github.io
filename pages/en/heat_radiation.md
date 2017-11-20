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

### Video

[PDF slides](/pdf/heat transfer 5 - short wave radiation.pdf)

<iframe src="https://player.vimeo.com/video/242213846?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

### Methodology

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

### View factors

View factors $$F_{ij}$$ are required to solve the radiative heat exchange between walls. Here are two formulas for view factors that two cover widespread specific cases:

<table>
<tr>
<th> <img src="images/view factor 1.png" style="width: 150px;"> </th>
<th style="font-weight: normal">
Two parallel planes of equal sizes:

$$ F_{12} = \frac{1}{\pi x y} \left[ \ln \frac{x_1^2 y_1^2}{x_1^2+y_1^2-1} + 2x\left(y_1 \arctan \frac{x}{y_1}-\arctan x \right) + 2y\left(x_1 \arctan \frac{y}{x_1}-\arctan y \right)  \right] $$

$$ \mathrm{with} \: x_1=\sqrt{1+x^2} \: ; \: y_1=\sqrt{1+y^2} \: ; \: x=W/H \: ; \: y=L/H $$

</th>
</tr>
</table>

<table>
<tr>
<th> <img src="images/view factor 2.png" style="width: 150px;"> </th>
<th style="font-weight: normal">
Two adjacent perpendicular rectangles:

$$ F_{12} = \frac{1}{\pi w} \left[ h \arctan \left(\frac{1}{h} \right) + w \arctan \left(\frac{1}{w} \right) - \sqrt{h^2+w^2} \arctan \left(\frac{1}{\sqrt{h^2+w^2}} \right) + \frac{1}{4} \ln \left( a \, b^{w^2} \, c^{h^2}\right) \right]$$

$$ \mathrm{with} \: a = \frac{(1+h^2)(1+w^2)}{1+h^2+w^2} \: ; \: b = \frac{w^2(1+h^2+w^2)}{(1+w^2)(h^2+w^2)} \: ; \: c = \frac{h^2(1+h^2+w^2)}{(1+w^2)(h^2+w^2)} $$

$$  h=H/L \: ; \: w=W/L $$

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
* The surface $$S_2$$ (the ground) is adiabatic.
* All other surfaces have a temperature of $$T = 20°C$$.

Calculate the radiative heat loss through the window, the net heat flux given by the radiator and the temperature of the ground.

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

Solution will be here soon.

</div>

</div>
