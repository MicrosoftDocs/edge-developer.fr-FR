---
description: Découvrez comment utiliser Microsoft Edge DevTools pour rechercher et corriger les bogues JavaScript.
title: Commencer à utiliser le débogage de JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325946"
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
# Commencer à déboguer JavaScript dans Microsoft Edge DevTools  

Cet article vous apprend le flux de travail de base pour le débogage d’un problème JavaScript dans DevTools.  

## Étape 1 : Reproduire le bogue  

La recherche d’une série d’actions qui reproduisent systématiquement un bogue est toujours la première étape du débogage.  

1.  Choose **Open Demo**.  Maintenez `Control` \(Windows, Linux\) ou `Command` \(macOS\) et ouvrez la démonstration dans un nouvel onglet de navigateur.  
    
    [Démonstration ouverte][OpenDebugJSDemo]  
    
1.  Entrez `5` dans la zone de texte Numéro **1.**  
1.  Entrez `1` dans la zone de texte Numéro **2.**  
1.  Choose **Add Number 1 and Number 2**.  L’étiquette sous le bouton indique `5 + 1 = 51` .  Le résultat doit être `6` .  Ensuite, corrigez l’erreur d’ajout qui est le bogue.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 entraîne 51, mais doit être 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` résultats `51` dans , mais doit être `6`  
    :::image-end:::  
    
## Étape 2 : Familiarisez-vous avec l’interface utilisateur du panneau Sources  

DevTools fournit de nombreux outils différents pour différentes tâches.  Les différentes tâches incluent la modification du CSS, le profilage des performances de chargement de page et la surveillance des demandes réseau.  Le **panneau Sources** est l’endroit où vous déboguer JavaScript.  

1.  Ouvrez DevTools en appuyant sur `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  Ce raccourci ouvre le panneau **Console.**  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Panneau console" lightbox="../media/javascript-console-empty.msft.png":::
       **L’outil Console**  
    :::image-end:::  
    
1.  Choisissez **l’outil Sources.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Panneau Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       Panneau **Sources**  
    :::image-end:::  
    
**L’interface utilisateur** du panneau Sources est en trois parties.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Les 3 parties de l’interface utilisateur du panneau Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Les 3 parties de l’interface utilisateur **du panneau Sources**  
:::image-end:::  

1.  Volet **Navigateur de** fichiers \(Section 1 dans la figure précédente\).  Chaque fichier demandé par la page web est répertorié ici.  
1.  Volet **Éditeur** de code \(Section 2 dans la figure précédente\).  Après avoir sélectionné un fichier dans **le** volet Navigateur de fichiers, le contenu de ce fichier s’affiche ici.  
1.  Volet **Debugging JavaScript** \(Section 3 dans la figure précédente\).  Divers outils permettant d’inspecter javaScript pour la page web.  Si votre fenêtre DevTools est large, ce volet s’affiche à droite du volet Éditeur **de** code.  
    
## Étape 3 : Suspendre le code avec un point d’arrêt  

Une méthode courante pour le débogage de ce type de problème consiste à insérer plusieurs instructions dans le code, puis à inspecter les valeurs à mesure que `console.log()` le script s’exécute.  Par exemple:  

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

La méthode peut faire le travail, mais les points d’arrêt `console.log()` le sont plus rapidement. ****  Un point d’arrêt vous permet de suspendre votre code au milieu de l’runtime et d’examiner toutes les valeurs à ce moment-là.  Les points d’arrêt ont quelques avantages par rapport à la `console.log()` méthode :  

*   Avec , vous devez ouvrir manuellement le code source, trouver le code approprié, insérer les instructions, puis actualiser la page web pour afficher les messages dans `console.log()` `console.log()` la **console**.  Avec les points d’arrêt, vous pouvez suspendre le code pertinent sans même savoir comment le code est structuré.  
*   Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous souhaitez inspecter.  Avec les points d’arrêt, DevTools affiche les valeurs de toutes les variables à ce moment-là.  Parfois, les variables qui affectent votre code sont masquées et obscurcies.  
    
En bref, les points d’arrêt peuvent vous aider à trouver et corriger les bogues plus rapidement que la `console.log()` méthode.  

Si vous revenir en arrière et réfléchissez au fonctionnement de l’application, vous pouvez deviner que la somme incorrecte \( \) est calculée dans l’écoute d’événements associée au bouton Ajouter le numéro 1 et le numéro `5 + 1 = 51` `click` **2.**  Ainsi, vous souhaitez probablement suspendre le code au moment où `click` l’écoute s’exécute.  **Les points d’arrêt du lanceur d’événements** vous permet d’y faire exactement les choses :  

