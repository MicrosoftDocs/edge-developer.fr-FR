---
description: Cette page fournit une vue d’ensemble des nouveautés de EdgeHTML 14.
title: Nouvelles fonctionnalités et API dans EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c99dcb4efb253959d55d96a13ca2249eb5164b68
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233145"
---
# Nouveautés de EdgeHTML 14  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Voici les modifications apportées à EdgeHTML 14, à partir de la [mise à jour anniversaire Windows 10](https://blogs.windows.com/windowsexperience/2016/06/29) (08/2016, Build 14393 \).  Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir [Présentation de la mise à jour anniversaire de Windows 10 EdgeHTML](https://blogs.windows.com/msedgedev/2016/08/04).  

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: [https://aka.ms/devguide_edgehtml_14](./edgehtml-14.md) .  

## Nouvelles fonctionnalités  

### Extensions  

Les extensions sont de petits programmes qui peuvent être utilisés pour ajouter de nouvelles fonctionnalités à Microsoft Edge ou pour modifier les fonctionnalités existantes.  Les extensions sont conçues pour améliorer l’utilisation de la navigation quotidienne d’un utilisateur en fournissant une fonctionnalité de niche essentielle pour les audiences ciblées.  Microsoft Edge prend en charge un nouveau modèle d’extension HTML, JavaScript et CSS.  Ce nouveau modèle est compatible chrome, ce qui signifie que les développeurs d’extensions chrome existants seront en mesure de migrer leurs extensions vers Microsoft Edge avec des modifications minimales.  Pour plus d’informations, consultez la documentation sur les [extensions Microsoft Edge extensions](../../extensions/index.md) .  

### API Fetch  
L' [API FETCH](https://fetch.spec.whatwg.org#fetch-api) utilise la `fetch` méthode permettant d’extraire des ressources.  Dans le passé, cela a été atteint `XMLHttpRequest` .  Non seulement est une extraction plus facile à utiliser, il offre également un accès de niveau inférieur aux requêtes et réponses.  En savoir plus sur l’API FETCH dans le billet de blog Microsoft Edge, [Fetch (ou les limitations pour XHR)](https://blogs.windows.com/msedgedev/2016/05/24).  

### JavaScript  

EdgeHTML 14 apporte un certain nombre de fonctionnalités nouvelles et expérimentales à chakra, le moteur JavaScript permettant de se mettre sur Microsoft Edge:  

#### Nouvelles fonctionnalités  

Activé par défaut  

*   [Paramètres par défaut](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) \ (ES2015 \)
*   [Opérateur d’élévation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) à la puissance \ (ES2016 \)
*   [Array. prototype. include](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) \ (ES2016 \)
*   [Objet. Values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) et [Object. Entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) \ (ES2017 \)  

#### Fonctionnalités JavaScript expérimentales  

Activé avec `about:flags`  

*   [Modules](https://blogs.windows.com/msedgedev/2016/05/17) \ (ES2015 \)  
*   [Async/await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) \ (ES2017 \)  
*   [Symboles Regex](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) \ (ES2015 \)  

Pour plus d’informations, consultez la [vue d’ensemble de la prévisualisation des modules ES6 et plus encore d’ES2015, de ES2016 et de](https://blogs.windows.com/msedgedev/2016/05/17) [code asynchrone plus facile avec la prise en charge des fonctions Async ES2016 dans Chakra et Microsoft Edge](https://blogs.windows.com/msedgedev/2015/09/30).  

### API d’authentification Web  

API Web de la 2,0  

L’API d’authentification Web (anciennement le 2,0 \) dans Microsoft Edge permet aux applications Web d’utiliser la biométrie [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) pour l’authentification des utilisateurs, afin que vous et vos utilisateurs puissiez éviter les problèmes liés à la gestion des mots de passe, y compris le processus de détection de mot de passe, les tentatives de hameçonnage et la journalisation.  L’implémentation actuelle de Microsoft Edge \ (@ `ms-` corrigée) est basée sur un brouillon antérieur de la spécification d’authentification Web et est susceptible d’être modifié à l’avenir.  En savoir plus sur l’authentification Web:  [authentification Web et Windows Hello](../windows-integration/web-authentication.md).

### Notifications Web
Les notifications Web permettent aux sites d’afficher des notifications pour avertir les utilisateurs en dehors du contexte de la page Web et du navigateur, en conformant les utilisateurs de nouveaux messages ou alertes et en permettant aux sites d’améliorer l’engagement des utilisateurs.  Les notifications Web dans Microsoft Edge sont entièrement intégrées à la plateforme de notification et au centre de notifications dans Windows 10 afin d’offrir une interface cohérente avec les autres applications du système et des contrôles simples sur les autorisations et les heures creuses.  Pour plus d’informations, voir [notifications Web dans Microsoft Edge](https://blogs.windows.com/msedgedev/2016/05/16) .  

### API Web Speech
L' [API Web Speech](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) est une API JavaScript composée de deux parties: reconnaissance vocale et synthèse vocale \ (ou conversion de texte par synthèse vocale).  Pour le moment, Microsoft Edge prend en charge uniquement la synthèse vocale.  La synthèse vocale implique la conversion de texte par synthèse vocale qu’un utilisateur entend par le biais de ses haut-parleurs.  Pour plus d’informations, consultez l’article Guide du développeur de synthèse [vocale](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) .  

## Nouvelles API dans EdgeHTML 14

Voici la liste complète des nouvelles API dans EdgeHTML 14.  Ils sont répertoriés au format de `[interface name].[api name]` .  

<iframe height='585' scrolling='no' title='Nouvelles API dans EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Reportez-vous au stylo <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> nouvelles API dans EdgeHTML 14 </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>  
