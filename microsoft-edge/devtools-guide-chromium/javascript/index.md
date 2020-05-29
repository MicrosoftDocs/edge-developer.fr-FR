---
title: Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 06df1fd4d6457a3f02be85b95959bdc353865495
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581823"
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







# Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools   



Ce didacticiel décrit le flux de travail de base pour le débogage d’un problème JavaScript dans DevTools.  

## Étape 1: reproduire le bogue   

La recherche d’une série d’actions qui reproduit régulièrement un bogue est toujours la première étape du débogage.  

1.  Cliquez sur **ouvrir la démonstration**.  Maintenez `Control` \ (Windows \) ou `Command` \ (MacOS \) et ouvrez la démonstration dans un nouvel onglet.  

    [Ouvrir la démonstration] [OpenDebugJSDemo]  

1.  Entrez `5` dans la zone de texte **numéro 1** .  
1.  Entrez `1` dans la zone de texte **numéro 2** .  
1.  Cliquez sur **Ajouter un numéro 1 et sur numéro 2**.  L’étiquette sous le bouton indique `5 + 1 = 51` .  Le résultat doit être `6` .  Voici le bogue que vous allez résoudre.  
    
    > ##### Figure1  
    > Le résultat de la valeur `5 + 1` `51` , mais doit être `6`  
    > ![Le résultat de 5 + 1 est 51, mais devrait être 6][ImageJSBugs]  

## Étape 2: Familiarisez-vous avec l’interface utilisateur du panneau sources   

DevTools fournit un grand nombre d’outils différents pour différentes tâches, comme le changement de CSS, la performance de chargement de la page de profil et la surveillance des requêtes réseau.  Le panneau **sources** vous permet de déboguer JavaScript.  

1.  Ouvrez devtools en appuyant sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Ce raccourci ouvre le panneau de la **console** .  
    
    > ##### Figure 2  
    > Panneau de la **console**  
    > ![Panneau de la console][ImageJSConsole]  

1.  Cliquez sur l’onglet **sources** .  
    
    > ##### Figure3  
    > Panneau **sources**  
    > ![Panneau sources][ImageJSSources]  

L’interface utilisateur du panneau **sources** comporte 3 parties:  

> ##### Figure 4  
> Les 3 parties de l’interface utilisateur du panneau **sources**  
> ![Les 3 parties de l’interface utilisateur du panneau sources][ImageJSSourcesAnnotated]  

