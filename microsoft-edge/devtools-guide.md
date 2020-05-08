---
description: Découvrir les outils de développement Microsoft Edge (EdgeHTML)
title: Outils de développement Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, outils F12, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629503"
---
# Outils de développement Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Microsoft Edge \ (EdgeHTML \) DevTools est [conçu avec la méthode de frappe][|::ref1::|Index], optimisée par une [source ouverte][GithubMicrosoftChakracore], optimisée pour les flux de travail frontal modernes et désormais disponible sous la forme d’une [application Windows 10 autonome][MicrosoftStoreEdgeDevtoolsPreview] sur le Microsoft Store.  

Pour plus d’informations sur les dernières fonctionnalités, consultez [devtools la dernière mise à jour de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Outils principaux  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
   Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Microsoft Edge \ (EdgeHTML \) DevTools inclut les éléments suivants:  

*   Panneau d' [éléments][DevtoolsGuideEdgehtml|::ref2::|] permettant de modifier les propriétés d’accessibilité, d’afficher les détecteurs d’événements et de définir des points d’arrêt de mutation DOM  
*   Une [console][DevtoolsGuideEdgehtml|::ref3::|] pour afficher et filtrer des messages de journaux, inspecter des objets JavaScript et des nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.  
*   Le [débogueur][DevtoolsGuideEdgehtml|::ref4::|] pour parcourir le code, définir des espions et des points d’arrêt, modifier votre code et inspecter les caches de stockage et de cookies Web  
*   Panneau [réseau][DevtoolsGuideEdgehtml|::ref5::|] permettant de surveiller et d’inspecter les demandes et les réponses du réseau et du cache du navigateur  
*   Panneau [performance][DevtoolsGuideEdgehtml|::ref6::|] pour le profil du temps et des ressources système requis par votre site  
*   Panneau [mémoire][DevtoolsGuideEdgehtml|::ref7::|] permettant de mesurer votre utilisation des ressources mémoire et de comparer les instantanés de tas à différents États du runtime du code  
*   Panneau de [stockage][DevtoolsGuideEdgehtml|::ref8::|] permettant d’inspecter et de gérer votre stockage Web, IndexedDB, les cookies et les données du cache  
*   Panneau des [travailleurs de services][DevtoolsGuideEdgehtmlServiceworkers] pour gérer et déboguer vos travailleurs de service  
*   Panneau d' [émulation][DevtoolsGuideEdgehtml|::ref9::|] pour tester votre site avec différents profils de navigateur, résolutions d’écran et coordonnées d’emplacement GPS  

Continuez à envoyer vos [commentaires et demandes de fonctionnalité](#feedback).  

> [!TIP]
> [Test sur Microsoft Edge \ (EdgeHTML \) gratuit depuis n’importe quel navigateur][BrowserstackEdgehtml].  
> L’équipe Microsoft Edge de Microsoft s’est associée à [BrowserStack][BrowserstackEdgehtml] pour fournir des tests gratuits en temps réel et automatisés sur Microsoft Edge \ (EdgeHTML \).  

## Application du MicrosoftStore  

Le **Microsoft Edge \ (EdgeHTML \) devtools** est [désormais disponible][DevtoolsGuideEdgehtmlWhatsnew] sous la forme d’une [application Windows 10 autonome à partir du Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], en plus de l’outil`F12`de navigation intégré dans le navigateur.  La version du Windows Store est une fenêtre de **sélection** qui permet de joindre des cibles de page locales et distantes ouvertes et une disposition avec onglets pour faciliter le basculement entre les instances devtools.  

### Débogage local  

Pour déboguer une page en local, lancez simplement l’application Microsoft Edge DevTools.  Le **panneau local** du sélecteur affiche tous les processus du contenu EdgeHTML actif, y compris les onglets du navigateur d’ouverture, en cours`WWAHost.exe` d’exécution [PWAS][PwasEdgehtmlIndex] \ (processus \) et les contrôles [WebView][HostingWebview] .  Sélectionnez la cible de votre choix pour joindre et ouvrir une nouvelle instance de l’onglet du DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Panneau local de l’application DevTools":::
   Panneau local de l’application DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Débogage à distance  

L’application Microsoft Edge DevTools présente une prise en charge de base pour le débogage de pages sur un ordinateur distant par le biais de notre [protocole devtools][DevtoolsProtocolEdgehtmlIndex]nouvellement publiée.  La version la plus récente est l’accès distant aux fonctionnalités principales du [débogueur][DevtoolsGuideEdgehtml|::ref10::|], des [éléments][DevtoolsGuideEdgehtml|::ref11::|] \ (pour les opérations en lecture seule \) et des panneaux de [console][DevtoolsGuideEdgehtml|::ref12::|] .  Le débogage à distance est limité à Microsoft Edge \ (EdgeHTML \) sur l’exécution des hôtes de bureau, avec la prise en charge d’autres hôtes EdgeHTML et des appareils Windows 10 dans les versions ultérieures.  

Pour commencer, consultez la section [*Microsoft Edge devtools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] des documents du [protocole devtools][DevtoolsProtocolEdgehtmlIndex] .  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Panneau distant de l’application DevTools":::
   Panneau distant de l’application DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Raccourcis clavier généraux  

> [!IMPORTANT]
> Tous les raccourcis ont été vérifiés dans la dernière version de Windows.  
> Si vous ne parvenez pas à utiliser un raccourci, Merci de mettre à jour votre version de Windows.  

Ces raccourcis contrôlent la fenêtre principale de DevTools et doivent fonctionner sur tous les outils.  

| Action | Raccourci |  
|:--- |:--- |  
| Afficher/masquer DevTools \ (s’ouvre au dernier panneau affiché \) | `F12`, `Ctrl`+`Shift`+`I` |  
| Basculer entre l’ancrage \ (déconnexion | `Ctrl`+`Shift`+`D` |  
| Ouvrir un fichier | `Ctrl`+`P`, `Ctrl`+`O` |  
| Afficher le code source HTML non modifiable dans le débogueur | `Ctrl`+`U` |  
| Afficher/masquer la console en bas de n’importe quel autre outil  | `Ctrl`+`` ` `` |  
| Basculer vers les éléments \ (Explorateur DOM \) | `Ctrl`+`1` |  
| Basculer vers la console |  `Ctrl`+`2` |  
| Basculer vers le débogueur | `Ctrl`+`3` |  
| Basculer en réseau | `Ctrl`+`4` |  
| Basculer vers performance | `Ctrl`+`5` |  
| Basculer en mémoire | `Ctrl`+`6` |  
| Basculer vers l’émulation | `Ctrl`+`7` |  
| Document d’aide | `F1` |  
| Outil suivant | `Ctrl`+`F6` |  
| Outil précédent | `Ctrl`+`Shift`+`F6` |  
| Outil précédent \ (de l’historique \) | `Ctrl`+`Shift`+`[` |  
| Outil suivant \ (de l’historique \) | `Ctrl`+`Shift`+`]` |  
| Sous-image suivante | `F6` |  
| Sous-cadre précédent | `Shift`+`F6` |  
| Résultat suivant dans la zone de recherche | `F3` |  
| Résultat précédent dans la zone de recherche | `Shift`+`F3` |  
| Rechercher dans la zone de recherche | `Ctrl`+`F` |  
| Mettre le focus sur la console en bas | `Alt`+`Shift`+`I` |  
| Lancer DevTools vers la console | `Ctrl`+`Shift`+`J` |  
| Actualiser la page | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> S’il s’agit d’un débogage et interrompu à un point d’arrêt, l’action **Actualiser la page** réactive d’abord le Runtime.  

## Commentaires  

Envoyez-nous vos commentaires pour vous aider à améliorer Microsoft Edge \ (EdgeHTML \) DevTools pour vous!  Ouvrez simplement les outils \ (`F12`\) et sélectionnez le bouton [Envoyer des commentaires](#microsoft-edge-edgehtml-developer-tools) .  

Participez au programme [Windows Insider][WindowsInsiderProgram] pour prévisualiser les [fonctionnalités les plus récentes disponibles dans le devtools][DevtoolsGuideEdgehtmlWhatsnew].  Utilisez l’application Hub de commentaires Windows pour publier, faire un vote, suivre et obtenir de l’aide sur les suggestions et problèmes généraux dans Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Débogueur"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elément"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Émulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Mémoires"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Équilibrage"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Les"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Travailleurs de service"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Capacité"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools la dernière mise à jour de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocole DevTools de Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clients du protocole Microsoft Edge DevTools Preview-DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) pour les applications Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Applications Web progressives (EdgeHTML) sur Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Programme Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test du navigateur Microsoft Edge gratuitement | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "Dactylographié"  
