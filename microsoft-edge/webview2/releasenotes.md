---
description: Notes de publication du SDK Microsoft Edge WebView2
title: Notes de publication de Microsoft Edge WebView2 pour Win32, WPF et WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: f0ddcbfe2d72c1285e6d4a42c3cb796b93495c55
ms.sourcegitcommit: 652c345b46aae8b7e3723eb55a01b71a4ef76bf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191442"
---
# Notes de publication pour WebView2 SDK  

L’équipe WebView2 met à jour le [SDK WebView2][NuGetGallery] sur une cadence de six semaines.  Passez en revue le contenu suivant pour obtenir des informations à jour sur les annonces produits, les ajouts, les modifications et les modifications apportées aux API.  

> [!NOTE]
> Recompilez votre application après avoir mis à jour le package NuGet.  

## 1.0.707-version préliminaire  

Date de publication: 23 novembre 2020  

[Package NuGet][NuGetGallery1.0.707-prerelease] \ | version de Microsoft Edge 86.0.616.0 minimum.  

#### Général  

###### Fonctionnalités  

*   Ajout de [stratégies de groupe WebView2][DeployedgeMicrosoftEdgeWebviewPolicies].  Pour plus d’informations sur les pratiques recommandées, accédez à [stratégies de groupe pour WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Modification en rupture**: déconseillé l’ancien emplacement du Registre.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
     
*   Ajout de la prise en charge de la [& glisser][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] dans WebView2.  
*   API ajoutées pour gérer la prise en charge des DPI.  
    *   A ajouté la propriété [RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetRasterizationscale] pour modifier l’échelle PPP pour le contenu WebView et les fenêtres contextuelles d’interface utilisateur, et événement [RasterizationScaleChanged][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseAddRasterizationscalechanged] associé.  
    *   Propriété [ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetShouldDetectMonitorScaleChanges] ajoutée pour mettre à jour automatiquement la `RasterizationScale` propriété si nécessaire.  
    *   La [propriété BoundsMode][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetBoundsMode] a été ajoutée pour spécifier que les limites sont des pixels de logique et permettre à WebView d’utiliser l' `RasterizationScale` affichage de pixels pour WebView2, et que le WebView applique la `RasterizationScale` `Bounds` taille physique.
*   Événement Updated `NewWindowRequested` pour gérer `Ctrl` + `click` et `Shift` + `click` .  \ ([\ #168][GithubMicrosoftedgeWebviewfeedbackIssue168] et [\ #371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  

#### .NET  

###### Fonctionnalités  

*   Activez le concepteur WinForms dans .NET Core 3.1 + et .NET 5.  
*   Amélioration de la gestion des cookies .NET.  \ ([\ #611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Renommé `CoreWebView2Ready` [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].

###### Correction de bogues

*   Un événement [AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] a été ajouté pour prendre en charge AcceleratorKey la pression dans WebView2.  \ ([\ #288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Suppression de fichiers inutiles de la sortie dans dossiers WebView2.  \ ([\ #461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API d’objet hôte améliorées.  \ ([\ #335][GithubMicrosoftedgeWebviewfeedbackIssue335] et [\ #525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  

## 1.0.664.37  

Date de publication: 20 novembre 2020  

[Package NuGet][NuGetGallery1.0.664.37] \ | version d’WebView2 Runtime minimum 86.0.616.0.  

#### Général  

> [!IMPORTANT]
> **Annonce**: .net WPF/WinForms WebView2 est désormais disponible dans le pays suivant:  À partir de cette version, les SDK de publication sont compatibles en avant.  Pour plus d’informations, accédez au billet de [blog d’annonce GA][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod].  

###### Fonctionnalités  

*   .NET WPF/WinForms WebView2 est désormais disponible dans la version actuelle.  
*   Le mode de distribution fixe \ (faire-votre propre \) a atteint la disponibilité.  

#### .NET  

###### Correction de bogues  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` empêche l’ouverture de nouvelle fenêtre \ ([\ #549][GithubMicrosoftedgeWebviewfeedbackIssue549]\) et \ ([\ #560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  


## 1.0.674-version préliminaire  

Date de publication: 19 octobre 2020  

[Package NuGet][NuGetGallery1.0.674-prerelease] \ | version d’WebView2 Runtime minimum 86.0.616.0.  

#### Général  

*   Ajout de la méthode [NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] qui vous permet de fournir des données de publication ou des en-têtes de requête supplémentaires lors de la navigation.
*   Un événement [DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] a été ajouté qui s’exécute lors du chargement et de l’analyse du document HTML initial.
*   A ajouté la propriété [Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] sur WebView2.  Cette propriété expose l’environnement WebView2 où une instance de WebView2 a été créée.
*   Ajout d’API de [gestion des cookies][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] permettant aux développeurs d’authentifier la session WebView2, ou de récupérer des cookies du WebView pour authentifier d’autres outils.  Nous envisageons d’apporter des améliorations spécifiques à la langue et à l’infrastructure.  Pour plus d’informations, accédez à [révision des API: gestion des cookies][GithubMicrosoftedgeWebview2AnnouncementIssue2].
*   Mise à jour de l’événement [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] , et ajout d’un [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] inaltérable et de [WebResourceResponseReceivedEventArgs::P opulateresponsecontent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] de devenir [WebResourceResponseView:: getContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].
*   Avez désactivé [Microsoft Defender application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] dans WebView2.
*   Ajout de [SystemCursorId][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] pour l’hébergement visuel.
*   Ajout d’une correction corrigée pour la méthode d’entrée dans l’hébergement visuel.
*   Les développeurs n’ont plus besoin d’inclure version. lib lors de l’utilisation de la bibliothèque statique WebView2.

#### .NET  

*   Classe [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] mise à jour pour exposer la variable CoreWebView2Environment.  
*   Les implémentations de classes EventArgs personnalisées dans l’espace de noms sont modifiées en tant que sous `Microsoft.Web.WebView2.Core` -classes de [System. EventArgs][DotnetApiSystemEventargs] ou [System. ComponentModel. CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \ ([\ #250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Ajout de la prise en charge de [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] dans WinForms.  \ ([\ #204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   Ajout d’API .NET [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .  \ ([\ #219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Mise à jour de la propriété [source][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] du concepteur WinForms sur la valeur par défaut ou la valeur null.  \ ([\ #177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Les limites de WebView2 mises à jour dans WebView2.Init () pour prendre en charge les modes PPP dont la taille est inférieure à 100%.  \ ([\ #432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Mise à jour de [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] et de [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] pour une fiabilité accrue.  \ ([\ #382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Mise à jour de la base du chargeur .NET pour charger le processus au lieu de l’architecture du système d’exploitation.  \ ([\ #431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Renommé `EdgeNotFoundExpection` [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].
 
## 1.0.622.22  

Date de publication: 19 octobre 2020  

[Package NuGet][NuGetGallery1.0.622.22] \ | version d’WebView2 Runtime minimum 86.0.616.0.  

#### Général  

> [!IMPORTANT]
> **Annonce**: Win32 C/C++ WebView2 est désormais disponible dans le pays suivant:  À partir de cette version, les SDK de publication sont compatibles en avant.  Pour plus d’informations, accédez au billet de [blog d’annonce GA][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*  Le [programme d’exécution et de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller]  Le programme d’amorçage, le lien en liaison descendante pour le programme d’amorçage et le programme d’installation autonome pour le runtime persistant sont disponibles dans [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Des exemples de code pour le flux de travail d’installation sont également disponibles dans le [référentiel Samples WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*  Le [mode de version fixe][Webview2ConceptsDistributionFixedVersionMode] est disponible pour la version préliminaire du développeur.  

## 0.9.628-version préliminaire  

Date de publication: 10 septembre 2020  

[Package NuGet][NuGetGallery0.9.628-prerelease] \ | version de Microsoft Edge 86.0.616.0 minimum.  

> [!IMPORTANT]
> **Annonce**: cette version préliminaire continue d’être mise à jour sur la base de la succursale Microsoft Edge 87.  À l’avenir, la version préliminaire du SDK correspond à la build des Canaries Microsoft Edge et la version normale est synchronisée avec Microsoft Edge stable.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: les API d’hébergement visuel apparaissent désormais sous aperçu.  WebView2 utilise l’hébergement visuel pour s’exécuter en même temps que des éléments visuels WinComp/DComp plutôt que des HWND.  Les interfaces se trouvent dans les expérimentaux.  Pour plus d’informations, accédez à [ICoreWebView2ExperimentalEnvironment][ReferenceWin32Icorewebview2experimentalenvironment09628].  

#### .NET  

*   Les fichiers binaires .NET sont désormais [fortement nommés][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   La cible NuGet mise à jour doit être incluse `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) et \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Mise à jour `WebResourceRequested` pour exposer les API [HttpRequestHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders] et [HttpResponseHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders] dans .net.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622.11  

Date de publication: 10 septembre 2020  

[Package NuGet][NuGetGallery0.9.622.11] \ | version d’WebView2 Runtime minimum 86.0.616.0.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: ce kit de développement logiciel (SDK) est l’option release candidate pour WebView2 Win32 C/C++ GA.  La version GA doit utiliser la même interface API et fonctionnalités.  

*   [Stratégies de navigateur][DeployedgeMicrosoftEdgePolicies]connectées.  
*   La propriété [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] a été ajoutée dans les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Mis à jour `ICoreWebView2NewWindowRequestedEventArgs` pour inclure la propriété [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] et le [ICoreWebView2WindowFeatures][ReferenceWin32Icorewebview2windowfeatures09622]associé.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Mise à jour `System.Windows.Rect`  à utiliser `System.Drawing.Rectangle` au lieu de `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Événement NewWindowRequested mis à jour pour gérer la `window.open()` requête sans paramètre.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Les [AdditionalBrowserArguments][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] définis à l’aide `ICoreWebView2EnvironmentOptions` d’une variable d’environnement ou de valeurs de registre ne sont pas ignorées.  Pour plus d’informations, accédez à [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  

## 0.9.579  

Date de publication: 20 juillet 2020  

[Package NuGet][NuGetGallery0.9.579] \ | version de Microsoft Edge 86.0.579.0 minimum.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: le runtime et le programme d’installation de WebView2 a été mis à la disposition de preview.  Pour plus d’informations, accédez à [distribution de WebView2] [Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
*   > [!IMPORTANT]
    > **Annonce**: les versions de kit de développement logiciel (SDK) WebView2 suivantes ne sont plus prises en charge après la publication du SDK suivant.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Les versions du kit de développement logiciel (SDK) WebView2 sont également marquées comme déconseillées sur nuget.org.  WebView2 vous recommande de rester à jour avec la dernière version d’WebView2.  

*   Ajout d’amélioration du thread du travailleur WebView.  \ ([\ #318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Désactivation du bloqueur de fenêtres publicitaires dans WebView.  Pour plus d’informations, accédez à la propriété [IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] de l' `NewWindowRequested` événement.  
*   L’événement de début de la navigation dans l’affichage WebView est déclenché pour `about:blank` .  À présent, `NavigationStarting` les événements sont déclenchés pour l’ensemble de la navigation, mais les annulations `about:blank` ou IFRAME srcdoc ne sont pas pris en charge et ignorés.  
*   `edge:// URI`Schéma bloqué dans WebView.  
*   Ajout de propriété expérimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] sur les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Ajout d’un événement [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] expérimental qui se déclenche une fois que le WebView a reçu et traité la réponse à une demande de webressource.  Les en-têtes d’authentification, le cas échéant, sont inclus dans l’objet Response.  

#### .NET  

*   Amélioration de la gestion du focus WPF.  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Propriété added du contrôleur WEBVIEW2 WPF.  

## 0.9.538  

[Package NuGet][NuGetGallery0.9.538] \ | version de Microsoft Edge 85.0.538.0 minimum.  

#### Général  

*   Abandon du support pour WebView2 SDK version [0.8.149](#08149).  WebView2 vous recommande de rester à jour avec la dernière version d’WebView2.  
*   Stratégie de groupe mise à jour sur le compte lors de la[#179][GithubMicrosoftedgeWebviewfeedbackIssue179]modification du chemin de profil du navigateur Microsoft Edge  

#### Win32 C/C++  

*   Ajout de [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538], qui se déclenche lorsque `window.open()` est exécuté et associé à [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Modification en rupture**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] déconseillée et remplacée par [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
*   > [!IMPORTANT]
    > **Modification**distante: pour veiller à ce que l’API WebView2 soit adaptée aux conventions d’affectation de noms des API Windows, l’équipe WebView a mis à jour les noms des éléments suivants.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] est désormais [AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
*   Mise à jour de [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538] pour garantir que les marqueurs d’objet hôte d’origine sont définis sur les objets proxy et sérialisés en tant qu’objet hôte lorsque ce paramètre est transmis en tant que paramètre dans le rappel JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (version préliminaire 0.9.538)  

*   Les exemples de WinForms et de WebView2API WPF, qui sont des guides complets du SDK WebView2.  Pour plus d’informations, accédez à [exemples de référentiel Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Ajout de la prise en charge des [API][ConceptsVersioningExperimentalApis]d’hébergement visuel et des fonctionnalités de fenêtre.  
*   > [!IMPORTANT]
    > **Changement de rupture**: les reports suivants implémentent désormais IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]et [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] et [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] ajoutés en tant que [CoreWebView2Environment][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] Statics.  

## 0.9.515-version préliminaire  

[Package NuGet][NuGetGallery0.9.515-prerelease] \ | version de Microsoft Edge 84.0.515.0 minimum.  

*   > [!IMPORTANT]
    > **Annonce**: WebView2 prend désormais en charge Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .net Core 3,0 ou version ultérieure dans le **package de version préliminaire**.  
*   Pour plus d’informations sur la création d’applications WPF, accédez au [Guide de mise en route de WPF][GettingstartedWpf] et à la [référence WPF][DotnetApiMicrosoftWebWebview2Wpf] WebView2 pour les API spécifiques de WPF.  
*   Pour plus d’informations sur la création d’applications Windows Forms, voir le [Guide de mise en route de Windows Forms][GettingstartedWinforms] et la [référence Windows Forms][DotnetApiMicrosoftWebWebview2Winforms] WebView2 pour les API spécifiques de Windows Forms.  
*   Pour plus d’informations sur les API CoreWebView2, accédez à [.net Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problèmes connus**: l’équipe WebView est consciente de certains problèmes dans la version préliminaire qui sont résolus dans les versions ultérieures.  
    > *   **Dpi Awareness**: WEBVIEW2 pour WPF n’est pas pris en charge par PPP.  Lors de l’initialisation de WebView2 sur les écrans haute résolution, il existe un problème connu qui consiste à initialiser le WebView à la première initialisation en tant que fraction de la fenêtre jusqu’à ce que la fenêtre soit redimensionnée.  
    > *   **Concepteur WPF**: le Concepteur WPF n’est pas pris en charge pour le moment.  Ajoutez le contrôle WebView2 dans votre application en modifiant directement le code XAML approprié dans un éditeur de texte.  

## 0.9.488  

[Package NuGet][NuGetGallery0.9.488] \ | version de Microsoft Edge 84.0.488.0 minimum.  

*   > [!IMPORTANT]
    > **Annonce**: à partir de la version 83 de Microsoft Edge version, le WebView persistant ne cible plus le canal de navigateur stable.  Au lieu de cela, il cible un autre jeu de fichiers binaires ( [WebView2][ConceptsDistributionEvergreenMode]), que vous pouvez mettre en chaîne pour l’installation par le biais d’un programme d’installation que l’équipe WebView développe actuellement.  Pour plus d’informations, accédez à [application-distribution][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Annonce**: à l’avenir, l’équipe WebView publie deux packages: un package précommercial avec des API d’expérimentation \ (pour vous en tester \) et un package de publication stable avec des API stables (pour votre confiance \).  Pour en savoir plus sur les différences, voir [Présentation des versions du navigateur et WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Modification**distante: afin de garantir que l’API WebView2 s’aligne sur les conventions d’affectation de noms des API Windows, l’équipe WebView a mis à jour les noms des interfaces suivantes.  
    > *   `CORE_WEBVIEW2_*` le préfixe est désormais `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] est désormais [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] est désormais [get_BrowserVersionString][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488].  
    > *   [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] est désormais [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] est désormais [RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` est maintenant `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Modification en rupture**: les `AddRemoteObject` méthodes proxy js sont également renommées.  
    > *   `getLocal` est maintenant `getLocalProperty` .  
    > *   `setLocal` est maintenant `setLocalProperty` .  
    > *   `getRemote` est maintenant `getHostProperty` .  
    > *   `setRemote` est maintenant `setHostProperty` .  
    > *   `applyRemote` est maintenant `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Modification en rupture**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] déconseillée et remplacée par [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
*   Un événement [FrameNavigationCompleted][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488] a été ajouté.  À présent, quand un IFRAME effectue une navigation, un événement est déclenché et renvoie le succès de la navigation et de l’ID de navigation.  
*   Interface [ICoreWebView2EnvironmentOptions][ReferenceWin32Icorewebview2environmentoptions09488] ajoutée, qui est susceptible d’être utilisée pour déterminer la version de WebView2 Runtime ciblée par l’application.  
*   Ajout du paramètre [IsBuiltInErrorPageEnabled][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488] .  À présent, vous pouvez choisir d’activer ou de désactiver la page d’erreur intégrée pour l’échec de la navigation et l’échec du processus de rendu.  
*   Mise à jour d’une injection d’objets distants pour prendre en charge les `IDispatch` [#113][GithubMicrosoftedgeWebviewfeedbackIssue113]implémentations .net.  
*   Un événement [NewWindowRequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] mis à jour pour gérer les demandes des[#108][GithubMicrosoftedgeWebviewfeedbackIssue108]menus contextuels.  
*   A publié le premier package de version préliminaire de WebView2 à partir duquel vous pouvez accéder aux API d’hébergement visuel.  L’équipe WebView a mis à jour [APISample][GithubMicrosoftedgeWebview2samplesMain] pour inclure les nouvelles API expérimentales.  
    *   Interface [ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] ajoutée, permettant de se connecter à une arborescence de composition et de fournir des informations pour le WebView.  
    *   Ajout de [ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488]contenant toutes les informations de a `POINTER_INFO` .  Cet objet est transmis à SendPointerInput pour injecter des entrées de pointeur dans le WebView.  
    *   Ajout de [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488], qui indique à l’application quand le curseur de la souris au-dessus de l’affichage doit être modifié.  Lorsque le pointeur de la souris se trouve sur une zone de texte sur le WebView, le curseur se transforme en flèche du sélecteur.  La `cursor` propriété de l' `CompositionController` élément indique à l’application ce qu’il doit actuellement pour le pointeur de la souris pour le WebView.  

## 0.9.430  

[Package NuGet][NuGetGallery0.9.430] \ | version de Microsoft Edge 82.0.430.0 minimum.  

Le kit de développement logiciel (SDK) WebView2 est la version bêta officielle de Win32 C++ qui incorpore plusieurs demandes de fonctionnalité à partir de commentaires.  L’équipe WebView tente de limiter le nombre de libérations avec les changements de rupture.  Dans la mesure où nous utilisons une disponibilité générale, il est possible d’intégrer de nombreuses modifications importantes dans la version bêta.  

*   > [!IMPORTANT]
    > **Modification**distante: en tant que version finale, l’équipe WebView a renommé le préfixe *IWebView2WebView*   en *ICoreWebView2*   afin de vous assurer que l’API WebView2 s’aligne sur la Convention d’affectation de noms des API Windows.  Par ailleurs, pour tirer parti du SDK WebView2 des infrastructures d’interface utilisateur, l’équipe WebView est divisée `ICoreWebView2` en [ICoreWebView2][ReferenceWin32Icorewebview209430] et [ICoreWebView2Host][ReferenceWin32Icorewebview2host09430].  `ICoreWebView2Host` prend en charge le redimensionnement, l’affichage et le masquage, le focus et d’autres fonctionnalités liés à la fenêtre et à la composition.  ICoreWebView2 prend en charge toutes les autres fonctionnalités de WebView2.  Pour en savoir plus sur l’intégration des modifications, accédez à la [demande de collecte][GithubMicrosoftedgeWebview2samplesPr17] de WebView2 dans le projet [APISample][GithubMicrosoftedgeWebview2samplesMain] WebView2.  
*   > [!IMPORTANT]
    > **Changement de rupture**: fractionner [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] en trois composants:  [SourceChanged][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]et [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  À présent, lorsque l’URL source change, l' `SourceChanged` événement est déclenché.  Lorsque l’état de l’historique est modifié `HistoryChanged` , l’événement est déclenché.  L' `ContentLoading` événement est déclenché avant le script initial lors du chargement d’un nouveau document.  
*   Ajout de la prise en charge de l’architecture ARM64.  
*   Ajout de la prise en charge du panneau de saisie (SIP \) pour les appareils à écran.  
*   Ajout de la prise en charge de Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 et Windows Server 2016.  
*   Ajout de [NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430], qui permet à la barre d’état de suivre la fenêtre en mode fenêtre.  Vous pouvez également implémenter cette modification en mode sans fenêtre afin que les fonctionnalités d’accessibilité fonctionnent.  
*   Ajout d’un paramètre [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] pour contrôler globalement s’il est possible d’accéder à une page par tous les objets distants.  Par défaut, `AreRemoteObjectsAllowed` est activé, ce qui signifie que les objets distants ajoutés par [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] sont accessibles à partir de la page.  Lorsque `AreRemoteObjectsAllowed` est désactivé, les objets ne sont pas accessibles à partir de la page.  Les modifications sont appliquées lors de l’événement de navigation suivant.  
*   Ajout du paramètre [IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] pour empêcher les utilisateurs d’influer sur le zoom du WebView à l’aide de `ctrl` + `+` et `ctrl` + `-` \ (ou `ctrl` + molette de la souris).  Le zoom peut toujours être défini à l’aide de [put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] lorsque le paramètre est désactivé.  
*   ZoomFactor modifié s’applique uniquement au WebView actuel.  Les modifications apportées à l’affichage WebView actuel n’ont aucun impact sur les autres vues Web que vous avez naviguées sur le même site d’origine.  Pour plus d’informations, accédez à [get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430].  
*   Interface utilisateur ZoomView HID pour WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Ajout de [SetBoundsAndZoomFactor][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430].  Vous pouvez maintenant définir le facteur de zoom et les limites d’un élément WebView en même temps.  
*   Un événement [WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] a été ajouté.  Pour plus d’informations, accédez à [add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Ajout de la prise en charge du `beforeunload` type de boîte de dialogue pour les événements de boîte de dialogue JavaScript et ajoutés [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] entrée d’énumération.  
*   A ajouté [GetHeaders][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] à HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] à HttpResponseHeaders et [get_HasCurrentHeader][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] propriété à HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Modification rupture**: `DevToolsProtocolEventReceived` comportement modifié.  Vous pouvez maintenant créer un [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] pour un événement de protocole devtools particulier et vous abonner/vous désabonner à un événement à l’aide de [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].
*   > [!IMPORTANT]
    > **Modification en rupture**: modification `WebMessageReceivedEventArgs` de [get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] propriété sur une méthode [TryGetWebMessageAsString][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430] .  
*   > [!IMPORTANT]
    > **Modification en rupture**: `AcceleratorKeyPressedEventArgs` méthode de [handle][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] modifiée sur une propriété de [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] .  

## 0.8.355

[Package NuGet][NuGetGallery0.8.355] \ | version de Microsoft Edge 80.0.355.0 minimum.

*   Exemple de WebView2API de parution, guide complet du SDK WebView2.  Pour plus d’informations, accédez à [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Ajout de la prise en charge IME pour toutes les langues autres que l’anglais \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Mise à jour de la surface de l’API de l' `WebResourceRequested` événement en réponse aux rapports de bogues.  La spécification simultanée d’un filtre et un événement lors de la création est désormais déconseillé.  Pour créer un événement de ressource Web demandé, utilisez [add_WebResourceRequested][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] pour ajouter l’événement et [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] pour ajouter un filtre.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] supprime le filtre \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Modification**distante: comportement fullscreen modifié.  [IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]déconseillé.  Par défaut, si un élément au sein d’un WebView (par exemple, une vidéo) est défini en mode plein écran, il remplit les limites du WebView.  Utilisez l’événement [ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] et [get_ContainsFullScreenElement][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] pour spécifier la façon dont l’application doit redimensionner le WebView si un élément veut entrer en mode plein écran.  

## 0.8.314  

[Package NuGet][NuGetGallery0.8.314] \ | version de Microsoft Edge 80.0.314.0 minimum.  

*   Ajout de la prise en charge de Windows 7, Windows 8 et Windows 8,1.  
*   Ajout de la prise en charge du débogage de code Visual Studio et Visual Studio pour WebView2.  Maintenant, déboguez votre script dans le WebView2 directement à partir de votre IDE.  Pour plus d’informations, accédez au [débogage lors du développement avec des contrôles WebView2][HowtoDebug].  
*   Ajouté `Native Object Injection` , ce qui permet au script qui s’exécute dans WebView2 d’accéder à un objet IDispatch à partir du composant Win32 de l’application et d’accéder aux propriétés de l’objet IDispatch.  Pour plus d’informations, accédez à [AddRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   `AcceleratorKeyPressed`Événement ajouté.  Pour plus d’informations, accédez à [add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Désactivé `Context Menus` .  Pour plus d’informations, accédez à [put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Mise à jour `DPI Awareness` .  À présent, la prise en charge des résolutions du WebView est identique à celle de l’application hôte.  
    
    > [!NOTE]
    > Si une autre application hybride est lancée à l’aide d’une sensibilité différente de celle du WebView d’origine, le nouveau WebView n’est pas lancé si le répertoire de données utilisateur est le même \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Mis à jour `Notification Change Behavior` de telle sorte que WebView2 rejette automatiquement les demandes d’autorisation de notification par le contenu Web hébergé sur le WebView.  

## 0.8.270  

[Package NuGet][NuGetGallery0.8.270] \ | version de Microsoft Edge 78.0.270.0 minimum.  

*   Un événement a été ajouté `DocumentTitleChanged` pour indiquer le changement de titre du document \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   `GetWebView2BrowserVersionInfo`API ajoutée \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   `NewWindowRequested`Événement ajouté.  
*   Fonction Updated `CreateWebView2EnvironmentWithDetails` à supprimer `releaseChannelPreference` .  Pour plus d’informations sur la `CreateWebView2EnvironmentWithDetails` fonction, accédez à [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Le remplacement de la variable de Registre et de l’environnement est toujours pris en charge.  La préférence de canal par défaut est utilisée sauf si elle est ignorée.  
    Lors de la recherche de canal, l’équipe WebView ignore toute version précédente du canal qui n’est pas compatible avec le kit de développement logiciel (SDK) WebView2.  
    L’équipe WebView sélectionne le canal plus stable pour garantir des comportements les plus cohérents pour l’utilisateur final.  Lorsque vous testez avec les versions les plus récentes des Canaries, vous devez créer un script pour définir la `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` variable d’environnement `1` avant de lancer l’application.  
*   Mise à jour de la `CreateWebView2EnvironmentWithDetails` fonction avec la logique permettant de sélectionner `userDataFolder` lorsqu’elle n’est pas spécifiée.  Pour plus d’informations sur la `CreateWebView2EnvironmentWithDetails` fonction, accédez à [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Si vous avez déjà utilisé l' `userDataFolder` emplacement par défaut, lorsque vous basculez vers le nouveau kit de développement logiciel (SDK), la valeur par défaut `userDataFolder` est Reset \ (définie à un nouvel emplacement dans le répertoire de code hôte \) et votre état est également réinitialisé.  
    Si le processus hôte n’est pas autorisé à écrire dans le répertoire spécifié, la `CreateWebView2EnvironmentWithDetails` fonction risque d’échouer.  Vous pouvez copier les données de l’ancien répertoire de données utilisateur vers le nouvel annuaire.  

## 0.8.230  

[Package NuGet][NuGetGallery0.8.230] \ | version de Microsoft Edge 77.0.230.0 minimum.  

*   `Stop`API ajoutée pour arrêter toutes les extractions de ressources de navigation et en attente \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   `.tlb`Fichier ajouté au package NuGet \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Ajout de projets .NET à la liste du programme d’installation du package NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Package NuGet][NuGetGallery0.8.190] \ | version de Microsoft Edge 77.0.190.0 minimum.  

*   Ajouté `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` pour contrôler si les utilisateurs peuvent ouvrir devtools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` A ajouté pour contrôler la présence de la barre d’État \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Ajouté `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` pour revenir en arrière et transférer via l’historique de navigation.  
*   A ajouté des types d’en-tête http \ ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) pour afficher et modifier les en-têtes HTTP dans WebView.  
*   Ajout de la prise en charge du WebView 32 sur les[#13][GithubMicrosoftedgeWebviewfeedbackIssue13]ordinateurs 64  
*   Un IDL WebView a été ajouté au kit de développement logiciel ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Ajout de lib pour prendre en charge les `IID\_\*` objets d’ID d’interface \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Un chemin d’accès d’inclusion, de liaison et de copie de fichiers DLL a été ajouté au `TARGET` fichier NuGet dans le SDK.  
*   Activation de la requête `window.open()` dans le script.  

## 0.8.149  

[Package NuGet][NuGetGallery0.8.149] \ | version de Microsoft Edge 76.0.149.0 minimum.  

Version préliminaire du développeur  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Mode de distribution de version fixe: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Comprendre le runtime et l’installation de WebView2-distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Stratégies de groupe pour WebView2-gestion des applications WebView2 Documents Microsoft"  
[ConceptsVersioning]: ./concepts/versioning.md "Présentation des versions de navigateur et de WebView2 | Documents Microsoft"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API expérimentales-présentation des versions de navigateur et WebView2 | Documents Microsoft"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Commencer à utiliser WebView2 dans les applications Windows Forms | Documents Microsoft"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF | Documents Microsoft"  
[HowtoDebug]: ./howto/debug.md "Comment déboguer lorsque vous développez avec des contrôles WebView2 | Documents Microsoft"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle-interface IWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Documents Microsoft"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-interface IWebView2Settings2 | Documents Microsoft"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-interface IWebView2Settings | Documents Microsoft"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString-interface IWebView2WebMessageReceivedEventArgs | Documents Microsoft"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed-interface IWebView2WebView4 | Documents Microsoft"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged-interface IWebView2WebView | Documents Microsoft"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject-interface IWebView2WebView4 | Documents Microsoft"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-global | Documents Microsoft"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled-interface ICoreWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo-interface ICoreWebView2Environment | Documents Microsoft"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-global | Documents Microsoft"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader-interface ICoreWebView2HttpHeadersCollectionIterator | Documents Microsoft"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders-interface ICoreWebView2HttpRequestHeaders | Documents Microsoft"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader-interface ICoreWebView2HttpResponseHeaders | Documents Microsoft"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString-interface ICoreWebView2WebMessageReceivedEventArgs | Documents Microsoft"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Documents Microsoft"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Documents Microsoft"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Documents Microsoft"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Documents Microsoft"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-global | Documents Microsoft"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Documents Microsoft"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-global | Documents Microsoft"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged-interface ICoreWebView2ExperimentalController | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode-interface ICoreWebView2ExperimentalController | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale-interface ICoreWebView2ExperimentalController | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges-interface ICoreWebView2ExperimentalController | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Espace de noms Microsoft. Web. WebView2. Core | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espace de noms Microsoft. Web. WebView2. WPF | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espace de noms Microsoft. Web. WebView2. WinForms | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2. WebView2RuntimeNotFound (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Classe CoreWebView2 (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Classe CoreWebView2Environment (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment. CompareBrowserVersions (chaîne, chaîne) méthode (Microsoft. Web. WebView2. Core) | Documents Microsoft"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Méthode CoreWebView2Environment. GetAvailableBrowserVersionString (String) (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Événement CoreWebView2. NewWindowRequested (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Événement CoreWebView2. PermissionRequested (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Événement CoreWebView2. ScriptDialogOpening (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Événement CoreWebView2. WebResourceRequested (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Classe CoreWebView2HttpRequestHeaders (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Classe CoreWebView2HttpResponseHeaders (Microsoft. Web. WebView2. Core) | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Classe CoreWebView2CreationProperties (Microsoft. Web. WebView2. WinForms) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Classe Webview2. source (Microsoft. Web. WebView2. WinForms) | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Méthode WebView2. BuildWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Méthode WebView2. DestroyWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "Microsoft. Web. webview2. WPF. webview2. acceleratorkeypressed | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Classe CoreWebView2InitializationCompletedEventArgs | Documents Microsoft"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-interface ICoreWebView2ExperimentalEnvironmentOptions | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Documents Microsoft"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "interface get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Documents Microsoft"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments-interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Documents Microsoft"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalEnvironment | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent-interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Documents Microsoft"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent-interface ICoreWebView2ExperimentalWebResourceResponseView | Documents Microsoft"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.707-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController3 | Documents Microsoft"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2-stratégies | Documents Microsoft"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender application Guard (Windows 10)-sécurité Windows | Documents Microsoft"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Classe CancelEventArgs (System. ComponentModel) | Documents Microsoft"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Classe EventArgs (système) | Documents Microsoft"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys avec nom fort | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 250"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 288"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 611"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Annonce référentiel samples pour MicrosoftEdge/WebViewAnnouncement problème 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Déplacer Project pour utiliser la dernière version du SDK WebView2 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Annonce de la disponibilité générale de Microsoft Edge WebView2 pour .NET et de la méthode de distribution fixe | blog .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Développeur pour Microsoft Edge"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galerie NuGet | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Galerie NuGet | Microsoft. Web. WebView2 v 1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Galerie NuGet | Microsoft. Web. WebView2 v 1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Galerie NuGet | Microsoft. Web. WebView2 v 1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 1.0.674"  
[NuGetGallery1.0.707-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.707-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 1.0.707"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Annonce de la disponibilité générale de Microsoft Edge WebView2 | Blog Microsoft Edge"  