1.  Dans le **volet Débogage JavaScript,** sélectionnez Points d’arrêt de l’écoute d’événements pour développer la section. ****  DevTools révèle une liste de catégories d’événements ex expandables, telles que **Animation** et **Presse-papiers.**  
1.  En de côté de la **catégorie d’événement Mouse,** choisissez **Expand** \( Expand ![ icon ][ImageExpandIcon] \).  DevTools révèle une liste d’événements de souris, tels que **le** clic et **le clic avec la souris.**  Chaque événement dispose d’une case à cocher en regard.  
1.  Cochez la case en regard de **cliquer.**  DevTools est désormais installé pour être automatiquement suspendu lors de l’erreur `click` d’événements.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Sélectionnez la case à cocher en regard de cliquer" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Sélectionnez la case à cocher en regard de **cliquer**  
    :::image-end:::  
    
1.  De retour à la démonstration, choisissez de nouveau **Ajouter le numéro 1 et le numéro 2.**  DevTools interrompt la démonstration et met en évidence une ligne de code dans le **panneau Sources.**  DevTools doit s’interrompre sur la ligne 16 dans `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si vous faites une pause sur une autre ligne de code, appuyez sur Reprendre l’exécution du **script** \( Reprendre l’exécution du script \) jusqu’à ce que vous arrêtiez ![ sur la ligne ][ImageResumeIcon] correcte.  
    
    > [!NOTE]
    > Si vous avez suspendu sur une autre ligne, vous avez une extension de navigateur qui inscrit un listener d’événement sur chaque `click` page web que vous visitez.  Vous avez été suspendu dans `click` l’écoute de l’extension.  Si vous utilisez le mode InPrivate pour parcourir en privé **,** ce qui désactive toutes les extensions, vous pouvez voir que vous mettez en pause la ligne de code souhaitée à chaque fois.  

<!--todo: add inprivate section when available -->  

**Les points d’arrêt de l’écoute** d’événements ne sont qu’un des nombreux types de points d’arrêt disponibles dans DevTools.  Mémorisez tous les différents types pour vous aider à déboguer les différents scénarios aussi rapidement que possible.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Étape 4 : Procédure pas à pas dans le code  

Une cause courante de bogues est lorsqu’un script s’exécute dans un mauvais ordre.  La procédure pas à pas de votre code vous permet de parcourir l’runtime de votre code.  Vous pouvez parcourir une ligne à la fois pour déterminer exactement où votre code s’exécute dans un ordre différent de celui prévu.  Essayez maintenant :  

1.  Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  DevTools exécute le code suivant sans y aller pas à pas.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools ignore quelques lignes de code.  En effet, étant donné que la qualité est false, le `inputsAreEmpty()` bloc de code de l’instruction ne `if` s’exécute pas.  
    
1.  Dans le panneau **Sources** de DevTools, sélectionnez Pas à pas dans l’appel de fonction suivante **\(** Pas à pas dans l’appel de fonction suivant \) pour exécuter la fonction, ligne par ![ ][ImageIntoIcon] `updateLabel()` ligne.  
    
Passer en revue une ligne à la fois est l’idée de base qui consiste à passer en revue le code pas à pas.  Si vous regardez le code dans , vous voyez que le bogue se trouve probablement quelque `get-started.js` part dans la `updateLabel()` fonction.  Au lieu d’aller pas à pas dans chaque ligne de code, vous pouvez utiliser un autre type de point d’arrêt pour suspendre le code plus près de l’emplacement probable du bogue.  

## Étape 5 : Définir un point d’arrêt de ligne de code  

Les points d’arrêt de ligne de code sont le type de point d’arrêt le plus courant.  Lorsque vous arrivez à la ligne de code spécifique que vous souhaitez suspendre, utilisez un point d’arrêt de ligne de code.  

1.  Regardez la dernière ligne de code dans `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À gauche, le numéro de cette ligne de code particulière s’affiche sous la couleur **34**.  Choisissez la **ligne 34**.  DevTools place une icône rouge à gauche de **34**.  L’icône rouge indique qu’un point d’arrêt de ligne de code se trouve sur cette ligne.  DevTools s’interrompt toujours avant l’utilisation de cette ligne de code.  
1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  Le script continue d’être en cours d’exécution jusqu’à atteindre la ligne 33.  Sur les lignes 31, 32 et 33, DevTools imprime les valeurs de , et à droite du point-virgule sur `addend1` `addend2` chaque `sum` ligne.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools s’interrompt sur le point d’arrêt de ligne de code sur la ligne 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools s’interrompt sur le point d’arrêt de ligne de code sur la ligne 34  
    :::image-end:::  
    
## Étape 6 : Vérifier les valeurs des variables  

Les valeurs `addend1` de , `addend2` et `sum` semblent suspectes.  Les valeurs sont wrapped entre guillemets.  Les guillemets signifient que la valeur est une chaîne, ce qui constitue une bonne hypothèse pour expliquer la cause du bogue.  Recueillez plus d’informations sur la situation.  DevTools fournit de nombreux outils pour examiner les valeurs des variables.  

### Méthode 1 : volet d’étendue  

