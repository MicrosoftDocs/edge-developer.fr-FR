---
description: Documentation canonique pour les Microsoft Edge clavier DevTools.
title: Microsoft Edge Raccourcis clavier DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f2b10bc763073632975248cd5a9caa523702e869
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565098"
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
# <a name="microsoft-edge-devtools-keyboard-shortcuts"></a>Microsoft Edge Raccourcis clavier DevTools  

Cet article est une référence aux raccourcis clavier dans Microsoft Edge DevTools.

Vous pouvez également trouver des raccourcis dans les bulles.  Pointez sur un élément d’interface utilisateur de DevTools pour afficher l’bulle.  Si l’élément possède un raccourci, l’bulle l’inclut.

## <a name="keyboard-shortcuts-for-opening-devtools"></a>Raccourcis clavier pour l’ouverture de DevTools  

Pour ouvrir DevTools, sélectionnez les raccourcis clavier suivants lorsque votre curseur est sélectionné sur la fenêtre d’affichage du navigateur.

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Ouvrez le panneau que vous avez utilisé en dernier | `F12` ou `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Ouvrir **l’outil Console** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Ouvrir **l’outil Éléments** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` ou `Command`+`Option`+`C` |  

## <a name="global-keyboard-shortcuts"></a>Raccourcis clavier globaux  

