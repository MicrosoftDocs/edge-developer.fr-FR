---
description: Les dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, expérimentation
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: 82d547c8c1ed0606bda9ade27d0dbddbfa2ca800
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11596998"
---
# <a name="experimental-features"></a>Fonctionnalités expérimentales  

Microsoft Edge DevTools permet d’accéder aux fonctionnalités expérimentales qui sont encore en développement.  Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la publication de chaque fonctionnalité.  

Bien que les fonctionnalités expérimentales soient disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide canal Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Activer les fonctionnalités expérimentales  

Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.  

1.  [Ouvrez DevTools][DevtoolsOpenIndex].  
    *   Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  
1.  Ouvrez [Paramètres][DevToolsCustomizeIndexSettings] volet.  
    *   Sélectionnez `Shift` + `?` .  Pour plus d’informations, [accédez Microsoft Edge raccourcis clavier DevTools.][DevtoolsShortcutsIndex]  
1.  Sur le côté gauche du volet **Paramètres,** choisissez la section **Expériences.**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Page Expériences dans Paramètres" lightbox="../media/experiments-devtools.msft.png":::
       Page **Expériences** dans **Paramètres**  
    :::image-end:::  
    
1.  Dans la page **Expériences,** parcourez la liste de toutes les fonctionnalités expérimentales disponibles et cochez la case en regard de chaque fonctionnalité à tester.  
1.  Fermez et rouvrez Microsoft Edge DevTools.  
    
> [!NOTE]
> Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.  Pour désactiver une fonctionnalité expérimentale, ouvrez la page **Expériences** et cochez la case de la fonctionnalité expérimentale que vous souhaitez désactiver.  

## <a name="highlighted-experimental-features"></a>Fonctionnalités expérimentales mises en évidence  

Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.  

