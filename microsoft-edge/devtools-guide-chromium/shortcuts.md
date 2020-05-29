---
title: Raccourcis clavier dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 031457d33bf3cf102380c01d9084619313612124
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601893"
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
   limitations under the License. -->





# Raccourcis clavier dans Microsoft Edge DevTools   





Cette page est une référence des raccourcis clavier dans Microsoft Edge DevTools.

Vous pouvez également accéder à des raccourcis dans les info-bulles. Pointez sur un élément de l’interface utilisateur de DevTools pour afficher son info-bulle. Si l’élément comporte un raccourci, l’info-bulle y est associée.

## Raccourcis clavier pour l’ouverture de DevTools   

Pour ouvrir DevTools, appuyez sur les raccourcis clavier suivants lorsque le curseur se trouve dans la fenêtre d’affichage du navigateur:

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Ouvrir le panneau de configuration que vous avez utilisé en dernier | `F12` ou`Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Ouvrir l’écran de la **console** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Ouvrir le panneau **éléments** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C`ou`Command`+`Option`+`C` |  

## Raccourcis clavier globaux   

Les raccourcis clavier suivants sont disponibles dans la plupart des panneaux de DevTools.

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Afficher les **paramètres** | `?` ou `F1` | `?` ou`Function`+`F1` |  
| Mettre le focus sur le panneau suivant | `Control`+`]` | `Command`+`]` |  
| Focus le panneau précédent | `Control`+`[` | `Command`+`[` |  
| Revenez à la [position d’ancrage][DevtoolsCustomizeIndexPlacement] que vous avez utilisée pour la dernière fois.  Si DevTools a été dans sa position par défaut pour l’ensemble de la session, ce raccourci détache DevTools dans une fenêtre séparée | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Activer/désactiver [DeviceMode][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Activer/désactiver le **mode d’élément Inspect** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Ouvrir le [menu de commandes][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Faire basculer le [tiroir][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Rechargement normal | `F5` ou`Control`+`R` | `Command`+`R` |  
| Chargement papier | `Control`+`F5`ou`Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Rechercher du texte dans le panneau actuel.  Non pris en charge dans les panneaux **d’audit, d'** **application**et de **sécurité** | `Control`+`F` | `Command`+`F` |  
| Ouvrir l’onglet **recherche** du [tiroir][DevtoolsCustomizeIndexDrawer]pour vous permettre de rechercher du texte sur toutes les ressources chargées | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Ouvrir un fichier dans le volet **sources** | `Control`+`O`ou`Control`+`P` | `Command`+`O`ou`Command`+`P` |  
| Effectuer un zoom avant | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Zoom arrière | `Control`+`-` | `Command`+`-` |  
| Restaurer le niveau de zoom par défaut | `Control`+`0` | `Command`+`0` |  
| Exécution d’un extrait | Appuyez sur `Control` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez `!` suivi du nom du script, puis appuyez sur `Enter` | Appuyez sur `Command` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez `!` suivi du nom du script, puis appuyez sur `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Raccourcis clavier du panneau éléments   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Annuler la modification | `Control`+`Z` | `Command`+`Z` |  
| Rétablir la modification | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Sélectionner l’élément au-dessus/en dessous de l’élément actuellement sélectionné | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Développez le nœud actuellement sélectionné. Si le nœud est déjà développé, ce raccourci sélectionne l’élément situé en dessous | `Right Arrow` | `Right Arrow` |  
| Réduire le nœud actuellement sélectionné. Si le nœud est déjà réduit, ce raccourci sélectionne l’élément situé au-dessus | `Left Arrow` | `Left Arrow` |  
| Développer ou réduire le nœud actuellement sélectionné et tous ses enfants | `Control` + `Alt` Puis cliquez sur l’icône en regard du nom de l’élément | `Option`Puis cliquez sur l’icône en regard du nom de l’élément |  
| Activer/désactiver le mode **modification des attributs** dans l’élément actuellement sélectionné | `Enter` | `Enter` |  
| Sélectionner l’attribut suivant/précédent après avoir entré le mode **modifier les attributs** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Masquer l’élément actuellement sélectionné | `H` | `H` |  
| Basculer la **modification en mode HTML** dans l’élément actuellement sélectionné | `Function`+`F2` | `F2` |  

### Raccourcis clavier du volet styles   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Accéder à la ligne où une valeur de propriété est déclarée | Mettre `Control` en attente, puis cliquez sur la valeur de la propriété | Mettre `Command` en attente, puis cliquez sur la valeur de la propriété |  
| Parcourir les représentations RBGA, HSLA et Hex d’une valeur de couleur | Mettre `Shift` en attente, puis cliquez sur la zone **Aperçu couleur** en regard de la valeur | Mettre `Shift` en attente, puis cliquez sur la zone **Aperçu couleur** en regard de la valeur |  
| Sélectionner la propriété ou la valeur suivante/précédente | Cliquez sur un nom ou une valeur de propriété, puis appuyez sur`Tab` / `Shift`+`Tab` | Cliquez sur un nom ou une valeur de propriété, puis appuyez sur`Tab` / `Shift`+`Tab` |  
| Incrémenter/décrémenter une valeur de propriété de 0,1 | Cliquez sur une valeur, puis appuyez sur Alt + flèche vers le haut/`Alt`+`Down Arrow` | Cliquez sur une valeur, puis appuyez sur `Option` + `Up Arrow` /option + flèche vers le bas |  
| Incrémenter/décrémenter une valeur de propriété de 1 | Cliquez sur une valeur, puis appuyez sur`Up Arrow` / `Down Arrow` | Cliquez sur une valeur, puis appuyez sur`Up Arrow` / `Down Arrow` |  
| Incrémenter/décrémenter une valeur de propriété de 10 | Cliquez sur une valeur, puis appuyez sur`Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Cliquez sur une valeur, puis appuyez sur`Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Incrémenter/décrémenter une valeur de propriété de 100 | Cliquez sur une valeur, puis appuyez sur`Control`+`Up Arrow` / `Control`+`Down Arrow` | Cliquez sur une valeur, puis appuyez sur`Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Raccourcis clavier du panneau sources   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Suspendre le script Runtime \ (s’il est en cours d’exécution \) ou reprendre \ (si vous êtes en pause) | `F8` ou`Control`+`\` | `F8` ou`Command`+`\` |  
| Étape au fil de l’appel de fonction suivante | `F10` ou`Control`+`'` | `F10` ou`Command`+`'` |  
| Passer à l’appel de fonction suivante | `F11` ou`Control`+`;` | `F11` ou`Command`+`;` |  
| Sortir de la fonction actuelle | `Shift`+`F11`ou`Control`+`Shift`+`;` | `Shift`+`F11`ou`Command`+`Shift`+`;` |  
| Accéder à une [ligne de code spécifique en pause][DevtoolsJavascriptBreakpointsLOC] | `Control`En attente, puis cliquez sur la ligne de code | `Command`En attente, puis cliquez sur la ligne de code |  
| Sélectionner l’image d’appel ci-dessous ou au-dessus de l’image actuellement sélectionnée | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Enregistrer les modifications apportées aux modifications locales | `Control`+`S` | `Command`+`S` |  
| Enregistrer toutes les modifications | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Atteindre le trait | `Control`+`G` | `Control`+`G` |  
| Atteindre un numéro de ligne du fichier actuellement ouvert | Appuyez sur `Control` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez `:` suivi du numéro de ligne, puis appuyez sur `Enter` | Appuyez sur `Command` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez `:` suivi du numéro de ligne, puis appuyez sur `Enter` |  
| Accéder à une colonne du fichier actuellement ouvert \ (par exemple, ligne 5, colonne 9 \) | Appuyez sur `Control` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez le numéro de ligne, puis `:` un autre `:` , puis le numéro de la colonne, puis appuyez sur `Enter` | Appuyez sur `Command` + `O` pour ouvrir le [menu de commandes][DevtoolsCommandMenuIndex], tapez le numéro de ligne, puis `:` un autre `:` , puis le numéro de la colonne, puis appuyez sur `Enter` |  
| Accédez à la déclaration d’une fonction \ (si le fichier est ouvert par le biais d’un fichier HTML ou d’un script ou d’un ensemble de règles \ (si le fichier est déjà ouvert est une feuille de style \) | Appuyez sur `Control` + `Shift` + `O` , puis tapez le nom de l’ensemble de déclarations/règles ou sélectionnez-le dans la liste des options. | Appuyez sur `Command` + `Shift` + `O` , puis tapez le nom de l’ensemble de déclarations/règles ou sélectionnez-le dans la liste des options. |  
| Fermer l’onglet actif | `Alt`+`W` | `Option`+`W` |  

### Raccourcis clavier de l’éditeur de code   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Supprimer tous les caractères du dernier mot, jusqu’au curseur | `Control`+`Delete` | `Option`+`Delete` |  
| Ajouter ou supprimer un [point d’arrêt de ligne de code][DevtoolsJavascriptBreakpointsLOC] | Focalisez le curseur sur la ligne, puis appuyez sur`Control`+`B` | Focalisez le curseur sur la ligne, puis appuyez sur`Command`+`B` |  
| Atteindre le crochet correspondant | `Control`+`M` | `Control`+`M` |  
| Basculer entre les commentaires d’une ligne. Si plusieurs lignes sont sélectionnées, DevTools ajoute un commentaire au début de chaque ligne. | `Control`+`/` | `Command`+`/` |  
| Sélectionner/désélectionner l’occurrence suivante du mot sur lequel se trouve le curseur. Chaque occurrence est mise en surbrillance en même temps | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Raccourcis clavier du panneau performances   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Démarrer/arrêter l’enregistrement | `Control`+`E` | `Command`+`E` |  
| Enregistrer un enregistrement | `Control`+`S` | `Command`+`S` |  
| Charger un enregistrement | `Control`+`O` | `Command`+`O` |  

## Raccourcis clavier du panneau mémoire 

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Démarrer/arrêter l’enregistrement | `Control`+`E` | `Command`+`E` |  

## Raccourcis clavier de l’écran de la console   

| Action | Windows | macOS |  
|:--- |:--- |:--- |  
| Accepter la suggestion de saisie semi-automatique | `Right Arrow` ou `Tab` | `Right Arrow` ou `Tab` |  
| Rejeter la suggestion de saisie semi-automatique | `Escape` | `Escape` |  
| Instruction Get Previous | `Up Arrow` | `Up Arrow` |  
| Instruction Get suivante | `Down Arrow` | `Down Arrow` |  
| Mettre le focus sur la **console** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Effacement de la **console** | `Control`+`L` | `Command`+`K`ou`Option`+`L` |  
| Forcer une entrée multiligne Notez que DevTools doit détecter par défaut les scénarios multilignes, ce qui signifie que ce raccourci est désormais généralement inutile | `Shift`+`Enter` | `Command`+`Return` |  
| Exécution | `Enter` | `Return` |  
| Développer toutes les sous-propriétés d’un objet connecté à la console | Maintenez la touche enfoncée `Alt` , puis cliquez sur **développer** ![ .][ImageExpandIcon] | Maintenez la touche enfoncée `Alt` , puis cliquez sur **développer** ![ .][ImageExpandIcon] |  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools"  
[DevtoolsCustomizeIndexPlacement]: /microsoft-edge/devtools-guide-chromium/customize/index#change-devtools-placement "Changer le positionnement de DevTools-personnaliser Microsoft Edge DevTools"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools"  
[DevtoolsJavascriptBreakpointsLOC]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de la ligne de code: comment mettre en pause votre code avec des points d’arrêt dans Microsoft Edge DevTools"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/shortcuts) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
