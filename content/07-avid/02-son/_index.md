+++
draft = false
title = 'Son'
summary = ""
weight = 2
slug = 'son'
editURL = 'https://github.com/sylvainconny/cours-eanis/edit/main/content/${FilePath}'
+++

À noter qu'Avid Media Composer gère par défaut les pistes son en dual mono.

## Waveform
Les Waveform ne sont pas affichées par défaut, il faut se rendre dans le *burger de la timeline > Audio Data > Waveform*.
Pour changer l'affichage des Waveform {{<kbd>}}Ctrl{{</kbd>}} \+ {{<kbd>}}Alt{{</kbd>}} \+ {{<kbd>}}K{{</kbd>}} et {{<kbd>}}Ctrl{{</kbd>}} \+ {{<kbd>}}Alt{{</kbd>}} \+ {{<kbd>}}L{{</kbd>}}.

## Gain
L'affichage du vuemètre se trouve dans **Tools > Audio Tool**. Pour un mixage efficace, on va également chercher *Tools > Audio Mixer*. Il peut également se gérer directement dans la timeline de façon moins précise sur un clip en l'affichant via *burger de la timeline > Audio Data > Clip Gain*.

À noter que que chaque piste dans l'audio mixer s'applique uniquement sur le clip sous la tête de lecture :

{{<video src="./audio-mixer.webm" autoplay="true" loop="true" muted="true">}}

Pour lier les pistes entre elles et ne pas avoir à changer manuellement chaque piste, on a le libellé **Gang** en haut de chaque piste son dans le mixeur. Les pistes de même couelur de Gang seront liées.

{{<video src="./gang.webm" autoplay="true" loop="true" muted="true">}}

Pour appliquer à toute la piste le gain du clip sous la tête de lecture, c'est dans le menu burger de la fenêtre audio mixer, l'option **Set clip Gain On Track Global**.

{{<video src="./track-global.webm" autoplay="true" loop="true" muted="true">}}

## Pan
Pour spatialiser l'audio, on utlise l'outil au-dessus des pistes dans l'Audio Mixer. On choisit à quel point à gauche (L) ou à quel point à droite (R) l'audio d'une piste doit être rendu. {{<kbd>}}Alt{{</kbd>}} \+ {{<kbd>}}Clic{{</kbd>}} sur l'outil de spatialisation.

Afin de faciliter le travail de mixage d'audio pendant le montage, il est pertinent d'aller dans *File > Settings > User > Setting > Audio*, il faut modifier *Default pan for mono tracks* en **Alterning L/R**.

{{<video src="./spatialisation.webm" autoplay="true" loop="true" muted="true">}}

## Keyframes
Pour gérer le volume : *burger de la timeline > Audio Data > Volume* et vérifier que l'Audio Keyframe soit activé dans la barre de la timeline, l'icône avec les deux triangles ou {{<kbd>}}Shift{{</kbd>}} \+ {{<kbd>}}Z{{</kbd>}}.

On créé une keyframe sur les pistes sélectionnées avec la touche {{<kbd>}}%{{</kbd>}}. On les supprime en les sélctionnant et en tapant {{<kbd>}}Backspace{{</kbd>}}. Pour changer le volume, c'est à la souris, si on peut les déplacer dans le temps, c'est {{<kbd>}}Alt{{</kbd>}} et souris.

{{<video src="./audio-keyframes.webm" autoplay="true" loop="true" muted="true">}}

On peut gérer également avec la spatialisation, en affichant le **Track control panel** et en réglant les keyframes sur *Pan*, alors les keyframes créées serviront à la spatialisation : en haut de la piste, le son sera à gauche, en bas l'inverse.

{{<video src="./pan-spatial.webm" autoplay="true" loop="true" muted="true">}}