Les raccourcis clavier suivants sont disponibles dans la plupart, sinon la plupart, des panneaux DevTools.

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Afficher **Paramètres** | `?` or `F1` | `?` ou `Function`+`F1` |  
| Focus sur le panneau suivant | `Control`+`]` | `Command`+`]` |  
| Focus sur le panneau précédent | `Control`+`[` | `Command`+`[` |  
| Revenir à la [position d’accueil que][DevtoolsCustomizeIndexPlacement] vous avez utilisée en dernier.  Si DevTools est à la position par défaut pour l’ensemble de la session, ce raccourci désespéra de DevTools dans une fenêtre distincte. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Basculez [l’émulation de l’appareil][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Ouvrir le [menu Commande][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Toggle the [Drawer][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Actualisation normale | `F5` ou `Control`+`R` | `Command`+`R` |  
| Actualisation en dur | `Control`+`F5` ou `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Recherchez du texte dans le panneau actuel.  Non pris en charge dans **les outils Audits,** **Application**et **Sécurité** | `Control`+`F` | `Command`+`F` |  
| Ouvre **l’onglet Recherche** dans le [caisse,][DevtoolsCustomizeIndexDrawer]ce qui vous permet de rechercher du texte sur toutes les ressources chargées | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Ouvrir un fichier dans l’outil **Sources** | `Control`+`O` ou `Control`+`P` | `Command`+`O` ou `Command`+`P` |  
| Zoom avant | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Zoom arrière | `Control`+`-` | `Command`+`-` |  
| Restaurer le niveau de zoom par défaut | `Control`+`0` | `Command`+`0` |  
| Exécuter l’extrait de code | Sélectionnez `Control` + `O` pour ouvrir le [menu Commande][DevtoolsCommandMenuIndex], `!` tapez suivi du nom du script, puis sélectionnez `Enter` | Sélectionnez `Command` + `O` pour ouvrir le [menu Commande][DevtoolsCommandMenuIndex], `!` tapez suivi du nom du script, puis sélectionnez `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## <a name="elements-tool-keyboard-shortcuts"></a>Raccourcis clavier de l’outil Éléments  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Annuler la modification | `Control`+`Z` | `Command`+`Z` |  
| Redo change | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Sélectionnez l’élément au-dessus/en dessous de l’élément actuellement sélectionné | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Développez le nœud actuellement sélectionné.  Si le nœud est déjà développé, ce raccourci sélectionne l’élément en dessous | `Right Arrow` | `Right Arrow` |  
| Réduire le nœud actuellement sélectionné.  Si le nœud est déjà réduire, ce raccourci sélectionne l’élément au-dessus | `Left Arrow` | `Left Arrow` |  
| Développer ou réduire le nœud actuellement sélectionné et tous les enfants | Maintenez `Control` + `Alt` la touche Maintenez, puis sélectionnez **l’icône** de flèche en haut du nom de l’élément. | Maintenez `Option` la touche Maintenez, puis sélectionnez **l’icône** de flèche en haut du nom de l’élément. |  
| Basculez le mode **Modifier les attributs** sur l’élément actuellement sélectionné | `Enter` | `Enter` |  
| Sélectionnez l’attribut suivant/précédent après avoir entré le mode **Modifier les attributs** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Masquer l’élément actuellement sélectionné | `H` | `H` |  
| Toggle **Edit as HTML** mode on the currently selected element | `Function`+`F2` | `F2` |  

### <a name="styles-panel-keyboard-shortcuts"></a>Raccourcis clavier du panneau Styles  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Accéder à la ligne dans laquelle une valeur de propriété est déclarée | Conserver, `Control` puis sélectionner la valeur de la propriété | Conserver, `Command` puis sélectionner la valeur de la propriété |  
| Faire passer en cycle les représentations RBGA, HSLA et Hex d’une valeur de couleur | Mettre `Shift` en attente, puis choisir la **zone d’aperçu** de couleur en de côté de la valeur | Mettre `Shift` en attente, puis choisir la **zone d’aperçu** de couleur en de côté de la valeur |  
| Sélectionnez la propriété ou la valeur suivante/précédente | Choisissez un nom ou une valeur de propriété, puis sélectionnez `Tab` / `Shift`+`Tab` | Choisissez un nom ou une valeur de propriété, puis sélectionnez `Tab` / `Shift`+`Tab` |  
| Incrémenter/décrémenter une valeur de propriété de 0,1 | Choisissez une valeur, puis sélectionnez `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Choisissez une valeur, puis `Option` + `Up Arrow` sélectionnez /Option+Flèche vers le bas |  
| Incrémenter/décrémenter une valeur de propriété de 1 | Choisissez une valeur, puis sélectionnez `Up Arrow` / `Down Arrow` | Choisissez une valeur, puis sélectionnez `Up Arrow` / `Down Arrow` |  
| Incrémenter/décrémenter une valeur de propriété de 10 | Choisissez une valeur, puis sélectionnez `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Choisissez une valeur, puis sélectionnez `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Incrémenter/décrémenter une valeur de propriété de 100 | Choisissez une valeur, puis sélectionnez `Control`+`Up Arrow` / `Control`+`Down Arrow` | Choisissez une valeur, puis sélectionnez `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## <a name="sources-tool-keyboard-shortcuts"></a>Raccourcis clavier de l’outil Sources  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Suspendre le runtime du script \(s’il est en cours d’exécution\) ou reprendre \(si actuellement suspendu\) | `F8` ou `Control`+`\` | `F8` ou `Command`+`\` |  
| Pas à pas sur l’appel de fonction suivant | `F10` ou `Control`+`'` | `F10` ou `Command`+`'` |  
| Pas à pas dans l’appel de fonction suivant | `F11` ou `Control`+`;` | `F11` ou `Command`+`;` |  
| Sortir de la fonction actuelle | `Shift`+`F11` ou `Control`+`Shift`+`;` | `Shift`+`F11` ou `Command`+`Shift`+`;` |  
| Continuer [jusqu’à une ligne de code spécifique en pause][DevtoolsJavascriptBreakpointsLOC] | Conserver, `Control` puis choisir la ligne de code | Conserver, `Command` puis choisir la ligne de code |  
| Sélectionnez le cadre d’appel sous/au-dessus de l’image actuellement sélectionnée | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Enregistrer les modifications apportées aux modifications locales | `Control`+`S` | `Command`+`S` |  
| Enregistrer toutes les modifications | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Accéder à la ligne | `Control`+`G` | `Control`+`G` |  
| Passer à un numéro de ligne du fichier actuellement ouvert | Sélectionnez `Control` + `O` pour ouvrir le [menu Commande][DevtoolsCommandMenuIndex], `:` tapez suivi du numéro de ligne, puis sélectionnez `Enter` | Sélectionnez `Command` + `O` pour ouvrir le [menu Commande][DevtoolsCommandMenuIndex], `:` tapez suivi du numéro de ligne, puis sélectionnez `Enter` |  
| Aller à une colonne du fichier actuellement ouvert \(par exemple, ligne 5, colonne 9\) | Sélectionnez `Control` + `O` pour ouvrir le [menu Commande,][DevtoolsCommandMenuIndex]tapez, puis le numéro de ligne, puis un autre, puis le numéro `:` de `:` colonne, puis sélectionnez `Enter` | Sélectionnez `Command` + `O` pour ouvrir le [menu Commande,][DevtoolsCommandMenuIndex]tapez, puis le numéro de ligne, puis un autre, puis le numéro `:` de `:` colonne, puis sélectionnez `Enter` |  
| Accédez à une déclaration de fonction, si le fichier actuel est html ou un script.  <br />  Accédez à un ensemble de règles, si le fichier actuel est une feuille de style.  | Sélectionnez, puis tapez le nom de la déclaration /ensemble de règles, ou `Control` + `Shift` + `O` sélectionnez-le dans la liste des options | Sélectionnez, puis tapez le nom de la déclaration /ensemble de règles, ou `Command` + `Shift` + `O` sélectionnez-le dans la liste des options |  
| Fermer l’onglet actif | `Alt`+`W` | `Option`+`W` |  

### <a name="code-editor-keyboard-shortcuts"></a>Raccourcis clavier de l’éditeur de code  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Supprimer tous les caractères du dernier mot, jusqu’au curseur | `Control`+`Delete` | `Option`+`Delete` |  
| Ajouter ou supprimer un [point d’arrêt de ligne de code][DevtoolsJavascriptBreakpointsLOC] | Concentrez votre curseur sur la ligne, puis sélectionnez `Control`+`B` | Concentrez votre curseur sur la ligne, puis sélectionnez `Command`+`B` |  
| Accéder à un crochet correspondant | `Control`+`M` | `Control`+`M` |  
| Basculez le commentaire d’une seule ligne.  Si plusieurs lignes sont sélectionnées, DevTools ajoute un commentaire au début de chaque ligne | `Control`+`/` | `Command`+`/` |  
| Activer ou désactiver l’occurrence suivante du mot sur le curseur.  Chaque occurrence est mise en surbrillance simultanément | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## <a name="performance-tool-keyboard-shortcuts"></a>Raccourcis clavier de l’outil de performance  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Démarrer/arrêter l’enregistrement | `Control`+`E` | `Command`+`E` |  
| Enregistrer l’enregistrement | `Control`+`S` | `Command`+`S` |  
| Enregistrement du chargement | `Control`+`O` | `Command`+`O` |  

## <a name="memory-tool-keyboard-shortcuts"></a>Raccourcis clavier de l’outil mémoire  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Démarrer/arrêter l’enregistrement | `Control`+`E` | `Command`+`E` |  

## <a name="console-tool-keyboard-shortcuts"></a>Raccourcis clavier de l’outil console  

| Action | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Accepter la suggestion de mise encomplet automatique | `Right Arrow` or `Tab` | `Right Arrow` or `Tab` |  
| Rejeter la suggestion de mise encomplet automatique | `Escape` | `Escape` |  
| Obtenir l’instruction précédente | `Up Arrow` | `Up Arrow` |  
| Obtenir l’instruction suivante | `Down Arrow` | `Down Arrow` |  
| Focus sur la **console** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Effacer la **console** | `Control`+`L` | `Command`+`K` ou `Option`+`L` |  
| Forcer une entrée multi-lignes.  Ce raccourci est principalement inutile, car DevTools doit détecter les scénarios multi-lignes par défaut | `Shift`+`Enter` | `Command`+`Return` |  
| Exécution | `Enter` | `Return` |  
| Développer toutes les sous-catégories d’un objet qui sont enregistrées dans la console | Hold, `Alt` then choose **Expand** \( ![ Expand ](../media/expand-icon.msft.png) \) | Hold, `Alt` then choose **Expand** \( ![ Expand ](../media/expand-icon.msft.png) \) |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Exécuter des commandes avec le menu de commande DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Caisse : personnaliser Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Modifier le placement de DevTools : personnaliser Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Points d’arrêt de ligne de code : comment suspendre votre code avec des points d’arrêt dans Microsoft Edge devTools | Documents Microsoft"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/shortcuts) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  