---
description: Découvrez comment utiliser Microsoft Edge DevTools pour rechercher et corriger les bogues JavaScript.
title: Commencer à déboguer JavaScript dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a60bd0c734df18ba7424cde6a828abbd9e7135a9
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519372"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a>Commencer à déboguer JavaScript dans Microsoft Edge DevTools  

Cet article vous apprend le flux de travail de base pour le débogage d'un problème JavaScript dans DevTools.  

## <a name="step-1-reproduce-the-bug"></a>Étape 1 : Reproduire le bogue  

La recherche d'une série d'actions qui reproduisent systématiquement un bogue est toujours la première étape du débogage.  

1.  Choisissez le lien **Ouvrir la démonstration** suivant et ouvrez la page web dans un nouvel onglet.  Pour ouvrir la démonstration dans un nouvel onglet, sélectionnez et maintenez `Ctrl` \(Windows, Linux\) ou `Command` \(macOS\), puis choisissez Ouvrir la **démonstration.**  
    
    [Ouvrir la démonstration][OpenDebugJSDemo]  
    
1.  Entrez `5` dans la zone de texte Numéro **1.**  
1.  Entrez `1` dans la zone de texte Numéro **2.**  
1.  Choose **Add Number 1 and Number 2**.  L'étiquette sous le bouton indique `5 + 1 = 51` .  Le résultat doit être `6` .  Ensuite, corrigez l'erreur d'ajout qui est le bogue.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 entraîne 51, mais doit être 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` résultats `51` dans , mais doit être `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a>Étape 2 : Familiarisez-vous avec l'interface utilisateur de l'outil Sources  

DevTools fournit de nombreux outils différents pour différentes tâches.  Les différentes tâches incluent la modification du CSS, le profilage des performances de chargement de page et la surveillance des demandes réseau.  **L'outil Sources** vous permet de déboguer JavaScript.  

1.  Pour ouvrir **l'outil Console** dans DevTools, sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="L'outil Console" lightbox="../media/javascript-console-empty.msft.png":::
       **L'outil Console**  
    :::image-end:::  
    
1.  Choisissez **l'outil Sources.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Outil Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       Outil **Sources**  
    :::image-end:::  
    
**L'interface utilisateur** de l'outil Sources est en trois parties.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Les 3 parties de l'interface utilisateur de l'outil Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Les 3 parties de l'interface utilisateur de l'outil **Sources**  
:::image-end:::  

1.  Volet **Navigateur** \(Section 1 dans la figure précédente\).  Chaque fichier demandé par la page web est répertorié ici.  
1.  Volet **Éditeur** \(Section 2 dans la figure précédente\).  Une fois que vous avez choisi un fichier dans le volet **Navigateur,** ce volet affiche le contenu du fichier.  
1.  Volet **Débogger** \(Section 3 dans la figure précédente\).  Ce volet fournit des outils permettant d'inspecter le JavaScript de la page web.  Si votre fenêtre DevTools est large, ce volet s'affiche à droite du **volet** Éditeur.  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a>Étape 3 : Suspendre le code avec un point d'arrêt  

Une méthode courante pour le débogage de ce type de problème consiste à insérer plusieurs instructions dans le code, puis à inspecter les valeurs à mesure que `console.log()` le script s'exécute.  Par exemple:  

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

La méthode peut faire le travail, mais les points d'arrêt `console.log()` le sont plus rapidement. ****  Un point d'arrêt vous permet de suspendre votre code au milieu de l'runtime et d'examiner toutes les valeurs à ce moment-là.  Les points d'arrêt ont les avantages suivants par rapport à la `console.log()` méthode.  

*   Avec , vous devez ouvrir manuellement le code source, trouver le code approprié, insérer les instructions, puis actualiser la page web pour afficher les messages dans `console.log()` `console.log()` la **console**.  Avec les points d'arrêt, vous pouvez suspendre le code pertinent sans même savoir comment le code est structuré.  
*   Dans vos `console.log()` instructions, vous devez spécifier explicitement chaque valeur que vous souhaitez inspecter.  Avec les points d'arrêt, DevTools vous montre les valeurs de toutes les variables à ce moment-là.  Parfois, les variables qui affectent votre code sont masquées et obscurcies.  
    
