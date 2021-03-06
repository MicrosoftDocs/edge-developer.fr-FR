---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, expérimentation
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398678"
---
# <a name="experimental-features"></a>Fonctionnalités expérimentales  

Microsoft Edge DevTools permet d’accéder aux fonctionnalités expérimentales qui sont encore en développement.  Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la publication de chaque fonctionnalité.  

Bien que les fonctionnalités expérimentales soient disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal Canary de Microsoft Edge.  

## <a name="turn-on-experimental-features"></a>Activer les fonctionnalités expérimentales  

Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.  

1.  [Ouvrez DevTools][DevtoolsOpenMain].  
    *   Sélectionnez `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevToolsShortcuts]  
1.  Ouvrez [le volet Paramètres.][DevToolsCustomizeIndexSettings]  
    *   Sélectionnez `Shift` + `?` .  Pour plus d’informations, accédez aux raccourcis clavier de [Microsoft Edge DevTools.][DevToolsShortcuts]  
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

| Fonctionnalité expérimentale | Version de Microsoft Edge |  
|:--- |:--- |  
| [Activer webhint](#enable-webhint) | 85 ou ultérieure |  
| [Activer la console réseau](#enable-network-console) | 85 ou ultérieure |  
| [Visionneuse de commandes source](#source-order-viewer) | 86 ou ultérieure |  
| [Activer l’éditeur de raccourci clavier](#enable-keyboard-shortcut-editor) | 87 ou ultérieure |  
| [Activer les couches composites en vue 3D](#enable-composited-layers-in-3d-view) | 87 ou ultérieure |  
| [Activer le nouvel outil Éditeur de polices dans le volet Styles](#enable-new-font-editor-tool-within-the-styles-pane) | 89 ou ultérieure |  
| [Activer les nouvelles fonctionnalités de débogage Flexbox CSS](#enable-new-css-flexbox-debugging-features) | 89 ou ultérieure |  
| [Activer les menus + onglet de bouton pour ouvrir d’autres outils](#enable--button-tab-menus-to-open-more-tools) | 89 ou ultérieure |  
| [Activer l’onglet Bienvenue](#enable-welcome-tool) | 89 ou ultérieure |  

### <a name="enable-new-css-grid-debugging-features"></a>Activer les nouvelles fonctionnalités de débogage de grille CSS  

Cette fonctionnalité expérimentale fournit un certain nombre de nouvelles visualisations pour vous aider à déboguer les dispositions de grille CSS.  Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activez cette expérience](#turn-on-experimental-features) et rechargez DevTools.  Cette expérience est en cours par défaut dans Microsoft Edge version 87 ou ultérieure.  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a>Affichage des superpositions de grille sur pointage à l’aide de l’outil Inspect  

**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions de grille CSS dans un site web en pointant dessus avec la souris.  Choisissez **l’icône Inspect** \( Inspect \) dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.  Ensuite, pointez sur `Grid` un élément de la page web que vous déboguer.  Les contours sont affichés autour de la grille, et l’inglage indique l’emplacement des espaces vides de la grille s’il est présent.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Affichage des grilles à l’aide de l’outil Inspect" lightbox="../media/grid-inspect.msft.png":::
   Affichage des grilles à l’aide de **l’outil Inspect**  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a>Affichage des superpositions de grilles persistantes  

Dans Microsoft Edge version 86 ou ultérieure, la fonctionnalité de grille CSS expérimentale offre également la possibilité d’activer les superpositions de grille persistantes.  Les superpositions persistantes offrent plusieurs avantages.  

*   Les superpositions persistantes restent visibles sur la page lorsque vous faites défiler, déplacez votre souris et utilisez d’autres fonctionnalités de DevTools.  
*   Plusieurs superpositions persistantes peuvent être allumées en même temps, ce qui vous permet de passer en revue plusieurs dispositions de grille à la fois.  
*   Les superpositions persistantes offrent de nombreuses options de configuration, telles que le masquage ou l’affichage de noms dans la zone de grille, les intervalles de grille, les tailles de suivi, etc.  
    
Les deux façons de faire basculer une superposition de grille persistante.  

*   Choisissez **l’icône ovale Grid** en face de tout élément Grid affiché dans l’arborescence DOM de **l’outil Elements.**  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icône Ovale de grille dans l’outil Éléments" lightbox="../media/grid-adorner.msft.png":::
       Icône Ovale de grille dans **l’outil Éléments**  
    :::image-end:::  
    
*   Ouvrez le nouveau **panneau de** disposition situé dans l’outil Éléments, puis cochez la case en regard de chaque élément Grid que vous souhaitez mettre en surbrillez.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panneau de disposition dans DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Panneau** de disposition dans DevTools  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a>Configuration des superpositions persistantes  

Dans Microsoft Edge version 86 **** ou ultérieure, le nouveau panneau de disposition se trouve dans l’outil **Éléments** avec les panneaux **Styles** **et** Calculés.  Le **panneau de** disposition offre des options de configuration pour les superpositions persistantes.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="../media/experiments-grid.msft.png":::
   Fonctionnalité de débogage de grille CSS  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a>Activer la prise en charge du déplacement des onglets entre les panneaux  

Normalement, les outils **** tels que **Éléments** et Réseau ne peuvent s’ouvrir que dans le panneau principal situé en haut de DevTools.  Des **outils** **tels que l’affichage 3D** et les problèmes qui s’ouvrent normalement uniquement dans le panneau de caisse situé en bas de DevTools. ****  Après avoir choisi l’expérience, vous pouvez déplacer les outils entre les panneaux supérieur et inférieur.  Pour déplacer un outil, pointez sur l’onglet, ouvrez le **** menu contextuel \(clic droit\), puis choisissez Déplacer vers le haut ou Vers **le bas.**   Cette expérience vous permet de personnaliser votre disposition DevTools.  Pour afficher ou masquer le **panneau de caisse,** sélectionnez `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Déplacement d’outils entre des panneaux" lightbox="../media/experiments-move-panels.msft.png":::
   Déplacement d’outils entre des panneaux  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a>Activer webhint  

