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

[PDF slides](/pdf/heat transfer 5 - long wave radiation.pdf)

<iframe src="https://player.vimeo.com/video/242213846?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

### Methodology

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

The problem can be solved either by using an equivalent electrical circuit as shown on the video, or by solving a linear system of equations with the method shown below.

Either the net heat flux or the temperature of each wall $$i$$ should be known. For each wall, write one of the following equations:

* If the temperature $$T_i$$ is known :

$$J_i =\varepsilon_i \sigma T_i^4 + \rho_i\sum_{j=1}^n J_j F_{ij}$$

* If the net heat flux $$\Phi_i$$ is known :

$$\frac{\Phi_i}{S_i} = J_i - \sum_{j=1}^n J_j F_{ij}$$

We can write a system of equations of the type $$Ax=b$$ where $$A$$ is a $$n \times n$$ matrix ($$n$$=number of surfaces) and $$x$$ is the vector of radiosities. Once the system is solved and the radiosities are known, the following formula can be used to calculate the temperatures and heat fluxes that were initially unknown:

$$\frac{\Phi_i}{S_i} = \frac{\varepsilon_i}{1-\varepsilon_i}(\sigma T_i^4-J_i) $$

An example of this methodology is proposed in the following exercise.

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

Calculate the radiative heat loss through the window, the net heat flux given by the radiator and the temperature of the ground. The emission coefficient of all surfaces is $$\varepsilon=0.85$$

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">


All the walls that have a temperature of $$T = 20°C$$ can be considered as a single surface. The question is therefore equivalent to heat exchange balance between 4 surfaces: we need to write 4 equations.

First, the view factors are required. The formulas shown above only need to be used three times, to find the following values:

$$ F_{25}=0.1174 \: ; \: F_{20}=0.081 \: ; \: F_{50}= 0.0477$$

All other view factors can be calculated from the simple formulas: $$S_iF_{ij}=S_jF_{ji}$$ et $$\sum_j F_{ij}=1$$.

We then need to write one equation for each surface. Surface 0 (the radiator) has a known temperature, which means:

$$J_0 =\varepsilon_0 \sigma T_0^4 + \rho_i\sum_{j=1}^n J_j F_{0j}$$

Surface 2 (the floor) has a known heat flux of zero since it is adiabatic:

$$0 = J_2 - \sum_{j=1}^n J_j F_{2j}$$

Surfaces 3 and 5 have the same kind of boundary condition as surface 2 (prescribed temperature): their equations are therefore similar. We end up with the following linear system of equations for the radiosities:

$$\begin{bmatrix} 1-\rho_0F_{00} & -\rho_0F_{02} & -\rho_0F_{03} & -\rho_0F_{05} \\ -F_{20} & 1-F_{22} & -F_{23} & -F_{25}  \\
-\rho_3F_{30} & -\rho_3F_{32} & 1-\rho_3F_{33} & -\rho_3F_{35} \\ -\rho_5F_{50} & -\rho_5F_{52} & \rho_5F_{53} & 1-\rho_5F_{55}
\end{bmatrix}
\begin{bmatrix} J_0 \\ J_2 \\ J_3 \\ J_5 \end{bmatrix} =
\begin{bmatrix} \varepsilon_0\sigma T_0^4 \\ 0 \\ \varepsilon_3\sigma T_3^4 \\ \varepsilon_5\sigma T_5^4 \end{bmatrix}
$$

Solving this system results in the following values in W/m$$^2$$:

$$ J_0 = 656.61 \: ; \: J_2 = 433.23 \: ; \: J_3 = 420.45 \: ; \: J_5 = 366.34 $$

The last step is to use this formula:

$$\frac{\Phi_i}{S_i} = \frac{\varepsilon_i}{1-\varepsilon_i}(\sigma T_i^4-J_i) $$

in order to find the target values of the exercise: floor temperature $$T_2$$, radiator heat flux $$\Phi_0$$ and net heat flux on the window $$\Phi_5$$:

$$T_2= 22.5°C \: ; \: \Phi_0=711.53 W \: ; \: \Phi_5=-410.27 W$$


</div>

</div>
