---
description: Découvrez toutes les façons dont vous pouvez suspendre votre code dans Microsoft Edge DevTools.
title: Comment suspendre votre code avec des points d’arrêt Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fda536deb7177b933013120fc11b0896acfbbe5c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564174"
---
<!-- Copyright Kayce Basques

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a>Comment suspendre votre code avec des points d’arrêt Microsoft Edge DevTools  

Utilisez des points d’arrêt pour suspendre votre code JavaScript.  Cet article explique chaque type de point d’arrêt disponible dans DevTools, ainsi que le moment où utiliser et comment définir chaque type.

Pour un didacticiel d’introduction utilisant une page web existante, accédez à Commencer à déboguer [JavaScript dans Microsoft Edge DevTools][DevtoolsJavascriptIndex].

## <a name="overview-of-when-to-use-each-breakpoint-type"></a>Vue d’ensemble de l’utilisation de chaque type de point d’arrêt  

Le type de point d’arrêt le plus connu est la ligne de code.  Toutefois, les points d’arrêt de ligne de code peuvent être inefficaces à définir, en particulier si vous ne savez pas exactement où rechercher, ou si vous travaillez avec une base de code de grande taille.  Vous pouvez gagner du temps lors du débogage en sachant comment et quand utiliser les autres types de points d’arrêt.  