[webhint est][WebhintMain] un outil open source qui fournit des commentaires en temps réel pour les sites web et les pages web locales.  Type de commentaires fourni par [webhint][WebhintMain].  

*   accessibilité  
*   compatibilité entre navigateurs  
*   sécurité  
*   performance  
*   Applications web progressives (P.A.S.)  
*   autres problèmes courants de développement web  
    
[L’expérience webhint][WebhintMain] affiche les commentaires sur le web dans le [panneau Problèmes.][DevtoolsIssues]  Choisissez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site web.  Choisissez un lien de ressource pour ouvrir **** le volet **Réseau,** **Sources**ou Éléments approprié dans DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../media/experiments-webhint.msft.png":::
   commentaires webhint dans le **panneau Problèmes**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a>Activer la console réseau  

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

### <a name="source-order-viewer"></a>Visionneuse de commandes source  

**L’Afficheur des** commandes source est une expérience qui affiche l’ordre des éléments dans la source de la page web.  L’ordre d’affichage à l’écran peut différer de l’ordre de la source, ce qui peut dérouter les utilisateurs du lecteur d’écran et du clavier.  Utilisez **l’expérience de l’Afficheur** des commandes source pour rechercher les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.  

Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser **l’Observateur de commandes source,** complétez les étapes suivantes.  

1.  Ouvrez **l’outil Éléments.**  
1.  Ouvrez **le volet Accessibilité** dans le panneau de caisse \(bas\).  
1.  Sous la section **Visionneuse de commandes** source, cochez la case Afficher la **commande source.**  
1.  Mettez en surbrillez n’importe quel élément HTML pour afficher une superposition que l’ordre dans la source de la page web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet Accessibilité" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Visionneuse de commandes source** dans **le volet** Accessibilité  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a>Activer l’éditeur de raccourci clavier

Une fois **l’expérience** d’éditeur de raccourci clavier activée, vous pouvez personnaliser les raccourcis clavier pour toute action dans DevTools.  Pour personnaliser le raccourci clavier pour une action spécifique, complétez les étapes suivantes.  

1.  [Ouvrez DevTools][DevtoolsOpenMain].  
1.  Ouvrez [Paramètres.][DevToolsCustomizeIndexSettings]  
    *   Sélectionnez `Shift` + `?` .  
