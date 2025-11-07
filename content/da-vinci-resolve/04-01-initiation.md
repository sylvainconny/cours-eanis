+++
draft = false
title = 'Initiation'
summary = "Démarrage d'un projet, raccourcis…"
weight = 1
slug = 'initiation'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

Contrairement à Adobe Premiere Pro, la gestion des projets se fait via des **Databases** (Bases de données) et non via des fichiers individuels par projet.

Pour stocker une database sur notre disque externe, il faut la créer dans l'interface de démarrage.

![Créer database](./creer-database.png)

À l'endroit indiqué, un dosser *Resolve Project Library* a été créé contenant la database qui apparaît sur la gauche de la bibliothèque de projets.

En sélectionnant bien notre nouvelle database, on peut créer un nouveau projet. L'emplacement média désigne le cache des pré-rendus. La nomenclature reste la même *YYYY-MM-DD-titre-projet*.

L'interface se présente en plusieurs onglets :
- **Média** où l'on gère l'importation des médias
- **Cut** qui est une version simplifiée du montage
- **Montage** qui est la partie complète du montage
- **Fusion**, pour le compositing en mode nodal
- **Etalonnage** pour la gestion des couleurs… 
- **Fairlight** dédié à la musique
- **Exportation**

Da Vinci est globalement moins modulable que les autres logiciels de montage, chaque onglet est optimisé pour sa fonction. Des panneaux peuvent être affichés à un endroit spécifique ou masqués, mais tout est prédéfini.

Par défaut les timelines créées auront les paramètres par défaut du projet (framerate, définition…).

## Média
![Page média](./page-media.png)

Dans le panneau **Espaces de stockage** on retrouve un explorateur de fichiers, on peut glisser / déplacer des dossiers dans les **favoris**. En naviguant dans les dossiers, on peut lire à la volée les fichiers vidéo / audio dans le lecteur avant même de les intégrer dans les chutiers.

En dessous, on a les chutiers, qui fonctionnent en arborescence depuis la racine Master. {{< kbd >}}Ctrl{{< /kbd >}} \+ {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}N{{< /kbd >}} pour créer un chutier. On peut y glisser déplacer l'ensemble des rushes du panneau *Espaces de stockage*.

Comme Premiere, il y a plusieurs méthodes d'affichage des médias dans les *chutiers* et les *Espaces de stockage* :
- par **liste** où on peut spécifier l'affichage des métadonnées avec un clic droit sur la partie en-tête du tableau
- par **vignette**, dont on peut changer la taille

D'autres panneaux sur la droite peuvent être affichés (conjointement éventuellement) :
- le panneau **audio** qui comporte notamment une vue *Forme d'onde*
- le panneau **métadonnées** permet en plus d'avoir accès aux informations du média, de personnaliser des informations, mettre des couleurs ou des drapeaux. À noter qu'on peut afficher *toutes les catégories* pour voir toutes les métadonnées
- le panneau **inspecteur** sera surtout utile dans le montage

![Panneaux audio et métadonnées](panneau-audio-metadonnees.png)

## Montage
![Page média](./page-montage.png)
De la même manière, il y a plusieurs panneaux sur la gauche et la droite.
À gauche on a :
- d'abord la **bibliothèque de médias* qui représente les chutiers
- les **Effets** qui contient tous les effets disponibles dans le logiciel
- **Index** qui référence les modifications de la timeline, les pistes et les marqueurs
- la **Sonothèque** listant des SFX fournis par Blackmagic cloud
- les **Keyframes** qui permet de gérer les effets en fonction du temps

Au centre, on a la visionneuse **Source** qui affiche le média sélectionné et la visionneuse de la timeline (fenêtre programme dans Premiere Pro).

Enfin à droite on retrouve :
- **exportation rapide** pour un export facilité sans changer d'onglet
- **mixeur** qui affiche un vumètres pour visualiser le niveau sonore de nos éléments ou un mixeur qui permet de moduler le son
- **métadonnées** comme sur l'onglet *Média*
- l'**inspecteur** où l'on règle tous les paramètres de l'élément et ses effets

### Timeline

Pour créer une séquence, on peut :
- glisser / déplacer un élément dans la timeline qui est créée automatiquement, qui sera nommée *Timeline 1* qui adoptera les paramètres du projet (définition, framerate…) qu'on peut retrouver en bas à droite sur la roue crantée dans *Configuration du projet > Format de la timeline*
- aller dans son *chutier 01_EDIT*, *clic droit > Timelines > Créer une nouvelle timeline* ou {{< kbd >}}Ctrl{{< /kbd >}} \+ {{< kbd >}}N{{< /kbd >}}

Par défaut le *Start timecode* affiche par convention (?) *01:00:00:00* (1h), on peut changer en *00:00:00:00*. On peut changer le nom, le nombre de pistes audio / vidéo (même si on peut revenir dessus plus tard) et le type de piste audio (mono, stéréo, 5.1, …). On peut également personnaliser les paramètres de la séquence en décochant *Use project settings*.

![New timeline](./new-timeline.png)

Bien différencier l'onglet Format de Moniteur, le premier désignant les paramètres de la timeline et moniteur ceux d'affichage dans la visionneuse qui permet d'alléger la lecture des rushes en choisissant une définition inférieure.

