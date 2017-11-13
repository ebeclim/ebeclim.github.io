---
title: Thermal-electrical analogy
summary: "Calculating heat transfer as if it were electric current"
permalink: heat_analogy.html
keywords: heat, transfer, electronic, analogy
tags: [heat]
sidebar: sidebar_en
topnav: topnav_en
folder: en
---

## Videos

### Video 1

Introduction to the thermal-electrical analogy. [PDF slides](/pdf/heat transfer 1 - electric diagram.pdf)

<iframe src="https://player.vimeo.com/video/242046233?color=ff9933" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

### Video 2

Some examples on how to use the thermal-electrical analogy to model a variety of transfer phenomena. [PDF slides](/pdf/heat transfer 2 - electric diagram 2.pdf)

<iframe src="https://player.vimeo.com/video/242058869?color=ff9933" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

## Formulas

The heat flux per square meter of a wall is proportional to the temperature difference across the wall $$\Delta T$$, and to its transmittance $$U$$ [W/(m$$^2$$.K)] :

$$ \varphi = U . \Delta T = \dfrac{1}{R} . \Delta T$$

The unit of this heat flux $$\varphi$$ is [W/m$$^2$$]. The total heat $$\phi$$ flowing across a wall of area $$S$$, in [W], is then:

$$ \phi = S . \varphi = S . U . \Delta T$$

We can also define a global heat loss coefficient such as $$ D = S.U $$ [W/K]

The thermal resistance $$R_i$$ of a component of thickness $$e_i$$ and heat conductivity $$\lambda_i$$ is:

$$R_i=\dfrac{e_i}{\lambda_i}$$

A wall made of several material layers behaves like a series circuit of resistances: their values add up.

$$ R = \sum_i R_i = \sum_i \dfrac{e_i}{\lambda_i}$$

A building envelope made of several separated parts (opaque wall, windows, roof...) can be modelled as a parallel circuit of resistances: heat flows through each surface $$S_i$$ (m$$^2$$) simultaneously with more or less intensity. The heat loss coefficients $$D$$ of each surface add up:

$$ D = S.U = \sum_i S_i.U_i $$

{% include warning.html content="Surface transfer coefficients must be summed in unit [W], not in [W/m$$^2$$]" %}

|  | Variable | Unit |  |
|-------|--------|---------|
| $$R$$ | Thermal resistance | (m$$^2$$.K)/W | can be summed in series |
| $$U$$ | Thermal transmittance | W/(m$$^2$$.K) |  |
| $$D$$ | Heat loss coefficient | W/K | can be summed in parallel |

Cette méthode peut être appliquée pour représenter les transferts à l'échelle de tout un bâtiment, y compris en incluant des transferts par renouvellement d'air (voir vidéo 2).

## Exercise

Calculate the heat loss coefficient of an insulated room.

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a class="noCrossRef" href="#enonce" data-toggle="tab">Questioning</a></li>
    <li><a class="noCrossRef" href="#correction" data-toggle="tab">Solution</a></li>
</ul>

<div class="tab-content">

<div role="tabpanel" class="tab-pane active" id="enonce" markdown="1">

The walls of a room are made of:

* 44 m$$^2$$ of concrete wall ($$e_c=15$$ cm, $$\lambda_c=2,3$$ W/(m.K)) with an insulation layer ($$e_{i}=10$$ cm, $$\lambda_{i}=0,04$$ W/(m.K))
* 8 m$$^2$$ of double glazing ($$U_v=3,3$$ W/(m$$^2$$.K))
* The indoor heat transfer coefficient is $$h_i = 0,11$$ (m$$^2$$.K)/W, the outdoor one is $$h_e = 0,07$$ (m$$^2$$.K)/W

The room is ventilated with an air renewal rate of 9 m$$^3$$/h.

Calculate the heating power that should be prescribed to maintain an indoor temperature of 19°C, if the outdoor temperature is 2°C.

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

The total heat loss of the room is the sum of three parts: heat flux through the concrete+insulation wall, heat flux through the windows and air renewal.

**1. Insulated concrete wall**

The thermal resistance is the sum of each layer's resistance, and the surface resistances:

$$R_1 = h_i + \dfrac{e_c}{\lambda_c} + \dfrac{e_{i}}{\lambda_{i}} + h_e = 0,11 + \dfrac{0,15}{2,3} + \dfrac{0,10}{0,04} + 0,07 = 2,75$$ (m$$^2$$.K)/W

The heat loss is the reciprocal of this total resistance, times the area of the wall:

$$D_1 = \dfrac{S_1}{R_1} = \dfrac{44}{2,75} = 16,03$$ W/K

**2. Windows**

The $$U_v$$ transmittance that describes the glazing probably doesn't include the heat transfer coefficients $$h_e$$ and $$h_i$$. They should be included in the equation of the total glazing heat loss coefficient:

$$D_2 = \dfrac{S_2}{h_i+\frac{1}{U_v}+h_e} = \dfrac{8}{0.11+\frac{1}{3,3}+0,07} = 16,56$$ W/K

**3. Air renewal**

If the air renewal rate is given in the unit (m$$^3$$/h), the heat loss associated to it can be calculated easily:

$$D_3 = 0,34 \, Q_v = 3,06$$ W/K

**Summary**

The total heating power lost by the room is the sum of these three types of heat loss, times the indoor-outdoor temperature difference:

$$\phi = \underbrace{(D_1+D_2+D_3)}_{W/K}.\underbrace{\Delta T}_{K} = (16,03 + 16,56 + 3,06 ). (19-2) = 606$$ W

</div>

</div>
