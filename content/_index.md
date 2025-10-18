+++
draft = false
title = 'Accueil'
type = 'home'
+++

## Sommaire

1. Bases de la vidéo
    1. [Définition image](./bases-video/definition-image)
    2. [Aspect Ratio](./bases-video/aspect-ratio)
    3. [Framerate](./bases-video/framerate)
    4. [Anamorphose](./bases-video/anamorphose)
    5. [Affichage](./bases-video/affichage)
    6. [Codecs](./bases-video/codecs)
2. Couleurs
    1. [Espaces colorimétriques](./couleurs/espaces-colorimetriques)
    2. [Échantillonage](./couleurs/echantillonage)
    3. [Quantification](./couleurs/quantification)


## Workflow recommandé

Pour chaque projet, créer une arborescence de ce genre :

```tree
- PROJETS_EANIS | folder
   - NOM_PROJET | folder
      - RUSHES | folder
         - PROXY | folder
         - AUDIO | folder
         - VIDEO | folder
      - SONS | folder
         - SFX | folder
         - MUSIQUES | folder
      - ELEMENTS | folder
         - TITRES | folder
         - MOTION | folder
         - STOCK | folder
      - PROJETS | folder
         - PREMIERE | folder
         - AFTER | folder
            - yyyymmdd_nom_projet.aep | fa-solid fa-wand-magic-sparkles | #9a9aff
            - yyyymmdd_nom_projet.aep | fa-solid fa-wand-magic-sparkles | #9a9aff
      - EXPORTS | folder
         - FINAL | folder
         - RENDUS_3D | folder
         - AFTER | folder
   - Resolve Project Library | folder
```