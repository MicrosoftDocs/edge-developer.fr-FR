---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Notes de publication de Microsoft Edge WebView2 pour Win32, WPF et WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 4a1eb48270e062838fee9223d0a6e0e59505278e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697321"
---
# Notes de publication pour WebView2 SDK  

L’équipe WebView2 fournira des mises à jour au [Kit de développement logiciel (SDK) WebView2][WebView2NuGetGallery] sur une cadence de 6 jours. Cette page vous permet de mettre à jour les éléments suivants: annonces de produit, ajouts et modifications apportées à la surface d’API et changements de rupture.

> [!IMPORTANT]
> Recompilez votre application après avoir mis à jour le package NuGet.

## 0.9.538

[Package NuGet][WebView2NuGetGallery0.9.538] | version de Microsoft Edge 85.0.538.0 minimum.

#### Général

* Suppression de la prise en charge du SDK version [0.8.149](#08149). Nous vous recommandons de rester à jour avec la dernière version de WebView2.
* Stratégie de groupe mise à jour sur le compte lors de la modification du chemin de profil du navigateur Microsoft Edge ([#179](https://github.com/MicrosoftEdge/WebViewFeedback/issues/179))

#### Win32 C/C++

* Ajout de [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures](reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures) qui se déclenche lorsque Window. Open () est appelé et [ICoreWebView2ExperimentalWindowFeatures](reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md)associé. ([#70](https://github.com/MicrosoftEdge/WebViewFeedback/issues/70))
* **Changement de rupture:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) a été déconseillé et remplacé par [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions)
* **Modification en rupture:** Pour vous assurer que notre API s’aligne sur les conventions d’affectation des API Windows, nous avons mis à jour les noms des éléments suivants:
  * [AreRemoteObjectsAllowed](reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed) est maintenant [AreHostObjectsAllowed](reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed)
* Mise à jour de [AddHostObjectToScript](reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript) pour garantir que les marqueurs de sérialiseurs d’objet d’origine sont définis sur les objets proxy et sérialisés en tant qu’objet hôte lorsqu’il est transmis en tant que paramètre dans le rappel JavaScript. ([#148](https://github.com/MicrosoftEdge/WebViewFeedback/issues/148))

#### .NET

* Des exemples de mise en logiciel de WebView2API et d’affichage de contenus sont des guides complets du SDK. Consultez la rubrique [exemples d’WebView2 référentiel Samples](https://github.com/MicrosoftEdge/WebView2Samples).
* Ajout de la prise en charge des [API](./concepts/versioning.md#experimental-apis) d’hébergement visuel et des fonctionnalités de fenêtre
* **Modification en rupture:** Les reports suivants implémentent désormais IDisposable: [ScriptDialogOpening](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening), [NewWindowRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested), [WebResourceRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested)et [PermissionRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested).
* [GetAvailableBrowserVersionString](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring) et [CompareBrowserVersions](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions) ajoutés en tant que [CoreWebView2Environment](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) Statics.

## 0.9.515-version préliminaire

[Package NuGet][WebView2NuGetGallery0.9.515-prerelease] | version de Microsoft Edge 84.0.515.0 minimum.

* **Annonce:** WebView2 prend désormais en charge Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .NET Core 3,0 ou version ultérieure dans la **version préliminaire du package** .
* Extraire le [Guide de mise en route de WPF](./gettingstarted/wpf.md) pour commencer à créer des applications WPF et notre [référence WPF](./reference/wpf/0-9-515-reference-webview2.md) pour les API spécifiques de WPF
* Extraire le Guide de mise en route de [Windows Forms](./gettingstarted/winforms.md) pour commencer à créer des applications Windows Forms et notre [référence Windows Forms](./reference/winforms/0-9-515-reference-webview2.md) pour les API spécifiques Windows Forms
* Extraire des [références .net](./reference/dotnet/0-9-515-reference-webview2.md) pour les API CoreWebView2
* **Problèmes connus:** Nous sommes au courant de certains problèmes dans cette version préliminaire que nous allons résoudre dans les futures versions
  * Compatibilité **PPP:** WebView2 pour WPF n’est actuellement pas compatible avec DPI. Lors de l’initialisation de WebView2 sur les écrans haute résolution, il existe un problème connu qui consiste à initialiser le WebView à la première initialisation en tant que fraction de la fenêtre jusqu’à ce que la fenêtre soit redimensionnée.
  * **Concepteur WPF:** Pour le moment, cette version ne prend pas en charge le Concepteur WPF. Placez le contrôle WebView2 dans votre application en modifiant directement le code XAML approprié dans un éditeur de texte.

## 0.9.488

[Package NuGet][WebView2NuGetGallery0.9.488] | version de Microsoft Edge 84.0.488.0 minimum.

* **Annonce:** À partir de la version 83 de Microsoft Edge, le NetView persistant ne ciblera plus le canal de navigateur stable. Au lieu de cela, il cible un autre jeu de fichiers binaires ( [Microsoft Edge WebView2 Runtime](./concepts/distribution.md#microsoft-edge-webview2-runtime)) qui peut être installé en chaîne par le biais d’un programme d’installation que nous développons actuellement. Informations supplémentaires dans [distribution](./concepts/distribution.md)de l’application.
* **Annonce:** À l’avenir, nous allons procéder à la publication de deux packages: un package préliminaire doté d’API expérimentales (à des fins d’évaluation) et d’un package de publication stable avec des API stables (vous pouvez dépendre). Pour en savoir plus sur les différences, consultez le [Kit de développement logiciel (SDK) Microsoft Edge WebView2](./concepts/versioning.md) .
* **Modification en rupture:** Pour vous assurer que notre API s’aligne sur les conventions d’affectation des API Windows, nous avons mis à jour les noms des interfaces suivantes:
  * Le préfixe CORE_WEBVIEW2_ * est désormais COREWEBVIEW2_ *.
  * [GetCoreWebView2BrowserVersionInfo](reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo) est maintenant [GetAvailableCoreWebView2BrowserVersionString](reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)
  * [get_BrowserVersionInfo](reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo) est désormais [get_BrowserVersionString](reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring)
  * [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) est maintenant [AddHostObjectToScript](reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript)
  * [RemoveRemoteObject](reference/win32/0-9-430/icorewebview2.md#removeremoteobject) est maintenant [RemoveHostObjectFromScript](reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript)
  * chrome. WebView. remoteObjects est désormais chrome. WebView. hostObjects
* **Modification en rupture:** Les méthodes de proxy de AddRemoteObject JS ont été également renommées.
  * getLocal est désormais getLocalProperty
  * setLocal est désormais setLocalProperty
  * getRemote est maintenant getHostProperty
  * setRemote est maintenant setHostProperty
  * applyRemote est maintenant applyHostFunction
* **Changement de rupture:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) est désormais déconseillé et a été remplacé par [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).  
* Un événement [FrameNavigationCompleted](reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted) a été ajouté. À présent, quand un IFRAME effectue une navigation, un événement est déclenché et renvoie le succès de la navigation et de l’ID de navigation.
* Interface [ICoreWebView2EnvironmentOptions](reference/win32/0-9-488/ICoreWebView2EnvironmentOptions.md) ajoutée qui peut être utilisée pour déterminer la version de WebView2 Runtime ciblée par l’application.
* Ajout du paramètre [IsBuiltInErrorPageEnabled](reference/win32/0-9-488/ICoreWebView2Settings.md#get_isbuiltinerrorpageenabled) . À présent, vous pouvez choisir d’activer ou de désactiver la page d’erreur intégrée pour l’échec de la navigation et l’échec du processus de rendu.
* Mise à jour d’une injection d’objets distants pour prendre en charge les implémentations de .NET IDispatch. ([#113](https://github.com/MicrosoftEdge/WebViewFeedback/issues/113))
* Événement [NewWindowRequested](reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested) mis à jour pour gérer les demandes des menus contextuels. ([#108](https://github.com/MicrosoftEdge/WebViewFeedback/issues/108))
* Nous avons publié notre premier package précommercial pour lequel vous pouvez accéder aux API d’hébergement visuel. Nous avons mis à jour [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) pour inclure ces nouvelles API expérimentales.
  * Interface [ICoreWebView2ExperimentalCompositionController](reference/win32/0-9-488/ICoreWebView2ExperimentalCompositionController.md) ajoutée, qui est utilisée pour la connexion à une arborescence de composition et l’entrée de données pour le WebView.
  * Ajout de [ICoreWebView2ExperimentalPointerInfo](reference/win32/0-9-488/ICoreWebView2ExperimentalPointerInfo.md) contenant toutes les informations d’une POINTER_INFO. Il est transmis à SendPointerInput pour injecter des entrées de pointeur dans le WebView.
  * Ajout de [ICoreWebView2ExperimentalCursorChangedEventHandler](reference/win32/0-9-488/ICoreWebView2ExperimentalCursorChangedEventHandler.md) qui indique à l’application quand le curseur de la souris au-dessus de l’affichage doit être modifié. Lorsque le pointeur de la souris se trouve sur une zone de texte sur le WebView, le curseur se transforme en flèche du sélecteur. La propriété Cursor de CompositionController indique à l’application ce qu’il doit actuellement pour le pointeur de la souris pour le WebView.

## 0.9.430

[Package NuGet][WebView2NuGetGallery0.9.430] | version de Microsoft Edge 82.0.430.0 minimum.

Ce kit de développement logiciel (SDK) est une version bêta Win32 en C++ qui incorpore plusieurs demandes de fonctionnalités que nous avons reçues. Nous avons essayé de limiter le nombre de libérations, mais, à l’approche de notre disponibilité générale, nous utilisons notre version bêta pour intégrer plusieurs variations majeures majeures en une seule fois.

* **Modification en rupture:**  À l’approche de notre version finale, nous avons renommé le préfixe *IWebView2WebView* en *ICoreWebView2* afin de vous assurer que notre API s’aligne sur la Convention d’affectation de noms des API Windows. Par ailleurs, pour rendre notre SDK extensible pour une utilisation par les infrastructures d’interface utilisateur, nous avons séparé ICoreWebView2 en [ICoreWebView2](reference/win32/0-9-430/icorewebview2.md) et [ICoreWebView2Host](reference/win32/0-9-430/icorewebview2host.md). ICoreWebView2Host prend en charge le redimensionnement, l’affichage et le masquage, le focus et d’autres fonctionnalités liés à la fenêtre et à la composition. ICoreWebView2 prend en charge toutes les autres fonctionnalités de WebView2. Pour en savoir plus sur l’intégration de ces modifications, consultez notre [demande d’extraction](https://github.com/MicrosoftEdge/WebView2Samples/pull/17) dans le projet [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) .
* **Modification en rupture:** Fractionnez [DocumentStateChanged](reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged) en trois composants: [SourceChanged](reference/win32/0-9-430/icorewebview2.md#add_sourcechanged), [ContentLoading](reference/win32/0-9-430/icorewebview2.md#add_contentloading)et [HistoryChanged](reference/win32/0-9-430/icorewebview2.md#add_historychanged). À présent, lorsque l’URL source change, l’événement SourceChanged est déclenché. Lorsque l’état de l’historique est modifié, l’événement HistoryChanged est déclenché. L’événement ContentLoading est déclenché avant le script initial lors du chargement d’un nouveau document.
* Ajout de la prise en charge de l’architecture ARM64
* Ajout de la prise en charge du panneau de saisie (SIP) pour les appareils à écran
* Ajout de la prise en charge des `Windows Server 2008 R2` , `Windows Server 2012/2012 R2` et `Windows Server 2016`
* Ajout de [NotifyParentWindowPositionChanged](reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged) qui permet à la barre d’état de suivre la fenêtre en mode fenêtre. Vous devez également implémenter en mode sans fenêtre pour que les fonctionnalités d’accessibilité fonctionnent.
* Ajout d’un paramètre [AreRemoteObjectsAllowed](reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed) pour contrôler globalement s’il est possible d’accéder à une page par tous les objets distants. Par défaut, AreRemoteObjectsAllowed est activé, ce qui signifie que les objets distants ajoutés par [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) sont accessibles à partir de la page. Lorsque AreRemoteObjectsAllowed est désactivée, les objets ne sont pas accessibles à partir de la page. Les modifications sont appliquées lors de l’événement de navigation suivant.
* Ajout du paramètre [IsZoomControlEnabled](reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled) pour empêcher les utilisateurs d’influer sur le zoom de l’affichage WebView à l’aide de ou de la `ctrl`  +  `+` / `-` `ctrl` roulette de la souris. Le zoom peut toujours être défini via [put_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor) lorsque ce paramètre est désactivé.  
* ZoomFactor modifié s’applique uniquement au WebView actuel. Les modifications apportées à l’affichage WebView actuel n’ont aucun impact sur les autres webvues qui se trouvent sur le même site d’origine. Pour en savoir plus, voir [get_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor) .
* Interface utilisateur ZoomView HID pour WebView. ([#95](https://github.com/MicrosoftEdge/WebViewFeedback/issues/95))
* Ajout de [SetBoundsAndZoomFactor](reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor). Vous pouvez à présent définir le facteur de zoom et les limites d’un élément WebView en même temps.
* Un événement [WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) a été ajouté. Pour en savoir plus, voir [add_WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . ([#119](https://github.com/MicrosoftEdge/WebViewFeedback/issues/119))
* Ajout de la prise en charge du type de boîte de dialogue beforeunload pour les événements de boîte de dialogue JavaScript et ajoutés [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD](reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind) entrée d’énumération.
* A ajouté [GetHeaders](reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders) à HttpRequestHeaders, [GetHeader](reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader) à HttpResponseHeaders et [get_HasCurrentHeader](reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader) propriété à HttpHeadersCollectionIterator.
* **Modification en rupture:** Modification du comportement de DevToolsProtocolEventReceived. Vous pouvez maintenant créer un [DevToolsProtocolEventReceiver](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md) pour un événement de protocole devtools particulier et vous abonner/vous désabonner à un événement à l’aide de [add_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived) / [remove_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived).
* **Modification en rupture:** Modification de WebMessageReceivedEventArgs' [get_WebMessageAsString](reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring) propriété sur une méthode [TryGetWebMessageAsString](reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring) .
* **Modification en rupture:** Modification de la méthode de [handle](reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle) AcceleratorKeyPressedEventArgs’en propriété [get_Handled](reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled) .

## 0.8.355

[Package NuGet][WebView2NuGetGallery0.8.355] | version de Microsoft Edge 80.0.355.0 minimum.

* Exemple de WebView2API de mise à l’État-Guide complet du SDK. Découvrez-le [ici](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample).
* Ajout de la prise en charge IME pour toutes les langues autres que l’anglais. ([#30](https://github.com/MicrosoftEdge/WebViewFeedback/issues/30))
* Mise à jour de la surface de l’API de l’événement WebResourceRequested en réponse aux rapports de bogues.  La spécification simultanée d’un filtre et un événement lors de la création est désormais déconseillé.  Pour créer un événement de ressource Web demandé, utilisez [add_WebResourceRequested](reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested) pour ajouter l’événement et [AddWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter) pour ajouter un filtre.  [RemoveWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter) supprime le filtre.  ([#36](https://github.com/MicrosoftEdge/WebViewFeedback/issues/36)) ([#74](https://github.com/MicrosoftEdge/WebViewFeedback/issues/74))  
* **Modification en rupture:**  Modification du comportement du mode plein écran. [IsFullScreenAllowed](reference/win32/0-8-190/IWebView2Settings.md#get_isfullscreenallowed_deprecated)déconseillé.  Par défaut, si un élément au sein d’un WebView (par exemple, une vidéo) est défini en mode plein écran, il remplit les limites du WebView.  Utilisez l’événement [ContainsFullScreenElementChanged](reference/win32/0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md#interface-iwebview2containsfullscreenelementchangedeventhandler) et [get_ContainsFullScreenElement](reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement) pour spécifier la façon dont l’application doit redimensionner le WebView si un élément veut entrer en mode plein écran.  

## 0.8.314

[Package NuGet][WebView2NuGetGallery0.8.314] | version de Microsoft Edge 80.0.314.0 minimum.

* Ajout de la prise en charge de Windows 7, Windows 8/8.1.
* Ajout de la prise en charge du débogage de code Visual Studio et Visual Studio pour WebView2. À présent, vous pouvez déboguer votre script dans le WebView2 directement à partir de votre IDE. Pour en savoir plus, cliquez [ici](/microsoft-edge/hosting/webview2#debugging-webview2) .  
* A été ajouté `Native Object Injection` , ce qui permet de transmettre le script en cours d’exécution dans WebView2 à un objet IDispatch à partir du composant Win32 de l’application et d’accéder aux propriétés de l’objet IDispatch.  Pour plus d’informations, consultez [AddRemoteObject](reference/win32/0-8-190/iwebview2webview4.md#addremoteobject) .  ([#17](https://github.com/MicrosoftEdge/WebViewFeedback/issues/17)).  
* `AcceleratorKeyPressed`Événement ajouté.  Pour en savoir plus, voir [add_AcceleratorKeyPressed](reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed) .  ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Désactivé `Context Menus` .  Pour plus d’informations ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)), voir [put_AreDefaultContextMenusEnabled](reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled) .  
* Mise à jour `DPI Awareness` . Maintenant, la prise en charge des résolutions du WebView est identique à celle de l’application hôte. Remarque: si une autre application hybride est lancée à l’aide d’une sensibilité différente de celle du WebView d’origine, le nouveau WebView ne sera pas lancé si le répertoire de données utilisateur est identique ([#1](https://github.com/MicrosoftEdge/WebViewFeedback/issues/1)).
* Mis à jour `Notification Change Behavior` de telle sorte que WebView2 rejette automatiquement les demandes d’autorisation de notification par le contenu Web hébergé sur le WebView.

## 0.8.270  

[Package NuGet][WebView2NuGetGallery0.8.270] | version de Microsoft Edge 78.0.270.0 minimum.  

* Un événement a été ajouté `DocumentTitleChanged` pour indiquer le changement de titre du document \ ([\ #27][MicrosoftEdgeWebViewFeedbackIssue27]\).  
* `GetWebView2BrowserVersionInfo`API ajoutée \ ([\ #18][MicrosoftEdgeWebViewFeedbackIssue18]\).  
* `NewWindowRequested`Événement ajouté.  
* Fonction Updated `CreateWebView2EnvironmentWithDetails` à supprimer `releaseChannelPreference` .  Pour plus d’informations, voir fonction [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  Le remplacement de la variable de Registre et de l’environnement est toujours pris en charge.  La préférence de canal par défaut est utilisée sauf si elle est ignorée.  
    Lors de la recherche de canal, nous n’avons pas à utiliser une version plus ancienne du canal qui n’est pas compatible avec le SDK WebView2.  
    Nous allons sélectionner le canal plus stable pour garantir les comportements les plus cohérents pour l’utilisateur final.  Lorsque vous testez avec les versions les plus récentes des Canaries, vous devez créer un script pour définir `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` la variable d’environnement sur `1` avant le lancement de l’application.  
* Fonction Updated `CreateWebView2EnvironmentWithDetails` avec logique de sélection `userDataFolder` en cas d’absence de spécification.  Pour plus d’informations, voir fonction [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  Si vous avez déjà utilisé l' `userDataFolder` emplacement par défaut, lorsque vous basculez vers le nouveau kit de développement logiciel (SDK), la valeur par défaut `userDataFolder` est Reset (définie à un nouvel emplacement dans le répertoire de code hôte) et votre état est également réinitialisé.  
    Si le processus hôte n’est pas autorisé à écrire dans le répertoire spécifié, `CreateWebView2EnvironmentWithDetails` il est possible qu’il échoue.  Vous pouvez copier les données de l’ancien répertoire de données utilisateur vers le nouvel annuaire.  

## 0.8.230  

[Package NuGet][WebView2NuGetGallery0.8.230] | version de Microsoft Edge 77.0.230.0 minimum.  

* `Stop`API ajoutée pour arrêter toutes les extractions de ressources de navigation et en attente \ ([\ #28][MicrosoftEdgeWebViewFeedbackIssue28]\).  
* Ajout du fichier. tlb au package NuGet \ ([\ #22][MicrosoftEdgeWebViewFeedbackIssue22]\).  
* Ajout de projets .NET à la liste du programme d’installation du package NuGet \ ([\ #32][MicrosoftEdgeWebViewFeedbackIssue32]\).  

## 0.8.190  

[Package NuGet][WebView2NuGetGallery0.8.190] | version de Microsoft Edge 77.0.190.0 minimum.  

* Ajouté `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` pour contrôler si les utilisateurs peuvent ouvrir devtools \ ([\ #16][MicrosoftEdgeWebViewFeedbackIssue16]\).  
* `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` A ajouté pour contrôler la présence de la barre d’État \ ([\ #19][MicrosoftEdgeWebViewFeedbackIssue19]\).  
* Ajouté `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` pour revenir en arrière et transférer via l’historique de navigation.  
* Ajout de types d’en-têtes HTTP ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) pour l’affichage et la modification des en-têtes HTTP dans WebView.  
* Ajout de la prise en charge du WebView 32 sur les[#13][MicrosoftEdgeWebViewFeedbackIssue13]ordinateurs 64  
* Un IDL WebView a été ajouté au kit de développement logiciel ([\ #14][MicrosoftEdgeWebViewFeedbackIssue14]\).  
* Ajout de lib pour prendre en charge les objets d’ID d’interface IID\_\ * \ ([\ #12][MicrosoftEdgeWebViewFeedbackIssue12]\).  
* Un chemin d’accès d’inclusion, de liaison et de copie automatique de fichiers DLL ont été ajoutés au fichier cible NuGet dans le SDK.  
* Activation de la requête `window.open` dans le script.  

## 0.8.149  

[Package NuGet][WebView2NuGetGallery0.8.149] | version de Microsoft Edge 76.0.149.0 minimum.  

Version préliminaire du développeur  

<!-- image links -->

<!-- Links -->
[MicrosoftEdgeWebViewFeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 12"  
[MicrosoftEdgeWebViewFeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 13"  
[MicrosoftEdgeWebViewFeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 14"  
[MicrosoftEdgeWebViewFeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 16"  
[MicrosoftEdgeWebViewFeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 18"  
[MicrosoftEdgeWebViewFeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 19"  
[MicrosoftEdgeWebViewFeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 22"  
[MicrosoftEdgeWebViewFeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 27"  
[MicrosoftEdgeWebViewFeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 28"  
[MicrosoftEdgeWebViewFeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Commentaires référentiel samples pour MicrosoftEdge/WebViewFeedback problème 32"  

[WebView2NuGetGallery]: https://aka.ms/webviewnuget "Galerie NuGet | Microsoft. Web. WebView2"  
[WebView2NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[WebView2NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[WebView2NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[WebView2NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[WebView2NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[WebView2NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galerie NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[WebView2NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.430"
[WebView2NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.488"
[WebView2NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galerie NuGet | Version préliminaire de Microsoft. Web. WebView2 v 0.9.515"
[WebView2NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galerie NuGet | Microsoft. Web. WebView2 v 0.9.538"

[WebViewsGlobalsCreateWebView2EnvironmentWithDetails]: reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "Fonction globale WebView-CreateWebView2EnvironmentWithDetails"  
