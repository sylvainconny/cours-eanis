+++
draft = false
title = 'Derush'
summary = "Différentes méthodes de derush"
weight = 3
slug = 'derush'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

## Méthode 1
Il peut être pertinent de créer une séquence **01_DERUSH** pour faire une présélection des rushes qu'on souhaite garder avec le montage en trois points. Puis une **02_OURS** pour un premier montage grossier avec les plans dans l'ordre, sans musique ni effet.

1. Sélectionner un rush en double-cliquant
2. Taper sur I (pour In) pour définir le début du rush à insérer dans la timeline
3. Taper sur O (pour Out) pour définir la fin du rush à insérer dans la timeline
4. Glisser / déplacer le rush prédécoupé dans la séquence ou taper sur la touche {{< kbd >}},{{< /kbd >}} pour l'ajouter en déplaçant / la touche {{< kbd >}};{{< /kbd >}} pour ajouter et écraser

## Méthode 2
1. Mettre tous les plans dans une nouvelle séquence **00_BAB** (pour Bout à Bout)
2. Dupliquer la séquence et la renommer **01_DERUSH**
3. Dans cette dernière, placer des points *in* et *out* avec {{< kbd >}}I{{< /kbd >}} et {{< kbd >}}O{{< /kbd >}} sur un plan et utiliser {{< kbd >}}Alt{{< /kbd >}} \+ {{< kbd >}}⬆{{< /kbd >}} pour remonter le plan découpé sur la piste du haut (piste V2) ; si tout le plan nous plait, le raccourci {{< kbd >}}X{{< /kbd >}} permet de placer le *in* et *out* sur l'ensemble du plan
4. Répéter cette action jusqu'à la fin du dérush
5. Une fois tous les éléments sélectionnés sur la piste V2, on veut supprimer ceux de la piste V1 contenant toutes les parties de plans qu'on ne souhaite pas conserver en utilisant l'outil Sélection en amont (A)


### Précautions
- si un plan est sélectionné (entouré de blanc), c'est lui qui sera remonté, pas la partie entre *in* et *out*
- bien vérifier également que le paramètre *Séquence > La sélection suit la tête de lecture* soit décoché
- il faut aussi que l'option *Sélection liée* soit bleue pour que la musique soit bien sélectionnée également
- la piste V2 ne doit pas être verrouillée

### Raccourcis à rajouter

Il peut être pertinent pour se faciliter la vie d'ajouter la touche {{< kbd >}}P{{< /kbd >}} en plus de {{< kbd >}}Alt{{< /kbd >}} \+ {{< kbd >}}⬆{{< /kbd >}} pour remonter les pistes, ainsi les touches {{< kbd >}}I{{< /kbd >}}, {{< kbd >}}O{{< /kbd >}} et {{< kbd >}}P{{< /kbd >}} sont à côté pour exécuter cette méthode de Dérush. Dans les Raccourcis clavier, c'est la commande *Décaler la sélection de l'élément vers le haut*.

On peut aussi rajouter le raccourci {{< kbd >}}U{{< /kbd >}} en plus de {{< kbd >}}Ctrl{{< /kbd >}} \+ {{< kbd >}}Maj{{< /kbd >}} \+ {{< kbd >}}X{{< /kbd >}} pour *Effacer l'entrée et la sortie* (annuler le *in* et *out*).