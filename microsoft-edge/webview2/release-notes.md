---
description: Notes de publication pour le SDK Microsoft Edge WebView2
title: Notes de publication pour Microsoft Edge WebView2 pour Win32, WPF et WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 50fb6aae0e98ae76ec7ba35e9676e1ccf7a51a24
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535916"
---
# <a name="release-notes-for-webview2-sdk"></a>Notes de publication pour le SDK WebView2  

L’équipe WebView2 met à jour le [SDK WebView2][NuGetGallery] sur une cadence de six semaines.  Examinez le contenu suivant pour obtenir des informations à jour sur les annonces, les ajouts, les modifications et les modifications importantes apportées aux API.  

> [!NOTE]
> Assurez-vous que vous re compilez votre application après avoir mis à jour le package NuGet.  L’équipe WebView vous recommande d’utiliser le canal Canary lorsque vous développez à l’aide des packages de version préalable, et le runtime WebView2 persistant lorsque vous utilisez les packages de publication.  Pour plus d’informations, [accédez aux versions d’runtime WebView2 correspondantes.][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]  

> [!NOTE]
> Les correctifs de bogue WebView2 sont spécifiques au runtime ou au SDK.  

## <a name="10865-prerelease"></a>1.0.865-prerelease  

Date de publication : 26 avril 2021  

[Package NuGet][NuGetGallery1.0.865-prerelease] \| Version minimale de Microsoft Edge à charger : 86.0.616.0 ou version plus récente \| Compatibilité complète des API : 91.0.865.0 ou version plus nouvelle  

### <a name="general"></a>Général  

#### <a name="experimental-features"></a>Fonctionnalités expérimentales  

*   Ajout du [paramètre IsPinchZoomEnabled.][Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled] Il vous permet d’activer ou de désactiver le contrôle de zoom d’échelle de page dans un paramètre.  
*   Ajout de [l’API add_DownloadStarting][Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting] personnalisée.  Il vous permet de bloquer les téléchargements, d’enregistrer dans un autre chemin d’accès et d’accéder aux métadonnées requises pour créer une interface utilisateur de téléchargement personnalisée.  
*   Ajout de la prise en charge des éléments `iframe` [à partir de AddHostObjectToScriptWithOrigins][Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins].  
*   Ajout d’un exemple de code [pour l’exemple d’application WPF][GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser] afin d’utiliser l’API pour désactiver les clés de fonction de navigateur.  
*   Ajout de [l’API UpdateRuntime,][Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime] pour mettre à jour facilement le runtime WebView2.  
    
