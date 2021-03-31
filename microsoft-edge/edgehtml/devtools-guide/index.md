---
description: Découvrir les outils de développement Microsoft Edge (EdgeHTML)
title: Outils de développement Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233033"
---
# Outils de développement Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

DevTools de Microsoft Edge \(EdgeHTML \) sont conçus avec [TypeScript][|::ref1::|Index], avec [Open source][GithubMicrosoftChakracore], optimisés pour les flux de travail frontaux modernes et désormais disponible sous la forme d'[application Windows10 autonome][MicrosoftStoreEdgeDevtoolsPreview] dans le Microsoft Store.  

Pour plus d’informations sur les fonctionnalités les plus récentes, consultez [DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Outils principaux  

:::image type="complex" source="./media/devtools.png" alt-text="DevTools Microsoft Edge (EdgeHTML)":::
   DevTools Microsoft Edge (EdgeHTML)
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

La DevTools Microsoft Edge (EdgeHTML) inclut:  

*   Un panneau [Éléments][DevtoolsGuideEdgehtml|::ref2::|] permettant de modifier les codes HTML et CSS, d’inspecter les propriétés d’accessibilité, d’afficher les écouteurs d’événement et de créer des points d’arrêt de mutation DOM  
*   Une [Console][DevtoolsGuideEdgehtml|::ref3::|] pour afficher et filtrer les messages journaux, examiner les objets JavaScript et les nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.  
*   Un [Débogueur][DevtoolsGuideEdgehtml|::ref4::|] pour parcourir le code, mettre en place des surveillances et des points d'arrêt, modifier en direct votre code et inspecter vos caches de stockage web et de cookies  
*   Un panneau [Réseau][DevtoolsGuideEdgehtml|::ref5::|] permettant de contrôler et d’inspecter les demandes et les réponses à partir du réseau et du cache du navigateur.  
*   Un panneau [Performance][DevtoolsGuideEdgehtml|::ref6::|] pour profiler l’heure et les ressources système requises par votre site  
*   Un panneau [Mémoire][DevtoolsGuideEdgehtml|::ref7::|] pour mesurer l’utilisation des ressources de mémoire et comparer les instantanés de tas aux différents états du runtime de code  
*   Un panneau [Stockage][DevtoolsGuideEdgehtml|::ref8::|] permettant d’inspecter et de gérer vos données de stockage web, de IndexedDB, de cookies et de cache  
*   Un panneau [Travailleurs de services][DevtoolsGuideEdgehtmlServiceworkers]pour gérer et déboguer vos travailleurs de services  
*   Un panneau [Émulation][DevtoolsGuideEdgehtml|::ref9::|] pour tester votre site avec différents profils de navigateur, des résolutions d’écran et des coordonnées d’emplacement GPS  

N’hésitez pas à nous envoyer vos [commentaires et demandes de fonctionnalité](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

> [!TIP]
> [Test sur Microsoft Edge \(EdgeHTML\) gratuit à partir de n'importe quel navigateur][BrowserstackEdgehtml].  
> L’équipe Microsoft Edge a collaboré avec [BrowserStack][BrowserstackEdgehtml] pour vous permettre d’effectuer des tests en ligne et automatisés gratuitement sur Microsoft Edge \(EdgeHTML\).  

## Application du MicrosoftStore  

Les **DevTools Microsoft Edge \(EdgeHTML\)** sont [désormais disponibles][DevtoolsGuideEdgehtmlWhatsnew] sous la forme d’une application autonome [Windows10 à partir du Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], en plus de l’expérience d’outils dans le navigateur \(`F12`\).  La version store est accompagnée d'un panneau de **Sélecteur** permettant d'associer des cibles de pages locales et distantes ouvertes et d'une mise en page à onglets permettant de passer facilement d'une instance DevTools à l'autre.  

### Débogage local  

Pour déboguer une page localement, lancez simplement l’application DevTools de Microsoft Edge.  Le panneau **Local** du sélecteur affiche tous les processus de contenu EdgeHTML actifs, y compris les onglets de navigateur ouvert, exécutant [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processus \), et les contrôles de panneau [vue web][HostingWebview].  Sélectionnez la cible souhaitée à joindre et ouvrez une nouvelle instance d’onglet de DevTools.  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Panneau local de l’application DevTools":::
   Panneau local de l’application DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Débogage à distance  

L’application DevTools Microsoft Edge présente la prise en charge de base pour le débogage de pages sur un ordinateur distant via le [Protocole DevTools][DevtoolsProtocolEdgehtmlIndex].  La dernière version inclut l’accès à distance aux fonctionnalités principales dans les panneaux [Débogage][DevtoolsGuideEdgehtml|::ref10::|],[Éléments][DevtoolsGuideEdgehtml|::ref11::|] \(pour les opérations en lecture seule \) et [Console][DevtoolsGuideEdgehtml|::ref12::|].  Le débogage distant est limité à Microsoft Edge \(EdgeHTML\) qui exécute les hôtes de bureau, avec la prise en charge d’autres hôtes EdgeHTML et de périphériques Windows10 dans les versions à venir.  

Pour commencer, consultez la section [*DevTools Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] de la documentation sur le [protocole DevTools][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Panneau distant de l’application DevTools":::
   Panneau distant de l’application DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Raccourcis généraux  

> [!IMPORTANT]
> Tous les raccourcis ont été vérifiés dans la version la plus récente de Windows.  
> Si vous ne parvenez pas à utiliser un raccourci, veuillez mettre à jour votre copie de Windows.  

Ces raccourcis contrôlent la fenêtre principale DevTools et doivent fonctionner sur tous les outils.  

| Action | Raccourci |  
|:--- |:--- |  
| Afficher/masquer DevTools \(s’ouvre sur le panneau dernier affichage\) | `F12`, `Ctrl`+`Shift`+`I` |  
| Basculer la station d’Accueil \(annuler la station d’accueil/bas/droite \) | `Ctrl`+`Shift`+`D` |  
| Ouvrir un fichier | `Ctrl`+`P`, `Ctrl`+`O` |  
| Afficher le code source HTML non modifiable dans le débogueur | `Ctrl`+`U` |  
| Afficher/masquer la console en bas de tout autre outil  | `Ctrl`+`` ` `` |  
| Basculer vers les éléments \(Explorateur DOM\) | `Ctrl`+`1` |  
| Basculer vers la console |  `Ctrl`+`2` |  
| Basculer vers le débogueur | `Ctrl`+`3` |  
| Basculer vers le réseau | `Ctrl`+`4` |  
| Basculer vers les performances | `Ctrl`+`5` |  
| Basculer vers la mémoire | `Ctrl`+`6` |  
| Basculer vers l’émulation | `Ctrl`+`7` |  
| Document d’aide | `F1` |  
| Outil suivant | `Ctrl`+`F6` |  
| Outil précédent | `Ctrl`+`Shift`+`F6` |  
| Outil précédent \(à partir de l’historique\) | `Ctrl`+`Shift`+`[` |  
| Outil suivant \(à partir de l’historique\) | `Ctrl`+`Shift`+`]` |  
| Sous-cadre suivant | `F6` |  
| Sous-cadre précédent | `Shift`+`F6` |  
| Correspondance suivante dans la zone de recherche | `F3` |  
| Correspondance précédente dans la zone de recherche | `Shift`+`F3` |  
| Rechercher dans la zone de recherche | `Ctrl`+`F` |  
| Placer le focus sur la console en bas | `Alt`+`Shift`+`I` |  
| Démarrer DevTools à la console | `Ctrl`+`Shift`+`J` |  
| Actualiser la page. | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Si vous déboguez un point d’arrêt et que vous l’avez suspendu, l’action **Actualiser la page** reprend l’exécution.  

## Contacter l’équipe DevTools MicrosoftEdge  

Envoyez-nous vos commentaires pour améliorer la DevTools de Microsoft Edge \(EdgeHTML \) pour vous.  Il vous suffit d’ouvrir les outils \(`F12`\) et de sélectionner le bouton [Envoyer des commentaires](#microsoft-edge-edgehtml-developer-tools).  

Devenez un [Windows Insider][WindowsInsiderProgram] pour prévisualiser le [dernières fonctionnalités en provenance de la DevTools][DevtoolsGuideEdgehtmlWhatsnew].  Utilisez l’application Hub de commentaires Windows pour publier, voter, effectuer le suivi et obtenir de l’aide sur les suggestions et problèmes généraux de Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Débogueur"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elément"  Éléments
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Émulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Mémoire"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Réseau"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Niveau de performance"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Travailleurs de service"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Sauvegarde"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools dans la dernière mise à jour de Windows10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocole DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Aperçu DevTools Microsoft Edge - Clients de protocole DevTools "  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) pour les applications Windows10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Applications web progressives (EdgeHTML) sur Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Aperçu de DevTools Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Programme WindowsInsider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test du navigateur Microsoft Edge gratuit | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
