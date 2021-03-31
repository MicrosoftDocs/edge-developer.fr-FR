---
description: Cette page fournit une vue d’ensemble des nouveautés de EdgeHTML 12.
title: Nouvelles fonctionnalités et API dans EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a96d75ff7decf2c6efdfee3be94736707fea5a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233143"
---
# Nouveautés de EdgeHTML 12  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge présente EdgeHTML, un nouveau moteur «vivant» conçu pour une interopérabilité à son cœur, afin de vous assurer que vous avez toujours accès à la version la plus récente de la plateforme Windows Web.  Microsoft Edge est un saut de passe net par le passé, gratuitement à partir du code hérité requis pour prendre en charge les contrôles ActiveX, les objets d’assistance du navigateur (BHO \) et d’autres pratiques de développement Web Bygone.  Par ailleurs, Microsoft Edge fournit une prise en charge native PDF.  À partir de IE11, les modes de document hérités ont été déconseillés, et avec Microsoft Edge, l’infrastructure de navigateur pour les prendre en charge n’existe pas.  Pour plus d’informations, consultez [IEBlog](/archive/blogs/ie/living-on-the-edge-our-next-step-in-interoperability) .  

Voici les modifications envoyées avec EdgeHTML 12 dans la version initiale de [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) \(07/2015, Build 10240 \).  Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir [une pause dans le passé: la naissance du nouveau moteur de rendu Web de Microsoft](https://blogs.windows.com/msedgedev/2015/02/26) et [un saut passé par le passé, 2e partie: dire adieu aux contrôles ActiveX, VBScript et AttachEvent...](https://blogs.windows.com/msedgedev/2015/05/06).  

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante:  [https://aka.ms/devguide_edgehtml_12](./edgehtml-12.md) .  

## Nouvelles fonctionnalités  

### Politique de sécurité du contenu 1,0  

Microsoft Edge implémente désormais la stratégie de sécurité du contenu \(CSP \) 1,0.  La norme de sécurité du fournisseur de services cryptographiques permet aux développeurs Web de contrôler les ressources \(script, CSS, plug-ins, images, etc.) qui peuvent être récupérées ou exécutées dans le cadre de la recherche de contenu malveillant dans le contexte d’une page Web digne de confiance.  Pour plus d’informations sur les fournisseurs de services cryptographiques dans Microsoft Edge, voir [stratégie de sécurité du contenu](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) .  

### Effets de filtre  

Microsoft Edge fournit un moyen facile d’ajouter des effets visuels aux éléments.  À l’aide de la `filter` propriété, vous pouvez ajouter des flous, ajuster la luminosité, ajouter une ombre portée, modifier l’opacité, etc.  À l’aide d’une feuille de style CSS uniquement, vous pouvez appliquer plusieurs effets de filtre à un élément et animer les filtres.  Pour plus d’informations, voir [effets de filtre](https://developer.mozilla.org/docs/Web/CSS/filter).  

### JavaScript  

La prise en charge de JavaScript varie légèrement entre la version finale d’Internet Explorer \(IE11 \) et Microsoft Edge.  Les nouvelles fonctionnalités de Microsoft Edge sont les suivantes:  

:::row:::
   :::column span="1":::
      **Relevés**  
   :::column-end:::
   :::column span="2":::
      [classe](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) \(expérimental \), [pour... de](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Objets**  
   :::column-end:::
   :::column span="2":::
      [Promesse](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [symbole](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [WeakSet](/scripting/javascript/reference/weakset-object-javascript)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Fonctions**  
   :::column-end:::
   :::column span="2":::
      [acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [IsNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [RAW](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Méthodes**  
   :::column-end:::
   :::column span="2":::
      [inclut](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [Keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) \(matrice \), [REPEAT](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) \(chaîne \), [valeurs](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) \(matrice \)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Autres fonctionnalités**  
   :::column-end:::
   :::column span="2":::
      [Fonctions](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) \(expérimental \), [générateurs](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators),  [itérateurs](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` indicateur d’expression régulière](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) \(expérimental \), [chaînes de modèle](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), caractères d’échappement de point de [code Unicode](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)  
   :::column-end:::
:::row-end:::  

Pour en savoir plus sur la prise en charge JavaScript entre les applications Internet Explorer, Microsoft Edge et Microsoft Store, voir [informations sur la version JavaScript](./javascript-version-information.md).  

### Capture multimédia et flux  

Microsoft Edge présente la prise en charge des API de capture multimédia et de flux, en fonction de la spécification de [capture et de flux de média W3C](https://w3c.github.io/mediacapture-main/getusermedia.html) .  Ces API JavaScript permettent aux pages Web d’accéder aux périphériques de capture multimédias, tels que des webcams ou des microphones, avec l’autorisation de l’utilisateur.  À l’aide des API de capture multimédia et de flux, vous pouvez créer des scénarios comme la capture d’une photo à l’aide d’une webcam ou la capture d’un message vocal à partir d’un micro.  Pour en savoir plus sur la capture multimédia dans Microsoft Edge, consultez le [blog du développeur Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/13).  

### Nouvel élément HTML et attributs  

*   `meter` élément  
*   `picture` élément  
*   `template` élément  
*   `image` élément: `srcset` et `sizes` attributs \( [billet de blog](https://blogs.windows.com/msedgedev/2015/06/08)du développeur Microsoft Edge \)  
*   `selectionDirection` attribut  
*   `input type=time` et `input type=datetime-local`  

### API RTC Object  

Les communications d’objets Real-Time \(ORTC \) permettent le contenu multimédia \(audio et/ou vidéo) en flux (envoyés et reçus) en temps réel entre les navigateurs Web, les appareils mobiles et les serveurs par le biais des API JavaScript natives.  Pour plus d’informations sur la validation de l’utilisation de la mise en route dans Microsoft Edge, voir [objet](https://ortc.org) sujet du Guide de développement.  

### Mode lecture  

Microsoft Edge fournit un mode lecture pour une connaissance plus rationalisée et plus agréable de la lecture de pages Web, sans la distraction de contenus non liés ou secondaires sur la page.  Le mode lecture peut être activé ou désactivé à partir du bouton lecture \(icône du livre \) sur la barre d’adresse ou avec `Ctrl` + `Shift` + `R` .  Pour plus d’informations, consultez le [mode lecture](../browser-features/reading-view.md) .  

### Découverte de moteur de recherche  

L’intégration de recherche complète est intégrée à la barre d’adresses Microsoft Edge, y compris aux suggestions de recherche, aux résultats provenant du Web, à votre historique de navigation et aux favoris.  Microsoft Edge suit la spécification [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) pour découvrir et utiliser les fournisseurs de recherche Web.  Si vous êtes un fournisseur de recherche, [en savoir plus](../browser-features/search-provider-discovery.md) sur la façon de s’assurer que Microsoft Edge prend en charge votre service.  

### Prise en charge des API WebKit  

Pour une meilleure compatibilité, Microsoft Edge prend en charge un large éventail d' `-webkit-` API préréglées.  Pour obtenir la liste complète des API prises en charge `-webkit-` , utilisez le [catalogue API](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).  

### Audio Web  

Microsoft Edge présente la prise en charge de la spécification de l' [API audio Web W3C](https://webaudio.github.io/web-audio-api) .  Le son Web est une API JavaScript de haut niveau permettant de traiter et de synthétiser du son dans les applications Web pour fournir des expériences audio et musicales plus riches.  Bien que l' `audio` élément HTML5 autorise la lecture de contenu audio en continu de base, l’API audio Web fournit une gamme d’API qui vous permettent de lire des sons multiples avec une synchronisation rapprochée et d’appliquer des gains, des fondus, des transitions et des effets de base sur le son mélangé.  En savoir plus sur [Web audio] (... /Multimedia/Web-audio.MD dans le Guide du développement et sur le [blog du développeur Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/19).  

### Pilote Web  

L' [API WebDriver W3C](https://w3.org/TR/webdriver) est une plate-forme et un protocole filaire qui autorisent des programmes ou des scripts à contrôler le comportement d’un navigateur Web.  Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur.  Cette fonction est différente de celle des tests unitaires JavaScript, car le WebDriver a accès aux fonctionnalités et aux informations que JavaScript en cours d’exécution dans le navigateur ne permet pas de simuler plus précisément les événements utilisateur ou au niveau du système d’exploitation.  Le Web Driver peut également gérer des tests sur plusieurs fenêtres, des onglets et des pages Web au sein d’une seule et même session de test.  Pour plus d’informations sur la manière de prendre en main le WebDriver pour Microsoft Edge, consultez le [WebDriver](../../webdriver/index.md).  

## Nouvelles API dans EdgeHTML 12  

Voici la liste complète des nouvelles API dans EdgeHTML 12.  Ils sont répertoriés au format de `[interface name].[api name]` .  

 > [!NOTE] 
 > Bon nombre de ces API étaient disponibles dans IE11.  Les données suivantes pour EdgeHTML 12 sont proposées comme référence pour comparer la version initiale de EdgeHTML aux versions ultérieures.  

<iframe height='580' scrolling='no' title='Nouvelles API dans EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Reportez-vous au stylo <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> nouvelles API dans EdgeHTML 12 </a> par docs Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .</iframe>  
