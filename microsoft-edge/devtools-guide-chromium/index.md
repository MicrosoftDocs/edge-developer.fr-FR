---
description: Découvrir les outils de développement Microsoft Edge (Chromium)
title: Vue d’ensemble des outils de développement Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3d91b0754f84579d770940503cf4a252e3926416
ms.sourcegitcommit: fa8bedfc83fbd1c4ce7bda8c69586c4f24007beb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11481409"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Vue d’ensemble des outils de développement Microsoft Edge (Chromium)  

Lorsque vous installez Microsoft Edge, vous obtenez un navigateur. En outre, vous obtenez un moyen puissant pour inspecter, déboguer et même créer des projets web.  Les outils de développement livrés avec le navigateur sont basés sur les outils du projet open source Chromium. Vous êtes donc peut-être déjà familiarisé avec les outils.  Pour que les descriptions soient plus courtes dans cet article, les descriptions sont désormais `Microsoft Edge Developer Tools` appelées `DevTools` .  

Utilisez DevTools pour passer en revue et en savoir plus sur les tâches de développement suivantes.  

*   [Inspectez et modifiez la page web actuelle en][DevtoolsGuideDomIndex] direct dans le navigateur.  
*   [Émuler le comportement de votre produit sur différents appareils][DevtoolsGuideDeviceModeIndex] et simuler un environnement mobile avec différentes conditions réseau.  
*   [Inspectez, ajustez et modifiez les styles][DevtoolsGuideInspectStylesEditFonts] des éléments de la page web à l’aide d’outils en direct avec une interface visuelle.  
*   [Déboguer votre javaScript à l’aide][DevtoolsGuideJavascriptIndex] du débogage de point d’arrêt et avec la [console en direct][DevtoolsGuideConsoleIndex].  
*   Recherchez les problèmes d’accessibilité, de [performances,][DevtoolsGuideIssuesIndex] de compatibilité et de sécurité dans vos produits et découvrez comment utiliser DevTools pour résoudre chacun d’eux.  
*   [Inspectez le trafic réseau et][DevtoolsGuideNetworkIndex] examinez l’emplacement des problèmes.  
*   [Inspectez l’endroit où le navigateur stockait le contenu][DevtoolsGuideStorageSessionstorage] dans différents formats.  
*   [Évaluez les performances][DevtoolsGuideEvaluatePerformanceIndex] de votre produit pour rechercher les [problèmes de mémoire][DevtoolsGuideMemoryProblemsIndex] et de [rendu.][DevtoolsGuideRenderingToolsIndex]  
*   [Utilisez un environnement de développement][DevtoolsGuideSourcesIndex] pour synchroniser les modifications dans [DevTools][DevtoolsGuideWorkspacesIndex] avec le système de fichiers et remplacer les fichiers [à][DevtoolsGuideJavascriptOverrides] partir du web.  
    
<!-- Is the link meant to be local or session storage for "inspect where the browser stored content"? -->  

Et bien plus encore.  Tout commence lorsque vous ouvrez DevTools et personnalisez chaque outil en vous adaptant à vos besoins.  

## <a name="open-the-devtools"></a>Ouvrez DevTools  

Pour ouvrir et explorer DevTools, utilisez l’une des actions suivantes.  

*   Pointez sur n’importe quel élément de la page web, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  Cette action ouvre **l’outil Éléments.**  
*   Sélectionnez `F12` .  
*   Sélectionnez `Ctrl` + `Shift` + `I` sur Windows/Linux `Command` + `Option` + `I` ou sur macOS.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect.msft.png" alt-text="Choose Inspect from the contextual menu on any element" lightbox="./media/devtools-intro-inspect.msft.png":::  
         Choose **Inspect** from the contextual menu on any element  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect-devtools-open.png" alt-text="DevTools s’ouvre avec l’élément choisi mis en surbrill" lightbox="./media/devtools-intro-inspect-devtools-open.png":::  
         DevTools s’ouvre avec l’élément choisi mis en surbrill  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

Il existe deux façons principales d’interagir avec les DevTools.
*   Utiliser la souris  
*   [Raccourcis clavier.][DevtoolsGuideShortcutsIndex]  Les raccourcis clavier offrent un moyen rapide d’accéder aux fonctionnalités et sont nécessaires pour l’accessibilité.  L’équipe Microsoft Edge DevTools travaille dur pour rendre tous les outils disponibles à l’aide du clavier et des technologies d’assistance telles que les lecteurs d’écran.  Pour plus d’informations sur l’ouverture des différentes fonctionnalités dans DevTools, accédez aux raccourcis clavier [de Microsoft Edge DevTools.][DevtoolsGuideOpenIndex]  