1.  Le volet **navigateur de fichiers** \ (section 1 dans la [figure 4](#figure-4)\).  Chaque fichier mentionné dans la page est répertorié ici.  
1.  Le volet de l' **éditeur de code** (section 2 dans la [figure 4](#figure-4)\).  Après avoir sélectionné un fichier dans le volet **navigateur de fichiers** , le contenu de ce fichier est affiché ici.  
1.  Le volet de **débogage JavaScript** \ (section 3 de la [figure 4](#figure-4)\).  Différents outils d’examen du code JavaScript pour la page.  Si votre fenêtre DevTools est large, ce volet est affiché à droite du volet de l' **éditeur de code** .  

## Étape 3: mettre en pause le code avec un point d’arrêt   

Une méthode courante pour le débogage d’un problème comme celui-ci consiste à insérer un grand nombre d' `console.log()` instructions dans le code afin d’inspecter les valeurs lors de l’exécution du script.  Exemple:  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

La `console.log()` méthode peut être exécutée, mais les **points d’arrêt** peuvent être plus productifs.  Un point d’arrêt vous permet d’interrompre votre code au milieu du runtime et d’examiner toutes les valeurs à ce moment-là.  Les points d’arrêt présentent quelques avantages par rapport à la `console.log()` méthode:  

*   Avec `console.log()` , vous devez ouvrir manuellement le code source, Rechercher le code approprié, insérer les `console.log()` instructions, puis recharger la page pour afficher les messages dans la console.  Avec les points d’arrêt, vous pouvez mettre en pause le code concerné sans même savoir comment le code est structuré.  
*   Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous voulez inspecter.  Les points d’arrêt DevTools vous montrent les valeurs de toutes les variables à ce moment précis.  Parfois, il existe des variables affectant votre code.  

En bref, les points d’arrêt permettent de rechercher et de résoudre les bogues plus rapidement que la `console.log()` méthode.  

Si vous vous prenez reculer et réfléchir au fonctionnement de l’application, vous pouvez faire en sorte que la somme incorrecte ( `5 + 1 = 51` ) soit calculée dans l' `click` écouteur d’événements associé au bouton **Ajouter un numéro 1 et 2** .  Par conséquent, il est probable que vous souhaitiez suspendre le code au bout du temps d’exécution de l' `click` écouteur.  Les **points d’arrêt écouteur d’événements** vous permettent d’effectuer les opérations suivantes:  

1.  Dans le volet **débogage JavaScript** , cliquez sur **points d’arrêt de l’écouteur d’événements** pour développer la section.  DevTools affiche une liste des catégories d’événements pouvant être développés, telles que l' **animation** et le **presse-papiers**.  
1.  En regard de la catégorie d’événement de **souris** , cliquez sur **développer** l' ![ icône développer ][ImageExpandIcon] .  DevTools révèle une liste d’événements de souris tels que **Click** et **MouseDown**.  Une case à cocher est associée à chaque événement.  
1.  Cochez la case **cliquez sur** .  DevTools est désormais configuré pour s’arrêter automatiquement lors *de l’exécution d’un* `click` écouteur d’événements.  
    
    > ##### Figure 5  
    > La case à cocher **Cliquer** est activée  
    > ![La case à cocher cliquer est activée][ImageJSClickCheckbox]  
    
1.  Dans la démonstration, cliquez à nouveau sur **Ajouter un numéro 1 et sur numéro 2** .  DevTools met en pause la démonstration et surligne une ligne de code dans le panneau **sources** .  DevTools doit suspendre la ligne 16 `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si vous placez le pointeur sur une autre ligne de code, appuyez sur la touche reprise de l' **exécution** du script ![ ][ImageResumeIcon] jusqu’à ce que vous pointiez sur la ligne appropriée.  
    
    > [!NOTE]
    > Si vous avez interrompu une autre ligne, vous disposez d’une extension de navigateur permettant d’inscrire un `click` écouteur d’événements sur chaque page que vous visitez.  Vous avez été suspendu dans l' `click` écouteur de l’extension.  Si vous utilisez le mode InPrivate pour effectuer une **recherche dans Private**, qui désactive toutes les extensions, il est possible que vous deviez suspendre chaque fois la ligne de code souhaitée.  

<!--todo: add inprivate section when available -->  

Les **points d’arrêt écouteur d’événements** ne sont qu’un type de nombreux types de points d’arrêt disponibles dans devtools.  Il est recommandé de mémoriser tous les types différents, car chaque type de fichier vous permet de déboguer différents scénarios le plus rapidement possible.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Étape 4: parcourir le code   

L’une des causes les plus fréquentes est qu’un script s’exécute dans un ordre incorrect.  Le passage en revue de votre code vous permet de parcourir le runtime de votre code, une ligne à la fois, et de rechercher exactement à l’endroit où il s’exécute dans un ordre différent de ce que vous attendiez.  Essayez-le maintenant:  

1.  Cliquez sur passer à la fonction **suivante lors** d’un ![ appel de fonction ][ImageOverIcon] .  DevTools exécute le code suivant sans s’y exécuter.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  

    > [!NOTE]
    > DevTools ignore quelques lignes de code.  Étant donné que l’argument `inputsAreEmpty()` évalue la valeur false, le bloc de code de l' `if` instruction ne s’exécute pas.  

1.  Dans le panneau **sources** de devtools, cliquez sur passer à la **fonction suivante** dans le ![ cadre de l’appel de fonction suivante ][ImageIntoIcon] pour passer d' `updateLabel()` une ligne à l’autre au moment de l’exécution de la fonction.  

Il s’agit de l’idée de base de l’exécution du code.  Si vous examinez le code dans `get-started.js` , vous constatez que le bogue est probablement quelque part dans la `updateLabel()` fonction.  Au lieu de parcourir chaque ligne de code, vous pouvez utiliser un autre type de point d’arrêt pour mettre le code plus près de l’emplacement probable du bogue.  

## Étape 5: définir un point d’arrêt de code de ligne   

Les points d’arrêt de la ligne sont le type le plus courant de point d’arrêt.  Lorsque vous obtenez la ligne de code spécifique sur laquelle vous voulez mettre en pause, utilisez un point d’arrêt de ligne de code:  

1.  Regardez la dernière ligne de code dans `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À gauche du code figure le numéro de ligne de cette ligne de code particulière, qui est **33**.  Cliquez sur **33**.  DevTools place une icône rouge à gauche de **33**.  Cela signifie qu’il y a un point d’arrêt de ligne de code sur ce trait.  DevTools est à présent mis en pause pour pouvoir exécuter cette ligne de code.  
1.  Cliquez **sur reprise de l’exécution** du script de ![ reprise ][ImageResumeIcon] .  Le script continue de s’exécuter jusqu’à ce qu’il atteigne la ligne 33.  Sur les lignes 30, 31 et 32, DevTools affiche les valeurs de `addend1` , `addend2` et `sum` à droite du point-virgule sur chaque ligne.  
    
    > ##### Figure 6  
    > DevTools s’arrête sur le point d’arrêt de ligne de code de la ligne 32  
    > ![DevTools s’arrête sur le point d’arrêt de ligne de code de la ligne 32][ImageJSLineOfCodeBreakpoint]  

## Étape 6: vérifier les valeurs des variables   

Les valeurs de `addend1` , `addend2` et il est `sum` suspect.  Ils sont encapsulés entre guillemets, ce qui signifie qu’il s’agit de chaînes.  C’est une bonne hypothèse d’expliquer la cause du bogue.  Maintenant, il est temps de recueillir des informations supplémentaires.  DevTools offre un grand nombre d’outils d’examen des valeurs des variables.  

### Méthode 1: volet d’étendue   

Lorsque vous placez le pointeur sur une ligne de code, le volet de l' **étendue** vous indique quelles variables locales et globales sont actuellement définies, ainsi que la valeur de chaque variable.  Il affiche également les variables de fermeture, le cas échéant.  Double-cliquez sur une valeur de variable pour la modifier.  Lorsque vous n’êtes pas en pause sur une ligne de code, le volet **étendue** est vide.  

> ##### Figure 7  
> Volet **cadre**  
> ![Volet cadre][ImageJSScope]  

### Méthode 2: espionner les expressions   

L’onglet **expressions espionnes** vous permet de surveiller les valeurs des variables dans le temps.  Comme son nom l’indique, les expressions espionnes ne sont pas simplement limitées aux variables.  Vous pouvez stocker toute expression JavaScript valide dans une expression espionne.  Essayez-le maintenant:  

1.  Cliquez sur l’onglet **Espion** .  
1.  Cliquez sur **Ajouter** une expression ![ ][ImageAddIcon] .  
1.  Entrez `typeof sum`.  
1.  Appuyez sur `Enter` .  DevTools affiche `typeof sum: "string"` .  La valeur à droite des deux-points est le résultat de l’expression espionne.  

> [!NOTE]
> Dans le volet des expressions espionnes (en bas à droite) de la [figure 8](#figure-8), l' `typeof sum` expression espionne est affichée.  S’il s’agit d’une fenêtre de DevTools de grande taille, le volet d’expressions espionnes se trouve à droite au-dessus du volet de **points d’arrêt du détecteur d’événements** .  

> ##### Figure8  
> Volet expression espionner  
> ![Volet expression espionner][ImageJSWatchExpression]  

Comme soupçonné, `sum` est évaluée en tant que chaîne, lorsqu’il devrait s’agir d’un nombre.  Vous avez vérifié qu’il s’agit de la cause du bogue.  

### Méthode 3: la console   

En plus de l’affichage des `console.log()` messages, vous pouvez également utiliser la console pour évaluer des instructions JavaScript arbitraires.  En termes de débogage, vous pouvez utiliser la console pour tester les correctifs potentiels pour les bogues.  Essayez-le maintenant:  

1.  Si le tiroir de la console n’est pas ouvert, appuyez sur `Escape` pour l’ouvrir.  Il s’ouvre en bas de la fenêtre DevTools.  
1.  Dans la console, tapez `parseInt(addend1) + parseInt(addend2)` .  Cette instruction fonctionne, car vous êtes en pause sur une ligne de code où vous vous `addend1` `addend2` trouvez dans l’étendue.  
1.  Appuyez sur `Enter` .  DevTools évalue l’instruction et imprime `6` , ce qui correspond au résultat attendu que la démonstration produira.  

> ##### Figure9  
> Le tiroir de la console, après évaluation `parseInt(addend1) + parseInt(addend2)`  
> ![Le tiroir de la console, après avoir évalué le sein de l’arborescence (addend1) + sein (addend2)][ImageJSConsoleEvaluated]  

## Étape 7: appliquer un correctif   

Si vous trouvez un correctif pour le bogue, essayez de résoudre le problème en modifiant le code et en exécutant de nouveau la démonstration.  Vous n’avez pas besoin de quitter DevTools pour appliquer le correctif.  Vous pouvez modifier le code JavaScript directement dans l’interface utilisateur DevTools.  Essayez-le maintenant:  

1.  Cliquez **sur reprise de l’exécution** du script de ![ reprise ][ImageResumeIcon] .  
1.  Dans l' **éditeur de code**, remplacez ligne 32, `var sum = addend1 + addend2` par `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer vos modifications.  
1.  Cliquez sur désactiver les points d' **arrêt** ![ Désactiver les points d’arrêt ][ImageDeactivateIcon] .  Il change de bleu pour indiquer qu’il est actif.  Si cette valeur est définie, DevTools ignore les points d’arrêt que vous définissez.  
1.  Testez la démonstration avec des valeurs différentes.  La démonstration est désormais correctement calculée.  

> [!CAUTION]
> Ce flux de travail s’applique uniquement au code exécuté dans votre navigateur.  Cela ne résout pas le code de tous les utilisateurs visitant votre page.  Pour ce faire, vous devez résoudre le code qui se trouve sur vos serveurs.  

## Étapes suivantes   

Félicitations!  Vous savez maintenant comment tirer le meilleur parti de Microsoft Edge DevTools lors du débogage JavaScript.  Les outils et méthodes que vous avez appris dans ce didacticiel pourront vous épargner des heures de comptage.  

Ce didacticiel ne vous a montré que deux manières de définir des points d’arrêt.  DevTools offre de nombreuses autres manières, notamment:  

*   Les points d’arrêt conditionnel qui sont uniquement déclenchés lorsque la condition que vous spécifiez est vrai.  
*   Points d’arrêt sur les exceptions interceptées ou non capturées.  
*   XHR points d’arrêt qui sont déclenchés lorsque l’URL demandée correspond à une sous-chaîne que vous fournissez.  

<!-- See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

<!--There are a couple of code stepping controls that were not explained in this tutorial.  See [Step over line of code][JSReferenceStepping] to learn more.  -->  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: /microsoft-edge/devtools-guide-chromium/media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageResumeIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  

[ImageJSBugs]: /microsoft-edge/devtools-guide-chromium/media/javascript-js-demo-bad.msft.png "Figure 1: le résultat de 5 + 1 est 51, mais devrait être 6"  
[ImageJSConsole]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-empty.msft.png "Figure 2: panneau de la console"  
[ImageJSSources]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections.msft.png "Figure 3: panneau sources"  
[ImageJSSourcesAnnotated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections-annotated.msft.png "Figure 4:3 parties de l’interface utilisateur du panneau sources"  
[ImageJSClickCheckbox]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png "Figure 5: la case à cocher Click est activée"  
[ImageJSLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused.msft.png "Figure 6: DevTools s’arrête sur le point d’arrêt de la ligne de code de la ligne 32"  
[ImageJSScope]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-scope.msft.png "Figure 7: volet d’étendue"  
[ImageJSWatchExpression]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-watch.msft.png "Figure 8: volet expression espionner"  
[ImageJSConsoleEvaluated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-console.msft.png "Le tiroir de la console, après avoir évalué le sein de l’arborescence (addend1) + sein (addend2)"  

<!-- links -->  

<!--[JSBreakpoints]: breakpoints.md "JavaScript Breakpoints"  -->  
<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->
[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "ouvrir une démonstration"  
<!--[JSReferenceStepping]: reference.md#stepping "Reference Stepping"  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
