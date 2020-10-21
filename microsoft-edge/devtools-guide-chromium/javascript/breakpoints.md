---
description: Découvrez toutes les manières dont vous pouvez mettre votre code en pause dans Microsoft Edge DevTools.
title: Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124809"
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

# Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools  

Utilisez des points d’arrêt pour suspendre votre code JavaScript.  Ce guide décrit chaque type de point d’arrêt disponible dans DevTools, ainsi que le mode d’utilisation et la définition de chaque type.  Pour un didacticiel d’exécution du processus de débogage, accédez à la section [prendre en main le débogage JavaScript dans Microsoft Edge devtools][DevtoolsJavascriptIndex].  

## Vue d’ensemble de l’utilisation de chaque type de point d’arrêt  

Le type de point d’arrêt le plus connu est le type de ligne de code.  Toutefois, en revanche, si vous ne savez pas exactement où il est possible de définir l’aspect exact du jeu de points d’arrêt et si vous travaillez avec un grand code base,  Vous pouvez gagner du temps lors du débogage en connaissant le mode d’utilisation des autres types de points d’arrêt.  

| Type de point d’arrêt | Utilisez cette opération lorsque vous souhaitez suspendre...  |  
|:--- |:--- |  
| [Code de ligne](#line-of-code-breakpoints) | Sur une zone de code exacte.  |  
| [Ligne de code conditionnelle](#conditional-line-of-code-breakpoints) | Sur une zone de code exacte, mais uniquement quand une autre condition est vraie.  |  
| [DOM](#dom-change-breakpoints) | Sur le code qui modifie ou supprime un nœud DOM spécifique ou les enfants.  |  
| [XHR](#xhrfetch-breakpoints) | Lorsqu’une URL XHR contient un modèle de chaîne.  |  
| [Écouteur d’événements](#event-listener-breakpoints) | Sur le code exécuté après un événement, par exemple `click` , s’exécute.  |  
| [Sauf](#exception-breakpoints) | Sur la ligne de code qui lève une exception interceptée ou non interceptée.  |  
| [Fonction](#function-breakpoints) | L’exécution d’une commande, d’une fonction ou d’une méthode spécifique.  |  

## Points d’arrêt de code de ligne  

Utilisez un point d’arrêt de code de ligne lorsque vous connaissez la région exacte de code que vous devez examiner.  DevTools interrompt toujours l’exécution de cette ligne de code.  

Pour définir un point d’arrêt de code de ligne dans DevTools:  

1.  Cliquez sur l’onglet **sources** .  
1.  Ouvrez le fichier contenant la ligne de code que vous voulez rompre.  
1.  Accédez à la ligne de code.  
1.  À gauche de la ligne de code se trouve la colonne numéro de ligne.  Cliquez dessus.  Une icône rouge apparaît en regard de la colonne numéro de ligne.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Un point d’arrêt de code de ligne  
    :::image-end:::  
    
### Points d’arrêt de code de ligne dans votre code  

Exécutez la `debugger` méthode à partir de votre code pour suspendre cette ligne.  Cela équivaut à un [point d’arrêt de ligne de code](#line-of-code-breakpoints), sauf que le point d’arrêt est défini dans votre code, et non dans l’interface utilisateur devtools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### Points d’arrêt conditionnels de ligne de code  

Utilisez un point d’arrêt de ligne de code conditionnel lorsque vous connaissez la région exacte de code que vous devez examiner, mais que vous ne voulez mettre en pause que si une autre condition est vraie.  

Pour définir un point d’arrêt de code de ligne conditionnelle:  

1.  Cliquez sur l’onglet **sources** .  
1.  Ouvrez le fichier contenant la ligne de code que vous voulez rompre.  
1.  Accédez à la ligne de code.  
1.  À gauche de la ligne de code se trouve la colonne numéro de ligne.  Cliquez avec le bouton droit sur le numéro de la ligne.  
1.  Choisissez **Ajouter un point d’arrêt conditionnel**.  Une boîte de dialogue s’affiche sous la ligne de code.  
1.  Entrez votre condition dans la boîte de dialogue.  
1.  Activez `Enter` cette option pour activer le point d’arrêt.  Une icône en regard de la colonne numéro de ligne.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Un point d’arrêt conditionnel de code de ligne  
    :::image-end:::  
    
### Gérer les points d’arrêt de code de ligne  

Utilisez le volet **points d’arrêt** pour désactiver ou supprimer des points d’arrêt de code de ligne à partir d’un emplacement unique.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Panneau **points d’arrêt**  
:::image-end:::  

*   Activez la case à cocher en regard d’une entrée pour désactiver ce point d’arrêt.  
*   Cliquez avec le bouton droit sur une entrée pour supprimer ce point d’arrêt.  
*   Cliquez avec le bouton droit n’importe où dans le volet **points d’arrêt** pour désactiver tous les points d’arrêt, désactiver tous les points d’arrêt ou supprimer tous les points d’arrêt.  La désactivation de tous les points d’arrêt revient à décocher chacun d’eux.  La désactivation de tous les points d’arrêt prescrit à DevTools d’ignorer tous les points d’arrêt de la ligne de code, mais de maintenir l’état activé de façon à ce qu’ils soient dans le même État qu’avant lorsque vous les réactivez chacun d’eux.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Points d’arrêt désactivé dans le volet **points d’arrêt**  
    :::image-end:::  
    
## DOM modifier les points d’arrêt  

Utilisez un point d’arrêt de modification DOM lorsque vous souhaitez suspendre le code qui modifie un nœud DOM ou les enfants.  

Pour définir un point d’arrêt de modification DOM:  

1.  Cliquez sur l’onglet **éléments** .  
1.  Accédez à l’élément sur lequel vous voulez définir le point d’arrêt.  
1.  Cliquez avec le bouton droit sur l’élément.  
1.  Placez le pointeur de la souris **sur arrêt**, puis sélectionnez **modifications de sous-arbres**, modifications d' **attributs**ou **Suppression de nœud**.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Menu contextuel pour la création d’un point d’arrêt de modification DOM  
    :::image-end:::  
    
### Types d’arrêts de modification de DOM  

*   **Modifications**de la sous-arborescence.  Déclenché lorsqu’un enfant du nœud actuellement sélectionné est supprimé ou ajouté, ou que le contenu d’un enfant a changé.  Ne sont pas déclenchées sur les changements d’attribut de nœud enfant ou sur les modifications apportées au nœud actuellement sélectionné.  
*   **Modifications d’attributs**: déclenché lors de l’ajout ou de la suppression d’un attribut sur le nœud actuellement sélectionné, ou en cas de modification d’une valeur d’attribut.  
*   **Suppression de nœud**: déclenchée lors de la suppression du nœud actuellement sélectionné.  
    
## Points d’arrêt XHR/Fetch  

Utilisez un point d’arrêt XHR lorsque vous souhaitez arrêter lorsque l’URL de requête d’un XHR contient une chaîne spécifiée.  DevTools s’arrête sur la ligne de code où XHR exécute la `send()` méthode.  

> [!NOTE]
> Cette fonctionnalité est également compatible avec les demandes d' [API FETCH][MDNFetchApi] .  

C’est le cas, par exemple, lorsque vous constatez qu’il s’agit d’une URL incorrecte et que vous voulez rapidement trouver le code source AJAX ou FETCH à l’origine de la demande incorrecte.  

Pour définir un point d’arrêt XHR:  

1.  Cliquez sur l’onglet **sources** .  
1.  Développez le volet **points d’arrêt XHR** .  
1.  Choisissez **Ajouter un point d’arrêt**.  
1.  Entrez la chaîne que vous voulez rompre.  DevTools s’interrompt lorsque cette chaîne est présente n’importe où dans une URL de requête XHR.  
1.  Sélectionnez `Enter` pour confirmer.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Créer un point d’arrêt XHR  
    :::image-end:::  
    
## Points d’arrêt de l’écouteur d’événements   

Utilisez des points d’arrêt de l’écouteur d’événements lorsque vous souhaitez suspendre le code de l’écouteur d’événements qui s’exécute après le déclenchement d’un événement.  Vous pouvez sélectionner des événements spécifiques, tels que `click` des catégories d’événements, tels que tous les événements de souris.  

1.  Cliquez sur l’onglet **sources** .  
1.  Développez le volet de **points d’arrêt du détecteur d’événements** .  DevTools affiche une liste de catégories d’événements, par exemple une **animation**.  
1.  Activez une de ces catégories pour suspendre chaque événement de cette catégorie ou développer la catégorie et vérifier un événement spécifique.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Créer un point d’arrêt d’écouteur d’événements  
    :::image-end:::  
    
## Points d’arrêt d’exception  

Utilisez des points d’arrêt d’exception lorsque vous voulez mettre en pause la ligne de code qui lève une exception interceptée ou non interceptée.  

1.  Cliquez sur l’onglet **sources** .  
1.  Sélectionnez **suspendre sur les exceptions** \ ( ![ suspendre sur les exceptions ][ImagePauseOnExceptionsIcon] \).  L’icône devient bleu lorsque l’option est activée.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Bouton **suspendre sur les exceptions**  
    :::image-end:::  
    
1.  **Facultatif**.  Activez la case à cocher **suspendre les exceptions interceptées** si vous souhaitez également suspendre les exceptions interceptées, en plus de celles qui ne sont pas capturées.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Un point d’arrêt de code de ligne" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Suspendu sur une exception non interceptée  
    :::image-end:::  
    
## Points d’arrêt de fonction  

Exécutez la `debug(method)` méthode, où `method` se trouve la commande, la fonction ou la méthode que vous voulez déboguer lorsque vous voulez faire dérouler chaque fois qu’une fonction spécifique est exécutée.  Vous pouvez insérer `debug()` dans votre code (par exemple `console.log()` , une instruction) ou exécuter la méthode à partir de la console devtools.  `debug()` équivaut à définir un [point d’arrêt de ligne de code](#line-of-code-breakpoints) sur la première ligne de la fonction.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### Vérifier que la fonction cible se trouve dans l’étendue  

DevTools lève une exception `ReferenceError` si la fonction que vous souhaitez déboguer n’est pas dans l’étendue.  

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

Il est difficile de garantir que la fonction cible se trouve dans l’étendue si vous exécutez la `debug()` méthode à partir de la console devtools.  Voici une stratégie:  

1.  Définissez un [point d’arrêt de ligne de code](#line-of-code-breakpoints) à un emplacement où la fonction est dans Scope.
1.  Déclenchez le point d’arrêt.  
1.  Exécutez la `debug()` méthode dans la console devtools lorsque le code est toujours suspendu sur le point d’arrêt de votre code.  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API Fetch | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
