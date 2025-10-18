+++
draft = false
title = 'Échantillonage'
summary = "Désigne la compression de la chrominance, du plus ou moins compressé"
weight = 20
slug = 'echantillonage'
+++

Chroma subsampling en anglais.
Désigne la compression de la chrominance, du plus ou moins compressé :
* 4:2:0, pour la diffusion, beaucoup compressé
* 4:2:2, pour le traitement, peu compressé
* 4:4:4, aussi pour le traitement, pas de compression

L'échantillonnage ne s'applique que sur les couleurs, la chrominance.

Le premier chiffre désigne le nombre de pixels traités, 4 indique deux lignes de 4 pixels.
Le deuxième et le troisième chiffre indiquent respectivement le niveau de compression sur la première et la deuxième ligne.

Dans le 4:4:4, les pixels sont laissés tels quels.
Dans le 4:2:2, on ne conserve que la moitié des pixels de chaque ligne, en faisant la moyenne des deux premiers pixels et la moyenne des deux suivants.
Dans le 4:2:0, on fait pareil pour la première ligne que dans le 4:2:2, mais la deuxième ligne elle sera remplacée par les pixels de la première.

![Schéma de l'échantillonnage](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Common_chroma_subsampling_ratios_YCbCr_CORRECTED.svg/1024px-Common_chroma_subsampling_ratios_YCbCr_CORRECTED.svg.png)

Si on n'évite de filmer en 4:2:0, c'est pour des problèmes d'aliasing ou de cross color. Par exemple, des rayures sur les vêtements peuvent être mal capturées, n'étant plus droites ou ajoutant des couleurs qui n'existent pas. Tourner du fond vert dans cet échantillonnage par exemple peut être problématique, les cheveux par exemple se retrouveraient mélangés avec le vert du fond.

![aliasing](https://upload.wikimedia.org/wikipedia/commons/f/fb/Moire_pattern_of_bricks_small.jpg)

![Cette image montre le décalage de luminance résultant du sous-échantillonnage chromatique.](https://upload.wikimedia.org/wikipedia/commons/3/36/Color-bars-vegas-dv.png)

Dans le codec Apple ProRes 4444, le dernier 4 indique la gestion d'une couche alpha, un masque du noir au blanc, où noir c'est non visible alors que blanc c'est visible.

![Le canal alpha](https://img.youtube.com/vi/VhgSCBdiakc/maxresdefault.jpg)