Si vous faites une pause **** sur une ligne de code, le volet Étendue affiche les variables locales et globales actuellement définies, ainsi que la valeur de chaque variable.  Il affiche également les variables de fermeture, le cas échéant.  Double-cliquez sur une valeur de variable pour la modifier.  Si vous ne faites pas de pause sur une ligne de code, **le** volet d’étendue est vide.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Volet d’étendue" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Volet **d’étendue**  
:::image-end:::  

### Méthode 2 : Expressions d’observation  

Le **volet Expressions** observateurs vous permet de surveiller les valeurs des variables au fil du temps.  Comme son nom l’indique, les **expressions** d’observation ne sont pas limitées aux variables.  Vous pouvez stocker n’importe quelle expression JavaScript valide dans une **expression d’observation.**  Essayez maintenant.  

1.  Choisissez le **volet** d’observation.  
1.  Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).  
1.  Entrez `typeof sum`.  
1.  Sélectionnez `Enter` .  DevTools affiche `typeof sum: "string"` .  La valeur à droite du deux-points est le résultat de votre Expression d’observation.  
    
> [!NOTE]
> Dans le **volet Expression** de l’observation \(en bas à droite\) de la figure suivante, l’Expression `typeof sum` d’observation s’affiche.  Si votre fenêtre DevTools est grande, le volet **Expression** d’observation se trouve à droite au-dessus du volet Points d’arrêt de l’écoute d’événements. ****  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Volet d’expression d’observation" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Volet **d’expression** d’observation  
:::image-end:::  

Comme on le suspecte, `sum` est évalué en tant que chaîne, lorsqu’il doit s’agit d’un nombre.  Vous avez maintenant confirmé que le type de valeur est la cause du bogue.  

### Méthode 3 : Console  

La **console** vous permet d’afficher les messages et vous pouvez également l’utiliser pour évaluer des `console.log()` instructions JavaScript arbitraires.  Pour le débogage, vous pouvez utiliser la **console** pour tester les correctifs potentiels pour les bogues.  Essayez maintenant.  

1.  Si le caisse de la **console** est fermé, `Escape` sélectionnez-le pour l’ouvrir.  Le **panneau** console s’ouvre dans le panneau inférieur de la fenêtre DevTools.  
1.  Dans la **console,** tapez `parseInt(addend1) + parseInt(addend2)` .  L’instruction de l’outil est suspendue sur une ligne de code où `addend1` et se trouve dans `addend2` l’étendue.  
1.  Sélectionnez `Enter` .  DevTools évalue l’instruction et imprime, ce qui est le résultat que vous attendez de `6` la démonstration.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Le caisse de la console, après avoir évalué parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       Le caisse **de** la console, après évaluation `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Étape 7 : Appliquer un correctif  

Si vous trouvez un correctif pour le bogue, essayez votre correctif en éditant le code et en réruisant la démonstration.  Vous pouvez modifier le code JavaScript directement dans l’interface utilisateur de DevTools et appliquer le correctif.  Essayez maintenant.  

1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  
1.  Dans **l’Éditeur de code,** remplacez la ligne 32, `var sum = addend1 + addend2` par `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer votre modification.  
1.  Choisissez **Désactiver les points d’arrêt** \( Désactiver les points ![ d’arrêt ][ImageDeactivateIcon] \).  Il change de bleu pour indiquer que l’option est active.  Lorsque **les points d’arrêt Deactivate sont définies,** DevTools ignore les points d’arrêt que vous définissez.  
1.  Essayez la démonstration avec des valeurs différentes.  La démonstration calcule maintenant correctement.  
    
> [!CAUTION]
> Ce flux de travail applique uniquement un correctif au code en cours d’exécution dans votre navigateur.  Il ne corrige pas le code pour tous les utilisateurs qui visitent votre page web.  Pour ce faire, vous devez corriger le code qui se trouve sur vos serveurs.  

## Étapes suivantes  

Félicitations!  Vous savez maintenant comment utiliser microsoft Edge DevTools lors du débogage de JavaScript.  Les outils et méthodes que vous avez appris dans cet article peuvent vous faire gagner un nombre d’heures.  

Cet article vous a appris uniquement deux façons de définir des points d’arrêt.  DevTools offre de nombreuses autres façons, y compris les paramètres suivants.  

*   Points d’arrêt conditionnels qui ne sont déclenchés que lorsque la condition que vous fournissez est vraie.  
*   Points d’arrêt sur les exceptions capturées ou non.  
*   Points d’arrêt XHR déclenchés lorsque l’URL demandée correspond à une sous-stration que vous fournissez.  
    
Pour plus d’informations sur le moment et la façon d’utiliser chaque type, accédez à [Suspendre votre code avec des points d’arrêt.][DevtoolsJavscriptBreakpoints]  

Quelques contrôles de code pas à pas ne sont pas expliqués dans cet article.  Pour plus d’informations, [accédez à la ligne de code][DevtoolsJavascriptReferenceStepThroughCode]Pas à pas.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d’arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Code pas à pas : référence de débogage JavaScript | Documents Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Ouvrir le | Glitch"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