| Fonctionnalité expérimentale | Microsoft Edge version |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | 85 ou ultérieure |  
| [Enable Network Console](#enable-network-console) | 85 ou ultérieure |  
| [Source Order Viewer](#source-order-viewer) | 86 ou ultérieure |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | 87 ou ultérieure |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | 89 ou ultérieure |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | 89 ou ultérieure |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | 89 ou ultérieure |  
| [Enable Welcome tab](#enable-welcome-tab) | 89 ou ultérieure |  

### Enable webhint  

[webhint est][WebhintMain] un outil open source qui fournit des commentaires en temps réel pour les sites web et les pages web locales.  Type de commentaires fourni par [webhint][WebhintMain].  

*   accessibilité  
*   compatibilité entre navigateurs  
*   sécurité  
*   performance  
*   Applications web progressives (P.A.S.)  
*   autres problèmes courants de développement web  
    
[L’expérience webhint][WebhintMain] affiche les commentaires sur le web dans le [panneau Problèmes.][DevtoolsIssuesIndex]  Choisissez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site web.  Choisissez un lien de ressource pour ouvrir **** le volet **Réseau,** **Sources**ou Éléments approprié dans DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../media/experiments-webhint.msft.png":::
   commentaires webhint dans le **panneau Problèmes**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

**Network Console est** le titre de travail d’une expérience pour effectuer des demandes de réseau synthétiques sur HTTP.  Vous pouvez utiliser l’expérience **console** réseau pour envoyer des demandes d’API web.  

Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser la **console réseau,** complétez les étapes suivantes.  

1.  Ouvrez **le volet** Réseau.  
1.  Recherchez la demande réseau que vous souhaitez modifier et renvoyer.  
1.  Ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**  
1.  Lorsque la **console réseau s’ouvre,** modifiez les informations de demande réseau.  
1.  Choose **Send**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console réseau dans le caisse de la console" lightbox="../media/network-network-console.msft.png":::
   **Console réseau dans** le caisse **de la** console  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

**Source Order Viewer** est une expérience qui affiche l’ordre des éléments dans la source de la page web.  L’ordre d’affichage à l’écran peut différer de l’ordre de la source, ce qui peut dérouter les utilisateurs du lecteur d’écran et du clavier.  Utilisez l’expérience pour rechercher les différences entre l’ordre d’affichage à l’écran **Source Order Viewer** et l’ordre de la source.  

Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser **Source Order Viewer** , complétez les étapes suivantes.  

1.  Ouvrez **l’outil Éléments.**  
1.  À droite de l’onglet **Styles,** sélectionnez **l’onglet** Accessibilité.  
1.  Sous la **Source Order Viewer** section, cochez **la case Afficher** la commande source.  
1.  Mettez en surbrillez n’importe quel élément HTML pour afficher une superposition que l’ordre dans la source de la page web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer) ::: in the Accessibility pane» lightbox=».. /media/experiments-source-order-viewer.msft.png»::: dans le volet **:::no-loc(Source Order Viewer** Accessibilité ****  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

Vous pouvez maintenant visualiser calques avec les index z et le modèle objet de document \(DOM\).  Cette fonctionnalité vous permet de déboguer sans changer de contexte aussi souvent.  Vous avez identifié que la réduction du basculement de contexte était un problème majeur.  Il n’est pas toujours évident de savoir comment le code que vous écrivez affecte votre application web.  Pour une expérience de débogage visuel complète, les couches composites et les couches 3D View composites sont désormais combinées.  

Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser **les couches composites,** complétez les étapes suivantes.  

1.  Dans le caisse, choisissez **3D View** l’outil.  
1.  Ouvrez **le volet Calques composites.**  
1.  Toutes les couches peints de l’application sont affichées.  Essayez cette fonctionnalité avec vos propres applications web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../media/experiments-layers.msft.png":::
   Volet des **couches composites**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

Vous pouvez désormais utiliser le nouvel éditeur de [polices][DevtoolsInspectStylesEditFonts] visuel pour modifier les polices.  Utilisez-la pour définir les polices et les caractéristiques de police.  Visual **Font Editor vous** aide à effectuer les actions suivantes.  

*   Basculer entre les unités concernant différentes propriétés de police  
*   Basculer entre les mots clés de différentes propriétés de police  
*   Convertir des unités  
*   Générer un code CSS précis  
    
Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser le nouvel éditeur de **polices**visuel, complétez les étapes suivantes.  

1.  Ouvrez **l’outil Éléments.**  
1.  Ouvrez **le volet Styles.**  
1.  Sélectionnez **l’icône Éditeur de** polices.  
    
Pour plus d’informations sur le nouvel éditeur de polices **visuel,** accédez à Modifier les styles de police CSS et les paramètres dans le volet Styles dans [DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Le volet Visual Font Editor est mis en surbrill" lightbox="../media/font-editor-open.msft.png":::
   Le volet **Visual Font Editor** est mis en surbrill  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

Cette fonctionnalité expérimentale fournit de nombreuses nouvelles visualisations pour vous aider à déboguer les dispositions flexbox CSS.  Pour afficher un aperçu des dernières fonctionnalités expérimentales, [allumez cette expérience](#turn-on-experimental-features) et rechargez DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Afficher des superpositions persistantes sur les dispositions Flexbox à l’aide de l’outil Inspect  

**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions flexbox CSS dans un site web en pointant dessus avec la souris.  Choisissez **l’icône Inspect** \( Inspect \) dans le ![ coin supérieur gauche de ](../media/inspect-icon.msft.png) DevTools.  Ensuite, lors du débogage du site web, pointez sur un conteneur flexible pour afficher les contours autour du conteneur flexible.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Afficher les conteneurs Flexbox avec l’outil Inspect" lightbox="../media/flexbox-hover.msft.png":::
   Afficher les conteneurs Flexbox avec **l’outil Inspect**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Afficher des superpositions persistantes sur les dispositions Flexbox  

Dans Microsoft Edge version 89 ou ultérieure, la fonctionnalité expérimentale CSS Flexbox offre également la possibilité d’activer les superpositions persistantes sur les dispositions Flexbox.  Les superpositions persistantes offrent les avantages suivants.  

*   Les superpositions persistantes restent visibles sur la page web lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.
*   Plusieurs superpositions persistantes peuvent être utilisées en même temps, pour vous permettre de passer en revue plusieurs dispositions Flexbox à la fois.  
*   Les superpositions persistantes offrent des options de configuration des couleurs.  
    
Pour faire bascule les superpositions persistantes sur la disposition Flexbox, utilisez l’une des actions suivantes.  

*   Choisissez **l’icône ovale Flexbox** en face de n’importe quel conteneur Flexbox affiché dans l’arborescence DOM de **l’outil Elements.**  
*   Ouvrez le nouveau **panneau de** disposition situé dans l’outil **Éléments,** puis cochez la case en regard de chaque conteneur Flexbox à mettre en surbrillion.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Icônes flexibles et panneau de disposition dans DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Icônes flexibles et **panneau de** disposition dans DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Configurer des superpositions persistantes  

Pour configurer les options des superpositions persistantes pour les grilles CSS ou les dispositions Flexbox, utilisez **le** volet Disposition.  Le **volet** Disposition se trouve dans l’outil **Éléments** en plus des **volets Styles** **et** Calculés.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panneau de disposition" lightbox="../media/flexbox-layout.msft.png":::
   Panneau de disposition  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

Vous pouvez maintenant ouvrir d’autres outils à l’aide de la nouvelle icône **Plus d’outils** `+` \( \).  Une fois que vous avez turn on the experiment and reload DevTools, un signe plus \( \) s’affiche à droite du groupe d’onglets en haut de **Enable + button tab menus to open more tools** `+` DevTools.  Pour afficher la liste des autres outils que vous pouvez ajouter à la barre d’onglets, choisissez la nouvelle icône Outils plus **\(** `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Autres outils dans le volet supérieur" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Autres outils** dans le volet supérieur
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

Cette expérience remplace **l’outil Nouveautés** par le nouvel outil **Welcome.**  Il affiche une conception actualisée pour le contenu suivant.  

*   Liens vers des documents de développement  
*   fonctionnalités les plus récentes  
*   notes de publication  
*   Option pour contacter l’Microsoft Edge devTools  
    
**L’outil** Welcome s’ouvre automatiquement après chaque mise à jour Microsoft Edge.  Pour empêcher l’affichage de l’outil **d’accueil** **** après chaque mise à jour, cochez la case en regard de l’onglet Ouvrir après chaque mise à jour sous le titre de **l’outil** d’accueil.  

Si vous préférez **l’outil Nouveautés d’origine,** accédez [à Paramètres][DevtoolsCustomizeIndexSettings]Expériences et supprimez la case à cocher en  >  **** regard **Enable Welcome tab** de .  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Outil d’accueil" lightbox="../media/experiments-welcome.msft.png":::
   **Outil d’accueil**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Fonctionnalités expérimentales précédentes  

*   [3D View][Devtools3dViewIndex]est désormais disponible et est allumé par défaut dans Microsoft Edge version 83 ou ultérieure.  
*   [Turn on support to move tabs between panels][DevtoolsCustomizeIndex]est désormais disponible et est allumé par défaut dans Microsoft Edge version 85 ou ultérieure.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]est désormais disponible et est allumé par défaut dans Microsoft Edge version 86 ou ultérieure.  
*   [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.  
*   [Turn on new CSS grid debugging features][DevtoolsCssGrid]est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.  
*   [Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables]est désormais disponible et est allumé par défaut dans Microsoft Edge version 90 ou ultérieure.  

## <a name="providing-feedback-on-experimental-features"></a>Commentaires sur les fonctionnalités expérimentales  

Pour fournir des commentaires sur Microsoft Edge expériences DevTools ou sur tout autre sujet lié à DevTools.  

*   Envoyez vos commentaires à l’aide **de l’icône** Envoyer des commentaires dans DevTools  
*   Tweet à [l'@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="L’Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   L’Icône **Envoyer des commentaires** dans Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "3D View | Documents Microsoft"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personnalisez Microsoft Edge devTools | Documents Microsoft"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Paramètres - Personnaliser Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edit keyboard shortcuts for any action in the DevTools | Documents Microsoft"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Documents Microsoft"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode Microsoft Edge devTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Raccourcis clavier DevTools | Documents Microsoft"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
