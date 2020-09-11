---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2
ms.openlocfilehash: ca31ddd3536350d3b3bdd02b445b4c47589f7dba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011110"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[BrowserProcessId](#browserprocessid) | ID de processus du processus de navigation qui héberge le WebView.
[CanGoBack](#cangoback) | Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.
[CanGoForward](#cangoforward) | Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.
[ContainsFullScreenElement](#containsfullscreenelement) | Indique si le WebView contient un élément HTML fullscreen.
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | Avertit en cas de modification de la propriété ContainsFullScreenElement.
[ContentLoading](#contentloading) | ContentLoading se déclenche avant le chargement du contenu, notamment les scripts ajoutés avec AddScriptToExecuteOnDocumentCreated ContentLoading ne se déclenchent pas si une même navigation de page se produit (par exemple par le biais des navigations ou de l’historique d’un fragment. pushState navigation).
[DocumentTitle](#documenttitle) | Titre du document de niveau supérieur actuel.
[DocumentTitleChanged](#documenttitlechanged) | L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.
[FrameNavigationCompleted](#framenavigationcompleted) | L’événement FrameNavigationCompleted se déclenche quand une image enfant est complètement chargée (le corps. OnLoad a déclenché) ou si le chargement a été arrêté avec une erreur.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent.
[HistoryChanged](#historychanged) | Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.
[NavigationCompleted](#navigationcompleted) | L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.
[NavigationStarting](#navigationstarting) | NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent.
[NewWindowRequested](#newwindowrequested) | Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open.
[PermissionRequested](#permissionrequested) | Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.
[ProcessFailed](#processfailed) | Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.
[ScriptDialogOpening](#scriptdialogopening) | L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView.
[Paramètres](#settings) | L’objet CoreWebView2Settings contient différents paramètres modifiables pour l’exécution
[Source](#source) | URI du document de niveau supérieur actuel.
[SourceChanged](#sourcechanged) | SourceChanged se déclenche lorsque la propriété source change.
[WebMessageReceived](#webmessagereceived) | Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .
[WebResourceRequested](#webresourcerequested) | Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.
[WebResourceResponseReceived](#webresourceresponsereceived) | L’événement WebResourceResponseReceived se déclenche après que le WebView a reçu et traité la réponse à une demande de ressource Resource.
[WindowCloseRequested](#windowcloserequested) | Se déclenche lorsque le contenu à l’intérieur du WebView est requis pour fermer la fenêtre, par exemple, après l’appel de Window. Close.
[AddHostObjectToScript](#addhostobjecttoscript) | Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Appelez une méthode DevToolsProtocol asynchrone.
[CapturePreviewAsync](#capturepreviewasync) | Capturez une image de l’affichage du WebView.
[ExecuteScriptAsync](#executescriptasync) | Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.
[GoBack](#goback) | Permet d’accéder à la page précédente de l’historique de navigation via le WebView.
[GoForward](#goforward) | Navigue vers la page suivante de l’historique de navigation du WebView.
[Rechercher](#navigate) | Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.
[NavigateToString](#navigatetostring) | Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.
[OpenDevToolsWindow](#opendevtoolswindow) | Ouvre la fenêtre DevTools pour le document actif dans le WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.
[Recharger](#reload) | Recharger la page active.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Supprimez le JavaScript correspondant ajouté via AddScriptToExecuteOnDocumentCreated avec l’ID de script spécifié.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.
[Stop](#stop) | Arrêtez toutes les navigations et les extractions de ressources en attente.

## Ses

#### BrowserProcessId 

ID de processus du processus de navigation qui héberge le WebView.

> public uint [BrowserProcessId](#browserprocessid)

#### CanGoBack 

Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.

> public bool [CanGoBack](#cangoback)

L’événement HistoryChanged se déclenche si CanGoBack change value.

#### CanGoForward 

Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.

> public bool [CanGoForward](#cangoforward)

L’événement HistoryChanged se déclenche si CanGoForward change value.

#### ContainsFullScreenElement 

Indique si le WebView contient un élément HTML fullscreen.

> public bool [ContainsFullScreenElement](#containsfullscreenelement)

#### ContainsFullScreenElementChanged 

Avertit en cas de modification de la propriété ContainsFullScreenElement.

> événement public EventHandler< objet > [ContainsFullScreenElementChanged](#containsfullscreenelementchanged)

Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran. Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran. L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.

#### ContentLoading 

ContentLoading se déclenche avant le chargement du contenu, notamment les scripts ajoutés avec AddScriptToExecuteOnDocumentCreated ContentLoading ne se déclenchent pas si une même navigation de page se produit (par exemple par le biais des navigations ou de l’historique d’un fragment. pushState navigation).

> événement public EventHandler< [CoreWebView2ContentLoadingEventArgs](microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)  >  [ContentLoading](#contentloading)

Cela suit les événements NavigationStarting et SourceChanged, ainsi que les événements HistoryChanged et NavigationCompleted.

#### DocumentTitle 

Titre du document de niveau supérieur actuel.

> [DocumentTitle](#documenttitle) de chaîne publique

Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.

#### DocumentTitleChanged 

L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.

> événement public EventHandler< objet > [DocumentTitleChanged](#documenttitlechanged)

#### FrameNavigationCompleted 

L’événement FrameNavigationCompleted se déclenche quand une image enfant est complètement chargée (le corps. OnLoad a déclenché) ou si le chargement a été arrêté avec une erreur.

> événement public EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [FrameNavigationCompleted](#framenavigationcompleted)

#### FrameNavigationStarting 

FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent.

> événement public EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [FrameNavigationStarting](#framenavigationstarting)

Cela se déclenche également pour les redirections.

#### HistoryChanged 

Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.

> événement public EventHandler< objet > [HistoryChanged](#historychanged)

Utilisez Facturationmodifier pour vérifier si la valeur CanGoBack/CanGoForward a changé. HistoryChanged est également déclenché pour l’utilisation de GoBack/GoForward. HistoryChanged se déclenche après SourceChanged et ContentLoading. Ajoutez un gestionnaire d’événements pour l’événement HistoryChanged.

#### NavigationCompleted 

L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.

> événement public EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [NavigationCompleted](#navigationcompleted)

#### NavigationStarting 

NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent.

> événement public EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [NavigationStarting](#navigationstarting)

Cela se déclenche également pour les redirections.

#### NewWindowRequested 

Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open.

> événement public EventHandler< [CoreWebView2NewWindowRequestedEventArgs](microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)  >  [NewWindowRequested](#newwindowrequested)

L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.

#### PermissionRequested 

Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.

> événement public EventHandler< [CoreWebView2PermissionRequestedEventArgs](microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)  >  [PermissionRequested](#permissionrequested)

#### ProcessFailed 

Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.

> événement public EventHandler< [CoreWebView2ProcessFailedEventArgs](microsoft-web-webview2-core-corewebview2processfailedeventargs.md)  >  [ProcessFailed](#processfailed)

#### ScriptDialogOpening 

L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView.

> événement public EventHandler< [CoreWebView2ScriptDialogOpeningEventArgs](microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)  >  [ScriptDialogOpening](#scriptdialogopening)

Cet événement est déclenché uniquement si la propriété CoreWebView2Settings. AreDefaultScriptDialogsEnabled est définie sur false. L’événement ScriptDialogOpening peut être utilisé pour supprimer des boîtes de dialogue ou remplacer les boîtes de dialogue par défaut par des boîtes de dialogue personnalisées.

#### Paramètres 

L’objet CoreWebView2Settings contient différents paramètres modifiables pour l’exécution

> [paramètres](#settings) du [CoreWebView2Settings](microsoft-web-webview2-core-corewebview2settings.md) public

#### Source 

URI du document de niveau supérieur actuel.

> [source](#source) de chaîne publique

Cette valeur peut éventuellement changer dans le cadre du déclenchement de l’événement SourceChanged dans certains cas, par exemple pour accéder à un site ou à un fragment de navigation différent. Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.

#### SourceChanged 

SourceChanged se déclenche lorsque la propriété source change.

> événement public EventHandler< [CoreWebView2SourceChangedEventArgs](microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)  >  [SourceChanged](#sourcechanged)

L’utilisation de l’fonction SourceChanged est déclenchée pour accéder à un site ou à un fragment de navigation différent. Il ne se déclenche pas pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active. SourceChanged se déclenche avant ContentLoading pour la navigation vers un nouveau document. Ajoutez un gestionnaire d’événements pour l’événement SourceChanged.

#### WebMessageReceived 

Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .

> événement public EventHandler< [CoreWebView2WebMessageReceivedEventArgs](microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)  >  [WebMessageReceived](#webmessagereceived)

La fonction postMessage est l' `void postMessage(object)` emplacement de tout objet pris en charge par la conversion JSON. Lorsque postMessage est appelée, le jeu CoreWebView2WebMessageReceivedEventHandler est appelé avec le paramètre d’objet postMessage converti en chaîne JSON.

#### WebResourceRequested 

Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.

> événement public EventHandler< [CoreWebView2WebResourceRequestedEventArgs](microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)  >  [WebResourceRequested](#webresourcerequested)

Au moins un filtre doit être ajouté pour que l’événement se déclenche.

#### WebResourceResponseReceived 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

L’événement WebResourceResponseReceived se déclenche après que le WebView a reçu et traité la réponse à une demande de ressource Resource.

> événement public EventHandler< [CoreWebView2WebResourceResponseReceivedEventArgs](microsoft-web-webview2-core-corewebview2webresourceresponsereceivedeventargs.md)  >  [WebResourceResponseReceived](#webresourceresponsereceived)

Les arguments d’événement incluent le WebResourceRequest envoyé par le filaire et WebResourceResponse reçu, y compris les en-têtes supplémentaires ajoutés par la pile réseau qui n’ont pas été inclus dans le cadre de l’événement WebResourceRequested associé, tels que les en-têtes d’authentification.

#### WindowCloseRequested 

Se déclenche lorsque le contenu à l’intérieur du WebView est requis pour fermer la fenêtre, par exemple, après l’appel de Window. Close.

> événement public EventHandler< objet > [WindowCloseRequested](#windowcloserequested)

L’application doit fermer la fenêtre WebView et la fenêtre de l’application associée si cela est pertinent pour l’application.

#### AddHostObjectToScript 

Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.

> public void [AddHostObjectToScript](#addhostobjecttoscript)(nom de chaîne, objet rawObject)

Les objets hôtes sont exposés en tant que proxy d’objet hôte via `window.chrome.webview.hostObjects.{name}` . Les proxies d’objet hôte sont promet et sont résolus en objet représentant l’objet hôte. Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject: 
```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```
 Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge. Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch. La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID. Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3. Les matrices de par types de référence ne sont pas prises en charge. VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL. Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.

De plus, tous les objets hôtes sont exposés en tant que `window.chrome.webview.hostObjects.sync.{name}` . Ici, les objets hôtes sont exposés en tant que proxy d’objets hôtes synchrones. Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute. En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.hostObjects.{name}` décrite ci-dessus.

Les proxies d’objet hôte synchrone et les proxys d’objets hôtes asynchrones peuvent à la fois proxy le même objet hôte. Les modifications distantes apportées par un proxy seront reflétées dans tout autre proxy de ce même objet hôte, qu’il s’agisse de proxys et synchrones ou asynchrones.

Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript. Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Les proxies d’objets hôtes sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode. Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement. De plus, toute propriété ou méthode du tableau `chrome.webview.hostObjects.options.forceLocalProperties` sera également exécutée localement. Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` . Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.

Il existe une méthode `chrome.webview.hostObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objet hôte.

Les proxys d’objets hôtes possèdent également les méthodes suivantes qui s’exécutent en local:

* applyHostFunction, getHostProperty, setHostProperty: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet hôte. Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété. Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy. Mais `proxy.applyHostFunction('toString')` s’exécute `toString` plutôt sur l’objet proxy de l’hôte.

* getLocalProperty, setLocalProperty: exécuter une propriété Get ou Property Set localement. Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet hôte lui-même plutôt que sur l’objet hôte qu’elle représente. Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy de l’hôte. Toutefois `proxy.getLocalProperty('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.

* synchronisation: les proxys d’objets hôtes asynchrones exposent une méthode de synchronisation qui renvoie une promesse de proxy d’objet hôte synchrone pour le même objet hôte. Par exemple, `chrome.webview.hostObjects.sample.methodCall()` retourne un proxy d’objet hôte asynchrone. Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet hôte synchrone à la place: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: les proxys d’objets d’hôte synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet hôte asynchrone pour le même objet hôte. Par exemple, `chrome.webview.hostObjects.sync.sample.methodCall()` retourne un proxy d’objet hôte synchrone. Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet hôte asynchrone pour le même objet hôte: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* ensuite: les proxies d’objet hôte asynchrone possèdent une méthode Then. Cela leur permet d’être await. `then` renverra une promesse qui est résolue en une représentation de l’objet hôte. Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement. Si le proxy représente une fonction, un proxy non-await est retourné. Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objet hôte.

Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance. Les proxys d’objets hôtes asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété. La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération. Les proxys d’objets hôtes synchrones fonctionnent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.

La définition d’une propriété sur un proxy d’objet hôte asynchrone fonctionne légèrement différemment. Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie. Il s’agit d’une condition requise de l’objet proxy JavaScript. Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setHostProperty qui renvoie une promesse comme décrit ci-dessus. La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.

#### AddScriptToExecuteOnDocumentCreatedAsync 

Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.

> Tâche asynchrone publique< chaîne > [AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync)(chaîne JavaScript)

##### Renvoie
Renvoie un ID de script qui est susceptible d’être transmis lors de l’appel de [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated). 

Le script injecté s’applique à tous les futurs documents de niveau supérieur et navigation de Frame enfant jusqu’à sa suppression avec RemoveScriptToExecuteOnDocumentCreated. Cette opération est appliquée de manière asynchrone et vous devez attendre que le gestionnaire d’achèvement s’exécute avant de vérifier que le script est prêt à être exécuté sur de futurs navigations.

Notez que si un document HTML comporte un sandbox d’un type quelconque via les propriétés [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou l' [en-tête HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , ce dernier affectera l’exécution du script. Par exemple, si le mot clé «allow-modaux» n’est pas défini, les appels à la `alert` fonction seront ignorés.

#### AddWebResourceRequestedFilter 

Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.

> public void [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI de chaîne, CoreWebView2WebResourceContext ResourceContext)

Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1). nullptr est l’équivalent de L "". Pour plus d’détails sur les filtres de contexte de ressources, voir l’énumération CoreWebView2WebResourceContext.

#### CallDevToolsProtocolMethodAsync 

Appelez une méthode DevToolsProtocol asynchrone.

> Tâche asynchrone publique< chaîne > [CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync)(chaîne MethodName, chaîne parametersAsJson)

##### Renvoie
Chaîne JSON qui représente l’objet de retour de la méthode. 

Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles. Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` . Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante. La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone. Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.

#### CapturePreviewAsync 

Capturez une image de l’affichage du WebView.

> [CapturePreviewAsync](#capturepreviewasync)de tâches asynchrones publiques (CoreWebView2CapturePreviewImageFormat ImageFormat; flux ImageStream)

Spécifiez le format de l’image avec le paramètre imageFormat. Les données binaires d’image obtenues sont écrites dans le paramètre imageStream fourni. Lorsque CapturePreview finit d’écrire dans le flux, la méthode Invoke du paramètre de gestionnaire fourni est appelée.

#### ExecuteScriptAsync 

Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.

> Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(chaîne JavaScript)

##### Renvoie
Renvoie une chaîne codée JSON qui représente le résultat de l’exécution du JavaScript fourni. 

Cette méthode exécute le JavaScript fourni de manière asynchrone et retourne le résultat du JavaScript fourni. Si le résultat du JavaScript fourni est `undefined` , contient un cycle de référence, ou ne peut pas être encodé dans JSON, la chaîne «NULL» est renvoyée. Si une fonction appelée dans le code JavaScript fourni ne possède aucune valeur de retour explicite, `undefined` est renvoyée. Si le JavaScript fourni lève une exception non gérée, «NULL» est retourné. Si cette méthode est appelée après un événement NavigationStarting, le JavaScript fourni est exécuté sur le nouveau document lors du chargement, en même temps que ContentLoading est déclenché. ExecuteScriptAsync fonctionne même si IsScriptEnabled est défini sur `FALSE` .

#### GetDevToolsProtocolEventReceiver 

Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.

> public CoreWebView2DevToolsProtocolEventReceiver [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(chaîne EventName)

Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles. Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` . Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante. La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone. Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.

#### GoBack 

Permet d’accéder à la page précédente de l’historique de navigation via le WebView.

> public void [GoBack](#goback)()

#### GoForward 

Navigue vers la page suivante de l’historique de navigation du WebView.

> public void [GoForward](#goforward)()

#### Rechercher 

Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.

> public void [Navigate](#navigate)(URI de chaîne)

Pour plus d’informations, voir événements de navigation. Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.

#### NavigateToString 

Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.

> public void [NavigateToString](#navigatetostring)(chaîne htmlContent)

Le paramètre htmlContent ne doit pas comporter plus de 2 Mo de caractères. L’origine de la nouvelle page va être vide.

#### OpenDevToolsWindow 

Ouvre la fenêtre DevTools pour le document actif dans le WebView.

> public void [OpenDevToolsWindow](#opendevtoolswindow)()

Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte.

#### PostWebMessageAsJson 

Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.

> public void [PostWebMessageAsJson](#postwebmessageasjson)(chaîne webMessageAsJson)

Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché. JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

Les arguments d’événement sont une instance de `MessageEvent` . Le paramètre CoreWebView2Settings. IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG. La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript. La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet. Pour plus d’informations sur l’envoi de messages à partir du document HTML du WebView vers l’hôte, voir SetWebMessageReceivedEventHandler. Ce message est envoyé de manière asynchrone. Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.

#### PostWebMessageAsString 

Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.

> public void [PostWebMessageAsString](#postwebmessageasstring)(chaîne webMessageAsString)

Ce comportement se comporte exactement de la même façon que PostWebMessageAsJson, mais la `window.chrome.webview` propriété Data de arg du message est une chaîne ayant la même valeur que webMessageAsString. Utilisez cette fonction au lieu de PostWebMessageAsJson si vous souhaitez communiquer via des chaînes simples plutôt que des objets JSON.

#### Recharger 

Recharger la page active.

> [rechargement](#reload)d’annulation publique ()

Il s’agit de la même façon que d’accéder à l’URI du document de niveau supérieur actuel, y compris tous les événements de navigation déclenchant et respectant les entrées dans le cache HTTP. Toutefois, l’historique en arrière-plan ne sera pas modifié.

#### RemoveHostObjectFromScript 

Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.

> public void [RemoveHostObjectFromScript](#removehostobjectfromscript)(String name)

Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet. Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.

#### RemoveScriptToExecuteOnDocumentCreated 

Supprimez le JavaScript correspondant ajouté via AddScriptToExecuteOnDocumentCreated avec l’ID de script spécifié.

> public void [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID de chaîne)

#### RemoveWebResourceRequestedFilter 

Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.

> public void [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI de chaîne, [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) ResourceContext)

Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective. Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.

#### Stop 

Arrêtez toutes les navigations et les extractions de ressources en attente.

> public void [Stop](#stop)()

Ne permet pas d’arrêter les scripts.

