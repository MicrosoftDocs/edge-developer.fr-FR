---
title: Nouvelles fonctionnalités et API dans EdgeHTML 17
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans EdgeHTML 17.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 75429528fd814963a8c78e27f85564223fb2d3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232945"
---
# Nouveautés de EdgeHTML 17  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Vous trouverez ci-dessous une liste des nouvelles fonctionnalités et mises à jour fournies dans la plate-forme Web [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30) , dans le cadre de la [mise à jour 2018 de Windows 10 d’avril](https://blogs.windows.com/windowsexperience/2018/04/27) (04/2018, Build 17134 \).  Pour plus d’informations sur les builds d’aperçu [Windows Insider](https://insider.windows.com) spécifiques, voir le Guide de [Microsoft Edge changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) et [les nouveautés dans EdgeHTML](../whats-new.md).  

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: [https://aka.ms/devguide_edgehtml_17](./edgehtml-17.md) .  

## Fonctionnalités nouvelles et mises à jour  

### Rôles, États et événements ARIA 1,1  

EdgeHTML 17 ajoute une prise en charge de différents rôles, États et propriétés à partir des [applications Internet enrichies accessibles (WAI-ARIA) 1,1](https://w3.org/TR/wai-aria-1.1), y compris les [flux](https://www.w3.org/TR/wai-aria-1.1#feed), le [formulaire](https://www.w3.org/TR/wai-aria-1.1#form), [Aria-haspopup](https://w3.org/TR/wai-aria-1.1#aria-haspopup), [Aria-PlaceHolder](https://w3.org/TR/wai-aria-1.1#aria-placeholder), et bien d’autres encore. Accédez à [la liste complète des mises à jour de Aria dans le changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299).  Avec cette mise à jour, EdgeHTML 17 prend désormais en charge tous les rôles et attributs définis dans le WAI-ARIA 1,1.  <!--  Check out the [Accessibility](../../accessibility.md) docs for more information about accessibility in Microsoft Edge.  -->  

### Masquage CSS  

EdgeHTML 17 inclut une prise en charge expérimentale du [masquage CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking).  L’implémentation partielle présente les propriétés de [masque CSS-image](https://developer.mozilla.org/docs/Web/CSS/mask-image) et [taille de masque](https://developer.mozilla.org/docs/Web/CSS/mask-size) .  Activez l’indicateur «activer le masquage CSS» dans à propos de: indicateurs pour faire des essais.  

### Transformations CSS sur des éléments SVG  

EdgeHTML 17 prend désormais en charge les transformations CSS sur les éléments et les attributs de présentation SVG.  Cela permet de manipuler visuellement des éléments SVG, y compris la rotation, la mise à l’échelle, le déplacement, l’inclinaison ou la traduction.  

### Extensions  

Microsoft Edge prend désormais en charge l' [API notification](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) qui affiche les notifications d’extensions.  Les développeurs d’extensions peuvent désormais créer différents types de notifications \ (standard, liste, image, etc.) qui prennent en charge l’interaction utilisateur complète.  Les notifications sont également automatiquement enregistrées dans le centre de notifications.  Consultez l' [exemple notifications](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) pour savoir comment utiliser cette API dans votre extension.  

EdgeHTML 17 prend désormais également en charge la `Tabs.reload()` méthode dans le cadre de la classe API des onglets standard.  Outre les nouveautés de la mise à jour 2018 de Windows 10, les utilisateurs peuvent désormais choisir d’autoriser les extensions lors de la navigation InPrivate.  

Pour plus d’informations sur les mises à jour d’extensions dans cette version, voir le billet de blog [nouvelles fonctionnalités pour les extensions de la mise à jour 2018 de Windows 10 d’avril](https://blogs.windows.com/msedgedev/2018/05/24).  

### DevTools  

Cette version du DevTools est fournie de deux manières: en tant qu’outils in-browser dans le navigateur `F12` Microsoft Edge et en prévisualisation en tant qu’application autonome [Windows 10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) à partir du Microsoft Store.  

:::image type="complex" source="../../devtools-protocol/media/microsoft-edge-devtools.png" alt-text="Application Microsoft Edge DevTools" lightbox="../../devtools-protocol/media/microsoft-edge-devtools.png":::
   Application Microsoft Edge DevTools  
:::image-end:::  

Les outils sont également mis à jour à l’aide d’un certain nombre de fonctionnalités importantes, notamment la prise en charge de base pour le débogage [à distance](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) \ (via notre nouveau [protocole devtools](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)\), les [fonctionnalités de débogage](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging)de IndexedDB, la [gestion du cache](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection), l' [ancrage vertical](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) et bien plus encore. Nous avons également continué la mise en route globale de la [refactorisation](./edgehtml-16.md) dans le cadre d’investissements en cours de performance et de fiabilité.  

Pour plus d’informations, visitez [la page devtools de la dernière mise à jour de Windows 10 (EdgeHTML 17)](../../devtools-guide/whats-new/edgehtml-17.md) .  

### JavaScript  

Avec EdgeHTML 17 le moteur JavaScript Chakra introduit des améliorations des performances dans plusieurs zones clés:  

:::row:::
   :::column span="1":::
      **Empreinte mémoire plus allégée**  
   :::column-end:::
   :::column span="2":::
      *   \ (Re-\) différer l’analyse des [fonctions](https://github.com/Microsoft/ChakraCore/pull/4105) et [méthodes de flèche sur des littéraux d’objets](https://github.com/Microsoft/ChakraCore/pull/4136)  
      *   [Refactorisation de bytecode RegExp](https://github.com/Microsoft/ChakraCore/pull/3915)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Compléments JavaScript plus rapides**
   :::column-end:::
   :::column span="2":::
      *   [Type de partage pour Object. Create](https://github.com/Microsoft/ChakraCore/pull/3901)  
      *   [Cache de ligne polymorpho pour l’objet. assigner](https://github.com/Microsoft/ChakraCore/pull/3792)  
      *   [Optimisations JSON. Parse/stringify](https://github.com/Microsoft/ChakraCore/pull/4077)  
      *   [Réécriture d’itérateurs de tableau en JavaScript et plus rapide pour... de](https://github.com/Microsoft/ChakraCore/pull/4095)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Assembly Web**
   :::column-end:::
   :::column span="2":::
      *   [Prise en charge de l’inlingo](https://github.com/Microsoft/ChakraCore/pull/3681)  
   :::column-end:::
:::row-end:::  

Pour en savoir plus, consultez la rubrique amélioration des performances des fonctions [JavaScript et Webassembly dans EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/06/19) .  

### Élément multimédia

EdgeHTML 17 inclut les mises à jour apportées à [HTMLMediaElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) , notamment:  

*   Le nouvel `preload` attribut sur l' [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) élément indique les données qui doivent être préchargées.
*   L’ajout de la [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) méthode et de la [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) propriété permet aux développeurs de sélectionner le périphérique de sortie audio.  
    
    > [!NOTE]
    > Ce n’est pas encore disponible dans RTC.  
    
### API de capture multimédia  

Microsoft Edge prend désormais en charge la capture d’écran dans RTC via l' [API de capture multimédia](https://w3c.github.io/mediacapture-screen-share).  Cette fonctionnalité permet de capturer la sortie du périphérique d’affichage d’un utilisateur, souvent utilisée pour diffuser un bureau pour les réunions virtuelles ou les présentations virtuelles sans plug-in.  

### Applications web progressives  

À partir de EdgeHTML 17, les travailleurs de services et les notifications de transmission sont activés par défaut \ (en savoir plus sur ces fonctionnalités dans le service de publication de blog [: sortir au-delà de la page](https://blogs.windows.com/msedgedev/2017/12/19)).  Cette opération a pour fin la suite de technologies \ (y compris les API FETCH Networking et de mise en cache \), qui comporte la Fondation technique pour les applications Web progressives (PWAs \) sur Windows 10.  

Les PWAs sont des applications Web qui ont été [progressivement améliorées](https://en.wikipedia.org/wiki/Progressive_enhancement) avec des fonctionnalités de type application native sur la prise en charge des plateformes et des moteurs de navigateur, tels que le lancement de l’écran de démarrage, la prise en charge hors ligne et les notifications de transmission.  Sur Windows 10 avec le moteur Microsoft Edge \ (EdgeHTML \), PWAs Profitez de l’avantage supplémentaire de s’exécuter indépendamment de la fenêtre du navigateur en tant qu’applications pour la [plateforme Windows universelle](/windows/uwp/get-started/whats-a-uwp) .  

Au-delà de PWAs, les travailleurs de services et l’API de cache permettent aux développeurs d’intercepter les requêtes réseau et de répondre à partir du cache.  Il n’est pas nécessaire qu’un site Web prenne en charge la mise en cache du service de travail pour la fiabilité et les performances de chargement des pages affinées, ainsi que la possibilité d’offrir une utilisation hors connexion pendant des périodes de connexion Internet ou médiocre.  

Pour en savoir plus sur les travailleurs de services et les détails sur PWAs sur Windows 10, consultez notre [site Web sur](../../progressive-web-apps/index.md) les documents Windows.  

### Sécurité Web  

EdgeHTML 17 apporte une prise en charge de l’intégrité des sous-ressources \ (SRI \).  [L’intégrité](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) des sous-ressources est une fonctionnalité de sécurité qui permet aux navigateurs de vérifier que les ressources récupérées (telles que les images, les scripts, les polices, etc.) sont transmises sans manipulation inattendue.  

Ajoutez un `integrity` attribut contenant une représentation de hachage de chiffrement de la ressource que vous prévoyez de charger sur votre page Web sur un `<script>` `<link>` élément ou, comme dans l’exemple ci-dessous.  Ensuite, Microsoft Edge compare la ressource demandée au hachage défini dans l' `integrity` attribut.  S’ils ne correspondent pas, Microsoft Edge n’exécutera pas la ressource et renverra une erreur au réseau.  

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```  

Par ailleurs, nouveau dans EdgeHTML 17, l’en-tête de requête [mise à niveau-demandes non sécurisées autorise les](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) navigateurs à demander une interface de navigation sécurisée.  Cet en-tête indique au serveur que le navigateur prend en charge la mise à niveau de toutes les demandes non sécurisées et que l’utilisateur doit être redirigé vers une version sécurisée du site, le cas échéant.  

### Polices variables
La prise en charge complète des polices variables \ (y compris CSS [font-variance-Settings](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) et [font-Sizing-dimensionnement](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)) est disponible dans EdgeHTML 17.  Les polices variables permettent aux développeurs d’obtenir l’apparence de différentes polices avec une seule police en ajustant différents axes, ce qui permet de réduire le nombre de fichiers de police et de meilleures performances.  

Retrouvez-nous sur [une expédition pour en savoir plus sur les polices variables fournies par les développeurs et les concepteurs Web](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts), et la manière de les utiliser sur votre site.  Pour en savoir plus sur les polices variables du billet de blog, [vous pouvez utiliser une typographie expressif et performante sur Microsoft Edge avec des polices variables](https://blogs.windows.com/msedgedev/2018/03/13).  

<iframe height='456' scrolling='no' title='Exemples de billets à Maré variable' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Reportez-vous à la rubrique <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> exemples de tickets de la variable PEN </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>  

## Nouvelles API dans EdgeHTML 17  

Voici la liste complète des nouvelles API dans EdgeHTML 17.  Ils sont répertoriés au format de `[interface name].[api name]` .  

> [!NOTE] 
> Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certains peut toujours être en développement.  Reportez-vous à la rubrique  [État de plateforme Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) pour le mot officiel sur la prise en charge des fonctionnalités.  

<iframe height='580' scrolling='no' title='Nouvelles API dans EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Reportez-vous au stylo <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> nouvelles API dans EdgeHTML 17 </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>  

> [!TIP]
> Nous nous sommes [associés à d'](https://blogs.windows.com/msedgedev/2017/10/18) autres navigateurs et à la communauté Web dans le cadre de l’adoption de [documents Web MDN](https://developer.mozilla.org) comme endroit définitif dans le cadre de la mise en place d’une documentation indépendante du navigateur pour les technologies Web actuelles et émergeantes.  Vous trouverez des informations détaillées sur la prise en charge de l’API EdgeHTML directement dans chaque page de la [bibliothèque de références Web MDN](https://developer.mozilla.org/docs/Web).  Pour obtenir les dernières fonctionnalités prises en charge dans Microsoft Edge, consultez l’état de la [plateforme](https://developer.microsoft.com/microsoft-edge/status) de Microsoft Edge.  

## Versions précédentes de EdgeHTML  

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)  

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)  

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)  

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)  