## <a name="dock-the-devtools-in-your-browser"></a>Ancrer les DevTools dans votre navigateur  

Lorsque vous ouvrez DevTools, il s’ancre à gauche de votre navigateur.  Pour modifier l’emplacement d’accueil des DevTools, effectuer les actions suivantes.  

1.  Choisissez le **bouton Personnaliser et contrôler DevTools** \( `...` \).  
1.  À droite de **Placement des DevTools** par rapport à la page \(**Dock side**\), choisissez une option côté station **d’accueil.**  
    
Pour plus d’informations, accédez à Modifier le [placement de Microsoft Edge DevTools (Undock, Dock To Bottom, Dock To Left)][DevtoolsGuideCustomizePlacement].  

:::image type="complex" source="./media/devtools-intro-docking-menu.msft.png" alt-text="Capture d’écran du menu côté station d’accueil dans DevTools" lightbox="./media/devtools-intro-docking-menu.msft.png":::  
   Capture d’écran du menu côté station d’accueil dans DevTools  
:::image-end:::  

Dans **dock side**, choisissez l’une des options de disposition suivantes.  

*   **Désédock dans une fenêtre distincte**.   Vous aide à travailler avec plusieurs moniteurs ou si vous avez besoin de travailler sur une application en plein écran.  
*   **Station d’accueil vers la** gauche **ou station d’accueil à droite.**  Vous aide à maintenir DevTools côte à côte avec votre produit web et est excellent lorsque vous émulez des appareils mobiles.  Les **options** **Station d’accueil vers la** gauche et Station d’accueil vers la droite fonctionnent mieux avec les affichages haute résolution.  Pour plus d’informations sur les appareils d’émulation, accédez à Émuler les appareils mobiles dans [Microsoft Edge DevTools.][DevtoolsGuideDeviceModeIndex]  
*   **Station d’accueil en bas**.  Vous aide lorsque vous n’avez pas suffisamment d’espace d’affichage horizontal ou que vous souhaitez déboguer du texte long dans le DOM ou la **console**.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-docking-left.msft.png" alt-text="Choisir Station d’accueil vers la gauche" lightbox="./media/devtools-intro-docking-left.msft.png":::  
         Choisir **Station d’accueil vers la gauche**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-bottom.msft.png" alt-text="Choose Dock To Bottom" lightbox="media/devtools-intro-docking-bottom.msft.png":::  
         Choose **Dock to Bottom**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  
:::row:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-right.msft.png" alt-text="Choose Dock To Right" lightbox="media/devtools-intro-docking-right.msft.png":::  
         Choose **Dock To Right**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-own-window.msft.png" alt-text="Choose Undock into separate window" lightbox="media/devtools-intro-docking-own-window.msft.png":::  
         Choose **Undock into separate window**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="learn-about-the-core-tools"></a>En savoir plus sur les outils de base  

DevTools vous offre une quantité incroyable d’énergie pour inspecter, déboguer et modifier le produit web actuellement affiché dans le navigateur.  La plupart des outils affichent les modifications en direct.  Les mises à jour en direct rendent les outils extrêmement utiles pour affiner l’apparence et la navigation ou les fonctionnalités d’un projet web sans avoir besoin de l’actualiser ou de le créer.  DevTools vous permet également de modifier des produits tiers basés sur le web sur votre ordinateur.  

DevTools a été développé sur une période de plusieurs années.  Vous pouvez supposer que DevTools est difficile à apprendre lorsque vous ouvrez pour la première fois l’un des outils.  Le texte suivant présente rapidement les différentes parties.  La barre d’outils principale vous propose quelques sections et les sections sont commandés de gauche à droite.  

:::image type="complex" source="./media/devtools-intro-menu-bar.msft.png" alt-text="Capture d’écran de la barre de menus de DevTools avec des étiquettes expliquant les différentes sections.  Dans l’ordre : Inspect Tool, Device Emulation tool, Tools tab group, JavaScript errors, Issues, Settings, Feedback, Customize, and Close." lightbox="./media/devtools-intro-menu-bar.msft.png":::  
   Capture d’écran de la barre de menus de DevTools avec des étiquettes expliquant les différentes sections.  Dans l’ordre : Inspect Tool, Device Emulation tool, Tools tab group, JavaScript Errors, Issues, Settings, Feedback, Customize, and Close.  
