---
description: Notes de publication du SDK Microsoft Edge WebView2
title: Notes de publication de Microsoft Edge WebView2 pour Win32, WPF et WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2e5676870ecfb4c02130d61e94e762625a8d903a
ms.sourcegitcommit: 65db518273b3cd69f1b3c528809600719b9b70aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016318"
---
# Notes de publication pour WebView2 SDK  

L’équipe WebView2 fournit des mises à jour au [Kit de développement logiciel (SDK) WebView2][NuGetGallery] sur une cadence de six semaines.  Passez en revue le contenu suivant pour obtenir des informations à jour sur les annonces du produit, les ajouts et les modifications apportées à la surface d’API, et les changements de rupture.  

> [!NOTE]
> Recompilez votre application après avoir mis à jour le package NuGet.  

> [!IMPORTANT]
> Si WebView2 est une version d’évaluation, les API .NET se trouvent dans le menu `prerelease package` .  

## 0.9.628-version préliminaire  

Date de publication: 10 septembre 2020  

[Package NuGet][NuGetGallery0.9.628-prerelease] \ | version de Microsoft Edge 87.0.628.0 minimum.  

> [!IMPORTANT]
> **Annonce**: cette version préliminaire continue d’être mise à jour sur la base de la succursale Microsoft Edge 87.  À l’avenir, la version préliminaire du SDK correspond à la build des Canaries Microsoft Edge et la version normale est synchronisée avec Microsoft Edge stable.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: les API d’hébergement visuel apparaissent désormais sous aperçu.  WebView2 utilise l’hébergement visuel pour s’exécuter en même temps que des éléments visuels WinComp/DComp plutôt que des HWND.  Les interfaces se trouvent dans les expérimentaux.  Pour plus d’informations, accédez à [ICoreWebView2ExperimentalEnvironment][ReferenceWin3209622Icorewebview2experimentalenvironment].  

#### .NET  

*   Les fichiers binaires .NET sont désormais [fortement nommés][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   La cible NuGet mise à jour doit être incluse `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) et \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Mise à jour `WebResourceRequested` pour exposer les API [HttpRequestHeaders][ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httprequestheaders] et [HttpResponseHeaders][ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httpresponseheaders] dans .net.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622  

Date de publication: 10 septembre 2020  

[Package NuGet][NuGetGallery0.9.622.11] \ | version d’WebView2 Runtime minimum 86.0.622.11.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: ce kit de développement logiciel (SDK) est l’option release candidate pour WebView2 Win32 C/C++ GA.  La version GA doit utiliser la même interface API et fonctionnalités.  

*   [Stratégies de navigateur][DeployedgeMicrosoftEdgePolicies]connectées.  
*   La propriété [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount] a été ajoutée dans les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Mis à jour `ICoreWebView2NewWindowRequestedEventArgs` pour inclure la propriété [WindowFeatures][ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures] et le [ICoreWebView2WindowFeatures][ReferenceWin3209622Icorewebview2windowfeatures]associé.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Mise à jour `System.Windows.Rect`  à utiliser `System.Drawing.Rectangle` au lieu de `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Événement NewWindowRequested mis à jour pour gérer la `window.open()` requête sans paramètre.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Les [AdditionalBrowserArguments][ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments] Set using ne `ICoreWebView2EnvironmentOptions` sont pas substituées par la variable d’environnement et la valeur du Registre.  Pour plus d’informations, accédez à [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions].  

## 0.9.579  

Date de publication: 20 juillet 2020  

[Package NuGet][NuGetGallery0.9.579] \ | version de Microsoft Edge 86.0.579.0 minimum.  

#### Général  

*   > [!IMPORTANT]
    > **Annonce**: le runtime et le programme d’installation de WebView2 a été mis à la disposition de preview.  Pour plus d’informations, accédez à [distribution de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
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
*   Désactivation du bloqueur de fenêtres publicitaires dans WebView.  Pour plus d’informations, accédez à la propriété [IsUserInitiated][ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated] de l' `NewWindowRequested` événement.  
*   L’événement de début de la navigation dans l’affichage WebView est déclenché pour `about:blank` .  À présent, `NavigationStarting` les événements sont déclenchés pour l’ensemble de la navigation, mais les annulations de `about:blank` ou IFRAME srcdoc n’est pas prise en charge et ignorée.  
*   `edge:// URI`Schéma bloqué dans WebView.  
*   Ajout de propriété expérimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled] sur les options d’environnement WebView2 pour activer l’accès conditionnel pour WebView.  
*   Ajout d’un événement [WebResourceResponseReceived][ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived] expérimental qui se déclenche une fois que le WebView a reçu et traité la réponse à une demande de webressource.  Les en-têtes d’authentification, le cas échéant, sont inclus dans l’objet Response.  

#### .NET  

*   Amélioration de la gestion du focus WPF.  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Propriété added du contrôleur WEBVIEW2 WPF.  

## 0.9.538  

[Package NuGet][NuGetGallery0.9.538] \ | version de Microsoft Edge 85.0.538.0 minimum.  

#### Général  

*   Abandon du support pour WebView2 SDK version [0.8.149](#08149).  WebView2 vous recommande de rester à jour avec la dernière version d’WebView2.  
*   Stratégie de groupe mise à jour sur le compte lors de la[#179][GithubMicrosoftedgeWebviewfeedbackIssue179]modification du chemin de profil du navigateur Microsoft Edge  

#### Win32 C/C++  

*   Ajout de [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures], qui se déclenche lorsque `window.open()` est exécuté et associé à [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin3209538Icorewebview2experimentalwindowfeatures] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Changement de rupture**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] est déconseillé et remplacé par [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions]].  
*   > [!IMPORTANT]
    > **Modification**distante: pour veiller à ce que l’API WebView2 soit adaptée aux conventions d’affectation de noms des API Windows, l’équipe WebView a mis à jour les noms des éléments suivants.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed] est désormais [AreHostObjectsAllowed][ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed].  
