+++
draft = false
title = 'Codecs'
summary = "Littéralement 'codeur / décodeur', permet de compresser les fichiers vidéo afin de les rendre plus légers, et de les décompresser pour les rendre lisibles"
weight = 60
slug = 'codecs'
+++

Littéralement "codeur / décodeur", permet de compresser les fichiers vidéo afin de les rendre plus légers, et de les décompresser pour les rendre lisibles.

Il existe plusieurs types de codecs :
* les codecs de diffusion permettant d'obtenir le fichier vidéo le plus léger possible tout en conservant la meilleure qualité visuelle possible
* les codecs de montage dont la priorité absolue est de conserver le plus d'information possible sans se préoccuper de la taille du fichier

## Codecs de diffusion
* MPEG-2 (norme et codec), le plus ancien, toujours utilisé par certaines chaînes de télévision
* H264 (ou AVC - Advanced Video Coding) fait partie de la norme MPEG-4 (différent de MP4, qui est un conteneur, voir plus bas)
* H265 (ou HEVC - High Efficiency Video Coding) qui à qualité visuelle également génèrera un fichier vidéo plus léger, il est surtout utilisé pour l'enregistrement dans des petits dispositifs qui capturent en 4K/UHD comme des drones ou des caméras d'action
* VP8/VP9, les codecs de Google sont plus performants que les H264 et H265, utilisé notamment par YouTube et qu'il est recommandé d'utiliser pour la publication sur la plateforme
* AV1, le plus performant actuellement, il est open source mais encore peu répandu même si très apprécié des plateformes de streaming

D'autres codecs sont à venir comme le H266 (ou VVC - Versatile Video Coding) et le AV2.

Pour les métiers des VFX ou de l'étalonnage, il est nécessaire d'avoir les fichiers avec le plus d'informations possibles. Ce n'est pas recommandé non plus en montage, car plus un fichier est compressé, plus le décodage à la volée demandera des ressources à l'ordinateur, et une quantité importante de vidéos compressées dans un logiciel de montage peut rendre l'expérience plus difficile. De plus, ces codecs utilisent une méthode de compréhension nommée **Long GOP** (Group Of Pictures) dont le principe est de compresser via des groupes d'images selon trois types :
* les I Frame (Intra Frame) où le codec va enregistrer toute l'image, elle est peu ou pas compressée, elle sert de référence
* les P Frame (Predictive Frame) et B Frame (Bidirectional predictive Frame) qui ne garderont les différences avec l'image de référence (I Frame)

![Schéma explicatif du long GOP](https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/I_P_and_B_frames.svg/1920px-I_P_and_B_frames.svg.png)

C'est pour cette raison, à chaque fois qu'on fait un arrêt sur une frame précise, qu'on a une chance sur X (dépend du codec) de tomber sur une P ou B Frame que l'ordinateur doit recalculer à partir de son image de référence, ce qui n'est absolument pas optimal.

À noter qu'il existe d'autres méthodes de compression comme l'INTRA qui ne contient que des I Frame, moins efficace que le Long GOP, plus utilisé dans les codecs de montage.

## Codecs de montage
Il en existe deux grandes familles. D'abord, dans la famille **Apple**, créés avec l'arrivée de Final Cut, dont les plus courants sont, du plus au moins compressif et donc du plus léger au plus lourd :
* Apple ProRes Proxy
* Apple ProRes 422
* Apple ProRes 422HQ
* Apple ProRes 4444
* Apple ProRes 4444 XQ

Ces différents codecs existent aussi pour répondre aux besoins différents métiers, les monteurs nécessitent moins d'informations que les étalonneurs ou les VFX.

Bien que le transcodage permette par exemple de changer la méthode de compression d'un codec de diffusion (H264) à un codec de montage (Apple ProRes Proxy), donc de Long GOP à INTRA, ce qui doit fluidifier le montage car il n'y a plus que des I Frame, cela ne peut pas pour autant recréer les informations qui ont été perdues à l'encodage.

L'autre famille c'est **DNx du constructeur AVID** avec deux sous-familles le DNxHD, plus ancienne avec des codecs permettant d'aller jusqu'au Full HD dans des framerates très normés, et le DNxHR pour tout le reste.

