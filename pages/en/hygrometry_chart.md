---
title: The psychrometric chart
summary: "How to read the psychrometric chart"
permalink: hygrometry_chart.html
keywords: humidity, psychrometrics, moisture
sidebar: sidebar_en
topnav: topnav_en
folder: en
---


## Video

[PDF slides](/pdf/airhumide1 - dah.pdf)

<iframe src="https://player.vimeo.com/video/99807194?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>


## Formulaire

Air is a mixture of dry air and water vapor. The psychrometric chart is a graphical depiction of the properties of this mixture. It shows up to 7 parameters:

| $$T$$ | °C | (Dry-bulb) Temperature |
| $$\mathrm{RH}$$ | - | Relative humidity |
| $$r$$ or $$w$$ | kg$$_{w}$$/kg$$_{a}$$ | Humidity ratio |
| $$h$$ | J/kg$$_{a}$$ | Specific enthalpy |
| $$v_s$$ | m$$^3$$/kg$$_{a}$$ | Specific volume |
| $$T_w$$ | °C | Wet-bulb temperature |
| $$T_{dp}}$$ | °C | Dew point temperature |

Starting from any combination of two of these parameters, the remaining parameters can be read on the chart. Alternatively, these properties can be calculated: **the psychrometric charts only replaces the following formulas**.

* The relative humidity is the ratio between the water vapor partial pressure $$p_{vap}$$ and the saturation pressure $$p_{sat}$$ at temperature $$T$$ (°C:)

$$ \mathrm{HR} = \frac{p_{vap}}{p_{sat}} $$

$$ \mathrm{log}_{10}(p_{sat}) = 2,7858 + \frac{7,5 \, T}{237,3 + T} $$

The humidity ratio $$r$$ is the proportion of mass of water vapor per unit mass of dry air. The specific volume $$v_s$$ is the volume of the mixture containing one unit of mass of dry air. Their formulas can be found from the ideal gas law, where $$R_{a}=287$$ J.kg$$^{-1}$$.K$$^{-1}$$ is the specific gas constant of dry air:

$$ r = 0,622 \frac{p_{vap}}{p_{atm}-p_{vap}} $$

$$ v_s = \frac{R_{a} \, T}{p_{atm}-p_{vap}} $$

* The specific enthalpy is the sum of the sensible heat of air, and the latent heat of water vapor:

$$h = c_{a}\, T + r \, (l_v+c_v\, T) $$

## Exercise

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a class="noCrossRef" href="#enonce" data-toggle="tab">Questioning</a></li>
    <li><a class="noCrossRef" href="#correction" data-toggle="tab">Solution</a></li>
</ul>

<div class="tab-content">

<div role="tabpanel" class="tab-pane active" id="enonce" markdown="1">

Une masse d'air a une enthalpie spécifique $$h = 67$$ J/kg$$_{as}$$ et une teneur en eau $$r = 0.014$$ kg$$_{eau}$$/kg$$_{as}$$.

* Calculer sa température, son humidité relative et son volume spécifique.

* Confirmer ces valeurs en les lisant sur le diagramme de l'air humide

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

Vous allez bien y arriver tous seuls non ?

</div>

</div>