En bref, les points d'arrêt peuvent vous aider à trouver et corriger les bogues plus rapidement que la `console.log()` méthode.  

Si vous revenir en arrière et réfléchissez au fonctionnement de l'application, vous pouvez deviner que la somme incorrecte \( \) est calculée dans l'écoute d'événements associée au bouton Ajouter le numéro 1 et le numéro `5 + 1 = 51` `click` **2.**  Ainsi, vous souhaitez probablement suspendre le code au moment où `click` l'écoute s'exécute.  **Les points d'arrêt du lanceur d'événements** vous permet d'y faire exactement les choses :  

1.  Dans le **volet Débogger,** sélectionnez Points d'arrêt de l'écoute d'événements pour développer la section. ****  DevTools révèle une liste de catégories d'événements ex expandables, telles que **l'animation** et **le Presse-papiers.**  
1.  En de côté de la **catégorie d'événement Mouse,** choisissez **Expand** \( Expand ![ icon ](../media/expand-icon.msft.png) \).  DevTools révèle une liste d'événements de souris, tels que **le** clic et **le clic avec la souris.**  Chaque événement dispose d'une case à cocher en regard.  
1.  Cochez la case en regard de **cliquer.**  DevTools est désormais installé pour être automatiquement suspendu lors de l'erreur `click` d'événements.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Sélectionnez la case à cocher en regard de cliquer" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Sélectionnez la case à cocher en regard de **cliquer**  
    :::image-end:::  
    
1.  De retour à la démonstration, choisissez de nouveau **Ajouter le numéro 1 et le numéro 2.**  DevTools interrompt la démonstration et met en évidence une ligne de code dans **l'outil Sources.**  DevTools doit s'interrompre sur la ligne 16 dans `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si vous faites une pause sur une autre ligne de code, sélectionnez Reprendre l'exécution du **script** \( Reprendre l'exécution du script \) jusqu'à ce que vous arrêtiez ![ sur la ligne ](../media/resume-script-run-icon.msft.png) correcte.  
    
    > [!NOTE]
    > Si vous avez suspendu sur une autre ligne, vous avez une extension de navigateur qui inscrit un listener d'événement sur chaque `click` page web que vous visitez.  Vous êtes suspendu dans `click` l'écoute de l'extension.  Si vous utilisez le mode InPrivate pour parcourir en privé **,** ce qui désactive toutes les extensions, vous pouvez voir que vous mettez en pause la ligne de code souhaitée à chaque fois.  

<!--todo: add inprivate section when available -->  

**Les points d'arrêt d'écoute d'événements** ne sont qu'un des nombreux types de points d'arrêt disponibles dans DevTools.  Mémorisez tous les différents types pour vous aider à déboguer les différents scénarios aussi rapidement que possible.  <!--  To learn when and how to use each type, navigate to [Pause your code with breakpoints][JSBreakpoints].  -->  

## <a name="step-4-step-through-the-code"></a>Étape 4 : Procédure pas à pas dans le code  

Une cause courante de bogues est lorsqu'un script s'exécute dans un mauvais ordre.  La procédure pas à pas de votre code vous permet de parcourir l'runtime de votre code.  Vous pouvez parcourir une ligne à la fois pour déterminer exactement où votre code s'exécute dans un ordre différent de celui prévu.  Essayez maintenant :  

1.  Choose **Step over next function call** \( Step over next function call ![ ](../media/step-over-icon.msft.png) \).  DevTools exécute le code suivant sans y aller pas à pas.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools ignore quelques lignes de code.  En effet, étant donné que la qualité est false, le `inputsAreEmpty()` bloc de code de l'instruction ne `if` s'exécute pas.  
    
1.  Dans l'outil **Sources** de DevTools, sélectionnez Pas à pas dans l'appel de fonction suivante **\(** Pas à pas dans l'appel de fonction suivant \) pour exécuter la fonction, une ligne à la ![ ](../media/step-into-icon.msft.png) `updateLabel()` fois.  
    
Passer en revue une ligne à la fois est l'idée de base qui consiste à passer en revue le code pas à pas.  Si vous examinez le code `get-started.js` dans , le bogue se trouve probablement quelque part dans la `updateLabel()` fonction.  Au lieu d'aller pas à pas dans chaque ligne de code, vous pouvez utiliser un autre type de point d'arrêt pour suspendre le code plus près de l'emplacement probable du bogue.  

## <a name="step-5-set-a-line-of-code-breakpoint"></a>Étape 5 : Définir un point d'arrêt de ligne de code  

Les points d'arrêt de ligne de code sont le type de point d'arrêt le plus courant.  Lorsque vous arrivez à la ligne de code spécifique que vous souhaitez suspendre, utilisez un point d'arrêt de ligne de code.  

1.  Regardez la dernière ligne de code dans `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À gauche, le numéro de cette ligne de code particulière s'affiche sous la couleur **34**.  Choisissez la **ligne 34**.  DevTools affiche une icône rouge à gauche de **34**.  L'icône rouge indique qu'un point d'arrêt de ligne de code se trouve sur cette ligne.  DevTools s'interrompt toujours avant l'utilisation de cette ligne de code.  
1.  Choose **Resume script execution** \( Resume script execution ![ ](../media/resume-script-run-icon.msft.png) \).  Le script continue à s'exécuter jusqu'à atteindre la ligne 33.  Sur les lignes 31, 32 et 33, DevTools imprime les valeurs de , et à droite du point-virgule sur `addend1` `addend2` chaque `sum` ligne.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools s'interrompt sur le point d'arrêt de ligne de code sur la ligne 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools s'interrompt sur le point d'arrêt de ligne de code sur la ligne 34  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a>Étape 6 : Vérifier les valeurs des variables  

