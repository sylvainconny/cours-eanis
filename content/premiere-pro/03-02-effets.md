+++
draft = false
title = 'Effets'
summary = "Effets et options d'effets"
weight = 2
slug = 'effets'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

## Options d'effet
**Transformation** permet de changer la position du plan sur le programme selon un axe y / x

**Echelle** peut agrandir ou réduire uniformément la taille du plan, à moins qu'on décoche *échelle uniforme* et là on peut distinctement changer la hauteur ou la largeur.

**Rotation** fait tourner le plan d'un angle de x [degrés grades](https://fr.wikipedia.org/wiki/Grade_(angle)) autour du **Point d'ancrage**. Ce dernier définit également le centre de *l'échelle*.

L'**Opacité** définit la transparence du plan, auquel on peut appliquer un masque (rectangle, sphère, personnalisé).
Les **[Modes de fusion](https://fr.wikipedia.org/wiki/Mode_de_fusion)** sont des règles de calcul pour combiner deux calques.

![Fenêtre d'option d'effet](./fenetre-options-effets.png)

Tous les effets peuvent varier en fonction du temps. Il faut cocher sur l'icône du chronomètre des effets que l'on souhaite animer.
À chaque moment clé on ajoute une **keyframe** avec des paramètres définis. Le logiciel se chargera de faire évoluer l'effet entre les deux keyframes.
Les keyframes se créent automatiquement quand on modifie un paramètre d'effet dans la timeline. Penser à utiliser la select box pour sélectionner et supprimer les keyframes indésirables. On peut placer autant de keyframes que l'on souhaite.
{{< video src="./keyframes.webm" autoplay="true" loop="true" muted="true" >}}

Noter que pour modifier subtilement ces éléments, on peut appuyer sur {{< kbd >}}Ctrl{{< /kbd >}} pour rendre le changement plus précis.

## Effets

Bibliothèque des effets que l'on peut rajouter à un plan, en plus des effets de base précisés ci-haut. Contient des transformations vidéo, des transitions, des effets de flou, d'incrustation, et pareillement pour l'audio.

![Fenêtre d'effet](./fenetre-effets.png)

## Effet stabilisation
Essaie de compenser les mouvements de la caméra. Si la caméra va vers le haut, l'effet va essayer de baisser l'image. Il fait le mouvement opposé à la caméra. Du coup, la stabilisation nécessite de zoomer dans l'image pour avoir de la marge de compensation. Plus on souhaite compenser, plus on zoome.
Cet effet a des options :
Si la caméra recule, l'effet zoome et inversement, un peu comme l'effet Vertigo du film d'Alfred Hitchcock ou le [travelling compensé](https://fr.wikipedia.org/wiki/Travelling_contrari%C3%A9)
![Effet Vertigo](https://upload.wikimedia.org/wikipedia/commons/9/9e/Alfred_Hitchcock%27s_Vertigo_trailer_-_Vertigo%27s_Effect.png)

Si les caméras bouge sur des axes plus complexes, le logiciel peut essayer de compenser les mouvements en déformant l'image.

[![Stabilisation](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/Video_image_stabilization.ogv/800px--Video_image_stabilization.ogv.jpg)](https://en.wikipedia.org/wiki/File:Video_image_stabilization.ogv)

{{< video src="[./keyframes.webm](https://upload.wikimedia.org/wikipedia/commons/d/d7/Video_image_stabilization.ogv)" autoplay="true" loop="true" muted="true" >}}

À noter que si les plans peuvent être ralentis pour limiter les tremblements ou autres mouvements de caméra, mais, s'ils sont ralentis il ne peuvent plus être stabilisés. Il faut mettre le plan en question dans une autre séquence qu'on intégrera à la place du plan et sur la séquence on peut appliquer l'effet de stabilisation.
