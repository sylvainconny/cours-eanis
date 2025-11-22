+++
draft = false
title = 'Espaces Colorimétriques'
summary = "Un espace colorimétrique c'est une zone définie dans le diagramme de chromaticité, lequel représente l'ensemble des chrominances (ou couleurs pures sous-entendu sans luminance, sans les nuances de luminosité) visibles à l'œil nu"
weight = 1
slug = 'espaces-colorimetriques'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

![Diagramme de chromaticité](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/SRGB_chromaticity_CIE1931.svg/800px-SRGB_chromaticity_CIE1931.svg.png)

Un espace colorimétrique c'est une zone définie dans le diagramme de chromaticité, lequel représente l'ensemble des chrominances (ou couleurs pures sous-entendu sans luminance, sans les nuances de luminosité) visibles à l'œil nu.

L'espace L*a*b* représente en 3D la chrominance par la luminance, donc le réel espace complet des couleurs visibles à l'œil nu.
![L'espace L*a*b](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c6/The_principle_of_the_CIELAB_colour_space.svg/800px-The_principle_of_the_CIELAB_colour_space.svg.png)

On parle aussi de Gamut pour la chrominance (soit l'ensemble des couleurs que l'on peut créer avec du vert pur, du bleu pur et du rouge pur) et de Gamma pour la luminance (soit les nuances de gris).

Si un espace colorimétrique couvre une partie de gamut, il est généralement associé à un gamma parmi lesquels 2.2, 2.4, 2.6, 2.8.

![Différents gamma](./gamma.jpg)

## Espaces de diffusion
Dans l'ordre d'apparition et de grandeur :

* Rec 601, le plus ancien, définit pour des normes SD
![Rec 601 dans le Diagramme de chromaticité](https://upload.wikimedia.org/wikipedia/commons/thumb/4/40/CIExy1931_Rec_601.svg/800px-CIExy1931_Rec_601.svg.png)
* Rec 709, définit initialement pour des normes HD et Full HD, même s'il est encore utilisé pour l'UHD
![Rec 709 dans le Diagramme de chromaticité](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/CIExy1931_Rec_709.svg/800px-CIExy1931_Rec_709.svg.png)
* Rec 2020, pour l'UHD
![Rec 2020 dans le Diagramme de chromaticité](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b6/CIExy1931_Rec_2020.svg/800px-CIExy1931_Rec_2020.svg.png)
* Rec 2100, pensé pour le 8K

Ces espaces colorimétriques représentent des gammes de couleurs disponibles différentes pour la capture, l'encodage et la diffusion, même si tous les écrans ne restituent pas forcément un espace à 100%.

Au cinéma, c'est le DCI P3 qui est utilisé. Il rentre dans la norme des fichiers DCP pour la projection cinéma.
![DCI P3 dans le Diagramme de chromaticité](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/DCI-P3_D65.svg/800px-DCI-P3_D65.svg.png)

Concernant le gamma, le Rec 709 étant généralement associé au 2.4 tandis que le cinéma plutôt au 2.6, cela peut dépendre du lieu de diffusion.

Dans le monde de la photo ou du web il existe également AdobeRGB et sRGB.
![Gamut du sRGB](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/SRGB_chromaticity_CIE1931.svg/800px-SRGB_chromaticity_CIE1931.svg.png)
![Gamut du AdobeRGB](https://upload.wikimedia.org/wikipedia/commons/thumb/d/dc/CIE1931xy_AdobeRGB.svg/800px-CIE1931xy_AdobeRGB.svg.png)

## Espaces de traitement
Dépend du constructeur de caméra, on parle souvent de Log mais c'est un abus de langage car le log n'est en fait qu'un gamma, associé à un gamut de traitement.

![Adobe Wide Gamut RGB](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/CIExy1931_AdobeWGRGB.png/800px-CIExy1931_AdobeWGRGB.png)

Le Log donne aux images cet aspect laiteux, mais c'est une conséquence de la largeur de son gamut et son gamma.

Parmi les plus courants :
* Sony : S-log 2 et S-log 3
* Canon : C-log
* Panasonic : V-log
* DJI : D-Log
* Arri : log C, log C3, log C4
* RED : REDlogFilm
* Blackmagic : BlackmagicFilm
* Apple : Apple Log 2

Ici ce qui change d'un log à l'autre, c'est bien le gamma, car chaque constructeur est également associé à un gamut de traitement propre, comme le ARRI Wide Gamut :
![ARRI Wide Gamut](https://blog.frame.io/wp-content/uploads/2024/04/reveal-arri-wide-gamut.jpg)

## LUT
Les Lookup Table ou tables de correspondances servent à passer d'un espace colorimétrique à un autre, comme de S-log 2 à Rec 709 par exemple.
Il y a deux types de LUT :
* les LUT 1D, qui ne modifient que le gamma, servant essentiellement à corriger des erreurs d'enregistrement (exemple : mauvais gamut sur un espace de traitement)
* les LUT 3D qui modifient le gamma et le gamut, qui sont les LUT les plus généralement utilisées pour passer d'un espace à l'autre.

L'utilité principale est pour l'étalonneur de pouvoir observer l'image dans l'espace de diffusion tout en conservant la grande quantité d'information des espaces de traitement.
Un étalonneur de cinéma va utiliser une LUT log vers DCI P3, pour la télévision vers Rec 709.
Ce qu'on connait mieux, ce sont les LUT artistiques qui servent à avoir facilement un rendu flatteur.

## ACES / DaVinci Wide Gamut
Ce sont des espaces colorimétriques "potentiels" allant au-delà de ce que l'oeil humain peut voir. Ils servent d'espace de travail entre l'espace d'origine et l'espace de sortie, et ne pose ainsi aucun problème de compatibilité entre les espaces colorimétriques des différentes sources.

Netflix utilise également l'ACES pour automatiser l'espace de diffusion en fonction des capacités de l'écran de visionnage.

![ACES](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/CIE_1931_chromaticity_ACES_sRGB_gamut_comparison_CreativeCommons_v06.svg/800px-CIE_1931_chromaticity_ACES_sRGB_gamut_comparison_CreativeCommons_v06.svg.png)