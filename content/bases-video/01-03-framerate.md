+++
draft = false
title = 'Framerate'
summary = "C'est le nombre d'images par seconde"
weight = 30
slug = 'framerate'
+++

C'est le nombre d'images par seconde, présente deux unités :

* FPS (Frames Per Second)
* IPS (Images Par Seconde)

Il existe trois grandes normes de diffusion :

* 24fps est la norme cinéma qu'on retrouve dans les DCP, issue de l 'apparition du son imposant ce minimum pour ne pas saccader le son lu en même temps que la pellicule
* 25fps est une norme télévisuelle héritée du PAL
* 29,97fps est une normale télévisuelle héritée du NTSC

Ces deux dernières fréquences viennent des différences de courant électrique, en 50Hz pour les pays concernés par le PAL/SECAM, et 60Hz pour les pays ayant adopté le NTSC. Cette idée persiste notamment avec les ampoules, toujours en 50 ou 60Hz où le flickering apparaît.

![Flickering](https://www.diffusioneshop.com/img/cms/perchè-sfarfallio-luci-video.webp)

Il existe bien d'autres framerates relativement courants comme 23.976, 48, 50, 59.94, 60, 120...

Ces différents framerates permettent par exemple de faire des ralentis : une vidéo 50ips dans un projet en 25 sera ralentie par deux.

L'interpolation (retime) d'image, c'est le fait de recréer des images manquantes. Dans un projet 25fps avec des sources 25fps, si on veut ralentir par deux un rush, il manquera des images et la vidéo sera saccadée. Le logiciel doit compléter ces lacunes :

* en interpolation par défaut, le logiciel recopie les images
* avec le frameblend, en fusionnant deux images avec une opacité à 50%
* ou l'optical flow (flux optique) où le logiciel calcule la différence entre deux images, mais fonctionne surtout pour les mouvements lents

Ça peut dépanner mais il vaut mieux prévoir dans son projet le framerate final et donc un framerate de captation plus élevé pour faire des ralentis.

{{< video src="https://upload.wikimedia.org/wikipedia/commons/a/a9/Interframe_motion_interpolation.webm" autoplay="true" loop="true" muted="true" >}}

À noter également qu'un tournage à haut framerate, si l'on souhaite garder un flou de mouvement naturel on doit augmenter la fréquence d'obturation (ex : 50fps => 1/100), ce qui implique moins de lumière en entrée pour chaque image, donc une vidéo plus sombre, qu'il faut compenser.

Dans un projet en 25ips où l'on souhaite intégrer un timelapse, il serait nécessaire de prendre assez de clichés pour en avoir 25 par secondes.