:::image-end:::  

*   L’outil Inspect vous permet de choisir un élément sur la page web actuelle.  Après l’avoir activé, vous pouvez déplacer votre souris sur différentes parties de la page web pour obtenir des informations détaillées sur l’élément et une superposition de couleurs pour afficher les dimensions, l’remplissage et la marge.  
    
    :::image type="complex" source="./media/devtools-intro-inspect-tool.msft.png" alt-text="Capture d’écran de l’outil Inspect avec le premier titre de cet article sélectionné" lightbox="./media/devtools-intro-inspect-tool.msft.png":::  
       Capture d’écran de l’outil d’inspection avec le premier titre de cet article sélectionné  
    :::image-end:::  
    
*   [L’outil Device Emulation][DevtoolsGuideDeviceModeIndex] affiche le produit web actuel en mode appareil émulé.  **L’outil Device Emulation** vous permet d’exécuter et de tester la façon dont votre produit réagit lorsque vous reizez le navigateur.  Il vous donne également une estimation de la disposition et du comportement sur un appareil mobile.  
    
    :::image type="complex" source="./media/devtools-intro-device-emulation.msft.png" alt-text="Capture d’écran de l’affichage DevTools de cet article sur un téléphone mobile émulé" lightbox="./media/devtools-intro-device-emulation.msft.png":::  
       Capture d’écran de l’affichage DevTools de cet article sur un téléphone mobile émulé  
    :::image-end:::  
    
*   Le groupe d’onglets Outils est un groupe d’onglets qui représentent différents outils utilisés dans différents scénarios.  Vous pouvez personnaliser chacun des outils et chaque outil peut changer en fonction du contexte.  Pour ouvrir un menu déroulant de plus d’outils, choisissez le bouton **Plus d’onglets** \( `>>` \).  Chacun des outils est présenté plus loin dans la section suivante.  
*   En plus du groupe d’onglets Outils, des raccourcis d’erreur et de problèmes sont facultatifs.  Les raccourcis s’affichent lorsque des erreurs ou des problèmes JavaScript se produisent sur la page web actuelle.  Le bouton Ouvrir la console pour afficher **les erreurs #, # avertissements** \(**Erreurs JavaScript**\) affiche un cercle rouge suivi du nombre d’erreurs `X` JavaScript.  Pour ouvrir la [console et][DevtoolsGuideConsoleIndex] en savoir plus sur l’erreur, sélectionnez le **bouton Erreurs JavaScript.**  Le **bouton Ouvrir les problèmes pour afficher # problèmes** \(**Problèmes**\) est une icône de message bleue suivie du nombre de problèmes.  Pour ouvrir [l’outil Problèmes,][DevtoolsGuideIssuesIndex] choisissez **le bouton** Problèmes.  
*   Le **bouton Paramètres** affiche une icône d’engrenage.  Pour ouvrir la page web **Paramètres** de DevTools, sélectionnez **le bouton Paramètres.**  La page web **Paramètres** affiche un menu pour modifier les **préférences,** activer les **expériences**et bien plus encore.  
*   Le **bouton Envoyer des commentaires** s’affiche avec une bulle de conversation à côté de celui-ci.  Pour ouvrir la boîte **de dialogue Envoyer des** commentaires, sélectionnez le bouton Envoyer **des** commentaires.  La **boîte de dialogue Envoyer** des commentaires vous permet d’entrer des informations pour décrire ce qui s’est passé et inclut automatiquement une capture d’écran.  Utilisez-le pour vous connecter avec l’équipe DevTools afin de signaler des problèmes, des problèmes ou des suggestions d’idées.  
*   Le **bouton Personnaliser et contrôler Devtools** \( `...` \) ouvre un menu déroulant.  Il vous permet de définir où ancrer devTools, rechercher, ouvrir différents outils, et bien plus encore.  
    
Dans le groupe d’onglets Outils, vous pouvez ouvrir les différents outils disponibles dans DevTools.  La liste suivante décrit les outils les plus couramment utilisés dans DevTools.  

