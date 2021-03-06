---
description: Ce guide fournit une vue d’ensemble des fonctionnalités et normes de développement incluses dans EdgeHTML 16.
title: Nouvelles fonctionnalités et API dans EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, développement web, html, css, javascript, développeur
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399196"
---
# <a name="whats-new-in-edgehtml-16"></a>Nouveautés de EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Voici une liste des fonctionnalités nouvelles et mises à jour livrées sur la plateforme web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) dans le cadre de [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).  Pour plus d’informations sur les modifications apportées aux builds Windows Insider Preview spécifiques, voir le microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) et les nouveautés dans [EdgeHTML](../whats-new.md).  

Voici le lien de la liste de modifications suivante  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) :  

## <a name="new-and-updated-features"></a>Fonctionnalités nouvelles et mises à jour  

### <a name="css-grid-layout"></a>Disposition de la grille CSS  

Microsoft Edge prend désormais en charge l’implémentation sans préfixe de la disposition de [grille CSS.](https://www.w3.org/TR/css-grid-1)  [La disposition en](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) grille définit un système de disposition en grille à deux dimensions qui offre plus de fluidité de disposition que possible avec le positionnement à l’aide de flottants ou de scripts.  L’exemple ci-dessous utilise la disposition de grille CSS pour créer la structure d’une page web de base.  

<iframe height='303' scrolling='no' title='Disposition de la grille CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Voir la disposition de la <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> grille CSS </a> stylet par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) sur </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

### <a name="css-object-fit-and-object-position"></a>Ajustement de l’objet CSS et position de l’objet  

EdgeHTML 16 introduit la prise en charge des propriétés CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) et [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Ces propriétés contrôlent la position et la taille du contenu remplacé dans la zone de contenu.  

### <a name="developer-tools"></a>Outils de développement  

Cette version a démarré un effort majeur de refactoriser Microsoft Edge DevTools pour améliorer la robustesse et les performances, et nous avons également ajouté de nouvelles fonctionnalités que vous pouvez commencer à utiliser aujourd’hui sur les builds [Windows Insider.](https://insider.windows.com)  Consultez le [guide Microsoft Edge DevTools pour](../whats-new.md) en savoir plus sur ce qui a changé !  

### <a name="javascript"></a>JavaScript  

[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) s’appuie sur les optimisations des performances JavaScript des versions précédentes en développez la capacité du moteur DeCaler à différer/différer des fonctions, à utiliser des caches en ligne polymorphes et à optimiser les fonctions avec des `try` / `finally` blocs.  

En outre, les fonctionnalités d’abord prévisualisations dans EdgeHTML 15 sont désormais stables et activées par défaut :  

#### <a name="new-features"></a>Nouvelles fonctionnalités  

Activé par défaut  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)  
*   [Mémoire partagée et atomiques](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a>API de demande de paiement  

[L’API](../windows-integration/payment-request-api.md) de demande de paiement est une norme ouverte inter-navigateur qui permet aux navigateurs d’agir en tant qu’intermédiaires entre les marchands, les consommateurs et les modes de paiement \(tels que les cartes de crédit\) que les consommateurs ont stockés dans le cloud.  L’API dans EdgeHTML 16 a été mise à jour pour correspondre à la dernière spécification de [l’API](https://w3c.github.io/payment-request) de demande de paiement W3C.  Cela inclut les opérations suivantes:  

*   Prise en charge de la `canMakePayment()` méthode  
*   Prise en charge de la `requestId` propriété  
*   Prise en charge de la `id` propriété  
*   La valeur par défaut du paramètre de la méthode est modifiée `complete()` de « » à « unknown `result` »  

### <a name="service-workers"></a>Worker du service  

[Les travailleurs de](https://www.w3.org/TR/service-workers-1) service sont des scripts pilotés par des événements qui s’exécutent en arrière-plan d’une page web.  Les employés de service activent des fonctionnalités auparavant disponibles uniquement avec les applications natives, telles que l’interception et la gestion des demandes en provenance du réseau, la gestion et la gestion de la synchronisation en arrière-plan, du stockage local et des notifications Push.  La prise en charge du service de travail est toujours en cours de développement, mais vous pouvez tester votre PWA dans Microsoft Edge avec notre support de travail de service expérimental en activant la fonctionnalité de travail de service dans `about:flags` .  

### <a name="webvr"></a>WebVR  

WebVR pour Microsoft Edge a ajouté la prise en charge des [contrôleurs de mouvement.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Ces contrôleurs ont une position précise dans l’espace, ce qui permet une interaction précise avec les objets numériques dans la réalité virtuelle.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Contrôleurs de mouvement" lightbox="../media/MotionControllers.jpg":::
   Contrôleurs de mouvement  
:::image-end:::  

WebVR a également été optimisé pour prendre en charge deux types d’expériences différents.  

**PC Windows Mixed Reality :** ordinateurs de bureau et ordinateurs portables avec des graphiques intégrés.  Lorsqu’ils sont branchés sur ces appareils, nos casques immersifs s’exécutent à 60 images par seconde.  
**PC Windows Mixed Reality Ultra :** ordinateurs de bureau et ordinateurs portables avec des graphiques discrets.  Lorsqu’ils sont branchés sur ces appareils, nos casques immersifs s’exécutent à 90 images par seconde.  

Les deux configurations ront les mêmes expériences immersives vidéo et de jeu.  

Pour plus d’informations sur les mises à jour Windows Mixed Reality à venir, consultez le billet de blog sur les mises à jour de [congés Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Pour obtenir des guides et des démonstrations, voir le Guide du développeur [WebVR.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Étant donné que les spécifications WebVR sont toujours en cours de développement, l’implémentation de Microsoft Edge peut changer ultérieurement.  

## <a name="new-apis-in-edgehtml-16"></a>Nouvelles API dans EdgeHTML 16  

Voici la liste complète des nouvelles API dans EdgeHTML 16.  Ils sont répertoriés au format `[interface name].[api name]` .

> [!NOTE] 
> Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certaines d’entre elles est peut-être encore en cours de développement.  Reportez-vous [à l’état de la](https://developer.microsoft.com/microsoft-edge/platform/status) plateforme Microsoft Edge pour le mot officiel sur la prise en charge des fonctionnalités.  

---  

<iframe height='559' scrolling='no' title='Nouvelles API dans EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Voir les nouvelles API stylet dans <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> EdgeHTML 16 </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) sur </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## <a name="previous-edgehtml-releases"></a>Versions EdgeHTML précédentes  

[EdgeHTML 12 / Windows build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Windows build 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Windows build 15063 (4/2017)](./edgehtml-15.md)  
