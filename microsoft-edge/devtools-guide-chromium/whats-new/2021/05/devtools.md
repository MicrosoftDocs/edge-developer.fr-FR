---
description: Bouton Plus d’outils, documentation en contexte pour commencer à utiliser l’extension DevTools, prise en charge accrue des lecteurs d’écran dans la console, etc.
title: Nouveautés de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590857"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Nouveautés de DevTools (Microsoft Edge 92)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> La **conférence Microsoft Build 2021** s’est tenue du 25 au 27 mai.  Voici une vidéo de Build sur les mises à jour de DevTools : [Microsoft Edge | État de la plateforme :][YoutubeEdgeStateOfThePlatform] Microsoft Edge une plateforme attrayante et cohérente avec des outils pour les développeurs.  À mesure que nos navigateurs hérités ne seront plus pris en charge, Edge sera bientôt le seul navigateur pris en charge par Microsoft sur Windows 10.  Rejoignez-nous pour en savoir plus sur la dernière version de la plateforme Edge, des outils et des applications web.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>Le bouton Fermer n’est plus masqué lorsque DevTools est étroit

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

Dans Microsoft Edge version 91 ou antérieure, **** le bouton Fermer pour fermer DevTools n’est pas affiché lorsque la vue DevTools est étroite.  Dans Microsoft Edge version 92, **** le bouton Fermer dans DevTools est toujours présent, quelle que soit la largeur de laport d’affichage DevTools.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Le bouton Fermer DevTools est désormais présent même lorsque la vue est étroite" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   Le **bouton Fermer** DevTools est désormais présent même lorsque la vue est étroite  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Ajouter rapidement des outils avec le nouveau bouton Plus d’outils

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

Il existe une nouvelle façon d’ouvrir d’autres outils dans **** Microsoft Edge DevTools : le menu Plus d’outils `+` (). Le menu **Plus d’outils** apparaît dans la barre d’outils du panneau principal et dans la barre d’outils du panneau. La sélection d’un outil dans le menu **Plus d’outils** l’ajoute à la barre d’outils.

Pour réorder les onglets de l’une ou l’autre barre d’outils, sélectionnez et faites glisser les onglets.  

Le menu **Plus d’outils** était disponible sous la forme d’une expérience Microsoft Edge version 89 et est désormais toujours présent.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Bouton Plus d’outils dans la barre d’outils supérieure et la barre d’outils de caisse" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   Bouton **Plus d’outils** dans la barre d’outils supérieure et la barre d’outils de caisse
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menu Plus d’outils" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   Menu **Plus d’outils**
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Améliorations apportées aux outils de pointage, de sélection et de fermeture

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Les onglets de chaque outil ont été reformatés pour réduire les risques de fermeture accidentelle d’un outil.  Dans chaque onglet de la barre d’outils principale et de la barre d’outils du caisse, nous avons ajouté :
*  Espacement autour de l’onglet.
*  Espacement autour du bouton fermer ( `x` ) dans l’onglet.
*  Couleur d’arrière-plan lorsque vous placez le pointage sur l’onglet.
*  Une boîte à outils pour le bouton fermer ( `x` ) de l’onglet.
*  Contraste plus élevé pour le bouton fermer ( `x` ) de l’onglet.

Par exemple, lorsque vous êtes dans l’outil **Performances** et que vous pointez sur l’onglet de l’outil Réseau, ces améliorations permettent d’éviter la fermeture accidentelle de l’outil Réseau. **** ****

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Onglets avant la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Onglets avant la reformatage :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Onglets après la reformatage" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Onglets après la reformatage :::image-end:::
    :::column-end:::
:::row-end:::

Ces améliorations sont particulièrement pertinentes pour les utilisateurs de DevTools localisées, dans lesquelles les onglets peuvent être plus étroits et plus faciles à fermer accidentellement.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="DevTools localisées avec des onglets étroits" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   DevTools localisées avec des onglets étroits
:::image-end:::

Nous avons également facilité la ré-ajout d’un outil que vous avez fermé en ajoutant un [menu](#add-tools-quickly-with-the-new-more-tools-button) Plus d’outils à la barre d’outils principale et à la barre d’outils des caisses.


## <a name="better-support-for-screen-readers-in-the-console"></a>Meilleure prise en charge des lecteurs d’écran dans la console

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Avant Microsoft Edge version 92, dans la **console,** les technologies d’assistance telles que les lecteurs d’écran n’annoncaient pas les suggestions de mise à jour automatique ou les résultats des expressions évaluées. This has been fixed now.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           Dans la **console,** les lecteurs d’écran annoncent désormais la suggestion de mise à l’écran sélectionnée :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="Dans la console, les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           Dans la **console,** les lecteurs d’écran annoncent désormais le résultat d’une expression évaluée :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Outils de développement Visual Studio Code version 1.1.8

Les [outils Microsoft Edge développeur][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Visual Studio Code version 1.1.8 pour Microsoft Visual Studio Code ont les modifications suivantes depuis la version précédente.  Microsoft Visual Studio Code met automatiquement à jour les extensions.  Pour mettre à jour manuellement la version 1.1.8, accédez à Mettre à jour [une extension manuellement.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

Vous pouvez déposer des problèmes et contribuer à l’extension sur le GitHub [vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Documentation en contexte et interface utilisateur pour faciliter l’utilisation de l’extension DevTools

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

La version 1.1.8 de l’extension [outils][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] de développement Microsoft Edge pour Visual Studio Code offre désormais un moyen plus simple de démarrer une nouvelle instance de Microsoft Edge, en présentant des instructions, des boutons, des liens et une page de documentation pour vous guider.

*  Lorsque vous sélectionnez le bouton **Outils Microsoft Edge** dans la barre d’activité de Visual Studio Code, le panneau **** **Outils Microsoft Edge** : Cibles présente désormais un texte explicatif, des boutons et des liens pour vous guider, au lieu d’un panneau vide.

*  Lorsque vous ouvrez une nouvelle instance de Microsoft Edge à partir de Visual Studio Code, Microsoft Edge affiche désormais une page de démarrage qui explique comment utiliser l’extension Outils de développement, au lieu d’une page vierge.

*  Le **panneau Microsoft Edge Outils** : Cibles possède désormais une launch.jsgénérer une **launch.js** sur le bouton et des instructions, pour vous aider à lancer votre projet pour le débogage dans Microsoft Edge.

Pour plus d’informations, accédez à [Utiliser les outils.][GithubIoDevToolsUsing]


## <a name="download-the-microsoft-edge-preview-channels"></a>Télécharger les canaux d’aperçu Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft][MicrosoftEdgePreviewChannels] Edge comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Utilisation des outils | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux de préversion de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Mettre à jour une extension manuellement - Extension Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils de développement pour Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge : état de la plateforme | YouTube"

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