*   **Bienvenue**.  Inclut des informations sur les nouvelles fonctionnalités de DevTools, comment contacter l’équipe et fournit des informations sur certaines fonctionnalités.  
*   **Éléments**.  Vous permet de modifier ou d’inspecter le code HTML et CSS.  Vous pouvez modifier les deux dans l’outil et afficher les modifications en direct dans le navigateur.  
*   [Console][DevtoolsGuideConsoleIndex].  Permet d’afficher et de filtrer les messages du journal.  Les messages journaux sont des journaux automatisés du navigateur, tels que les demandes réseau et les journaux générés par le développeur.  Vous pouvez également exécuter JavaScript directement dans la **console** dans le contexte de la fenêtre ou du cadre actuel.  
*   [Sources][DevtoolsGuideSourcesIndex].  Un éditeur de code et un débogger JavaScript.  Vous pouvez modifier des projets, gérer des extraits de code et déboguer votre projet actuel.  
*   [Réseau][DevtoolsGuideNetworkIndex].  Vous permet de surveiller et d’inspecter les demandes ou les réponses du réseau et du cache du navigateur.  Vous pouvez filtrer les demandes et les réponses en réponse à vos besoins et simuler différentes conditions réseau.  D’autres outils spécialisés sont également disponibles, tels que **Performance,** **Mémoire,** **Application,** **Sécurité**et **Audits.**  

## <a name="power-tip-use-the-command-menu"></a>Conseil d’alimentation : utiliser le menu de commandes  

DevTools fournit un grand nombre de fonctionnalités à utiliser avec votre produit web.  Accédez aux différentes parties de DevTools de plusieurs façons, mais le moyen le plus rapide d’accéder aux fonctionnalités dont vous avez besoin consiste à utiliser le menu de commandes.  Pour plus d’informations, accédez à Exécuter des commandes avec le menu de commande [Microsoft Edge DevTools.][DevtoolsGuideCommandMenuIndex]  Pour ouvrir le menu de commandes, terminez l’une des actions suivantes.  

*   Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
*   Choose **Customize And Control DevTools** \( `...` \), and then choose Run **Command**.  

:::image type="complex" source="./media/devtools-intro-command-menu.msft.png" alt-text="Capture d’écran du menu de commande dans DevTools" lightbox="./media/devtools-intro-command-menu.msft.png":::  
Capture d’écran du menu de commande dans DevTools  
:::image-end:::  

Le menu de commandes vous permet de taper des commandes pour afficher, masquer ou exécuter des fonctionnalités dans DevTools.  Une fois le menu de commande ouvert, entrez le mot **change,** puis choisissez **Changements d’afficher les caisses.**  **L’outil Changes** s’ouvre, ce qui est utile lorsque vous modifiez CSS, mais est difficile à trouver dans l’interface utilisateur de DevTools.  

:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-command-menu-show-changes.msft.png" alt-text="Le menu commande affiche les options après avoir tapé les modifications" lightbox="./media/devtools-intro-command-menu-show-changes.msft.png":::  
         Le menu commande affiche les options après avoir tapé `changes`  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-showing-changes.msft.png" alt-text="DevTools avec l’outil Changes ouvert" lightbox="./media/devtools-intro-showing-changes.msft.png":::  
         DevTools avec l’outil **Changes** ouvert  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="customize-the-devtools"></a>Personnaliser de DevTools  

DevTools est personnalisable pour répondre à vos besoins ou à votre façon de travailler.  Pour modifier les paramètres, effectuer l’une des actions suivantes.  

*   Choose **Settings** \(the gear icon on the top right\)  
*   Select `F1` ou `?` .  
    
Dans la section **Préférences,** vous pouvez modifier plusieurs parties de DevTools.  Par exemple, vous pouvez utiliser le paramètre de langue Match **du** navigateur pour utiliser la même langue dans devTools que dans votre navigateur.  Pour un autre exemple, utilisez le **paramètre Thème** pour modifier le thème de DevTools.  

:::image type="complex" source="media/devtools-intro-all-settings.msft.png" alt-text="Capture d’écran de tous les paramètres dans DevTools" lightbox="./media/devtools-intro-all-settings.msft.png":::  
   Capture d’écran de tous les paramètres dans DevTools  
:::image-end:::  

Vous pouvez également modifier les paramètres des fonctionnalités avancées, y compris les fonctionnalités suivantes.    