#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Correction du handler `Chromium DevTools Protocol` d’un message avec des données `POST` binaires dans WebView2.  
*   Désactivé `OpenSaveAsAwareness` l’interface utilisateur de téléchargement, car elle inclut des liens vers `edge://settings` .  \([\#1120][GithubMicrosoftedgeWebviewfeedbackIssue1120]\).  
*   Suppression de la marque de la boîte de dialogue de partage d’écran.  \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\).  
*   Bogue résolu dans lequel la [fonction SetWindowDisplayAffinity][WindowsWin32ApiWinuserSetWindowDisplayAffinity] a interrompu WebView2 lors de l’arrêt de la capture d’écran dans une application WebView2.  \([\#841][GithubMicrosoftedgeWebviewfeedbackIssue841]\).
*   Correction d’un bogue pour l’hébergement de composition où l’entrée de souris a cessé de fonctionner si une entrée de stylet a été envoyée à WebView2.  
*   Correction d’un bogue qui erait l’entrée de la souris après une entrée de stylet.  Cette modification est spécifique au runtime.  
    
### <a name="net"></a>.NET  

#### <a name="experimental-features"></a>Fonctionnalités expérimentales  

*   Ajout de l’outil concepteur WebView2 à la boîte à outils WPF.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Ajout de l’élément d’interface utilisateur WebView2 en mode .NET Designer.  
    
#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Descriptions améliorées des exceptions COM en veloppant chacune d’elles dans une exception .NET plus détaillée.  \([\#338][GithubMicrosoftedgeWebviewfeedbackIssue338]\).  Cette modification est spécifique au runtime.  
*   Correction d’un bogue provoqué lorsque vous choisissez de déplacer le focus a provoqué le crash du contrôle `tab` WebView2 dans Microsoft Visual Studio Tools for Office.  \([\#589][GithubMicrosoftedgeWebviewfeedbackIssue589] et [\#933][GithubMicrosoftedgeWebviewfeedbackIssue933]\).  Cette modification est spécifique au runtime.  
*   Amélioration du niveau de chargement du .NET Framework pour être plus robuste.  \([\#946][GithubMicrosoftedgeWebviewfeedbackIssue946]\).
*   Correction d’un bogue qui provoquait un incident lorsque vous essayez d’actualiser avant la fin de la première navigation.  \([\#1011][GithubMicrosoftedgeWebviewfeedbackIssue1011]\).
*   Initialisation fixe de sorte que la navigation a lieu pendant `CoreWebView2InitializationCompleted` .  \([\#1050][GithubMicrosoftedgeWebviewfeedbackIssue1050]\).
*   Amélioration de la gestion des erreurs d’incident du processus de navigateur .NET.  Vous pouvez maintenant recréer des contrôles après avoir géré un `ProcessFailed` événement sans incident.  \([\#996][GithubMicrosoftedgeWebviewfeedbackIssue996]\).  
    
## <a name="1081841"></a>1.0.818.41  

Date de publication : 21 avril 2021  

[Package NuGet][NuGetGallery1.0.818.41] \| Version d’runtime minimale à charger : 86.0.616.0 ou version plus récente \| Compatibilité complète des API : 90.0.818.41 ou version plus nouvelle  

### <a name="general"></a>Général  

#### <a name="features"></a>Fonctionnalités  

*   Extension de `ProcessFailed` l’événement.  Il se raise maintenant pour les processus enfants non-renderer et les renderers d’images.  
*   Ajout de la `iframe` prise en charge des éléments pour `AddScriptToExecuteOnDocumentCreated` .  
*   Amélioration du code WebView2 pour être plus résilient aux fichiers d’application avec des informations `.exe` de version mal formatées.  \([\#850][GithubMicrosoftedgeWebviewfeedbackIssue850]\).  
*   Supprimée de la ligne de commande du processus de navigateur WebView, elle a été désactivée par d’autres options de ligne de `--winhttp-proxy-resolver` commande proxy pour WebView2.  
    
## <a name="10824-prerelease"></a>1.0.824-prerelease  

Date de publication : 8 mars 2021  

[Package NuGet][NuGetGallery1.0.824-prerelease] \| Version minimale de Microsoft Edge à charger : 86.0.616.0 ou version plus récente \| Compatibilité complète des API : 91.0.824.0 ou version plus nouvelle  

### <a name="general"></a>Général  

#### <a name="features"></a>Fonctionnalités  

*   Extension de `ProcessFailed` l’événement.  Il se raise maintenant pour les processus enfants non-renderer et les renderers d’images.  
*   Ajout du [paramètre expérimental AreBrowserAcceleratorKeysEnabled.][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]  Vous pouvez empêcher le navigateur de répondre aux raccourcis clavier liés à la navigation, l’impression, l’enregistrement et d’autres fonctions spécifiques au navigateur.  
*   Ajout de la `iframe` prise en charge des éléments pour `AddScriptToExecuteOnDocumentCreated` .  
    
#### <a name="promotion"></a>Promotion  

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] L’API est désormais promue à Stable.  
*   Les API d’échelle de rastérisation \( propriété[RasterizationScale,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]  [événement RasterizationScaleChanged,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] [propriété BoundsMode][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]et [propriété ShouldDetectMonitorScaleChanges\)][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] sont désormais promues à Stable.  
    
#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Types de projets C++ et .NET pris en charge, tels que MFC et ATL.  \([\#506,][GithubMicrosoftedgeWebviewfeedbackIssue506] [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669]et [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Correction d’un bogue dans le cadre de la fuite de l’entrée du pare-feu entrant par le runtime WebView2 persistant.  
*   Réponse de paramètre fixe pendant `WebResourceRequested` l’événement.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Correction d’un bogue qui a pour origine `edge://` la sortie du processus de navigateur.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Correction d’un bogue qui limitait la limite WebView2 à la taille de l’écran en mode d’hébergement visuel.  
    
## <a name="1077444"></a>1.0.774.44  

Date de publication : 8 mars 2021  

[Package NuGet][NuGetGallery1.0.774.44] \| Version d’runtime minimale à charger : 86.0.616.0 ou version plus récente \| Compatibilité complète des API : 89.0.774.44 ou version plus nouvelle  

### <a name="general"></a>Général  

#### <a name="features"></a>Fonctionnalités  

*   Désactivé différents services de navigateur Microsoft Edge dans WebView2.  
*   Les API d’hébergement visuel sont désormais généralement disponibles.  
    
#### <a name="promotions"></a>Promotions  

*   Les API expérimentales suivantes sont désormais promues à Stable.  
    *   [API associées de prise][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] en charge des DPI  
    *   API d’hébergement visuel  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend et Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Correction d’un bogue qui limitait la limite WebView2 à la taille de l’écran en mode d’hébergement visuel.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Date de publication : 10 février 2021  

[NuGet package][NuGetGallery1.0.790-prerelease] \| Microsoft Edge version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

> [!IMPORTANT]
> **Modification de**la rupture : le package pré-version WebView2 1.0.781 est supprimé.  Arrêter le développement avec le package 1.0.781.  

> [!IMPORTANT]
> Le package de pré-version WebView2 0.9.430 est supprimé avec la prochaine version.  Si votre application WebView utilise le package, l’équipe WebView vous recommande de passer à un package plus nouveau.  

#### <a name="features"></a>Fonctionnalités  

*   Ajout des [méthodes TrySuspend et Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] pour suspendre et reprendre les webViews.  
*   Ajout de [la méthode SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] qui mappe un nom d’hôte virtuel à un chemin d’accès au répertoire.  \([\#37,][GithubMicrosoftedgeWebviewfeedbackIssue37] [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]et [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Ajout de la [propriété DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] pour définir la couleur et le canal alpha de l’arrière-plan.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Ajout de la [propriété UserAgent][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] pour obtenir ou définir l’agent utilisateur.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Remplacement de `CreateCookieWithCookie` la méthode par la `CopyCookie` méthode.  
*   Ajout de la prise en charge de l’hébergement visuel à l’aide de l’interface [ICoreWebView2CompositionController,][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] qui est créée à l’aide de la `CreateCoreWebView2CompositionController` nouvelle méthode à partir de `ICoreWebView2Environment3` .  
    
#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Désactivé la fonctionnalité Microsoft Edge Achats dans WebView2.  
*   Désactivé le menu contexto dans la visionneuse PDF quand `AreDefaultContextMenusEnabled` c’est le `false` cas.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Correction d’un bogue renvoyé `E_NOINTERFACE` lors de l’interrogation `ICoreWebView2` pour `ICoreWebView2Experimental` .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Correction d’un bogue qui permettait la navigation avec des URL malformées `CoreWebView2NavigationStartingEventArgs.Cancel` lorsqu’elle était définie sur `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Correction d’un bogue qui bloquait les fenêtres `window.print()` pop-up avec des handlers d’événements associés à des `NewWindowRequested` événements.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Correction d’un problème de DPI dynamique lors du déplacement d’applications entre différents moniteurs.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Amélioration des `HRESULT` instances transmises par [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke].  
*   Bouton Gérer la resserrement automatique désactivé.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Correction Visual Studio se crashe lorsque vous vous `WebView2.Dispose` exécutez lorsqu’il est hébergé dans plusieurs fenêtres.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\) et [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Correction d’un bogue pour afficher le contrôle WebView2 dans Visual Studio Boîte à outils.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Réduction des problèmes élevés d’utilisation du processeur.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Correction des problèmes avec le package de pré-édition 1.0.781 supprimé.  \([\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [et \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Promotions  

*   Les API expérimentales suivantes sont désormais promues à Stable.  
    *   API d’hébergement visuel  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Résolutions de bogues  

*   Correction d’un bogue qui s’est produit sur les applications WebView qui utilisent le SDK WPF.  L’incident s’est produit lorsque vous avez `F4` choisi de fermer une fenêtre.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   L’écran d’initialisation de WebView2 est désormais transparent, au lieu de gris.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Date de publication : 25 janvier 2021  

[NuGet package][NuGetGallery1.0.705.50] \| WebView2 Runtime version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

#### <a name="promotions"></a>Promotions  

*   Les API expérimentales suivantes sont désormais promues à Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de gestion des cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propriété WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
## <a name="10721-prerelease"></a>1.0.721-prerelease  

Date de publication : 8 décembre 2020  

[NuGet package][NuGetGallery1.0.721-prerelease] \| Microsoft Edge version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

> [!IMPORTANT]
> **Modification de**la rupture : le package pré-version WebView2 1.0.707 et le package 0.9.628 sont supprimés.  Arrêter le développement avec le package 1.0.707 et package0.9.628.  

#### <a name="features"></a>Fonctionnalités  

*   Ajout de [stratégies de groupe WebView2.][DeployedgeMicrosoftEdgeWebviewPolicies]  Pour plus d’informations sur les pratiques recommandées, accédez aux [stratégies de groupe pour WebView2.][Webview2ConceptsEnterpriseGroupPoliciesForWebview2]  
*   > [!IMPORTANT]
    > **Modification de la**rupture : l’ancien emplacement du Registre a été supprimé.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Prise en charge supplémentaire de [glisser-déposer][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] dans WebView2.  
*   Ajout d’API pour gérer la prise en charge des DPI.  
    *   Ajout de [la propriété RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] pour modifier l’échelle DPI pour le contenu WebView et les fenêtres pop-up d’interface utilisateur, ainsi que l’événement [RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] associé.  
    *   Ajout de [la propriété ShouldDetectMonitorScaleChanges pour][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] mettre à jour automatiquement la propriété si `RasterizationScale` nécessaire.  
    *   Ajout de la propriété [BoundsMode][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] pour spécifier que les limites sont des pixels logiques et autoriser WebView à utiliser pour l’affichage de pixels WebView2, et WebView l’utiliser avec pour obtenir la taille `RasterizationScale` `RasterizationScale` `Bounds` physique.  
*   Événement mis `NewWindowRequested` à jour à gérer et `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] et [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Les API expérimentales suivantes sont désormais promues à Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de gestion des cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propriété WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Fonctionnalités  

*   A allumé le concepteur WinForms dans .NET Core 3.1+ et .NET 5.  
*   Amélioration de la gestion des cookies .NET.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Remplacé `CoreWebView2Ready` par [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  
    
#### <a name="bug-fixes"></a>Résolutions de bogues

*   Ajout de [l’événement AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] pour prendre en charge `AcceleratorKey` la sélection dans WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Suppression des fichiers inutiles de la sortie vers les dossiers WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API d’objet hôte améliorée.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] et [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Date de publication : 20 novembre 2020  

[NuGet package][NuGetGallery1.0.664.37] \| WebView2 Runtime version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

> [!IMPORTANT]
> **Annonce**: les SDK .NET WPF/WinForms WebView2 sont désormais généralement disponibles \(GA\).  À partir de cette version, les SDK release sont compatibles avec les avants.  Pour plus d’informations, accédez au [billet de blog d’annonce de la ga.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

#### <a name="features"></a>Fonctionnalités  

*   .NET WPF/WinForms WebView2 est désormais disponible en général \(GA\).  
*   Le mode de distribution fixe \(Bring-your-own\) a atteint la ga.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Résolutions de bogues  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` empêche l’ouverture d’une nouvelle fenêtre.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] et [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Date de publication : 19 octobre 2020  

[NuGet package][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

*   Ajout de [la méthode NavigateWithWebResourceRequest][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] pour fournir des données de publication ou d’autres en-têtes de requête lors de la navigation.  
*   Ajout de [l’événement DOMContentLoaded][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] qui s’exécute lors du chargement et de l’examen du document HTML initial.  
*   Ajout de la [propriété Environment][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] sur WebView2.  Cette propriété expose l’environnement WebView2 dans lequel une instance de WebView2 a été créée.  
*   Ajout d’API de gestion des [cookies][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] qui permettent aux développeurs d’authentifier la session WebView2 ou de récupérer des cookies à partir de WebView pour authentifier d’autres outils.  L’équipe Webview prévoit d’apporter des améliorations spécifiques à la langue ou à l’infrastructure.  Pour plus d’informations, accédez à [La révision de l’API : Gestion des cookies.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Mise à jour de [l’événement WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] et ajout de [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] et [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] à [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent].  
*   Désactivée [Protection d’application Microsoft Defender (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] dans WebView2.  
*   Ajout de [SystemCursorId pour][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] l’hébergement visuel.  
*   Ajout d’un bogue résolu pour la méthode d’entrée dans l’hébergement visuel.  
*   Les suppressions incluent les conditions `version.lib` requises pour l’utilisation de la bibliothèque statique WebView2.  
    
### <a name="net"></a>.NET  

*   Mise à jour de la classe [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] pour exposer la `CoreWebView2Environment` variable.  
*   Implémentations modifiées des classes EventArgs personnalisées dans l’espace de noms en `Microsoft.Web.WebView2.Core` sous-classes [de System.EventArgs][DotnetApiSystemEventargs] ou [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Prise en charge supplémentaire [de CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] dans WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   Ajout des [API .NET WebResourceRequested.][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Mise à jour de la propriété Source [de][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] WinForms Designer sur valeur par défaut ou réinitialisation sur null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Limites WebView2 mises à jour WebView2.Init() pour prendre en charge les modes DPI inférieurs à 100 %.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Mise à [jour de BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [et DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] pour renforcer la robustesse.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Base .NET Loader mise à jour pour se charger sur le bit de processus au lieu de l’architecture du système d’exploitation.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Renommé `EdgeNotFoundException` [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Date de publication : 19 octobre 2020  

[NuGet package][NuGetGallery1.0.622.22] \| WebView2 Runtime version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

> [!IMPORTANT]
> **Annonce**: Win32 C/C++ WebView2 est désormais disponible en général \(GA\).  À partir de cette version, les SDK release sont compatibles avec les avants.  Pour plus d’informations, accédez au billet de blog sur les [annonces ga.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [Le runtime WebView2 persistant et le programme d’installation][Webview2ConceptsDistributionUnderstandRuntimeInstaller] sont GA.  Bootstrapper, lien de lien vers le bas pour le programme d’a bootstrapper et le programme d’installation autonome pour le runtime WebView2 persistant sont disponibles [sur Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Un exemple de code pour le flux de travail d’installation est également disponible dans le [repo WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   [Le mode version fixe][Webview2ConceptsDistributionFixedVersionDistributionMode] est disponible pour la prévisualisation pour les développeurs.  
    
## <a name="0962211"></a>0.9.622.11  

Date de publication : 10 septembre 2020  

[NuGet package][NuGetGallery0.9.622.11] \| WebView2 Runtime version 86.0.616.0 ou version plus récente  

### <a name="general"></a>Général  

*   > [!IMPORTANT]
    > **Annonce**: ce SDK est le release candidate pour WebView2 Win32 C/C++ GA.  La version GA doit utiliser la même interface API et la même fonctionnalité.  
    
*   Stratégies [de navigateur déconnectées.][DeployedgeMicrosoftEdgePolicies]  
*   Ajout de [la propriété AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] sur les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Mise à `ICoreWebView2NewWindowRequestedEventArgs` jour pour inclure la propriété [WindowFeatures][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] et la propriété [ICoreWebView2WindowFeatures associée.][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Mis à `System.Windows.Rect`  jour pour être utilisé à la place de `System.Drawing.Rectangle` `System.Windows.Rect` [\( \#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Événement NewWindowRequested mis à jour pour gérer `window.open()` la demande sans paramètres.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Les autres valeursBrowserArguments][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] spécifiées avec ne sont pas overridées par des variables d’environnement ou des valeurs `ICoreWebView2EnvironmentOptions` de Registre.  Pour plus d’informations, [accédez à CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## <a name="09579"></a>0.9.579  

Date de publication : 20 juillet 2020  

[NuGet package][NuGetGallery0.9.579] \| Microsoft Edge version 86.0.579.0.  

### <a name="general"></a>Général  

*   > [!IMPORTANT]
    > **Annonce**: le runtime et le programme d’installation WebView2 persistants sont publiés pour prévisualisation.  Pour plus d’informations, [accédez à Distribution de WebView2.][Webview2ConceptsDistributionUnderstandRuntimeInstaller]  
    
*   > [!IMPORTANT]
    > **Annonce**: les versions suivantes du SDK WebView2 ne sont plus pris en charge après la prochaine version du SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Les versions du SDK WebView2 sont également marquées comme nuget.org.  WebView2 recommande de rester à jour avec la dernière version de WebView2.  
    
*   Ajout des améliorations apportées aux threads de travail WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Désactivé le bloqueur de fenêtres popup dans WebView.  Pour plus d’informations, accédez à la [propriété IsUserInitiated][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] dans l’événement. `NewWindowRequested`  
*   Événement de démarrage de navigation WebView garanti pour `about:blank` .  À présent, les événements sont exécutés pour toute la navigation, mais les annulations pour ou pour l’élément ne sont pas pris en charge `NavigationStarting` `about:blank` et `srcdoc` `iframe` ignorés.  
*   Blocage de `edge://` certains schémas d’URI dans WebView.  
*   Ajout de la propriété [expérimentale IsSingleSignOnUsingOSPrimaryAccountEnabled][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] sur les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Ajout de [l’événement Expérimental WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] qui s’exécute après que WebView a reçu et traite la réponse d’une demande WebResource.  Les en-têtes d’authentification, s’il y en a, sont inclus dans l’objet de réponse.  
    
### <a name="net"></a>.NET  

*   Amélioration de la gestion du focus WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Ajout `ZoomFactor` d’une propriété sur le contrôleur Webview2 WPF.  
    
## <a name="09538"></a>0.9.538  

[NuGet package][NuGetGallery0.9.538] \| Microsoft Edge version 85.0.538.0.  

### <a name="general"></a>Général  

*   Suppression de la prise en charge du SDK WebView2 Version [0.8.149](#08149).  WebView2 recommande de rester à jour avec la dernière version de WebView2.  
*   Stratégie de groupe mise à jour pour tenir compte du moment où le chemin d’accès du Microsoft Edge est modifié \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   Ajout [d’ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures], qui se déclenche lors de l’utilisation et est associé à `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Modification de**la rupture : afin de s’assurer que l’API WebView2 s’aligne sur les conventions d’attribution de noms d’API Windows, l’équipe WebView a mis à jour les noms des informations suivantes.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] est désormais [AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   Mise à [jour de AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript].  Les marqueurs du sérialisateur d’objet hôte d’origine sont désormais définies sur les objets proxy.  Ensuite, les marqueurs du sérialisateur d’objet hôte sont sérialisés en tant qu’objet hôte lorsqu’ils sont transmis en tant que paramètres dans le rappel JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
### <a name="net-09538-pre-release"></a>.NET (pré-version 0.9.538)  

*   Exemples WinForms et WPF WebView2API publiés, qui sont des guides complets du SDK WebView2.  Pour plus d’informations, [accédez à Repo d’exemples.][GithubMicrosoftedgeWebview2samplesMain]  
*   Ajout de la prise en charge des API expérimentales d’hébergement visuel et de [fenêtre.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Modification**de rupture : les reports suivants implémentent désormais IDisposable :  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]et [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Ajout de [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] et [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] en tant que [statiques CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[NuGet package][NuGetGallery0.9.515-prerelease] \| Microsoft Edge version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Annonce**: WebView2 prend désormais en charge Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .NET Core 3.0 ou version ultérieure dans le **package pré-version.**  
    
*   Pour plus d’informations sur la création d’applications [WPF,][Webview2GetStartedWpf] accédez au Guide Prise en main WPF et à la référence [WPF][DotnetApiMicrosoftWebWebview2Wpf] WebView2 pour les API propres à WPF.  
*   Pour plus d’informations sur la création d’applications Windows Forms, accédez au [Guide Windows Forms Prise en main][Webview2GetStartedWinforms] et à la référence de formulaires WebView2 [Windows][DotnetApiMicrosoftWebWebview2Winforms] pour les API Windows Forms spécifiques.  
*   Pour plus d’informations sur les API CoreWebView2, accédez à [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problèmes connus**: l’équipe WebView est au courant de certains problèmes de la version pré-publiée qui sont résolus dans les prochaines publication.  
    > 
    > *   **Sensibilisation aux DPI**: WebView2 pour WPF n’est actuellement pas pris en compte.  Lors de l’initialisation de WebView2 sur des moniteurs à hautes proportions, il existe un problème connu où WebView s’initialise d’abord en tant que fraction de la fenêtre jusqu’à ce que la fenêtre soit re resserrée.  
    > *   **Concepteur WPF :** le concepteur WPF n’est actuellement pas pris en charge.  Ajoutez le contrôle WebView2 dans votre application en modifiant directement le XAML approprié dans un éditeur de texte.  
    
## <a name="09488"></a>0.9.488  

[NuGet package][NuGetGallery0.9.488] \| Microsoft Edge version 84.0.488.0.  

*   > [!IMPORTANT]
    > **Annonce**: à compter de la Microsoft Edge version 83, Le WebView persistant ne cible plus le canal de navigateur stable.  Au lieu de cela, il cible un autre ensemble de binaires, le [runtime WebView2][Webview2ConceptsDistributionEvergreenDistributionMode]persistant, que vous pouvez chaine-installer via un programme d’installation que l’équipe WebView développe actuellement.  Pour plus d’informations, [accédez à App-Distribution][Webview2ConceptsDistribution].  
    
*   > [!IMPORTANT]
    > **Annonce**: à l’avenir, l’équipe WebView publie deux packages : un package de pré-version avec des API expérimentales \(pour que vous essayiez\) et un package de publication stable avec des API stables \(pour votre confiance\).  Pour en savoir plus sur les différences, accédez à [Understanding browser versions and WebView2][Webview2ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Modification**de la rupture : afin de s’assurer que l’API WebView2 s’aligne sur les conventions d’attribution de noms d’API Windows, l’équipe WebView a mis à jour les noms des interfaces suivantes.  
    > 
    > *   `CORE_WEBVIEW2_*` préfixe est maintenant `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] est désormais [GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] est désormais [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject est][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] désormais [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject est][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] désormais [RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` est maintenant `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Modification de la**rupture : les `AddRemoteObject` méthodes proxy JS sont également renommées.  
    > 
    > *   `getLocal` est maintenant `getLocalProperty` .  
    > *   `setLocal` est maintenant `setLocalProperty` .  
    > *   `getRemote` est maintenant `getHostProperty` .  
    > *   `setRemote` est maintenant `setHostProperty` .  
    > *   `applyRemote` est maintenant `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   Ajout de [l’événement FrameNavigationCompleted.][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]  À présent, lorsqu’un élément termine la navigation, un événement est exécuté et renvoie la réussite de la navigation et de `iframe` l’ID de navigation.  
*   Ajout de l’interface [ICoreWebView2EnvironmentOptions,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] qui peut être utilisée pour déterminer la version de l’application WebView2 Runtime persistante ciblée par votre application.  
*   Ajout du [paramètre IsBuiltInErrorPageEnabled.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  À présent, vous pouvez choisir d’activer ou de désactiver la page web d’erreur intégrée en cas d’échec de navigation et d’échec du processus de rendu.  
*   Mise à jour de l’injection d’objets distants pour prendre en charge les implémentations .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Événement [NewWindowRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] mis à jour pour gérer les demandes provenant de menus contextux \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Publication du premier package de pré-version WebView2 distinct dans lequel vous pouvez accéder aux API d’hébergement visuel.  L’équipe WebView a mis à [jour APISample][GithubMicrosoftedgeWebview2samplesMain] pour inclure les nouvelles API expérimentales.  
    *   Ajout de [l’interface ICoreWebView2ExperimentalCompositionController,][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] pour se connecter à une arborescence de composition et fournir des entrées pour Le WebView.  
    *   Ajout [d’ICoreWebView2ExperimentalPointerInfo][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease], qui contient toutes les informations d’un `POINTER_INFO` .  Cet objet est transmis à SendPointerInput pour injecter une entrée de pointeur dans le WebView.  
    *   Ajout [d’ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease], qui indique à l’application quand le curseur de la souris sur le WebView doit être modifié.  Lorsque la souris se trouve au-dessus d’une zone de texte dans Le WebView, le curseur change de flèche en sélecteur.  La propriété sur l’application indique à l’application ce que doit être le curseur de la souris `cursor` `CompositionController` pour le WebView.  
        
## <a name="09430"></a>0.9.430  

[NuGet package][NuGetGallery0.9.430] \| Microsoft Edge version 82.0.430.0.  

Le SDK WebView2 est la version bêta de Win32 C++ officielle, qui intègre plusieurs demandes de fonctionnalités provenant de commentaires.  L’équipe WebView tente de limiter le nombre de sorties avec des modifications importantes.  En tant qu’approches de disponibilité générale, plusieurs changements majeurs majeurs sont incorporés dans la version bêta.  

*   > [!IMPORTANT]
    > **Modification**de la rupture : à mesure que la version finale approche, l’équipe WebView a renommé le préfixe afin de s’assurer que l’API WebView2 s’aligne sur la convention d’attribution de noms `IWebView2WebView` d’API `ICoreWebView2` Windows.  En outre, pour tirer parti du SDK WebView2 à partir des frameworks d’interface utilisateur, l’équipe WebView s’est séparée en `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] et [ICoreWebView2Host][Webview2ReferenceWin32Icorewebview2hostViewWebview209430].  `ICoreWebView2Host` prend en charge le re revirement, l’affichage et le masquage, la mise au point et d’autres fonctionnalités liées à la fenêtre et à la composition.  ICoreWebView2 prend en charge toutes les autres fonctionnalités WebView2.  Pour en savoir plus sur l’incorporation des [][GithubMicrosoftedgeWebview2samplesPr17] modifications, accédez à la demande de pull WebView2 dans le projet [APISample][GithubMicrosoftedgeWebview2samplesMain] WebView2.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Split [DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] en trois composants :  [SourceChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged], [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]et [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Maintenant, lorsque l’URL source change, `SourceChanged` l’événement est exécuté.  Lorsque l’état de l’historique est modifié, `HistoryChanged` l’événement est exécuté.  `ContentLoading`L’événement est exécuté avant le script initial lors du chargement d’un nouveau document.  
    
*   Prise en charge supplémentaire de l’architecture ARM64.  
*   Ajout de la prise en charge du panneau d’entrée (SIP)\) pour les périphériques d’écran tactile.  
*   Prise en charge supplémentaire de Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 et Windows Server 2016.  
*   Ajout de [NotifyParentWindowPositionChanged pour][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] que la barre d’état suive la fenêtre en mode fenêtre.  Implémenter également la modification en mode sans fenêtre pour que les fonctionnalités d’accessibilité fonctionnent.  
*   Ajout du [paramètre AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] pour contrôler globalement si une page web peut être accessible par des objets distants.  Par défaut, il est allumé, de sorte que les objets `AreRemoteObjectsAllowed` distants ajoutés par [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] sont accessibles à partir de la page web.  Quand `AreRemoteObjectsAllowed` il est désactivé, les objets ne sont pas accessibles à partir de la page web.  Les modifications sont appliquées à l’événement de navigation suivant.  
*   Ajout du [paramètre IsZoomControlEnabled][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] pour empêcher les utilisateurs d’avoir un impact sur le zoom du contrôle WebView à l’aide de `ctrl` + `+` `ctrl` + `-` \(ou + roulette `ctrl` de souris\).  Il se peut que le zoom soit toujours [put_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] lorsque le paramètre est désactivé.  
*   Modifié ZoomFactor pour s’appliquer uniquement au WebView actuel.  Les modifications de zoom apportées au WebView actuel n’affectent pas les autres affichages WebView que vous avez accédés à l’aide du même site d’origine.  Pour plus d’informations, [accédez à get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Interface utilisateur Hid ZoomView pour WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Ajout de [SetBoundsAndZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor].  Vous pouvez maintenant définir le facteur de zoom et les limites d’un élément WebView en même temps.  
*   Ajout de [l’événement WindowCloseRequested.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]  Pour plus d’informations, [accédez à add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Ajout de la prise en charge du type de boîte de dialogue pour les événements de boîte de dialogue JavaScript et ajout `beforeunload` CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD’entrée [][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] d’enum.  
*   Ajout de [GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] à HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] à HttpResponseHeaders et [get_HasCurrentHeader][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] à HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Modification de rupture**: comportement `DevToolsProtocolEventReceived` modifié.  Maintenant, vous pouvez créer un [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] pour un événement de protocole DevTools particulier et vous abonner/vous désabonner à cet événement à l’aide de [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived].  
    
*   > [!IMPORTANT]
    > **Modification de rupture**: `WebMessageReceivedEventArgs` [modification get_WebMessageAsString][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] propriété à une méthode [TryGetWebMessageAsString.][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]  
    
*   > [!IMPORTANT]
    > **Modification de la**rupture : modification `AcceleratorKeyPressedEventArgs` [de la][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] méthode Handle en [get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] propriété.  
    
## <a name="08355"></a>0.8.355  

[NuGet package][NuGetGallery0.8.355] \| Microsoft Edge version 80.0.355.0.  

*   Publication de l’exemple WebView2API, guide complet du SDK WebView2.  Pour plus d’informations, accédez à [l’exemple d’API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Ajout de la prise en charge de l’IME pour toutes les langues en plus de[l’anglais][GithubMicrosoftedgeWebviewfeedbackIssue30]\( #30 \).  
*   Mise à jour de la surface API de `WebResourceRequested` l’événement en réponse aux rapports de bogues.  La spécification simultanée d’un filtre et d’un événement lors de la création est désormais dépréciée.  Pour créer un événement de ressource web demandé, utilisez [add_WebResourceRequested][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] pour ajouter l’événement et [AddWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] pour ajouter un filtre.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] supprime le filtre \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Modification de la rupture**: modification du comportement en plein écran.  Estprecated [IsFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  À présent, par défaut, si un élément dans un contrôle WebView \(par exemple, une vidéo\) est mis en plein écran, il remplit les limites de WebView.  Utilisez [l’événement ContainsFullScreenElementChanged][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] et [get_ContainsFullScreenElement][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] pour spécifier comment l’application doit resizer le WebView si un élément souhaite entrer en mode plein écran.  
    
## <a name="08314"></a>0.8.314  

[NuGet package][NuGetGallery0.8.314] \| Microsoft Edge version 80.0.314.0.  

*   Prise en charge supplémentaire pour Windows 7, Windows 8 et Windows 8.1.  
*   Ajout de Visual Studio et Visual Studio Code de débogage pour WebView2.  À présent, déboguer votre script dans WebView2 directement à partir de votre IDE.  Pour plus d’informations, accédez [à Comment déboguer lors du développement avec des contrôles WebView2][Webview2HowToDebug].  
*   Ajout du script en cours d’exécution dans WebView2 pour accéder à un objet IDispatch à partir du composant Win32 de l’application et accéder aux propriétés de l’objet `Native Object Injection` IDispatch.  Pour plus d’informations, [accédez à AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Ajout `AcceleratorKeyPressed` d’un événement.  Pour plus d’informations, [accédez à add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Désactivé. `Context Menus`  Pour plus d’informations, [accédez à put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Mise à jour `DPI Awareness` .  À présent, la prise en compte des DPI de WebView est identique à la prise en compte des DPI de l’application hôte.  
    
    > [!NOTE]
    > Si une autre application hybride est lancée avec une sensibilisation DPI différente de celle du WebView d’origine, le nouveau WebView n’est pas lancé s’il s’agit du même `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Mise à jour de sorte que WebView2 rejette automatiquement les demandes d’autorisation de notification à l’invite du contenu `Notification Change Behavior` web hébergé dans Le WebView.  
    
## <a name="08270"></a>0.8.270  

[NuGet package][NuGetGallery0.8.270] \| Microsoft Edge version 78.0.270.0.  

*   Ajout `DocumentTitleChanged` d’un événement pour indiquer le changement de titre du document[\( \#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Ajout de `GetWebView2BrowserVersionInfo` l’API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Ajout `NewWindowRequested` d’un événement.  
*   Fonction mise `CreateWebView2EnvironmentWithDetails` à jour à `releaseChannelPreference` supprimer.  Pour plus d’informations sur `CreateWebView2EnvironmentWithDetails` la fonction, accédez [à CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Le remplacement des variables du Registre et de l’environnement est toujours pris en charge.  La préférence de canal par défaut est utilisée, sauf si elle est overridée.  
    Pendant la recherche de canal, l’équipe WebView ignore toute version précédente du canal qui n’est pas compatible avec le SDK WebView2.  
    L’équipe WebView sélectionne le canal le plus stable pour garantir les comportements les plus cohérents pour l’utilisateur final.  Lorsque vous testez les dernières builds canary, vous devez créer un script pour définir la variable d’environnement avant de `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` lancer l’application.  
*   Mise à jour de `CreateWebView2EnvironmentWithDetails` la fonction avec la logique de sélection `userDataFolder` lorsqu’elle n’est pas spécifiée.  Pour plus d’informations sur `CreateWebView2EnvironmentWithDetails` la fonction, accédez [à CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Si vous avez déjà utilisé l’emplacement par défaut, lorsque vous basculez vers le nouveau SDK, la valeur par défaut est reset \(définie sur un nouvel emplacement dans le répertoire de `userDataFolder` code hôte\) et votre état est également réinitialisé. `userDataFolder`  Si le processus hôte n’est pas autorisé à écrire dans le répertoire spécifié, la `CreateWebView2EnvironmentWithDetails` fonction peut échouer.  Vous pouvez copier les données de l’ancien `user data folder` dans le nouveau répertoire.  
    
## <a name="08230"></a>0.8.230  

[NuGet package][NuGetGallery0.8.230] \| Microsoft Edge version 77.0.230.0.  

*   Ajout de l’API pour arrêter toutes les navigations et les extractions de ressources en attente `Stop` \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Fichier `.tlb` ajouté au package NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Ajout de projets .NET à la liste du programme d’installation dans NuGet package \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## <a name="08190"></a>0.8.190  

[NuGet package][NuGetGallery0.8.190] \| Microsoft Edge version 77.0.190.0.  

*   Ajouté pour `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` contrôler si les utilisateurs peuvent ouvrir DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Ajouté pour contrôler si la barre d’état est affichée `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Ajouté pour `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` revenir en arrière et en avant via l’historique de navigation.  
*   Ajout des types d’en-tête HTTP \( \) pour l’affichage et la modification des en-têtes `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` HTTP dans WebView.  
*   Ajout de la prise en charge de WebView 32 bits sur les ordinateurs 64 bits[\( \#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Ajout de l’IDL WebView au SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Ajout de lib pour prendre en charge les `IID\_\*` objets d’ID d’interface \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Ajout du chemin d’accès, de la liaison et de l’auto-NuGet fichiers DLL dans `TARGET` le SDK.  
*   A désactivé la demande `window.open()` dans le script.  
    
## <a name="08149"></a>0.8.149  

[NuGet package][NuGetGallery0.8.149] \| Microsoft Edge version 76.0.149.0.  

Version d’évaluation initiale pour les développeurs.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Mode de distribution persistant : distribution des applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Mode de distribution de version fixe : distribution des applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Comprendre le runtime et le programme d’installation WebView2 - Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Stratégies de groupe pour WebView2 : gestion des applications WebView2 | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions de navigateur et les | WebView2 Documents Microsoft"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API expérimentales : comprendre les versions de navigateur et les | WebView2 Documents Microsoft"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Correspondance des versions d’runtime WebView2 : comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Mise en place de WebView2 dans Windows forms | Documents Microsoft"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Mise en place de WebView2 dans WPF | Documents Microsoft"  
[Webview2HowToDebug]: ./how-to/debug.md "Comment déboguer lors du développement avec des contrôles WebView2 | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental2?view=webview2-1.0.865-prerelease&preserve-view=true#add_downloadstarting  "add_DownloadStarting - interface ICoreWebView2Experimental2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment3?view=webview2-1.0.865-prerelease&preserve-view=true#updateruntime  "UpdateRuntime - interface ICoreWebView2ExperimentalEnvironment3 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalframe?view=webview2-1.0.865-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins  "AddHostObjectToScriptWithOrigins - interface ICoreWebView2ExperimentalFrame | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings4?view=webview2-1.0.865-prerelease&preserve-view=true#ispinchzoomenabled  "IsPinchZoomEnabled - interface ICoreWebView2ExperimentalSettings4 | Documents Microsoft" 

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings2?view=webview2-1.0.824&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed - interface ICoreWebView2ExperimentalSettings | Documents Microsoft" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - interface ICoreWebView2_2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping : interface ICoreWebView2_3 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend - interface ICoreWebview2_3 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled - interface ICoreWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "interface ICoreWebView2CompositionController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor - interface ICoreWebView2Controller2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest - interface ICoreWebView2Environment | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount - interface ICoreWebView2EnvironmentOptions | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments - interface ICoreWebView2EnvironmentOptions | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo - interface ICoreWebView2Environment | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString - interface ICoreWebView2Environment | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController3 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged - interface ICoreWebView2ExperimentalController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode - interface ICoreWebView2ExperimentalController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale - interface ICoreWebView2ExperimentalController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges - interface ICoreWebView2ExperimentalController | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled - interface ICoreWebView2ExperimentalEnvironmentOptions | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent - interface ICoreWebView2ExperimentalSettings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest - interface ICoreWebView2Experimental | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent - interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor - interface ICoreWebView2Host | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged - interface ICoreWebView2Host | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor - interface ICoreWebView2Host | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor - interface ICoreWebView2Host | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader - interface ICoreWebView2HttpHeadersCollectionIterator | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders - interface ICoreWebView2HttpRequestHeaders | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader - interface ICoreWebView2HttpResponseHeaders | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated interface ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled - interface ICoreWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled - interface ICoreWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed - interface ICoreWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - interface ICoreWebView2 | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString : interface ICoreWebView2WebMessageReceivedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke - interface ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Documents Microsoft" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle - interface IWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled - interface IWebView2Settings2 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated - interface IWebView2Settings | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString - interface IWebView2WebMessageReceivedEventArgs | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed - interface IWebView2WebView4 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject - interface IWebView2WebView4 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested - interface IWebView2WebView5 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter - interface IWebView2WebView5 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement - interface IWebView2WebView5 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter - interface IWebView2WebView5 | Documents Microsoft" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged - interface IWebView2WebView | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Documents Microsoft" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 - Stratégies | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft.Web.WebView2.Core | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Classe CoreWebView2 (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Classe CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Méthode CoreWebView2Environment.CompareBrowserVersions(String, String) (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Méthode CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Classe CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Classe CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Événement CoreWebView2.NewWindowRequested (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Événement CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Événement CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Événement CoreWebView2.WebResourceRequested (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Classe CoreWebView2InitializationCompletedEventArgs | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft.Web.WebView2.WinForms | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Classe CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Classe Webview2.Source (Microsoft.Web.WebView2.Winforms) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft.Web.WebView2.Wpf | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Méthode WebView2.BuildWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Méthode WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Documents Microsoft"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Classe CancelEventArgs (System.ComponentModel) | Documents Microsoft"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Classe EventArgs (système) | Documents Microsoft"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys à nom fort | Documents Microsoft"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protection d’application Microsoft Defender (Windows 10) : Windows sécurité | Documents Microsoft"  
[WindowsWin32ApiWinuserSetWindowDisplayAffinity]: /windows/win32/api/winuser/nf-winuser-setwindowdisplayaffinity "Fonction SetWindowDisplayAffinity (winuser.h) : applications Win32 | Documents Microsoft"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repo d’annonce pour MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2WpfBrowser "WebView2WpfBrowser - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Déplacer le projet pour utiliser le dernier SDK WebView2 0.9.430 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 878"  
[GithubMicrosoftedgeWebviewfeedbackIssue1120]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1120 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 1120"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 940"
[GithubMicrosoftedgeWebviewfeedbackIssue841]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/841 "Repo de commentaires pour le problème MicrosoftEdge/WebViewFeedback 841"
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 210"
[GithubMicrosoftedgeWebviewfeedbackIssue338]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/338 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 338"
[GithubMicrosoftedgeWebviewfeedbackIssue589]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/589 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 589"
[GithubMicrosoftedgeWebviewfeedbackIssue933]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/933 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 933"
[GithubMicrosoftedgeWebviewfeedbackIssue946]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/946 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 946"
[GithubMicrosoftedgeWebviewfeedbackIssue1011]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1011 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 1011"
[GithubMicrosoftedgeWebviewfeedbackIssue1050]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1050 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 1050"
[GithubMicrosoftedgeWebviewfeedbackIssue996]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/996 "Repo de commentaires pour MicrosoftEdge/WebViewFeedback Issue 996"
[GithubMicrosoftedgeWebviewfeedbackIssue850]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/850 "Repo de commentaires pour MicrosoftEdge/Problème WebViewFeedback 850"

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Annonce de la disponibilité générale de Microsoft Edge WebView2 pour .NET et la méthode de distribution fixe | blog .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Edge Développeur"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet Galerie | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet Galerie | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet Galerie | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet Galerie | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v0.9.515 prerelease"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet Galerie | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet Galerie | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet Galerie | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v0.9.628 prerelease"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v1.0.674 prerelease"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v1.0.721 prerelease"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v1.0.790 prerelease"  
[NuGetGallery1.0.818.41]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.818.41 "NuGet Galerie | Microsoft.Web.WebView2 v1.0.818.41"  
[NuGetGallery1.0.824-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.824-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v1.0.824 prerelease"  
[NuGetGallery1.0.865-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.865-prerelease "NuGet Galerie | Microsoft.Web.WebView2 v1.0.865 prerelease"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Annonce de la Microsoft Edge la disponibilité générale de WebView2 | Microsoft Edge Blog"  