*   Mise à jour de [AddHostObjectToScript][ReferenceWin3209538Icorewebview2Addhostobjecttoscript] pour garantir que les marqueurs d’objet hôte d’origine sont définis sur les objets proxy et sérialisés en tant qu’objet hôte lorsque ce paramètre est transmis en tant que paramètre dans le rappel JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (version préliminaire 0.9.538)  

*   Les exemples de WinForms et de WebView2API WPF, qui sont des guides complets du SDK WebView2.  Pour plus d’informations, accédez à [exemples de référentiel Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Ajout de la prise en charge des [API][ConceptsVersioningExperimentalApis]d’hébergement visuel et des fonctionnalités de fenêtre.  
*   > [!IMPORTANT]
    > **Changement de rupture**: les reports suivants implémentent désormais IDisposable:  [ScriptDialogOpening][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]et [PermissionRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   [GetAvailableBrowserVersionString][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] et [CompareBrowserVersions][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] ajoutés en tant que [CoreWebView2Environment][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment] Statics.  

## 0.9.515-version préliminaire  

[Package NuGet][NuGetGallery0.9.515-prerelease] \ | version de Microsoft Edge 84.0.515.0 minimum.  

*   > [!IMPORTANT]
    > **Annonce**: WebView2 prend désormais en charge Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .net Core 3,0 ou version ultérieure dans le **package de version préliminaire**.  
*   Pour plus d’informations sur la création d’applications WPF et la [référence WPF][ReferenceWpf09515Reference] WebView2 pour les API spécifiques de WPF, accédez au [Guide de mise en route de WPF][GettingstartedWpf].  
*   Pour plus d’informations sur la création d’applications Windows Forms et la [référence WebView2 Windows Forms][ReferenceWinforms09515Reference] pour les API spécifiques Windows Forms, voir le Guide de mise en route de [Windows Forms][GettingstartedWinforms].  
*   Pour plus d’informations sur les API CoreWebView2, accédez à [.net Reference][ReferenceDotnet09515Reference].  
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
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo] est désormais [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo] est désormais [get_BrowserVersionString][ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring].  
    > *   [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] est désormais [AddHostObjectToScript][ReferenceWin3209488Icorewebview2Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][ReferenceWin3209430Icorewebview2Removeremoteobject] est désormais [RemoveHostObjectFromScript][ReferenceWin3209488Icorewebview2Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` est maintenant `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Modification en rupture**: les `AddRemoteObject` méthodes proxy js sont également renommées.  
    > *   `getLocal` est maintenant `getLocalProperty` .  
    > *   `setLocal` est maintenant `setLocalProperty` .  
    > *   `getRemote` est maintenant `getHostProperty` .  
    > *   `setRemote` est maintenant `setHostProperty` .  
    > *   `applyRemote` est maintenant `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Changement de rupture**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] est déconseillé et remplacé par [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions].  
*   Un événement [FrameNavigationCompleted][ReferenceWin3209488Icorewebview2AddFramenavigationcompleted] a été ajouté.  À présent, quand un IFRAME effectue une navigation, un événement est déclenché et renvoie le succès de la navigation et de l’ID de navigation.  
*   Interface [ICoreWebView2EnvironmentOptions][ReferenceWin3209488Icorewebview2environmentoptions] ajoutée, qui est susceptible d’être utilisée pour déterminer la version de WebView2 Runtime ciblée par l’application.  
*   Ajout du paramètre [IsBuiltInErrorPageEnabled][ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled] .  À présent, vous pouvez choisir d’activer ou de désactiver la page d’erreur intégrée pour l’échec de la navigation et l’échec du processus de rendu.  
*   Mise à jour d’une injection d’objets distants pour prendre en charge les[#113][GithubMicrosoftedgeWebviewfeedbackIssue113]implémentations de .net IDispatch.  
*   Un événement [NewWindowRequested][ReferenceWin3209488Icorewebview2AddNewwindowrequested] mis à jour pour gérer les demandes des[#108][GithubMicrosoftedgeWebviewfeedbackIssue108]menus contextuels.  
*   A publié le premier package de version préliminaire de WebView2 à partir duquel vous pouvez accéder aux API d’hébergement visuel.  L’équipe WebView a mis à jour [APISample][GithubMicrosoftedgeWebview2samplesMain] pour inclure les nouvelles API expérimentales.  
    *   Interface [ICoreWebView2ExperimentalCompositionController][ReferenceWin3209488Icorewebview2experimentalcompositioncontroller] ajoutée, permettant de se connecter à une arborescence de composition et de fournir des informations pour le WebView.  
    *   Ajout de [ICoreWebView2ExperimentalPointerInfo][ReferenceWin3209488Icorewebview2experimentalpointerinfo]contenant toutes les informations de a `POINTER_INFO` .  Cet objet est transmis à SendPointerInput pour injecter des entrées de pointeur dans le WebView.  
    *   Ajout de [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler], qui indique à l’application quand le curseur de la souris au-dessus de l’affichage doit être modifié.  Lorsque le pointeur de la souris se trouve sur une zone de texte sur le WebView, le curseur se transforme en flèche du sélecteur.  La `cursor` propriété de l' `CompositionController` élément indique à l’application ce qu’il doit actuellement pour le pointeur de la souris pour le WebView.  

## 0.9.430  

[Package NuGet][NuGetGallery0.9.430] \ | version de Microsoft Edge 82.0.430.0 minimum.  

Le kit de développement logiciel (SDK) WebView2 est la version bêta officielle de Win32 C++ qui incorpore plusieurs demandes de fonctionnalité à partir de commentaires.  L’équipe WebView tente de limiter le nombre de libérations avec des modifications importantes, mais dans la mesure où la disponibilité générale est apportée, la version bêta est utilisée pour incorporer plusieurs variations majeures majeures dans une feuille de passe.  

*   > [!IMPORTANT]
    > **Modification**distante: en tant que version finale, l’équipe WebView a renommé le préfixe *IWebView2WebView*   en *ICoreWebView2*   afin de vous assurer que l’API WebView2 s’aligne sur la Convention d’affectation de noms des API Windows.  Par ailleurs, pour tirer parti du SDK WebView2 des infrastructures d’interface utilisateur, l’équipe WebView est divisée `ICoreWebView2` en [ICoreWebView2][ReferenceWin3209430Icorewebview2] et [ICoreWebView2Host][ReferenceWin3209430Icorewebview2host].  `ICoreWebView2Host` prend en charge le redimensionnement, l’affichage et le masquage, le focus et d’autres fonctionnalités liés à la fenêtre et à la composition.  ICoreWebView2 prend en charge toutes les autres fonctionnalités de WebView2.  Pour en savoir plus sur l’intégration des modifications, accédez à la [demande de collecte][GithubMicrosoftedgeWebview2samplesPr17] de WebView2 dans le projet [APISample][GithubMicrosoftedgeWebview2samplesMain] WebView2.  
*   > [!IMPORTANT]
    > **Changement de rupture**: fractionner [DocumentStateChanged][ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged] en trois composants:  [SourceChanged][ReferenceWin3209430Icorewebview2AddSourcechanged], [ContentLoading][ReferenceWin3209430Icorewebview2AddContentloading]et [HistoryChanged][ReferenceWin3209430Icorewebview2AddHistorychanged].  À présent, lorsque l’URL source change, l' `SourceChanged` événement est déclenché.  Lorsque l’état de l’historique est modifié `HistoryChanged` , l’événement est déclenché.  L' `ContentLoading` événement est déclenché avant le script initial lors du chargement d’un nouveau document.  
*   Ajout de la prise en charge de l’architecture ARM64.  
*   Ajout de la prise en charge du panneau de saisie (SIP \) pour les appareils à écran.  
*   Ajout de la prise en charge de Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 et Windows Server 2016.  
*   Ajout de [NotifyParentWindowPositionChanged][ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged] qui permet à la barre d’état de suivre la fenêtre en mode fenêtre.  La modification doit également être implémentée en mode sans fenêtre afin que les fonctionnalités d’accessibilité fonctionnent.  
*   Ajout d’un paramètre [AreRemoteObjectsAllowed][ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed] pour contrôler globalement s’il est possible d’accéder à une page par tous les objets distants.  Par défaut, `AreRemoteObjectsAllowed` est activé, ce qui signifie que les objets distants ajoutés par [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] sont accessibles à partir de la page.  Lorsque `AreRemoteObjectsAllowed` est désactivé, les objets ne sont pas accessibles à partir de la page.  Les modifications sont appliquées lors de l’événement de navigation suivant.  
*   Ajout du paramètre [IsZoomControlEnabled][ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled] pour empêcher les utilisateurs d’influer sur le zoom du WebView à l’aide de `ctrl` + `+` et `ctrl` + `-` \ (ou `ctrl` + molette de la souris).  Le zoom peut toujours être défini à l’aide de [put_ZoomFactor][ReferenceWin3209430Icorewebview2hostPutZoomfactor] lorsque le paramètre est désactivé.  
*   ZoomFactor modifié s’applique uniquement au WebView actuel.  Les modifications apportées à l’affichage WebView actuel n’ont aucun impact sur les autres webvues sur lesquelles vous avez navigué vers le même site d’origine.  Pour plus d’informations, accédez à [get_ZoomFactor][ReferenceWin3209430Icorewebview2hostGetZoomfactor].  
*   Interface utilisateur ZoomView HID pour WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Ajout de [SetBoundsAndZoomFactor][ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor].  Vous pouvez maintenant définir le facteur de zoom et les limites d’un élément WebView en même temps.  
*   Un événement [WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] a été ajouté.  Pour plus d’informations, accédez à [add_WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Ajout de la prise en charge du `beforeunload` type de boîte de dialogue pour les événements de boîte de dialogue JavaScript et ajoutés [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind] entrée d’énumération.  
*   A ajouté [GetHeaders][ReferenceWin3209430Icorewebview2httprequestheadersGetheaders] à HttpRequestHeaders, [GetHeader][ReferenceWin3209430Icorewebview2httpresponseheadersGetheader] à HttpResponseHeaders et [get_HasCurrentHeader][ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader] propriété à HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Modification rupture**: `DevToolsProtocolEventReceived` comportement modifié.  Vous pouvez maintenant créer un [DevToolsProtocolEventReceiver][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver] pour un événement de protocole devtools particulier et vous abonner/vous désabonner à un événement à l’aide de [add_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived].
*   > [!IMPORTANT]
    > **Modification de rupture**: modification de WebMessageReceivedEventArgs' [get_WebMessageAsString][ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring] propriété sur une méthode [TryGetWebMessageAsString][ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring] .  
*   > [!IMPORTANT]
    > **Modification en rupture**: `AcceleratorKeyPressedEventArgs` méthode de [handle][ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle] modifiée sur une propriété de [get_Handled][ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled] .  

## 0.8.355

[Package NuGet][NuGetGallery0.8.355] \ | version de Microsoft Edge 80.0.355.0 minimum.

*   Exemple de WebView2API de parution, guide complet du SDK WebView2.  Pour plus d’informations, accédez à [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Ajout de la prise en charge IME pour toutes les langues autres que l’anglais \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Mise à jour de la surface de l’API de l' `WebResourceRequested` événement en réponse aux rapports de bogues.  La spécification simultanée d’un filtre et un événement lors de la création est désormais déconseillé.  Pour créer un événement de ressource Web demandé, utilisez [add_WebResourceRequested][ReferenceWin3208190Iwebview2webview5AddWebresourcerequested] pour ajouter l’événement et [AddWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter] pour ajouter un filtre.  [RemoveWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter] supprime le filtre \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Modification**distante: comportement fullscreen modifié.  [IsFullScreenAllowed][ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]déconseillé.  Par défaut, si un élément au sein d’un WebView (par exemple, une vidéo) est défini en mode plein écran, il remplit les limites du WebView.  Utilisez l’événement [ContainsFullScreenElementChanged][ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler] et [get_ContainsFullScreenElement][ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement] pour spécifier la façon dont l’application doit redimensionner le WebView si un élément veut entrer en mode plein écran.  

## 0.8.314  

[Package NuGet][NuGetGallery0.8.314] \ | version de Microsoft Edge 80.0.314.0 minimum.  

*   Ajout de la prise en charge de Windows 7, Windows 8 et Windows 8,1.  
*   Ajout de la prise en charge du débogage de code Visual Studio et Visual Studio pour WebView2.  Maintenant, déboguez votre script dans le WebView2 directement à partir de votre IDE.  Pour plus d’informations, accédez au [débogage lors du développement avec des contrôles WebView2][HowtoDebug].  
*   Ajouté `Native Object Injection` , ce qui permet au script qui s’exécute dans WebView2 d’accéder à un objet IDispatch à partir du composant Win32 de l’application et d’accéder aux propriétés de l’objet IDispatch.  Pour plus d’informations, accédez à [AddRemoteObject][ReferenceWin3208190Iwebview2webview4Addremoteobject] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   `AcceleratorKeyPressed`Événement ajouté.  Pour plus d’informations, accédez à [add_AcceleratorKeyPressed][ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Désactivé `Context Menus` .  Pour plus d’informations, accédez à [put_AreDefaultContextMenusEnabled][ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Mise à jour `DPI Awareness` .  À présent, la prise en charge des résolutions du WebView est identique à celle de l’application hôte.  
    
    > [!NOTE]
    > Si une autre application hybride est lancée à l’aide d’une sensibilité différente de celle du WebView d’origine, le nouveau WebView n’est pas lancé si le répertoire de données utilisateur est le même \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Mis à jour `Notification Change Behavior` de telle sorte que WebView2 rejette automatiquement les demandes d’autorisation de notification par le contenu Web hébergé sur le WebView.  

## 0.8.270  

[Package NuGet][NuGetGallery0.8.270] \ | version de Microsoft Edge 78.0.270.0 minimum.  

*   Un événement a été ajouté `DocumentTitleChanged` pour indiquer le changement de titre du document \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   `GetWebView2BrowserVersionInfo`API ajoutée \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   `NewWindowRequested`Événement ajouté.  
*   Fonction Updated `CreateWebView2EnvironmentWithDetails` à supprimer `releaseChannelPreference` .  Pour plus d’informations sur la `CreateWebView2EnvironmentWithDetails` fonction, accédez à [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Le remplacement de la variable de Registre et de l’environnement est toujours pris en charge.  La préférence de canal par défaut est utilisée sauf si elle est ignorée.  
    Lors de la recherche de canal, l’équipe WebView ignore toute version antérieure du canal qui n’est pas compatible avec le kit de développement logiciel (SDK) WebView2.  
    L’équipe WebView sélectionne le canal plus stable pour garantir des comportements les plus cohérents pour l’utilisateur final.  Lorsque vous testez avec les versions les plus récentes des Canaries, vous devez créer un script pour définir la `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` variable d’environnement `1` avant de lancer l’application.  
*   Mise à jour de la `CreateWebView2EnvironmentWithDetails` fonction avec la logique permettant de sélectionner `userDataFolder` lorsqu’elle n’est pas spécifiée.  Pour plus d’informations sur la `CreateWebView2EnvironmentWithDetails` fonction, accédez à [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Si vous avez déjà utilisé l' `userDataFolder` emplacement par défaut, lorsque vous basculez vers le nouveau kit de développement logiciel (SDK), la valeur par défaut `userDataFolder` est Reset \ (définie à un nouvel emplacement dans le répertoire de code hôte \) et votre état est également réinitialisé.  
    Si le processus hôte n’est pas autorisé à écrire dans le répertoire spécifié, la `CreateWebView2EnvironmentWithDetails` fonction peut échouer.  Vous pouvez copier les données de l’ancien répertoire de données utilisateur vers le nouvel annuaire.  

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
*   Un chemin d’accès d’inclusion, de liaison et de copie automatique de fichiers DLL ont été ajoutés au `TARGET` fichier NuGet dans le SDK.  
*   Activation de la requête `window.open()` dans le script.  

## 0.8.149  

[Package NuGet][NuGetGallery0.8.149] \ | version de Microsoft Edge 76.0.149.0 minimum.  

Version préliminaire du développeur  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Mode de distribution persistant: distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./concepts/distribution.md#understand-the-webview2-runtime-and-installer-preview "Comprendre le runtime et le programme d’installation WebView2 (Preview)-distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[ConceptsVersioning]: ./concepts/versioning.md "Présentation des versions de navigateur et de WebView2 | Documents Microsoft"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API expérimentales-présentation des versions de navigateur et WebView2 | Documents Microsoft"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Commencer à utiliser WebView2 dans les applications Windows Forms | Documents Microsoft"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF | Documents Microsoft"  
[HowtoDebug]: ./howto/debug.md "Comment déboguer lorsque vous développez avec des contrôles WebView2 | Documents Microsoft"  

[ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle]: ./reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle "Handle-interface IWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft"  
[ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler]: ./reference/win32/0-8-190/iwebview2containsfullscreenelementchangedeventhandler.md "interface IWebView2ContainsFullScreenElementChangedEventHandler | Documents Microsoft"  
[ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled]: ./reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-interface IWebView2Settings2 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]: ./reference/win32/0-8-190/iwebview2settings.md#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-interface IWebView2Settings | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring]: ./reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring "get_WebMessageAsString-interface IWebView2WebMessageReceivedEventArgs | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed]: ./reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed "add_AcceleratorKeyPressed-interface IWebView2WebView4 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged]: ./reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged "add_DocumentStateChanged-interface IWebView2WebView | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview4Addremoteobject]: ./reference/win32/0-8-190/iwebview2webview4.md#addremoteobject "AddRemoteObject-interface IWebView2WebView4 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview5AddWebresourcerequested]: ./reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested "add_WebResourceRequested-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement]: ./reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement "get_ContainsFullScreenElement-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-interface IWebView2WebView5 | Documents Microsoft"  
[ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails]:  ./reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-global | Documents Microsoft"  

[ReferenceWin3209430Icorewebview2]: ./reference/win32/0-9-430/icorewebview2.md "interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled]: ./reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled "get_Handled-interface ICoreWebView2AcceleratorKeyPressedEventArgs | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2AddContentloading]: ./reference/win32/0-9-430/icorewebview2.md#add_contentloading "add_ContentLoading-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2AddHistorychanged]: ./reference/win32/0-9-430/icorewebview2.md#add_historychanged "add_HistoryChanged-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2Addremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#addremoteobject "AddRemoteObject-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2AddSourcechanged]: ./reference/win32/0-9-430/icorewebview2.md#add_sourcechanged "add_SourceChanged-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2AddWindowcloserequested]: ./reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested "add_WindowCloseRequested-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind]: ./reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md "interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo]: ./reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo "get_BrowserVersionInfo-interface ICoreWebView2Environment | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2host]: ./reference/win32/0-9-430/icorewebview2host.md "interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo]: ./reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-global | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2hostGetZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor "get_ZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged]: ./reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2hostPutZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor "put_ZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor "SetBoundsAndZoomFactor-interface ICoreWebView2Host | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader]: ./reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader "get_HasCurrentHeader-interface ICoreWebView2HttpHeadersCollectionIterator | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2httprequestheadersGetheaders]: ./reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders "GetHeaders-interface ICoreWebView2HttpRequestHeaders | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2httpresponseheadersGetheader]: ./reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader "GetHeader-interface ICoreWebView2HttpResponseHeaders | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2Removeremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#removeremoteobject "RemoveRemoteObject-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled]: ./reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled "get_IsZoomControlEnabled-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring]: ./reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring "TryGetWebMessageAsString-interface ICoreWebView2WebMessageReceivedEventArgs | Documents Microsoft"  

[ReferenceWin3209488Icorewebview2AddFramenavigationcompleted]: ./reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted "add_FrameNavigationCompleted-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2AddNewwindowrequested]: ./reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested "add_NewWindowRequested-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring]: ./reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring " | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2environmentoptions]: ./reference/win32/0-9-488/icorewebview2environmentoptions.md "interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcompositioncontroller]: ./reference/win32/0-9-488/icorewebview2experimentalcompositioncontroller.md "interface ICoreWebView2ExperimentalCompositionController | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]: ./reference/win32/0-9-488/icorewebview2experimentalcursorchangedeventhandler.md "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalpointerinfo]: ./reference/win32/0-9-488/icorewebview2experimentalpointerinfo.md "interface ICoreWebView2ExperimentalPointerInfo | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2Removehostobjectfromscript]: ./reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript "RemoveHostObjectFromScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled]: ./reference/win32/0-9-488/icorewebview2settings.md#get_isbuiltinerrorpageenabled " | Documents Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-global | Documents Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Documents Microsoft"  
[ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring]: ./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-global | Documents Microsoft"  

[ReferenceDotnet09515Reference]: ./reference/dotnet/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWinforms09515Reference]: ./reference/winforms/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[ReferenceWpf09515Reference]: ./reference/wpf/0-9-515-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  


[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment | Documents Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions "CompareBrowserVersions-Microsoft. Web. WebView2. Core. CoreWebView2Environment classe | Documents Microsoft"
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring "GetAvailableBrowserVersionString-Microsoft. Web. WebView2. Core. CoreWebView2Environment classe | Documents Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested "NewWindowRequested-Microsoft. Web. WebView2. Core. CoreWebView2 classe | Documents Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested "PermissionRequested-Microsoft. Web. WebView2. Core. CoreWebView2 classe | Documents Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening "ScriptDialogOpening-Microsoft. Web. WebView2. Core. CoreWebView2 classe | Documents Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested "WebResourceRequested-Microsoft. Web. WebView2. Core. CoreWebView2 classe | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-interface ICoreWebView2 | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived]: ./reference/win32/0-9-538/icorewebview2experimental.md#add_webresourceresponsereceived "add_WebResourceResponseReceived-interface ICoreWebView2Experimental | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled]: ./reference/win32/0-9-538/icorewebview2experimentalenvironmentoptions.md#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-interface ICoreWebView2ExperimentalEnvironmentOptions | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalwindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md "interface ICoreWebView2ExperimentalWindowFeatures | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated]: ./reference/win32/0-9-538/icorewebview2newwindowrequestedeventargs.md#get_isuserinitiated "interface get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed]: ./reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed "get_AreHostObjectsAllowed-interface ICoreWebView2Settings | Documents Microsoft"  
[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Documents Microsoft"  

[ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount]: ./reference/win32/0-9-622/icorewebview2environmentoptions.md#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments]: ./reference/win32/0-9-622/icorewebview2environmentoptions.md#put_additionalbrowserarguments "put_AdditionalBrowserArguments-interface ICoreWebView2EnvironmentOptions | Documents Microsoft"  
[ReferenceWin3209622Icorewebview2experimentalenvironment]: ./reference/win32/0-9-622/icorewebview2experimentalenvironment.md "interface ICoreWebView2ExperimentalEnvironment | Documents Microsoft"  
[ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-622/icorewebview2newwindowrequestedeventargs.md#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2NewWindowRequestedEventArgs | Documents Microsoft"  
[ReferenceWin3209622Icorewebview2windowfeatures]: ./reference/win32/0-9-622/icorewebview2windowfeatures.md "interface ICoreWebView2WindowFeatures | Documents Microsoft"  
[ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-622/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-global | Microsoft Edge"  

[ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httprequestheaders]: ./reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2httprequestheaders.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders | Documents Microsoft"  
[ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: ./reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2httpresponseheaders.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders | Documents Microsoft"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-stratégies | Documents Microsoft"  

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
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 185"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 235"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 318"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Déplacer Project pour utiliser la dernière version du SDK WebView2 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemple d’API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

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
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 0.9.628"  
