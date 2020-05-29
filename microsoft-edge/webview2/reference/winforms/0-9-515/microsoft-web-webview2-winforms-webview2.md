---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 532c898845125564ad5af6460dc8d1ff6464abfb
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687803"
---
# Classe Microsoft. Web. WebView2. WinForms. WebView2 

Espace de noms: Microsoft. Web. WebView2. WinForms \
Assembly: Microsoft. Web. WebView2. WinForms. dll

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

Ctrl pour incorporer WebView2 dans WinForms.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.
[CoreWebView2Ready](#corewebview2ready) | Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.
[NavigationStarting](#navigationstarting) | NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.
[SourceChanged](#sourcechanged) | SourceChanged dispatchs après modification de la propriété source.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .
[CoreWebView2](#corewebview2) | CoreWebView2 sous-jacente.
[Source](#source) | La propriété source est l’URI du document de niveau supérieur du WebView2.
[ZoomFactor](#zoomfactor) | Facteur de zoom pour le WebView.
[CanGoBack](#cangoback) | Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.
[CanGoForward](#cangoforward) | Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.
[ExecuteScriptAsync](#executescriptasync) | Exécute le script fourni dans le document de niveau supérieur du WebView2.
[GoBack](#goback) | Revenir à la page précédente de l’historique de navigation.
[GoForward](#goforward) | Accédez à la page suivante de l’historique de navigation.
[NavigateToString](#navigatetostring) | Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.
[Recharger](#reload) | Rechargez le document de niveau supérieur du WebView2.
[Stop](#stop) | Arrêtez la navigation en cours dans le WebView2.
[WebView2](#webview2) | Créer un contrôle WinForms WebView2.

## Ses

#### ContentLoading 

ContentLoading est distribué après le début d’une navigation sur un nouvel URI et le contenu de cet URI commence à être restitué.

> événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Cela équivaut à l’événement ContentLoading sur CoreWebView2. Pour plus d’informations, consultez la documentation CoreWebView2. ContentLoading.

#### CoreWebView2Ready 

Cet événement est déclenché lors de l’initialisation de l' [CoreWebView2](#corewebview2) du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.

> événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes).

Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.

#### NavigationCompleted 

NavigationCompleted Dispatches après qu’une navigation du document de niveau supérieur effectue un rendu correct ou non.

> événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Cela équivaut à l’événement NavigationCompleted sur CoreWebView2. Pour plus d’informations, consultez la documentation CoreWebView2. NavigationCompleted.

#### NavigationStarting 

NavigationStarting dispatchs avant le début de la navigation dans le document de niveau supérieur de la WebView2.

> événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Cela équivaut à l’événement NavigationStarting sur CoreWebView2. Pour plus d’informations, consultez la documentation CoreWebView2. NavigationStarting.

#### SourceChanged 

SourceChanged dispatchs après modification de la propriété source.

> événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

Cela se produit au cours d’une navigation ou, dans le cas contraire, le script de la page modifie l’URI du document. Cela équivaut à l’événement SourceChanged sur le CoreWebView2. Pour plus d’informations, voir la documentation relative à CoreWebView2. SourceChanged.

#### WebMessageReceived 

WebMessageReceived de distribution de contenu Web permet d’envoyer un message à l’hôte de l’application par le biais de `chrome.webview.postMessage` .

> événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Cela équivaut à l’événement WebMessageReceived sur CoreWebView2. Pour plus d’informations, consultez la documentation CoreWebView2. WebMessageReceived.

#### CoreWebView2 

CoreWebView2 sous-jacente.

> public CoreWebView2 [CoreWebView2](#corewebview2)

Utilisez cette propriété pour effectuer davantage d’opérations sur le contenu WebView2 que ce qui est exposé sur le WebView2. Cette valeur est null jusqu’à ce qu’elle soit initialisée. Vous pouvez forcer l’initialisation du CoreWebView2 sous-jacent via la méthode InitializeAsync.

#### Source 

La propriété source est l’URI du document de niveau supérieur du WebView2.

> [source](#source) URI publique

Le fait de définir la source est l’équivalent d’appeler CoreWebView2. Navigate. Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, il s’agit de la propriété «about: Blank». Si la propriété est définie sur un URI non absolu ou null, la propriété reste inchangée. Pour plus d’informations, voir CoreWebView2. Navigate.

#### ZoomFactor 

Facteur de zoom pour le WebView.

> double [ZoomFactor](#zoomfactor) public

#### CanGoBack 

Retourne true si WebView peut accéder à une page précédente de l’historique de navigation via la méthode GoBack.

> public bool [CanGoBack](#cangoback)

Cela équivaut à la propriété CanGoBack sur CoreWebView2. Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false. Pour plus d’informations, consultez la documentation CoreWebView2. CanGoBack.

#### CanGoForward 

Retourne true si WebView peut accéder à une page suivante de l’historique de navigation via la méthode GoForward.

> public bool [CanGoForward](#cangoforward)

Cela équivaut à la propriété CanGoForward sur CoreWebView2. Si l’CoreWebView2 sous-jacent n’est pas encore initialisé, cette propriété a la valeur false. Pour plus d’informations, consultez la documentation CoreWebView2. CanGoForward.

#### EnsureCoreWebView2Async 

Déclenchez explicitement l’initialisation de [CoreWebView2](#corewebview2)du contrôle.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)

##### Parameters
* `environment` CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2. La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé. Si vous passez la valeur null (valeur par défaut), un environnement par défaut sera créé et utilisé automatiquement. 

##### Renvoie
Tâche qui représente le processus d’initialisation en arrière-plan. Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null). Notez que l’événement [CoreWebView2Ready](#corewebview2ready) du contrôle est appelé avant la fin de la tâche. 

L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel. L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété [source](#source) n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours. 

##### Exceptions
* `System.InvalidOperationException` Levée en cas d’appel à partir d’un thread sans interface utilisateur.

#### ExecuteScriptAsync 

Exécute le script fourni dans le document de niveau supérieur du WebView2.

> Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(script de chaîne)

Cela équivaut à la méthode ExecuteScriptAsync sur CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException. Pour plus d’informations, consultez la documentation CoreWebView2. ExecuteScriptAsync.

#### GoBack 

Revenir à la page précédente de l’historique de navigation.

> public void [GoBack](#goback)()

Cela équivaut à la méthode GoBack sur le CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet. Pour plus d’informations, voir la documentation CoreWebView2. GoBack.

#### GoForward 

Accédez à la page suivante de l’historique de navigation.

> public void [GoForward](#goforward)()

Cela équivaut à la méthode GoForward sur le CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet. Pour plus d’informations, voir la documentation CoreWebView2. GoForward.

#### NavigateToString 

Affichez le code HTML fourni en tant que document de niveau supérieur du WebView2.

> public void [NavigateToString](#navigatetostring)(chaîne htmlContent)

Cela équivaut à la méthode NavigateToString sur CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException. Pour plus d’informations, consultez la documentation CoreWebView2. NavigateToString.

#### Recharger 

Rechargez le document de niveau supérieur du WebView2.

> [rechargement](#reload)d’annulation publique ()

Cela équivaut à la méthode reload sur le CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode lève une exception InvalidOperationException. Pour plus d’informations, voir CoreWebView2. Reload documentation.

#### Stop 

Arrêtez la navigation en cours dans le WebView2.

> public void [Stop](#stop)()

Cela équivaut à la méthode Stop sur le CoreWebView2. Si la CoreWebView2 sous-jacente n’est pas encore initialisée, cette méthode n’a aucun effet. Pour plus d’informations, voir la documentation CoreWebView2. Stop.

#### WebView2 

Créer un contrôle WinForms WebView2.

> public [WebView2](#webview2)()

Après construction, la propriété CoreWebView2 a la valeur null. Appelez [EnsureCoreWebView2Async](#ensurecorewebview2async) pour initialiser la CoreWebView2 sous-jacente.

