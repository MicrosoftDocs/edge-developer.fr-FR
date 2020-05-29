---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans Microsoft Edge.
title: Guide du développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 36c5e6530ff584a97e4b42910757495362a1960d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564715"
---
# Nouveautés de EdgeHTML 16

Vous trouverez ci-dessous une liste des nouvelles fonctionnalités et mises à jour qui sont incluses dans la mise à jour de [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17/edgehtml-16-fall-creators-update/) Web, dans le cadre de la [mise à jour de Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update/) pour les créateurs (10/2017, Build 16299). Pour plus d’informations sur les builds d’aperçu Windows Insider spécifiques, voir le Guide de [Microsoft Edge changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/) et [les nouveautés dans EdgeHTML](../whats-new.md).

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: [https://aka.ms/devguide_edgehtml_16](https://aka.ms/devguide_edgehtml_16) .

## Fonctionnalités nouvelles et mises à jour

### Disposition Grille CSS

Microsoft Edge prend désormais en charge l’implémentation sans préfixe de la [disposition Grid CSS](https://www.w3.org/TR/css-grid-1/). La [disposition Grille](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) définit un système de disposition sur une grille en deux dimensions qui permet d’utiliser une fluidité de la disposition avec des valeurs flottantes ou des scripts. L’exemple ci-dessous utilise la disposition Grid CSS pour créer la structure d’une page Web de base.


<iframe height='303' scrolling='no' title='Disposition Grille CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Pour en savoir plus sur les feuilles de style CSS de stylet <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> </a> , voir MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .
</iframe>


### Feuilles CSS `object-fit` et `object-position`

EdgeHTML 16 instaure une prise en charge des propriétés CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) et [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Ces propriétés contrôlent la position et la taille du contenu remplacé au sein de la zone de contenu.  

### Outils de développement

Dans cette version, nous avons commencé un important effort de refactorisation de Microsoft Edge DevTools pour améliorer la fiabilité et les performances, ainsi que les nouvelles fonctionnalités que vous pouvez commencer à utiliser aujourd’hui sur les builds [Windows Insider](https://insider.windows.com/) .  Consultez le [Guide Microsoft Edge devtools](../../devtools-guide/whats-new.md) pour en savoir plus sur les modifications.

### JavaScript

[EdgeHTMLx](https://blogs.windows.com/msedgedev/2017/10/31/optimizations-webassembly-sharedarraybuffer-atomics-edgehtml-16/#FodxEPHxR4WkbtyA.97) , xxx xxxxxxx XX xxxxxxx XX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XX xxxxxxx XX xxxxxxx, xxxxxxx, xxx xxxxxxxxx xxxxxxxxx *try/finally* xxx xxxxxxx xxxxxxxxx XX XXX xxxxxxx.

De plus, les fonctionnalités d’abord prévisualisées dans EdgeHTML 15 sont désormais stables et activées par défaut:

#### Nouvelles fonctionnalités (option activée par défaut)

* [Ensemble d’assemblys](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP ([démo](https://webassembly.org/demo/))
* [Mémoire partagée et Atomic.](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

### API de demande de paiement

L' [API de demande de paiement](../windows-integration/payment-request-api.md) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.  L’API dans EdgeHTML 16 a été mise à jour pour correspondre à la dernière spécification de l' [API de demande de paiement](https://w3c.github.io/payment-request/) du W3C. Cela inclut les opérations suivantes:
* Prise en charge de la `canMakePayment()` méthode
* Prise en charge de la `requestId` propriété
* Prise en charge de la `id` propriété
* La valeur par défaut du `complete()` paramètre de la méthode est `result` passée de «» à «Unknown».

### Travailleurs de service

Les [travailleurs de service](https://www.w3.org/TR/service-workers-1/) sont des scripts pilotés par des événements qui s’exécutent en arrière-plan d’une page Web. Les travailleurs de service activent les fonctionnalités qui ne sont disponibles que pour les applications natives telles que l’interception et la gestion des demandes à partir du réseau, la gestion et la gestion de la synchronisation en arrière-plan et des notifications de transmission. La prise en charge du travailleur de service est en cours de développement, mais vous pouvez tester votre PWA dans Microsoft Edge avec le support technique de votre service expérimentée en activant la fonctionnalité du travailleur de service dans **à propos de: indicateurs**.

### WebVR
WebVR pour Microsoft Edge a ajouté la prise en charge des [contrôleurs de mouvement](https://developer.microsoft.com/windows/mixed-reality/motion_controllers). Ces contrôleurs disposent d’une position précise dans l’espace, ce qui permet d’interagir avec une fine graine avec des objets numériques dans la réalité virtuelle.

![Contrôleurs de mouvement](../media/MotionControllers.jpg)

WebVR a également été optimisé pour prendre en charge deux types d’expériences différents.

PCs-ordinateurs de bureau et ordinateurs portables **Windows mixte** avec graphiques intégrés.  Lorsque vous êtes branché sur ces appareils, nos casques immersives s’exécutent à 60 images par seconde.  
**Windows mixte Real Real PC** -ordinateurs de bureau et ordinateurs portables avec graphiques discrets. Lorsque vous êtes branché sur ces appareils, nos casques immersives s’exécutent à 90 images par seconde.   

Les deux installation prennent en charge les mêmes expériences de vidéo et de jeu. 

Pour plus d’informations sur les prochaines mises à jour de Windows Mixed Reality, consultez le billet de blog consacré à la mise à jour des congés pour [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update/) . 

Pour les guides et les démonstrations, voir le [Guide du développeur de WebVR](https://docs.microsoft.com/microsoft-edge/webvr/).

 > [!NOTE] 
 > Dans la mesure où la spécification WebVR est toujours en développement, la mise en œuvre de Microsoft Edge peut changer plus tard.

## Nouvelles API dans EdgeHTML 16

Voici la liste complète des nouvelles API dans EdgeHTML 16. Ils sont répertoriés au format **[nom de l’interface]. [ nom de l’API]**.

> [!NOTE] 
> Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certains peut toujours être en développement. Reportez-vous à la rubrique [État de plateforme Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) pour le mot officiel sur la prise en charge des fonctionnalités.

<iframe height='559' scrolling='no' title='Nouvelles API dans EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Voir le stylet <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> nouvelles API dans EdgeHTML 16 </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe></p>

<h2 id="previous-edgehtml-releases">Versions précédentes de EdgeHTML</h2>
<p><a href="https://aka.ms/devguide_edgehtml_12" data-raw-source="[EdgeHTML 12 / Windows build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)">EdgeHTML 12/Windows Build 10240 (7/2015)</a>

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)