Les valeurs `addend1` de , `addend2` et `sum` semblent suspectes.  Les valeurs sont wrapped entre guillemets.  Les guillemets signifient que la valeur est une chaîne, ce qui constitue une bonne hypothèse pour expliquer la cause du bogue.  Recueillez plus d'informations sur la situation.  DevTools fournit de nombreux outils pour examiner les valeurs des variables.  

### <a name="method-1-the-scope-pane"></a>Méthode 1 : volet d'étendue  

Si vous faites une pause **** sur une ligne de code, le volet Étendue affiche les variables locales et globales actuellement définies, ainsi que la valeur de chaque variable.  Il affiche également les variables de fermeture, le cas échéant.  Double-cliquez sur une valeur de variable pour la modifier.  Si vous ne faites pas de pause sur une ligne de code, **le** volet d'étendue est vide.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Volet d'étendue" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Volet **d'étendue**  
:::image-end:::  

### <a name="method-2-watch-expressions"></a>Méthode 2 : Expressions d'observation  

Le **volet** Observateur vous permet de surveiller les valeurs de variables (par exemple) ou `sum` d'expressions (telles que `typeof sum` ).  Vous pouvez stocker n'importe quelle expression JavaScript valide dans une expression d'observation.  

1.  Choisissez le **volet** d'observation.  
1.  Choose **Add watch expression** \( Add watch expression ![ ](../media/add-expression-icon.msft.png) \).  
1.  Tapez `typeof sum`.  
1.  Sélectionnez `Enter` .  DevTools `typeof sum: "string"` s'affiche.  La valeur à droite du deux-points est le résultat de votre Expression d'observation.  
    
> [!NOTE]
> Dans la figure suivante, `typeof sum` l'Expression d'observation s'affiche dans le **volet** d'observation.  Si votre fenêtre DevTools **** est large, le volet **** Montre s'affiche dans le volet Débogueur, qui apparaît ensuite à droite.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Volet d'observation" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Volet **d'observation**  
:::image-end:::  

Comme on le suspecte, `sum` est évalué en tant que chaîne, lorsqu'il doit s'agit d'un nombre.  Vous avez maintenant confirmé que le type de valeur est la cause du bogue.  

### <a name="method-3-the-console"></a>Méthode 3 : Console  

La **console** vous permet d'afficher la `console.log()` sortie.  Vous pouvez également utiliser la **console pour** évaluer des instructions JavaScript arbitraires pendant que le débogger est suspendu au niveau d'une instruction de code.  Pour le débogage, vous pouvez utiliser la **console** pour tester les correctifs potentiels pour les bogues.

