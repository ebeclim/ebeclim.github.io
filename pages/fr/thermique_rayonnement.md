---
title: Rayonnement
summary: "Comment inclure le soleil et les échanges radiatifs dans les calculs thermiques"
permalink: thermique_rayonnement.html
keywords: thermique, bâtiment, énergie, rayonnement
tags: [thermique]
sidebar: sidebar_fr
topnav: topnav_fr
folder: fr
---

## Apports solaires (courtes longueurs d'onde)

Première vidéo sur le rayonnement : comment calculer les apports solaires directs et diffus sur une paroi à partir des données météo. [Diapos au format PDF](/pdf/thermique4 - rayonnement CLO.pdf)

<iframe src="https://player.vimeo.com/video/142485394?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

La chaleur totale $$\Phi$$ que le soleil apporte à une surface $$S$$ d'absorptivité $$\alpha$$ est la somme de l'ensoleillement direct $$E_{dir}$$, diffus $$E_{dif}$$ et réfléchi sur les surfaces voisines $$E_{ref}$$. Chacun de ces termes se calcule avec un peu de trigonométrie en fonction de l'angle de la paroi et la position du soleil.

$$ \Phi_{CLO} = \alpha . S . (E_{dir}+E_{dir}+E_{ref}) $$

$$\Phi$$ est exprimée ici en W et non en W/m$$^2$$, puisqu'on a multiplié la somme des ensoleillements par la surface $$S$$.

## Echanges radiatifs entre parois (grandes longueurs d'onde)

Deuxième vidéo sur le rayonnement, où on aborde le calcul des températures des parois sous l’effet des échanges radiatifs, et la description de la température radiante moyenne. [Diapos au format PDF](/pdf/thermique5 - rayonnement GLO.pdf)

<iframe src="https://player.vimeo.com/video/142616863?color=ff9933&portrait=0" width="640" height="480" frameborder="1" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

Pour résoudre un problème d'échange radiatif (grandes longueurs d'onde) entre parois, il faut d'abord connaître tous les facteurs de forme $$F_{ij}$$

<table>
<tr>
<th> <img src="images/thermique GLO1.png" style="width: 450px;"> </th>
<th style="font-weight: normal">
On peut ensuite établir un schéma électrique équivalent à l'ensemble des échanges, où les noeuds sont des émissivités ou des radiosités. Le système peut être résolu si chaque paroi a soit une température connue, soit un flux net de chaleur connu (par exemple une paroi adiabatique). Selon le cas, on peut alors exprimer le flux net de chaque paroi par l'une ou l'autre de ces formules :
<br>
<img src="images/thermique GLO2.png" style="width: 200px;">

</th>
</tr>
</table>

## Exercice

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a class="noCrossRef" href="#enonce" data-toggle="tab">Enoncé</a></li>
    <li><a class="noCrossRef" href="#correction" data-toggle="tab">Correction</a></li>
</ul>

<div class="tab-content">

<div role="tabpanel" class="tab-pane active" id="enonce" markdown="1">

On considère une pièce parallélépipédique aux dimensions suivantes :

<img src="images/thermique rayonnement exo.png" style="width: 250px;">

* La surface $$S_5$$ (mur vertical gauche) est une baie vitrée à la température $$T_5 = 8°C$$.
* La surface $$S_0$$ est un radiateur couvrant la moitié de la hauteur du mur de droite, à la température $$T_0 = 60°C$$.
* Toutes les autres parois sont à la température $$T_0 = 20°C$$.

Calculer les pertes radiatives de la pièce par la fenêtre, et le flux net radiatif cédé par le radiateur.

</div>

<div role="tabpanel" class="tab-pane" id="correction" markdown="1">

Correction à venir.

</div>

</div>