| Type de point d’arrêt | Utilisez-le lorsque vous souhaitez suspendre... |  
|:--- |:--- |  
| [Ligne de code](#line-of-code-breakpoints) | Sur une zone de code exacte.  |  
| [Ligne de code conditionnelle](#conditional-line-of-code-breakpoints) | Sur une zone de code exacte, mais uniquement lorsqu’une autre condition est vraie.  |  
| [DOM](#dom-change-breakpoints) | Sur le code qui modifie ou supprime un nœud DOM spécifique, ou les enfants.  |  
| [XHR](#xhrfetch-breakpoints) | Lorsqu’une URL XHR contient un modèle de chaîne.  |  
| [Listener d’événements](#event-listener-breakpoints) | Sur le code qui s’exécute après un événement, tel `click` que , s’exécute.  |  
| [Exception](#exception-breakpoints) | Sur la ligne de code qui lance une exception capturée ou non.  |  
| [Fonction](#function-breakpoints) | Chaque fois qu’une commande, une fonction ou une méthode spécifique est exécuté.  |  

## <a name="line-of-code-breakpoints"></a>Points d’arrêt de ligne de code  

Utilisez un point d’arrêt de ligne de code lorsque vous connaissez la région exacte du code que vous devez examiner.  DevTools s’interrompt toujours avant l’utilisation de cette ligne de code.  

Pour définir un point d’arrêt de ligne de code dans DevTools :  

1.  Choisissez **l’outil Sources.**  
1.  Ouvrez le fichier contenant la ligne de code sur laquelle vous souhaitez rompre.  
1.  Aller à la ligne de code.  
1.  À gauche de la ligne de code se trouve la colonne de numéro de ligne.  Sélectionnez-le.  Une icône rouge s’affiche en côté de la colonne de numéro de ligne.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d’arrêt de ligne de code" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Un point d’arrêt de ligne de code  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a>Points d’arrêt de ligne de code dans votre code  

Exécutez `debugger` la méthode à partir de votre code pour suspendre cette ligne.  Cela équivaut à un point d’arrêt de ligne de [code,](#line-of-code-breakpoints)sauf que le point d’arrêt est définie dans votre code, et non dans l’interface utilisateur de DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a>Points d’arrêt de ligne de code conditionnels  

Utilisez un point d’arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte du code que vous devez examiner, mais que vous souhaitez suspendre uniquement lorsqu’une autre condition est vraie.  

Pour définir un point d’arrêt de ligne de code conditionnel :  

1.  Choisissez **l’outil Sources.**  
1.  Ouvrez le fichier contenant la ligne de code sur laquelle vous souhaitez rompre.  
1.  Aller à la ligne de code.  
1.  À gauche de la ligne de code se trouve la colonne de numéro de ligne.  Pointez sur le numéro de ligne et ouvrez le menu contextuel \(clic droit\).  
1.  Choisissez **Ajouter un point d’arrêt conditionnel.**  Une boîte de dialogue s’affiche sous la ligne de code.  
1.  Entrez votre condition dans la boîte de dialogue.  
1.  Activez `Enter` le point d’arrêt.  Icône en de côté de la colonne de numéro de ligne.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un point d’arrêt de ligne de code conditionnel" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Un point d’arrêt de ligne de code conditionnel  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a>Gérer les points d’arrêt de ligne de code  

Utilisez le **volet Points d’arrêt** pour désactiver ou supprimer des points d’arrêt de ligne de code à partir d’un emplacement unique.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panneau Points d’arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Panneau **Points d’arrêt**  
:::image-end:::  

*   Cochez la case en regard d’une entrée pour désactiver ce point d’arrêt.  
*   Pointez sur une entrée et ouvrez le menu contextuel \(clic droit\) pour supprimer ce point d’arrêt.  
*   Pointez n’importe où dans le volet Points d’arrêt et ouvrez le menu contextuel \(clic droit\) pour désactiver tous les points d’arrêt, désactiver tous les points d’arrêt ou supprimer tous les points d’arrêt. ****  La désactivation de tous les points d’arrêt équivaut à désactiver chacun d’eux.  La désactivation de tous les points d’arrêt indique à DevTools d’ignorer tous les points d’arrêt de ligne de code, mais de maintenir également l’état activé afin que chacun d’eux soit dans le même état qu’auparavant lorsque vous réactivez chacun d’eux.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Points d’arrêt désactivés dans le volet Points d’arrêt" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Points d’arrêt désactivés dans le volet Points **d’arrêt**  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a>Points d’arrêt des changements DOM  

Utilisez un point d’arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.  

Pour définir un point d’arrêt de modification DOM :  

1.  Choisissez **l’outil Éléments.**  
1.  Go the element on which you want to set the breakpoint.  
1.  Pointez sur l’élément et ouvrez le menu contextuel \(clic droit\).  
1.  Pointez sur **Pause,** puis choisissez **Modifications de sous-arbre,** **Modifications d’attribut**ou suppression **de nœud.**  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menu contexté pour la création d’un point d’arrêt de modification DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Menu contexté pour la création d’un point d’arrêt de modification DOM  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a>Types de points d’arrêt de modification DOM  

*   **Modifications de sous-arbre**.  Déclenché lorsqu’un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou lorsque le contenu d’un enfant est modifié.  Ne se déclenche pas lors des modifications apportées à l’attribut de nœud enfant ou aux modifications apportées au nœud actuellement sélectionné.  
*   **Modifications des attributs**: déclenchées lorsqu’un attribut est ajouté ou supprimé sur le nœud actuellement sélectionné, ou lorsqu’une valeur d’attribut change.  
*   **Suppression de nœud**: déclenchée lorsque le nœud actuellement sélectionné est supprimé.  
    
## <a name="xhrfetch-breakpoints"></a>Points d’arrêt XHR/Fetch  

Utilisez un point d’arrêt XHR lorsque vous souhaitez rompre lorsque l’URL de demande d’un XHR contient une chaîne spécifiée.  DevTools s’interrompt sur la ligne de code où le XHR exécute la `send()` méthode.  

> [!NOTE]
> Cette fonctionnalité fonctionne également avec les [demandes d’API Fetch.][MDNFetchApi]  

Par exemple, cela est utile lorsque votre page web demande une URL incorrecte et que vous souhaitez trouver rapidement le code source AJAX ou Fetch à l’origine de la demande incorrecte.  

Pour définir un point d’arrêt XHR :  

1.  Choisissez **l’outil Sources.**  
1.  Développez le **panneau Points d’arrêt XHR.**  
1.  Choisissez **Ajouter un point d’arrêt.**  
1.  Entrez la chaîne sur laquelle vous souhaitez rompre.  DevTools s’interrompt lorsque cette chaîne est présente n’importe où dans une URL de demande XHR.  
1.  Sélectionnez `Enter` pour confirmer.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Créer un point d’arrêt XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Créer un point d’arrêt XHR  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a>Points d’arrêt de l’écoute d’événements  

Utilisez des points d’arrêt de l’écoute d’événements lorsque vous souhaitez suspendre le code de l’écoute d’événement qui s’exécute après le déclenché d’un événement.  Vous pouvez sélectionner des événements spécifiques, tels que, ou des catégories d’événements, tels que tous `click` les événements de souris.  

1.  Choisissez **l’outil Sources.**  
1.  Développez le **panneau Points d’arrêt de l’écoute d’événements.**  DevTools affiche une liste des catégories d’événements, **telles**que Animation .  
1.  Vérifiez l’une de ces catégories pour suspendre chaque fois qu’un événement de cette catégorie est déclenché, ou développez la catégorie et vérifiez un événement spécifique.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Créer un point d’arrêt d’écoute d’événements" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Créer un point d’arrêt d’écoute d’événements  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a>Points d’arrêt d’exception  

Utilisez des points d’arrêt d’exception lorsque vous souhaitez suspendre la ligne de code qui lance une exception capturée ou non.  

1.  Choisissez **l’outil Sources.**  
1.  Choose **Pause on exceptions** \( ![ Pause on exceptions ](../media/pause-on-exceptions-icon.msft.png) \).  L’icône devient bleue lorsqu’elle est activée.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Bouton Pause sur les exceptions" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Bouton **Pause sur les exceptions**  
    :::image-end:::  
    
1.  **Facultatif**.  Cochez la case Pause sur les **exceptions** capturées si vous souhaitez également suspendre les exceptions capturées, en plus des exceptions non capturées.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Suspendu sur une exception nonc qu’il n’a pas" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Suspendu sur une exception nonc qu’il n’a pas  
    :::image-end:::  
    
## <a name="function-breakpoints"></a>Points d’arrêt des fonctions  

Exécutez la méthode, où se trouve la commande, la fonction ou la méthode que vous souhaitez déboguer, lorsque vous souhaitez suspendre chaque fois qu’une `debug(method)` `method` fonction spécifique est exécuté.  Vous pouvez insérer dans votre code (comme une instruction) ou exécuter la méthode à partir `debug()` `console.log()` de la console DevTools.  `debug()` équivaut à définir un [point d’arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a>Assurez-vous que la fonction cible est dans l’étendue  

DevTools throws a `ReferenceError` if the function you want to debug is not in scope.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Il est difficile de s’assurer que la fonction cible est dans l’étendue si vous exécutez la méthode à partir `debug()` de la console DevTools.  Voici une stratégie :  

1.  Définissez [un point d’arrêt de ligne](#line-of-code-breakpoints) de code quelque part où la fonction est dans l’étendue.
1.  Déclenchez le point d’arrêt.  
1.  Exécutez `debug()` la méthode dans la console DevTools alors que le code est toujours suspendu sur votre point d’arrêt de ligne de code.  
    
## <a name="related-articles"></a>Articles connexes

*   [Utilisez les fonctionnalités du débogger][DevtoolsJavascriptReference] : à l’aide de l’interface utilisateur du débogger dans **l’outil Sources.**
*   [Commencer à déboguer JavaScript dans Microsoft Edge DevTools][DevtoolsJavascriptIndex] : didacticiel d’introduction utilisant une page web existante.
*   [Vue d’ensemble][DevtoolsSourcesIndex] de l’outil Sources : le débogger fait partie de l’outil **Sources,** qui inclut un éditeur JavaScript.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"  

[DevtoolsJavascriptIndex]: index.md "Commencer à déboguer JavaScript dans Microsoft Edge devTools | Documents Microsoft"  

[DevtoolsSourcesIndex]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Récupérer les | API MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