*   [Espaces de travail][DevtoolsGuideWorkspacesIndex].  
*   Filtrez le code de la bibliothèque avec **la liste Ignorer.**  
*   Définissez les **appareils** que vous souhaitez inclure dans le mode test et de simulation d’appareil.  Pour plus d’informations, accédez à [Émuler des appareils mobiles dans Microsoft Edge DevTools.][DevtoolsGuideDeviceModeIndex]  
*   Choisissez un profil **de limitation du** réseau.  
*   Définissez des emplacements **simulés.**  
*   Personnalisez les raccourcis clavier.  Pour utiliser les mêmes raccourcis dans devTools que Visual Studio Code, complétez les actions suivantes.  
    1.  Choose **Match shortcuts from preset**.  
    1.  Choose **Visual Studio Code**.  
        
    :::image type="complex" source="./media/devtools-intro-match-keys.msft.png" alt-text="Capture d’écran de tous les raccourcis clavier et du menu à mettre en correspondance avec les raccourcis dans Visual Studio Code" lightbox="./media/devtools-intro-match-keys.msft.png":::  
       Capture d’écran de tous les raccourcis clavier et du menu à mettre en correspondance avec les raccourcis dans Visual Studio Code  
    :::image-end:::  
    
## <a name="try-experimental-features"></a>Essayer des fonctionnalités expérimentales  

L’équipe DevTools fournit de nouvelles fonctionnalités en tant qu’expériences dans DevTools.  Pour obtenir la liste complète des expériences, accédez aux **paramètres**DevTools, puis choisissez **Expériences.**  Vous pouvez activer ou désactiver chacune des expériences.  Déterminez l’une des expériences qui vous est utile.  Pour plus d’informations sur les expériences, accédez aux [fonctionnalités expérimentales.][DevtoolsGuideExperimentalFeaturesIndex]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Si vous souhaitez prévisualiser les dernières fonctionnalités à venir dans [DevTools][DevtoolsGuideWhatsNew202102Devtools], téléchargez [Microsoft Edge Canary][MicrosoftedgeinsiderDownload], qui est builds tous les soirs.  

## <a name="see-also"></a>Voir également  

*   [DevtoolsGuide for Beginners: Get Started with HTML and the DOM][DevtoolsGuideBeginnersHtml]  
*   [Protocole DevTools Microsoft Edge (Chromium)][DevtoolsProtocolIndex]  
    
<!-- links -->  

[DevtoolsGuideBeginnersHtml]: ./beginners/html.md "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"  
[DevtoolsGuideCommandMenuIndex]: ./command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  
[DevtoolsGuideConsoleIndex]: ./console/index.md "Vue d’ensemble de la console | Documents Microsoft"  
[DevtoolsGuideCustomizePlacement]: ./customize/placement.md "Modifier le placement de Microsoft Edge DevTools (Undock, Dock To Bottom, Dock To Left) | Documents Microsoft"  
[DevtoolsGuideDeviceModeIndex]: ./device-mode/index.md "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideDomIndex]: ./dom/index.md "Commencer à afficher et modifier les | DOM Documents Microsoft"  
[DevtoolsGuideEvaluatePerformanceIndex]: ./evaluate-performance/index.md "Commencer à analyser les performances d’exécution | Documents Microsoft"  
[DevtoolsGuideExperimentalFeaturesIndex]: ./experimental-features/index.md "Fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsGuideMemoryProblemsIndex]: ./memory-problems/index.md "Résoudre les problèmes de mémoire | Documents Microsoft"  
[DevtoolsGuideInspectStylesEditFonts]: ./inspect-styles/edit-fonts.md "Modifier les styles et paramètres de police CSS dans le volet Styles | Documents Microsoft"  
[DevtoolsGuideIssuesIndex]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideJavascriptIndex]: ./javascript/index.md "Commencer à déboguer JavaScript dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideJavascriptOverrides]: ./javascript/overrides.md "Remplacer les ressources de page web avec des copies locales à l’aide de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideNetworkIndex]: ./network/index.md "Inspecter l’activité réseau dans microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideOpenIndex]: ./open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideRenderingToolsIndex]: ./rendering-tools/index.md "Analyser les performances d’exécution | Documents Microsoft"  
[DevtoolsGuideShortcutsIndex]: ./shortcuts/index.md "Raccourcis clavier Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideSourcesIndex]: ./sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
[DevtoolsGuideStorageSessionstorage]: ./storage/sessionstorage.md "Afficher et modifier le stockage de session avec Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsGuideWhatsNew202102Devtools]: ./whats-new/2021/02/devtools.md "Nouveautés de DevTools (Microsoft Edge 90) | Documents Microsoft"  
[DevtoolsGuideWorkspacesIndex]: ./workspaces/index.md "Modifier des fichiers à l'| Documents Microsoft"  
[DevtoolsProtocolIndex]: ../devtools-protocol-chromium/index.md "Vue d’ensemble du protocole Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge Add-ons"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensions | Chrome Web Store"  
