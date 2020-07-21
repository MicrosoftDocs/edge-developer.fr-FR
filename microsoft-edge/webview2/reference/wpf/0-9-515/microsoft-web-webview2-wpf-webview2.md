---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. WPF. WebView2
ms.openlocfilehash: e7f5d11b540d1d7ad9630aa674ef5bc0073195c2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885295"
---
# Classe Microsoft. Web. WebView2. WPF. WebView2 

Espace de noms: Microsoft. Web. WebView2. WPF \
Assemblage: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

Contrôle pour incorporer du contenu Web dans une application WPF.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.
[CoreWebView2Ready](#corewebview2ready) | Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.
[NavigationCompleted](#navigationcompleted) | Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.
[NavigationStarting](#navigationstarting) | Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.
[SourceChanged](#sourcechanged) | Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.
[WebMessageReceived](#webmessagereceived) | Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.
[ZoomFactorChanged](#zoomfactorchanged) | L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.
[CanGoBack](#cangoback) | Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.
[CanGoForward](#cangoforward) | Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.
[CoreWebView2](#corewebview2) | Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.
[CreationProperties](#creationproperties) | Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.
[Source](#source) | L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).
[ZoomFactor](#zoomfactor) | Facteur de zoom pour le WebView.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.
[ExecuteScriptAsync](#executescriptasync) | Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.
[GoBack](#goback) | Permet d’accéder à la page précédente de l’historique de navigation via le WebView.
[GoForward](#goforward) | Navigue vers la page suivante de l’historique de navigation du WebView.
[NavigateToString](#navigatetostring) | Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.
[Recharger](#reload) | Recharge la page active.
[Stop](#stop) | Arrête toutes les navigations et les extractions de ressources en attente.
[WebView2](#webview2) | Crée une nouvelle instance d’un contrôle WebView2.

Ce contrôle est en réalité un wrapper qui entoure l’API COM WebView2, qui vous trouverez de la documentation pour cet emplacement: [https://aka.ms/webview2](https://aka.ms/webview2) vous pouvez accéder directement à l’interface ICoreWebView2 sous-jacente et à toutes ses fonctionnalités en accédant à la propriété CoreWebView2. Certaines des fonctionnalités COM les plus courantes sont également accessibles directement via les méthodes d’encapsulation/propriétés/événements du contrôle.

Lors de la création, la propriété CoreWebView2 du contrôle est null. En effet, la création de CoreWebView2 est une opération onéreuse qui implique des opérations comme le lancement de processus de navigateur Edge. Il existe deux façons d’entraîner la création du CoreWebView2:1) appeler la méthode EnsureCoreWebView2Async. On parle d’initialisation explicite. 2) définissez la propriété source (qui peut être exécutée à partir du balisage, par exemple). On parle d’initialisation implicite. L’une des deux options commencera l’initialisation en arrière-plan et renverra l’appelant sans attendre la fin de celle-ci. Pour spécifier des options concernant le processus d’initialisation, transmettez votre propre CoreWebView2Environment à EnsureCoreWebView2Async ou définissez la propriété CreationProperties du contrôle avant l’initialisation.

Une fois l’initialisation terminée (quel que soit le mode de déclenchement), les éléments suivants se produisent, dans l’ordre suivant: 1) l’événement CoreWebView2Ready du contrôle est appelé. Si vous devez effectuer une opération de configuration ponctuelle sur le CoreWebView2 avant de l’utiliser, vous devez le faire dans un gestionnaire pour cet événement. 2) si un URI a été défini pour la propriété source, le contrôle commencera à y accéder en arrière-plan (c’est-à-dire, ces étapes continuent sans attendre la fin de la navigation). 3) la tâche renvoyée par EnsureCoreWebView2Async sera terminée.

Pour plus d’informations sur les méthodes/propriétés/événements impliqués dans le processus d’initialisation, voir sa documentation spécifique.

Dans la mesure où le contrôle CoreWebView2 est un objet très haute densité (qui peut être responsable de plusieurs processus en cours d’exécution et de mégaoctets d’espace disque), le contrôle implémente IDisposable pour fournir un moyen explicite de le libérer. L’appel de dispose va libérer le CoreWebView2 et ses ressources sous-jacentes (sauf s’ils sont également utilisés par d’autres WebViews) et réinitialiser CoreWebView2 sur null. Après avoir appelé la méthode CoreWebView2 ne peut pas être réinitialisée, et toute tentative d’utilisation de la fonctionnalité qui nécessite qu’elle lèvera une opération ObjectDisposedException.

Notez que ce contrôle étend HwndHost afin d’incorporer des fenêtres qui résident en dehors de l’écosystème WPF. Cela a quelques implications sur le comportement de l’entrée et de la sortie du contrôle, ainsi que sur les fonctionnalités qu’il hérite de l’élément UIElement et de FrameworkElement. Pour plus d’informations, consultez la documentation sur l’interopérabilité HwndHost et WPF/Win32.

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## Ses

#### ContentLoading 

Wrapper de l’événement CoreWebView2. ContentLoading de CoreWebView2.

> événement public EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

La seule différence entre cet événement et CoreWebView2. ContentLoading est le premier paramètre passé aux gestionnaires. Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. ContentLoading recevront l’instance CoreWebView2.

#### CoreWebView2Ready 

Cet événement est déclenché lors de l’initialisation de l’CoreWebView2 du contrôle (quelle que soit l’origine du déclenchement de l’initialisation), mais avant qu’elle ne soit utilisée pour n’importe quelle opération.

> événement public EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Vous devez gérer cet événement si vous avez besoin d’effectuer des opérations d’installation ponctuelles sur le CoreWebView2 que vous voulez affecter à l’ensemble de ses utilisations (par exemple, ajout de gestionnaires d’événements, configuration des paramètres, installation de scripts de création de documents, ajout d’objets hôtes). Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

Cet événement ne fournit aucun argument et l’expéditeur sera le contrôle WebView2, dont la propriété CoreWebView2 sera désormais valide (c’est-à-dire non null) pour la première fois.

#### NavigationCompleted 

Wrapper de l’événement CoreWebView2. NavigationCompleted de CoreWebView2.

> événement public EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

La seule différence entre cet événement et CoreWebView2. NavigationCompleted est le premier paramètre passé aux gestionnaires. Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationCompleted recevront l’instance CoreWebView2.

#### NavigationStarting 

Wrapper de l’événement CoreWebView2. NavigationStarting de CoreWebView2.

> événement public EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

La seule différence entre cet événement et CoreWebView2. NavigationStarting est le premier paramètre passé aux gestionnaires. Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. NavigationStarting recevront l’instance CoreWebView2.

#### SourceChanged 

Wrapper entourant l’événement CoreWebView2. SourceChanged de CoreWebView2.

> événement public EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

La seule différence entre cet événement et CoreWebView2. SourceChanged est le premier paramètre passé aux gestionnaires. Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. SourceChanged reçoivent l’instance CoreWebView2.

#### WebMessageReceived 

Wrapper de l’événement CoreWebView2. WebMessageReceived de CoreWebView2.

> événement public EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

La seule différence entre cet événement et CoreWebView2. WebMessageReceived est le premier paramètre passé aux gestionnaires. Le gestionnaire de cet événement reçoit le contrôle WebView2, alors que les gestionnaires de CoreWebView2. WebMessageReceived recevront l’instance CoreWebView2.

#### ZoomFactorChanged 

L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.

> événement public EventHandler< EventArgs > [ZoomFactorChanged](#zoomfactorchanged)

Cet événement révèle directement CoreWebView2Controller. ZoomFactorChanged, en savoir plus sur sa documentation.

#### CanGoBack 

Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.

> public bool [CanGoBack](#cangoback)

Wrapper dans la propriété CoreWebView2. CanGoBack de CoreWebView2. Si CoreWebView2 n’est pas initialisé, retourne false.

#### CanGoForward 

Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.

> public bool [CanGoForward](#cangoforward)

Wrapper dans la propriété CoreWebView2. CanGoForward de CoreWebView2. Si CoreWebView2 n’est pas initialisé, retourne false.

#### CoreWebView2 

Accédez à l’ensemble des fonctionnalités de l’API COM Core. CoreWebView2 sous-jacente.

> public CoreWebView2 [CoreWebView2](#corewebview2)

Retourne la valeur null jusqu’à la fin de l’initialisation. Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

##### Exceptions
* `InvalidOperationException` Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur). Pour plus d’informations, voir DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### CreationProperties 

Obtient ou définit un sac d’options qui sont utilisées lors de l’initialisation de la CoreWebView2 du contrôle.

> public CoreWebView2CreationProperties [CreationProperties](#creationproperties)

La définition de cette propriété ne fonctionnera pas une fois l’initialisation du CoreWebView2 du contrôle démarrée (l’ancienne valeur sera conservée). Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

#### Source 

L’URI de niveau supérieur sur lequel est actuellement affiché le WebView (ou s’affichera une fois l’initialisation de son CoreWebView2 terminée).

> [source](#source) URI publique

En règle générale, l’affichage de cette propriété est équivalent à l’utilisation de la propriété CoreWebView2. source de CoreWebView2 et la définition de cette propriété (sur une valeur différente) revient à appeler la méthode CoreWebView2. Navigate sur CoreWebView2. La valeur null a la même signification que «about: Blank» (voir Remarques pour plus d’informations). L’accès à cette propriété avant l’initialisation de CoreWebView2 permet de récupérer le dernier URI qui lui a été défini, ou null (valeur par défaut) s’il n’y a pas eu. Le fait de définir cette propriété avant l’initialisation de CoreWebView2 entraînera le démarrage de l’initialisation en arrière-plan (si ce n’est pas déjà fait), après lequel WebView2 accède à l’URI spécifié. Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

Si cette propriété est null, la CoreWebView2 affichera «about: Blank» (ou si elle est définie sur null, CoreWebView2 sera accédé à «about: Blank»). Il est également possible que cette propriété ait (ou soit définie pour) la valeur explicite «about: Blank», qui a le même effet sur le CoreWebView2. En d’autres termes, si CoreWebView2 affiche «à propos de», la valeur de cette propriété peut être null ou «à propos: Blank». Toutefois, les valeurs NULL et «about: Blank» sont des valeurs distinctes de cette propriété et ne sont pas considérées comme égales les unes aux autres. Il est important d’initialiser le contrôle, car cela signifie que la modification de la valeur null (par défaut) en "about: blank" est toujours un changement et déclenche l’initialisation implicite. 

##### Exceptions
* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### ZoomFactor 

Facteur de zoom pour le WebView.

> double [ZoomFactor](#zoomfactor) public

Cette propriété expose directement CoreWebView2Controller. ZoomFactor, en savoir plus sur la documentation pour en savoir plus. L’accès à cette propriété avant l’initialisation de CoreWebView2 permet de récupérer la dernière valeur définie, ou 1,0 (valeur par défaut) si elle n’a pas été activée. La valeur la plus récente définie pour cette propriété avant l’initialisation de CoreWebView2 sera définie dessus après l’initialisation.

#### EnsureCoreWebView2Async 

Déclenchez explicitement l’initialisation de CoreWebView2 du contrôle.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tâches publiques (environnement CoreWebView2Environment)

Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

##### Parameters
* `environment` CoreWebView2Environment précréé qui doit être utilisé pour créer le CoreWebView2. La création de votre propre environnement vous donne le contrôle de plusieurs options qui affectent la manière dont CoreWebView2 est initialisé. Si vous passez un environnement à cette méthode, elle remplacera tout paramètre spécifié sur la propriété CreationProperties. Si vous passez la valeur null (valeur par défaut) et qu’aucune valeur n’a été définie pour CreationProperties, un environnement par défaut sera créé et utilisé automatiquement. 

##### Renvoie
Tâche qui représente le processus d’initialisation en arrière-plan. Lorsque la tâche se termine, la propriété CoreWebView2 peut être utilisée (c’est-à-dire non null). Notez que l’événement CoreWebView2Ready du contrôle est appelé avant la fin de la tâche. 

L’appel de cette méthode pour les autres temps n’aura aucun effet (l’environnement spécifié est ignoré) et renvoie la même tâche que le premier appel. L’appel de cette méthode une fois l’initialisation déclenchée implicitement, la définition de la propriété source n’aura aucun effet (aucun environnement spécifié n’est ignoré) et renvoyez simplement une tâche représentant cette initialisation déjà en cours. Notez que bien que cette méthode soit asynchrone et renvoie une tâche, celle-ci doit toujours être appelée sur le thread d’interface utilisateur, comme la plupart des fonctionnalités publiques de la plupart des contrôles d’interface utilisateur. 

##### Exceptions
* `InvalidOperationException` Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur). Pour plus d’informations, voir DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### ExecuteScriptAsync 

Exécute le code JavaScript du paramètre javaScript du document de niveau supérieur actuel affiché dans le WebView.

> Tâche asynchrone publique< chaîne > [ExecuteScriptAsync](#executescriptasync)(chaîne JavaScript)

Équivalent pour appeler CoreWebView2.ExecuteScriptAsync sur CoreWebView2

##### Exceptions
* `InvalidOperationException` Levée si CoreWebView2 n’a pas encore été initialisé.

* `InvalidOperationException` Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur). Pour plus d’informations, voir DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### GoBack 

Permet d’accéder à la page précédente de l’historique de navigation via le WebView.

> public void [GoBack](#goback)()

L’équivalent de l’appel à CoreWebView2. GoBack sur CoreWebView2 si CoreWebView2 n’a pas encore été initialisé, ne fait rien.

##### Exceptions
* `InvalidOperationException` Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur). Pour plus d’informations, voir DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### GoForward 

Navigue vers la page suivante de l’historique de navigation du WebView.

> public void [GoForward](#goforward)()

Équivalent à l’appel de la méthode CoreWebView2. GoForward sur CoreWebView2 si CoreWebView2 n’a pas été initialisée pour le moment.

##### Exceptions
* `InvalidOperationException` Levée si le thread appelant n’est pas le thread qui a créé cet objet (généralement le thread d’interface utilisateur). Pour plus d’informations, voir DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Levée si dispose est déjà appelé sur le contrôle.

#### NavigateToString 

Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.

> public void [NavigateToString](#navigatetostring)(chaîne htmlContent)

Équivalent à l’appel de CoreWebView2. NavigateToString sur CoreWebView2

##### Exceptions
* `InvalidOperationException` Levée si CoreWebView2 n’a pas encore été initialisé.

" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).  Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.

#### Recharger 

Recharge la page active.

> [rechargement](#reload)d’annulation publique ()

Équivalent à l’appel de CoreWebView2. Reload sur CoreWebView2

##### Exceptions
* `InvalidOperationException` Levée si CoreWebView2 n’a pas encore été initialisé.

" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).  Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.

#### Stop 

Arrête toutes les navigations et les extractions de ressources en attente.

> public void [Stop](#stop)()

Équivalent à l’appel de CoreWebView2. Stop sur CoreWebView2

##### Exceptions
* `InvalidOperationException` Levée si CoreWebView2 n’a pas encore été initialisé.

" <exception cref="InvalidOperationException"> Levé si le thread d’appel n’est pas le thread qui a créé cet objet (habituellement le thread d’interface utilisateur).  Pour plus d’informations, voir DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Levée si dispose est déjà appelé sur le contrôle.

#### WebView2 

Crée une nouvelle instance d’un contrôle WebView2.

> public [WebView2](#webview2)()

Notez que le CoreWebView2 du contrôle est null jusqu’à son initialisation. Pour obtenir une vue d’ensemble de l’initialisation, consultez la documentation de la classe WebView2.

