---
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans EdgeHTML 15.
title: Nouvelles fonctionnalités et API dans EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/02/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: 4fd0bbc06d27bace424ea99cfe9941aabc737fee
ms.sourcegitcommit: 204a284e21bf2da5cdc862c5e8b5839245abbbbc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "11094360"
---
# Nouveautés de EdgeHTML 15  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Voici les modifications apportées à la version actuelle de la plateforme Microsoft Edge, à partir de [Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) \ (04/2017, Build 15063 \).  Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir [Nouveautés de Microsoft Edge dans Windows 10 Creators Update](https://blogs.windows.com/msedgedev/2017/04/11).  

Pour plus d’informations sur les modifications apportées aux versions préliminaires de Windows Insider Preview, voir [Nouveautés de EdgeHTML](../whats-new.md).  

Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante:  [https://aka.ms/devguide_edgehtml_15](./edgehtml-15.md) .  

## Nouvelles fonctionnalités  

### Propriétés personnalisées CSS  

Microsoft Edge prend désormais en charge les [propriétés personnalisées CSS](https://drafts.csswg.org/css-variables), une variable. k. une variable CSS.  Les variables CSS vous permettent de créer des propriétés CSS personnalisées qui peuvent être réutilisées dans toutes les feuilles de style afin de réduire la quantité de données dupliquées, par exemple les couleurs répétées.  L’utilisation de variables CSS est simple:  

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Observateur d’intersection  

EdgeHTML 15 présente la spécification de l' [API d’observation d’intersection](https://w3c.github.io/IntersectionObserver) .  L’API d’observation d’intersection vous permet d’interroger de manière asynchrone la position et la visibilité des éléments DOM par rapport à d’autres éléments ou à la fenêtre d’affichage globale.  Cette API élimine le besoin d’utiliser du code coûteux personnalisé en créant une méthode pour avertir efficacement les éléments lorsqu’ils sont en vue.  

### JavaScript  

Les optimisations de performance prennent du temps central avec la rév. EdgeHTML 15 du moteur JavaScript Chakra.  À l’aide de Windows 10 Creators Update, chakra enregistre de la mémoire en redifférant les fonctions et en optimisant les arguments du tas et améliore les performances du code minified.  

De plus, le EdgeHTML 15 présente les aperçus des fonctionnalités suivants:  

#### Fonctionnalités JavaScript expérimentales  

Activé avec `about:flags`  

*   [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) \ ([démonstration](https://webassembly.org/demo)\)  
*   [Mémoire partagée et Atomic.](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

Pour plus d’informations [, voir amélioration des performances JavaScript, de l’assemblage webassemblage et de la mémoire partagée dans Microsoft Edge](https://blogs.windows.com/msedgedev/2017/04/20) .  

### API de demande de paiement  

L' [API de demande de paiement](https://w3.org/TR/payment-request) est désormais prise en charge, ce qui permet d’extraire et de payer plus facilement sur le Web sur des PC et téléphones Windows 10.  Cette API permet à Microsoft Edge d’agir en tant qu’intermédiaire entre les commerçants, les consommateurs et les modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.  Pour plus d’informations sur l’API de demande de paiement, consultez l’article utilisation de l’API de [demande](https://blogs.windows.com/msedgedev/2016/12/15) de paiement et Guide du développeur de l’API de [demande de paiement](/microsoft-edge/dev-guide/device/payment-request-api) .  

### TCP Fast Open (TFO)  
TCP Fast Open est une fonctionnalité qui réduit le nombre de boucles nécessaires pour ouvrir une connexion TCP et améliorer les performances réseau du navigateur.  Pour plus d’informations, consultez [création d’un site Web plus rapide et plus sécurisé avec TCP Fast Open](https://blogs.windows.com/msedgedev/2016/06/15).  En raison de différences d’interopérabilité de diverses topologies réseau, cette fonctionnalité n’est pas activée par défaut dans Microsoft Edge.  Pour l’activer, tapez `about:flags` votre barre d’adresses, puis activez la case à cocher **activer le protocole TCP Fast Open** dans la section **réseau** .  

### Prise en charge du codec vidéo WebRTC et interopérable RTC  

EdgeHTML 15 prend en charge un sous-ensemble de l’API 1,0 d’WebRTC pour l’interopérabilité avec des applications créées avec des versions antérieures de l’API WebRTC-PC sur 2015.  Pour plus d’informations, voir la référence de l' [API WebRTC](/previous-versions//mt806139(v=vs.85)) .  

Pour tirer parti des fonctionnalités plus avancées de la communication audio et vidéo d’égal à égal, nous vous recommandons d’utiliser l' [API Object Real-Time communications)](https://ortc.org).  L’API ORTC est mieux adaptée aux situations dans lesquelles vous souhaitez configurer les appels audio et vidéo de groupe, ou contrôler directement les objets de transport, d’expéditeur et de destinataire.  

Le Microsoft Edge prend en charge les fonctions H. 264/AVC et VP8 avec la fonction ORTC et WebRTC [1,0, et](https://tools.ietf.org/html/rfc4588)fournit les fonctionnalités suivantes pour la prise en charge des deux types de codec: [ABS-Send-Time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time) [,](https://tools.ietf.org/html/rfc4585)utilisation de la [fonction](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03)d’affichage de contenu  

Pour plus d’informations, reportez-vous à [Présentation de WebRTC 1,0 et interopérabilité en temps réel dans Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31).  

### WebVR  

Microsoft Edge est désormais pris en charge par [WebVR](https://immersive-web.github.io/webxr), une API expérimentale qui connecte les affichages de la tête de la fenêtre mixte Windows mixte et Microsoft Edge.  Cette connexion permet d’avoir accès au contenu VR au sein d’un site Web, ce qui signifie que les expériences de VR ne sont plus limitées aux applications de bureau.  

La réalité virtuelle dans Microsoft Edge est optimisée par WebGL, une API JavaScript pour le rendu des graphismes 3D et 2D.  Les applications WebGL et applications créées avec des bibliothèques WebGL telles que BabylonJS sont prises en charge.  Une fois connecté, WebVR envoie des visuels correspondant à la position et aux informations de capteur du casque.  L’API WebVR prend également en charge les contrôleurs spatiaux grâce à une extension de l' [API de boîtier](../dom/gamepad-api.md)de commandes.  Cette API est activée par défaut, il n’est donc pas nécessaire de basculer sur un indicateur.  

Pour plus d’informations, voir les informations de référence sur les API [WebVR](/previous-versions//mt806281(v=vs.85)) et le [boîtier](https://developer.mozilla.org/docs/Web/API/Gamepad_API) de connexion.  

 > [!NOTE] 
 > Dans la mesure où la spécification WebVR est toujours en développement, la mise en œuvre de Microsoft Edge peut changer plus tard.  

## Fonctionnalités mises à jour  

### Stratégie de sécurité du contenu (niveau 2)  

Les sites utilisant déjà un fournisseur de services cryptographiques 1 doivent continuer à utiliser la prise en charge de Microsoft Edge pour FSC 2, mais il est préférable de basculer entre les directives permettant de `frame-src` charger les scripts de travail dans la nouvelle `child-src` directive afin de vérifier l’évolution de votre site.  \ (Dans FSC 3, `frame-src` ne s’appliquera plus à travailleurs. \) le fournisseur de services de cryptographie 2 ajoute également ce qui suit:  

:::row:::
   :::column span="1":::
      Nouvelles directives  
   :::column-end:::
   :::column span="2":::
      `base-uri`, `child-src` , `form-action` `frame-ancestors` et `plugin-types` .  Pour plus d’informations, voir [directives CSP prises en charge par Microsoft Edge](../security/content-security-policy.md) .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Support pour les travailleurs  
   :::column-end:::
   :::column span="2":::
      Les scripts de travail en arrière-plan sont régis par leur propre stratégie, indépendamment de la stratégie de chargement du document.  Comme pour les documents hôtes, vous pouvez définir le CSP d’un travailleur dans l’en-tête de réponse.  Par ailleurs, le nouveau fournisseur de services cryptographiques 2 a pour  `allow-scripts` `allow-same-origin` `sandbox` effet d’affecter la création de threads de travail.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Scripts et styles Inline  
   :::column-end:::
   :::column span="2":::
      Le FSC 2 autorise l’exécution de scripts et de blocs de style inline en fournissant des nonces et des hachements en tant que mécanisme d’entrée de texte.  Les nonces sont des valeurs de base 64 aléatoires générées lors de chaque chargement de page qui s’affiche dans la stratégie de FSC et dans les balises de script de la page.  Lorsque la page est générée dynamiquement au chargement, le serveur génère une valeur nonce, l’insère dans le NonceToken de la page et la déclare dans l’en-tête HTTP de la stratégie de sécurité du contenu.  Les hachages sont des valeurs statiques générées \ (en utilisant les algorithmes SHA256, SHA384 ou SHA512) à partir du contenu d’un `<script>` `<style>` élément ou qui est ensuite spécifié \ (à l’aide `script-src` de `style-src` directives ou \) dans la stratégie CSP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Rapport de violation des CSP  
   :::column-end:::
   :::column span="2":::
      Un nouvel événement `SecurityPolicyViolationEvent` est désormais déclenché lors des violations du fournisseur de services d’appel.  Le mécanisme antérieur pour la création de rapports de FSC, `report-uri` continue d’être pris en charge.  Plusieurs nouveaux champs ont été ajoutés aux rapports de violation communs aux deux éléments, y compris `effectiveDirective` \ (la stratégie qui a été violée \), `statusCode` \ (le code de réponse http \), `sourceFile` \ (l’URL de la ressource contrevenante \), `lineNumber` et `columnNumber` .  
   :::column-end:::
:::row-end:::  

### Authentification web  

La prise en charge de Microsoft Edge pour l' [API d’authentification Web](../device/web-authentication.md) émergeant à l’aide de [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) biométrique a été mise à jour avec les modifications suivantes:  

*   [Dans le cadre de la](https://blogs.windows.com/msedgedev/2016/08/04) mise à jour anniversaire de Windows 10, la build 10240, 7/2016 \) a été exposée à l’aide des API MS-préfixé ( [MSCredentials](/previous-versions//mt697639(v=vs.85)) interface \).  Même si ces API sont toujours disponibles dans EdgeHTML 15, elles sont désormais déconseillées en faveur des API et des comportements non prédéfinis et prédéfinis définis dans un [instantané plus récent](https://w3.org/TR/2016/WD-webauthn-20160928) de la spécification, et sont susceptibles de continuer à changer à mesure que les spécifications arrivent à l’évolution de la normalisation.  

*   La dernière mise en œuvre de Microsoft Edge est désactivée par défaut et est fournie derrière un indicateur \ (tapez `about:flags` dans la barre d’adresse pour activer la fonctionnalité \).  

*   Microsoft Edge ne prend pas encore en charge les informations d’identification externes telles que les clés USB ou les appareils Bluetooth.  L’API actuelle est limitée aux informations d’identification incorporées stockées dans le module de plateforme sécurisée.  Un remplacement logiciel est utilisé si la plateforme sécurisée n’est pas disponible sur l’appareil.  

*   Le compte d’utilisateur Windows actuellement connecté doit être configuré de manière à prendre en charge au moins un code confidentiel, et de préférence au visage ou à l’empreinte digitale biométriques.  Cela permet de s’assurer que Windows peut authentifier l’accès au module de plateforme sécurisée.  

*   Parmi les [Extensions prédéfinies](https://w3.org/TR/webauthn/#extension-predef) décrites dans la spécification, Microsoft Edge ne prend en charge que l' [AppID](https://w3.org/TR/webauthn/#extension-appid) d’équipe \ ( `webauthn_txAuthSimple` \) pour le moment.  

*  L' `timeoutSeconds` option n’est pas évaluée actuellement  

### WebDriver  

EdgeHTML 15 apporte quelques mises à jour du service clientèle, notamment la prise en charge de l’indicateur de ligne de commande Silent et de nouveaux points de terminaison de commande:  

| Méthode | Modèle d’URI | Commande |  
|:--- |:---  |:--- |    
| POST | ID/session/{session/Alert/Accept | [Accepter l’alerte](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert) |  
| POST | ID/session/{session/Alert/dismiss | [Ignorer l’alerte](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert) |  
| GET | ID/session/{session/Alert/Text | [Obtenir le texte d’une alerte](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text) |  
| POST | ID/session/{session/Alert/Text | [Envoyer un message d’alerte](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text) |  
| POST | ID/session/{session/Execute/Async | [Exécuter le script Async](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script) |  
| POST | ID/session/{session/Execute/Sync | [Exécuter le script](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script) |  
| GET | ID/session/{session/Window | [Handle de fenêtre Get](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle) |  
| GET | ID/session/{session/Window/Handles | [Obtenir des poignées de fenêtre](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles) |  

Pour plus d’informations et l’état des autres fonctionnalités du WebDriver, voir [WebDriver](../../webdriver.md).  

## Nouvelles API dans EdgeHTML 15  

Voici la liste complète des nouvelles API dans EdgeHTML 15.  Ils sont répertoriés au format de `[interface name].[api name]` .  

<iframe height='582' scrolling='no' title='Nouvelles API EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Voir le stylo <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> nouvelles API EdgeHTML15 </a> par Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Versions précédentes de EdgeHTML  

[EdgeHTML 12/Windows Build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13/Windows Build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14/Windows Build 14393 (8/2016)](./edgehtml-14.md)  