1.  Accédez à la page **Raccourcis.**  
1.  Choisissez l’action que vous souhaitez personnaliser.  
1.  Sélectionnez **l’icône** Modifier \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Choisir l’action à personnaliser à partir de la page Raccourcis dans Paramètres" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Choisir l’action à personnaliser à partir de la page **Raccourcis** dans [Paramètres][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  Sur le clavier, sélectionnez les touches à lier à l’action.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Choisissez les clés que vous souhaitez affecter à l’action" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Choisissez les clés que vous souhaitez affecter à l’action  
    :::image-end:::  
    
1.  Pour enregistrer votre nouveau raccourci clavier, sélectionnez la coche \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) icône.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Sélectionnez l’icône de coche pour enregistrer votre nouveau raccourci clavier" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Sélectionnez l’icône de coche pour enregistrer votre nouveau raccourci clavier  
    :::image-end:::  
    
1.  Sélectionnez votre nouveau raccourci clavier pour déclencher l’action dans DevTools.  
    
Dans la page **Raccourcis,** l’icône Raccourci clavier personnalisé **\(** ![ CustomKeyboardShortcut \) affiche les raccourcis clavier que vous ](../media/custom-keyboard-shortcut-icon.msft.png) avez personnalisés.  Pour réinitialiser tous les raccourcis, **sélectionnez Restaurer les raccourcis par défaut.**  

Pour ignorer vos modifications pendant que vous modifiez les raccourcis clavier d’une action, choisissez l’icône X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Pour supprimer les raccourcis d’une action spécifique, sélectionnez l’icône Supprimer le **raccourci** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  Pour ajouter plusieurs raccourcis pour une action, choisissez **Ajouter un raccourci.**  

> [!NOTE]
> Si un raccourci clavier est actuellement affecté à une autre action, il se peut que vous ne l’enregistrez pas pour une nouvelle action.  Vous devez d’abord supprimer le raccourci clavier de l’action précédente, puis l’ajouter à la nouvelle action.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a>Activer les couches composites en vue 3D  

Vous pouvez maintenant visualiser calques avec les index z et le modèle objet de document \(DOM\).  Cette fonctionnalité vous permet de déboguer sans changer de contexte aussi souvent.  Vous avez identifié que la réduction du basculement de contexte était un problème majeur.  Il n’est pas toujours clair comment le code que vous écrivez affecte votre application web.  Pour une expérience complète de débogage, l’affichage 3D et les couches composites sont désormais combinés.  

Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser **les couches composites,** complétez les étapes suivantes.  

1.  Dans le caisse, choisissez **l’outil d’affichage 3D.**  
1.  Ouvrez **le volet Calques composites.**  
1.  Toutes les couches peints de l’application sont affichées.  Essayez cette fonctionnalité avec vos propres applications web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../media/experiments-layers.msft.png":::
   Volet des **couches composites**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a>Activer le nouvel outil Éditeur de polices dans le volet Styles  

Vous pouvez désormais utiliser le nouvel éditeur de [polices][DevtoolsInspectStylesEditFonts] visuel pour modifier les polices.  Utilisez-la pour définir les polices et les caractéristiques de police.  Visual **Font Editor vous** aide à effectuer les actions suivantes.  

*   Basculer entre les unités pour différentes propriétés de police  
*   Basculer entre les mots clés pour différentes propriétés de police  
*   Convertir des unités  
*   Générer un code CSS précis  
    
Après avoir activer l’expérience, assurez-vous de redémarrer de DevTools.  Pour utiliser le nouvel éditeur de **polices**visuel, complétez les étapes suivantes.  

1.  Ouvrez **l’outil Éléments.**  
1.  Ouvrez **le volet Styles.**  
1.  Sélectionnez **l’icône Éditeur de** polices.  
    
