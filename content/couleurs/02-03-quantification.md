+++
draft = false
title = 'Quantification'
summary = "Désigne la compression de la luminance du plus au moins compressés et donc le nombre de nuances de gris"
weight = 3
slug = 'quantification'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

En anglais, Grayscale quantization ou level quantization.
Désigne la compression de la luminance du plus au moins compressés et donc le nombre de nuances de gris :
* 8 bits (2^8 soit 256 nuances de gris)
* 10 bits (2^10 = 1024)
* 12 bits (2^12 = 4096)
* 14 bits (2^14 = 16 384)
* 16 bits (2^16 = 65 536)
* 32 bits (2^32 = 4 294 967 296)

La diffusion se fait essentiellement en 8 bits, exception faite des Blu-Ray qui peuvent monter jusqu'à 10 bits. Les caméras captent de 8 à 14 bits, sauf la Sony Venice 2 qui peut aller jusqu'à 16 bits. Le 32 bits ne peut être créé que numériquement.

![Exemple de quantification](https://www.researchgate.net/profile/Saddam-Bekhet/publication/318818149/figure/fig4/AS:525091446038533@1502202964332/grayscale-levels-quantized-into-two-different-levels.png)

Ainsi, quand on fait la synthèse additive avec les vert, bleu et rouge purs, en 8 bits donc 256 nuances par couleur ça fait 256x256x256 = 16 millions de couleurs.

![Synthèse additive](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Synthese%2B.svg/800px-Synthese%2B.svg.png)

Du coup, en 8 bits, ce vert pur s'écrit R0 V255 B0 #00FF00.

Pour éviter l'effet de banding, on peut monter la quantification, mais vu qu'on diffuse en 8 bits la plupart du temps, c'est difficile à éviter.

![Banding](https://upload.wikimedia.org/wikipedia/commons/9/9a/Colour_banding_example01.png)

À noter qu'en lumière / vidéo, les couleurs primaires sont rouge / vert / bleu tandis qu'en peinture c'est rouge / jaune / bleu.