1.  Si **l'outil Console** est fermé, `Esc` sélectionnez-le pour l'ouvrir.  **L'outil** Console s'ouvre dans le volet inférieur de la fenêtre DevTools.  
1.  Dans la **console,** tapez `parseInt(addend1) + parseInt(addend2)` .  L'instruction de l'outil est suspendue sur une ligne de code où `addend1` et se trouve dans `addend2` l'étendue.  
1.  Sélectionnez `Enter` .  DevTools évalue l'instruction et imprime, ce qui est le résultat que vous attendez de `6` la démonstration.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="L'outil Console, après avoir évalué parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       **L'outil Console,** après évaluation `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a>Étape 7 : Appliquer un correctif  

Nous avons identifié un correctif possible pour le bogue.  Ensuite, modifiez le code JavaScript directement dans l'interface utilisateur de DevTools, puis réexécutez la démonstration pour tester le correctif, comme suit.

1.  Choose **Resume script execution** \( Resume script execution ![ ](../media/resume-script-run-icon.msft.png) \).  
1.  Dans le **volet** Éditeur, remplacez la `var sum = addend1 + addend2` ligne par `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer votre modification.  
1.  Choisissez **Désactiver les points d'arrêt** \( Désactiver les points ![ d'arrêt ](../media/deactivate-breakpoints-button-icon.msft.png) \).  Il change de bleu pour indiquer que l'option est active.  Lorsque **les points d'arrêt Deactivate sont définies,** DevTools ignore les points d'arrêt que vous définissez.  
1.  Essayez la démonstration avec des valeurs différentes.  La démonstration calcule maintenant correctement.  
    
> [!CAUTION]
> Ce flux de travail applique uniquement un correctif à une copie locale du code envoyé à partir du serveur.  Lors du débogage de votre projet, après avoir identifié le correctif, vous devez appliquer ce correctif au code sur le serveur, par exemple en éditant votre code source local, puis en déployant à nouveau votre code fixe sur le serveur.

## <a name="next-steps"></a>Étapes suivantes  

Félicitations!  Vous savez maintenant comment utiliser microsoft Edge DevTools lors du débogage de JavaScript.  Les outils et méthodes que vous avez appris dans cet article peuvent vous faire gagner un nombre d'heures.  

Cet article a présenté deux façons de définir des points d'arrêt.  DevTools fournit également des moyens de définir des points d'arrêt pour suspendre votre code lorsque certaines conditions sont remplies, telles que :

*   Points d'arrêt conditionnels qui ne sont déclenchés que lorsque la condition que vous fournissez est vraie.  
*   Points d'arrêt sur les exceptions capturées ou non.  
*   Points d'arrêt XHR déclenchés lorsque l'URL demandée correspond à une sous-stration que vous fournissez.  
    
Pour plus d'informations sur le moment et la façon d'utiliser chaque type, accédez à [Suspendre votre code avec des points d'arrêt.][DevToolsJavscriptBreakpoints]  

Quelques contrôles de code pas à pas ne sont pas expliqués dans cet article.  Pour plus d'informations, accédez à la ligne pas à pas dans l'article « Utiliser les fonctionnalités du débogger ». [][DevToolsJavascriptReferenceStepThroughCode]

### <a name="see-also"></a>Voir également

*   [Utilisez les fonctionnalités du débogger][DevToolsJavascriptReference] : à l'aide de l'interface utilisateur du débogger dans l'outil Sources.
*   [Vue d'ensemble][DevToolsSourcesIndex] de l'outil Sources : présente le débogger JavaScript et l'éditeur de code.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptReference]: ./reference.md "Utiliser les fonctionnalités de débogger | Documents Microsoft"  
[DevToolsSourcesIndex]: ../sources/index.md "Vue d'ensemble de l'outil Sources | Documents Microsoft"  
[DevToolsJavscriptBreakpoints]: ./breakpoints.md "Comment suspendre votre code avec des points d'arrêt dans Microsoft Edge DevTools | Documents Microsoft"
[DevToolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Code pas à pas : utiliser les fonctionnalités de débogger | Documents Microsoft"

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