- {{< kbd >}}Alt{{< /kbd >}} \+ {{< kbd >}}molette{{< /kbd >}} ou {{< kbd >}}Ctrl{{< /kbd >}} \+ {{< kbd >}}\ +{{< /kbd >}} et {{< kbd >}}Ctrl{{< /kbd >}} \+ {{< kbd >}}-{{< /kbd >}} pour zoomer / dézoomer la timeline par rapport à la tête de lecture
- {{< kbd >}}j{{< /kbd >}}, {{< kbd >}}k{{< /kbd >}}, {{< kbd >}}l{{< /kbd >}} pour naviguer
- {{< kbd >}}⬆{{< /kbd >}} ou {{< kbd >}}⬇{{< /kbd >}} pour un déplacement de cut en cut
- les touches {{< kbd >}}⬅{{< /kbd >}} / {{< kbd >}}➡{{< /kbd >}} du clavier pour un déplacement précis
- {{< kbd >}}Alt{{< /kbd >}} \+ {{< kbd >}}⬆ / ⬇{{< /kbd >}} déplace un plan d'une ligne à l'autre

On peut désactiver la **sélection liée** en cliquant sur les chaînes au-dessus de la timeline ou en cliquant avec {{< kbd >}}Alt{{< /kbd >}} enfoncé sur l'élément audio ou vidéo.

On peut aussi afficher les onglets timeline à la Adobe Premiere Pro dans les options d'affichage à gauche et cocher **Afficher les timelines superposées**. Au même niveau sur la droite, on peut afficher une timeline l'une au-dessus de l'autre (et plus encore).

![Superposition de timeline](./superposition-timeline.png)

### Insertion
Comme dans Premiere Pro, la source permet de ne récupérer que le son ou que la vidéo

- {{< kbd >}}F9{{< /kbd >}} pour insérer un élément sans écraser
- {{< kbd >}}F10{{< /kbd >}} pour insérer un élément en écrasant
- {{< kbd >}}F11{{< /kbd >}} pour remplacer l'élément sous la tête de lecture
- {{< kbd >}}F12{{< /kbd >}} pour placer l'élément au-dessus au niveau de la tête de lecture
- {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}F10{{< /kbd >}} (écraser et *ripple*) insère l'élément en écrasant entièrement l'élément au niveau de la tête de lecture et raccorde les éléments
- {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}F11{{< /kbd >}} insère l'élément en écrasant entièrement l'élément au niveau de la tête de lecture et adapte la durée du plan inséré en le ralentissant ou en l'accélérant
- {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}F12{{< /kbd >}} pour placer l'élément à la fin de la timeline
- {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}Backspace{{< /kbd >}} pour supprimer un élément et raccorder

À noter que tous ces raccourcis peuvent être retrouvés dans le menu *Edition*

{{< video src="./insertions.webm" autoplay="true" loop="true" muted="true" >}}

En glisser / déplacer, on peut aussi n'importer que la vidéo d'un élément de la *Bibliothèque de médias* en maintenant la touche {{< kbd >}}Alt{{< /kbd >}} et uniquement l'audio en maintenant la touche {{< kbd >}}Maj{{< /kbd >}}.

### Couleurs et drapeaux

On peut dans la *bibliothèque de médias*, on peut définir des drapeaux et une couleur de plan pour chaque élément, qui se retrouveront dans la timeline :

[Couleurs et drapeaux](./couleurs-drapeaux.png)

À noter que si on change à nouveau la couleur du plan dans la timeline, cela n'impactera pas sa couleur dans la bibliothèque.

Il est plus simple d'accéder éventuellement à la couleur ou aux drapeaux dans la fenêtre métadonnées.

### Barre d'outils

[Barre d'outils](./barre-outil.png)

#### Mode sélection {{< kbd >}}A{{< /kbd >}}
Permet de raccourcir ou rallonger un plan avec écrasement, ou de changer la coupe, sélectionner et déplacer un ou plusieurs éléments. Il est intéressant de noter que Da Vinci affiche avec des rectangles blancs les limites des plans

#### Mode trim {{< kbd >}}T{{< /kbd >}}

Similaire à la fonction précédente et de changer la durée des plans mais sans écrasement et fait le raccordement. On voit le résultat en temps réél. Il peut aussi sélectionner les coupes mais les éléments. En sélectionnant la partie haute du plan, il déplace le *in* et *out* comme la fonction *Y* sur Premiere Pro, en sélectionnant la partie basse, il ne change pas la durée du plan mais le déplace en raccordant les plans autour, comme la fonction *U* sur le logiciel d'Adobe

{{< video src="./trim.webm" autoplay="true" loop="true" muted="true" >}}


#### Mode rasoir (blade) {{< kbd >}}B{{< /kbd >}}
Avantage sur l'outil cutter d'Adobe Premier pro, il déroule dans la visionneuse les images survolées par la souris. D'ailleurs, ça fait apparaît au moment du cut des pointillés noirs indiquant que la coupe n'a pas vraiment lieu, la dernière image du premier plan précède bien la première image du second plan et se suivent.

### Options des Pistes