Pour plus d’informations sur le nouvel éditeur de **polices**visuel, accédez à Modifier les styles de police CSS et les paramètres dans le volet Styles dans [DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Le volet Visual Font Editor est mis en surbrill" lightbox="../media/font-editor-open.msft.png":::
   Le volet **Visual Font Editor** est mis en surbrill  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a>Activer les nouvelles fonctionnalités de débogage Flexbox CSS  

Cette fonctionnalité expérimentale fournit de nombreuses nouvelles visualisations pour vous aider à déboguer les dispositions flexbox CSS.  Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activer cette expérience](#turn-on-experimental-features) et recharger DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Afficher des superpositions persistantes sur les dispositions Flexbox à l’aide de l’outil Inspect  

**L’outil Inspect** permet d’identifier et de visualiser rapidement les dispositions flexbox CSS dans un site web en pointant dessus avec la souris.  Choisissez **l’icône Inspect** \( Inspect \) dans le coin supérieur gauche ![ de ](../media/inspect-icon.msft.png) DevTools.  Ensuite, lors du débogage du site web, pointez sur un conteneur flexible pour afficher les contours autour du conteneur flexible.  

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

Pour configurer les options des superpositions persistantes pour les grilles CSS ou les dispositions Flexbox, utilisez **le** volet De disposition.  Le **volet** Disposition se trouve dans l’outil **Éléments** en côté des **volets Styles** **et** Calculés.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panneau de disposition" lightbox="../media/flexbox-layout.msft.png":::
   Panneau de disposition  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a>Activer les menus + onglet de bouton pour ouvrir d’autres outils  

Vous pouvez maintenant ouvrir d’autres outils à l’aide de la nouvelle icône **Plus d’outils** `+` \( \).  Une fois que vous avez activé les menus Onglet Activer **+** bouton pour ouvrir d’autres outils et recharger DevTools, un signe plus \( \) s’affiche à droite du groupe d’onglets en haut de `+` DevTools.  Pour afficher la liste des autres outils que vous pouvez ajouter à la barre d’onglets, choisissez la nouvelle icône Outils plus **\(** `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Autres outils dans le volet supérieur" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Autres outils** dans le volet supérieur
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a>Activer l’outil d’accueil

Cette expérience remplace **l’outil Nouveautés** par le nouvel **outil Welcome.**  Il affiche une conception actualisée pour le contenu suivant.  

*   Liens vers des documents de développement  
*   fonctionnalités les plus récentes  
*   notes de publication  
*   Option de contact de l’équipe Microsoft Edge DevTools  
    
**L’outil** Welcome s’ouvre automatiquement après chaque mise à jour de Microsoft Edge.  Pour empêcher l’affichage de l’outil **Welcome** après **** chaque mise à jour, cochez la case en regard de l’onglet Ouvrir après chaque mise à jour sous le titre de **l’outil** Welcome.  

Si vous préférez **l’outil Nouveautés d’origine,** accédez à [Expériences][DevtoolsCustomizeIndexSettings]de paramètres et supprimez la case à cocher en regard de l’onglet  >  **** **Activer l’accueil.**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Outil d’accueil" lightbox="../media/experiments-welcome.msft.png":::
   **Outil d’accueil**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Fonctionnalités expérimentales précédentes  

*   [L’affichage 3D][Devtools3dViewIndex] est désormais disponible et est allumé par défaut dans Microsoft Edge version 83 ou ultérieure.  
*   [Activer la prise en charge pour déplacer des onglets][DevtoolsMoveTabs] entre les panneaux est désormais disponible et est désactivée par défaut dans Microsoft Edge version 85 ou ultérieure.  
*   [Personnaliser les raccourcis clavier][DevtoolsCustomKeyboardShortcuts] est désormais disponible et est allumé par défaut dans Microsoft Edge version 86 ou ultérieure.  
*   [Émulation : le mode double écran][DevtoolsDeviceModeDualScreenAndFoldables] de prise en charge est désormais disponible et est allumé par défaut dans Microsoft Edge version 89 ou ultérieure.  
*   [Activer les nouvelles fonctionnalités][DevtoolsCssGrid] de débogage de grille CSS est désormais disponible et est désactivé par défaut dans Microsoft Edge version 89 ou ultérieure.  
    
## <a name="providing-feedback-on-experimental-features"></a>Commentaires sur les fonctionnalités expérimentales  

Pour fournir des commentaires sur les expériences DevTools de Microsoft Edge ou sur tout autre point lié à DevTools.  

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

[Devtools3dViewIndex]: ../3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevtoolsCssGrid]: ../css/grid.md "Inspect CSS Grid in Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsMoveTabs]: ../customize/index.md "Personnaliser microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles de DevTools | Documents Microsoft"  
[DevtoolsIssues]: ../issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsShortcuts]: ../shortcuts/index.md "Raccourcis clavier Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personnaliser les raccourcis clavier dans la | Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsOpenMain]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Expériences web à double écran | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools | Documents Microsoft"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
