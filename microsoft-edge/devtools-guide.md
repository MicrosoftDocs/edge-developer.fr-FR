---
description: Découvrez  la rubrique des Outils du Développeur Microsoft Edge (EdgeHTML)
title: Auteur des Outils du Développeur Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, f12 tools, devtools
experimental: true
experiment_id: "51fe4b97-3e55-41"
ms.localizationpriority: high
---

# Outils du Développeur Microsoft Edge (EdgeHTML):  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Les Microsoft Edge (EdgeHTML) DevTools sont conçues avec [TypeScript][TypeScriptIndex], par [open source][GithubMicrosoftChakracore], optimisés pour les flux de travail frontaux modernes, et désormais disponibles comme [application Windows 10 autonome][MicrosoftStoreEdgeDevtoolsPreview] dans Microsoft Store!  

Pour plus d’informations sur les fonctionnalités les plus récentes, consultez [DevTools dans la dernière mise à jour de Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Outils de Base  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
  Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Les DevTools de Microsoft Edge (EdgeHTML) comprennent:  

*   Un panneau[Eléments][DevtoolsGuideEdgehtmlElements] permettant la modification des éléments HTML et CSS, l’inspection des propriétés d’accessibilité, l’affichage des écouteurs d’événement et la création des points d’arrêt de la mutation DOM  
*   Une [Console][DevtoolsGuideEdgehtmlConsole] permettant l’affichage et le filtrage des messages de journaux, l’inspection des objets JavaScript et des nœuds DOM et l’exécution JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.  
*   [Un débogueur][DevtoolsGuideEdgehtmlDebugger] servant à parcourir le code,  déterminer les Watches et les points d’arrêt, modifier votre code en direct et inspecter votre stockage Web et vos caches cookies.  
*   Un panneau [Réseau][DevtoolsGuideEdgehtmlNetwork] permettant de contrôler et d’inspecter les demandes et les réponses à partir du réseau et du cache du navigateur.  
*   Un panneau de [Performance][DevtoolsGuideEdgehtmlPerformance] pour profiler l’heure et les ressources système requises par votre site  
*   Un panneau[Mémoire][DevtoolsGuideEdgehtmlMemory] pour mesurer l’utilisation des ressources de mémoire et comparer les instantanés de tas aux différents états du runtime de code  
*   Un panneau de[Stockage][DevtoolsGuideEdgehtmlStorage] permettant d’inspecter et de gérer votre stockage Web, votre IndexedDB, et vos données de cookies et de cache  
*   Un panneau des [Travailleurs du Service][DevtoolsGuideEdgehtmlServiceworkers] pour gérer et déboguer les travailleurs de votre service.  
*   Un panneau [d’Emulation][DevtoolsGuideEdgehtmlEmulation] pour tester votre site avec différents profils de navigateur, des résolutions d’écran et des coordonnées de localisation GPS.  

Continuez à envoyer [vos commentaires et vos demandes relatives à la fonctionnalité](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [! Conseil]
> [Testez sur Microsoft Edge (EdgeHTML) gratuitement à partir de n’importe quel navigateur][BrowserstackEdgehtml].  
> L’équipe de Microsoft Edge a collaboré avec [BrowserStack][BrowserstackEdgehtml] pour vous permettre d’effectuer des tests en direct et automatisés gratuitement sur Microsoft Edge (EdgeHTML).  

## Application Microsoft Store  

Les **DevTools Microsoft Edge (EdgeHTML)** sont désormais disponibles sous la forme d’une application autonome Windows 10 à partir de Microsoft Store, en plus de l’expérience d’outils intégrée dans le navigateur (F12). La version Store est accompagnée d’un panneau de **sélection** permettant de joindre des pièces aux cibles des pages ouvertes locales et distantes, ainsi qu’une mise en page par onglets pour une commutation facile entre les instances DevTools.  

### Débogage local  

Pour déboguer une page localement, lancez simplement l’application Microsoft Edge DevTools. Le panneau **Local** du sélectionneur affiche tous les processus du contenu EdgeHTML actif, y compris les onglets du navigateur Edge ouverts, les [PWAs][PwasEdgehtmlIndex] (les processus`WWAHost.exe`) exécutés, et les contrôles [webview][HostingWebview]. Sélectionnez la cible à joindre et ouvrez une nouvelle instance d’onglet de DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="DevTools app Local panel":::
 Panneau local de l’application DevTools
::: image-end :::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Débogage à distance  

L’application Microsoft Edge DevTools présente la prise en charge de base pour le débogage de pages sur un ordinateur à distance via le nouveau [Protocole DevTools][DevtoolsProtocolEdgehtmlIndex]. La dernière version offre l’accès à distance aux fonctionnalités principales du [Débogueur][DevtoolsGuideEdgehtmlDebugger], des [Elements][DevtoolsGuideEdgehtmlElements] (pour les opérations de lecture uniquement) et des panneaux de Console. Le débogage à distance est limité aux hôtes de bureau Microsoft Edge (EdgeHTML) exécutés. La prise en charge d’autres hôtes EdgeHTML et d’appareils Windows 10 est prévue dans les versions à venir.  

Pour commencer, consultez la section Microsoft Edge DevTools relative aux documents du [Protocole DevTools][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./devtools-guide/media/chooser\_remote.png" alt-text="DevTools app Remote panel":::
  Panneau à distance de l’application DevTools
::: image-end :::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Raccourcis Généraux  

> [! IMPORTANT]
> Tous les raccourcis ont été vérifiés dans la version la plus récente de Windows.  
> Si vous ne parvenez pas à utiliser un raccourci, veuillez mettre à jour votre copie de Windows.  

Ces raccourcis contrôlent la fenêtre principale DevTools et doivent fonctionner sur tous les outils.  

| Action | Raccourci |  
|:--- |:--- |  
| Afficher/masquer les DevTools (s’ouvre au dernier panneau affiché) | `F12`, `Ctrl`+`Maj`+`I` |  
| Toggle docking (Undock/Bottom/Right) | `Ctrl`+`Maj`+`D` |  
| Ouvrir un fichier | `Ctrl`+`P`, `Ctrl`+`O` |  
| Afficher le code source HTML non modifiable dans le débogueur | `Ctrl`+`U` |  
| Afficher/masquer la console en bas de tout autre outil | `Ctrl`+`` ' `` |  
| Basculer vers les Eléments (Explorateur DOM) | `Ctrl`+`1` |  
| Basculer vers la Console | `Ctrl`+`2` |  
| Basculer vers le Débogueur | `Ctrl`+`3` |  
| Basculer vers le Réseau | `Ctrl`+`4` |  
| Basculer vers la Performance | `Ctrl`+`5` |  
| Basculer vers la Mémoire | `Ctrl`+`6` |  
| Basculer vers l’Emulation | `Ctrl`+`7` |  
| Document d’Aide | `F1` |  
| Outil suivant | `Ctrl`+`F6` |  
| Outil précédent | `Ctrl`+`Maj`+`F6` |  
| Outil précédent (de l’historique) | `Ctrl`+`Maj`+`[` |  
| Outil suivant (de l’historique) | `Ctrl`+`Maj`+`]` |  
| Sous-cadre Suivant | `F6` |  
| Sous-cadre Précédent | `Maj`+`F6` |  
| Correspondance suivante dans la zone de recherche | `F3` |  
| Correspondance précédente dans la zone de recherche | `Maj`+`F3` |  
| Rechercher dans la zone de recherche | `Ctrl`+`F` |  
| Placer le focus sur la console en bas | `Alt`+`Maj`+`I` |  
| Lancez DevTools sur la console | `Ctrl`+`Maj`+`J` |  
| Actualiser la page | `Ctrl`+`Maj`+`F5`, `Ctrl`+`R` |  

> [! REMARQUE]
> Si vous déboguez et marquez un point d’arrêt, l’action **Actualiser la page** reprend l’exécution.  

## Contacter l’équipe de Microsoft Edge DevTools  

Envoyez-nous vos commentaires pour l’amélioration de DevTools Microsoft Edge (EdgeHTML). Ouvrez simplement les outils (`F12`), puis sélectionnez le bouton [Envoyer des commentaires](#microsoft-edge-edgehtml-developer-tools).  

Devenez un [Windows Insider][WindowsInsiderProgram] pour prévisualiser les dernières fonctionnalités de DevTools. Utilisez l’application Hub de commentaires Windows pour publier, voter, effectuer le suivi et obtenir de l’aide sur les suggestions et problèmes généraux de Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Débogueur"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Éléments"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Émulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Mémoire"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Réseau"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Performances"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Travailleurs de service"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Stockage"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools dans la dernière mise à jour de Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocole Microsoft Edge (EdgeHTML) DevTools"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Aperçu de Microsoft Edge DevTools - Clients du Protocole DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) pour les applications Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Applications Web progressifs (EdgeHTML) sur Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Aperçu Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programme Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test du navigateur Microsoft Edge Gratuitement | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