Dans l'ordre du plus au moins compressif :
* DNxHD LB (anciennement *DNxHD 36*)
* DNxHD SQ (anciennement *DNxHD 120*)
* DNxHD HQ (anciennement *DNxHD 185*)
* DNxHD HQx (anciennement *DNxHD 185x*)
et
* DNxHR LB
* DNxHR SQ
* DNxHR HQ
* DNxHR HQx
* DNxHR 444

À cas d'usage similaire, un codec équivalent de chaque famille est quasiment identique à quelques subtilités près.

À noter que le *x* de HQx indique qu'il peut aller jusqu'à 10 bits de profondeur de pixel.

## Codecs "d'enregistrement"
Ces codecs issus essentiellement des fabricants de caméras compressent extrêmement peu. Ils peuvent en sortir régulièrement, et tous les logiciels ne sont pas compatibles avec tous ces codecs, il peut être utile de se renseigner auprès du constructeur afin de connaître son utilisation dans son workflow. Quand bien même ils possèdent souvent la dénomination RAW, c'est un abus de langage car le simple fait que ce soit un codec n'en fait pas du RAW.

Dans les plus courants, on a :
* Blackmagic RAW
* REDcode RAW
* Sony X-OCN
* ArriRAW
* Apple ProRes RAW

Bien qu'étant peu compressés, ces codecs ne sont pas adaptés au montage car l'immense quantité de données des fichiers en question rend la lecture très compliquée dû à la vitesse trop limitée des solutions de stockage (HDD, SDD). C'est pourquoi on utilise des proxys parmi les codecs de montage.

## Bitrate / Débit vidéo
Définit comme la quantité d'information par seconde de vidéo, notée en bits/seconde. Les codecs de montage n'étant pas concerné par la question du poids, on s'intéressera surtout au bitrate pour les codecs de diffusion.

Par exemple, pour un fichier 1080p25 encodé en H264, la meilleure qualité visuelle atteignable se trouve pour un bitrate de 15Mbits/s. C'est une valeur de référence connue. Dans ce cas, il est donc inutile d'aller plus haut et à l'inverse, on peut donc réduire le bitrate pour alléger le fichier, aux dépends de la qualité, sachant qu'on garde une image magnifique entre 10 et 15Mbits/s.

Logiquement pour une vidéo H264 en UHD à 25ips aura une qualité maximale à 60Mb/s (4 fois plus de pixels), 30Mb/s pour une vidéo Full HD à 50ips (2 fois plus d'images).
Pour les autres codecs, notamment plus performants comme VP8/VP9 ou AV1, forcément à qualité égale le bitrate sera plus faible, mais connaître cette valeur "maximale" est à chercher.

## CBR / VBR
Ce sont deux traitements de débit vidéo différents :
* CBR : Constant BitRate
* VBR : Variable BitRate

Dans le premier cas c'est simple, chaque seconde de vidéo aura un bitrate fixe, par exemple 15Mb/s. Dans le deuxième, on choisit une fourchette, entre 10 et 15Mb/s par exemple, alors le codec donnera plus de bitrate pour les scènes compliquées à encoder, et moins pour les scènes plus simples. Ainsi, en VBR, la qualité sera équivalente au CBR mais le poids du fichier sera sensiblement plus léger, plus optimisé.

![Comparaison CBR / VBR](https://streaminglearningcenter.com/wp-content/uploads/2021/07/OTT_MI_5-476x525.png)

## Les conteneurs
Différent du codec, improprement appelés extension, c'est le grand tiroir dans lequel on range tous les flux (audio / vidéo / sous-titres…) du fichier vidéo.

Quelques exemples connus :
* MOV (Apple QuickTime)
* MP4  (MPEG4)
* AVI
* MXF (AVID)
* MKV Matroska
* WebM

Les conteneurs sont relativement indépendants des codecs, un MOV peut contenir du H264 comme du ProRes, le MP4 peut contenir du H264 également.

## Fichiers RAW
Les fichiers RAW contiennent des images directement issues du capteur sans codec. Mais du coup, elles ne sont pas lisibles, l'intérêt étant de pouvoir choisir le codec, et un espace colorimétrique, on appelle ça la débayerisation.

![Matrice de Bayer](https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/Bayer_pattern_on_sensor.svg/1024px-Bayer_pattern_on_sensor.svg.png)

Bien que la dénomination RAW sur les codecs d'enregistrement, ils permettent tout de même d'avoir plus la main sur le fichier et de pouvoir appliquer des traitements supplémentaires.