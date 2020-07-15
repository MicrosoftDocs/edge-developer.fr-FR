---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2Controller
ms.openlocfilehash: 581343b2373dac43dd89582f7ea6e551507f3a6c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878959"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Controller 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Cette classe est le propriétaire de l’objet CoreWebView2 et prend en charge le redimensionnement, l’affichage et le masquage, le focus, ainsi que d’autres fonctionnalités relatives à la fenêtre et à la composition.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AcceleratorKeyPressed](#acceleratorkeypressed) | AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé.
[Limites](#bounds) | Les limites de l’affichage WebView.
[CoreWebView2](#corewebview2) | Obtient le CoreWebView2 associé à cet CoreWebView2Controller.
[GotFocus](#gotfocus) | GotFocus se déclenche lorsque WebView a le focus.
[IsVisible](#isvisible) | La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.
[LostFocus](#lostfocus) | LostFocus se déclenche lorsque WebView perd le focus.
[MoveFocusRequested](#movefocusrequested) | MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView.
[FenêtreParent](#parentwindow) | Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.
[ZoomFactor](#zoomfactor) | Facteur de zoom pour le WebView.
[ZoomFactorChanged](#zoomfactorchanged) | L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.
[Fermer](#close) | Ferme le WebView et nettoie l’instance de navigateur sous-jacente.
[MoveFocus](#movefocus) | Déplacer le focus sur le WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Mettez à jour les propriétés de limites et de ZoomFactor en même temps.

Le CoreWebView2Controller possède CoreWebView2, et si toutes les références au CoreWebView2Controller disparaissent, le WebView sera fermé.

## Ses

#### AcceleratorKeyPressed 

AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé.

> événement public EventHandler< [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)  >  [AcceleratorKeyPressed](#acceleratorkeypressed)

AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé. Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:

1. Ctrl ou Alt est en cours de conservation ou

1. la touche appuyée ne correspond pas à un caractère. Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift. La touche Échap est toujours considérée comme un accélérateur.

Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement. Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.

En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone. Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Toutes les méthodes de l’API CoreWebView2 fonctionneront toutefois.

En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone. L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.

Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.

#### Limites 

Les limites de l’affichage WebView.

> [limites](#bounds) de rectangle public

Les limites sont relatives au HWND parent. L’application peut positionner un WebView de deux manières:

1. Créer un HWND enfant qui est le HWND parent WebView. Positionnez cette fenêtre dans laquelle le WebView devrait être. Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).

1. Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage. Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application. Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.

#### CoreWebView2 

Obtient le CoreWebView2 associé à cet CoreWebView2Controller.

> public [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) [CoreWebView2](#corewebview2)

#### GotFocus 

GotFocus se déclenche lorsque WebView a le focus.

> événement public EventHandler< objet > [GotFocus](#gotfocus)

#### IsVisible 

La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.

> public bool [IsVisible](#isvisible)

Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché. Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateCoreWebView2Controller). Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible. Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée. Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée. Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.

#### LostFocus 

LostFocus se déclenche lorsque WebView perd le focus.

> événement public EventHandler< objet > [LostFocus](#lostfocus)

Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested. Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.

#### MoveFocusRequested 

MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView.

> événement public EventHandler< [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)  >  [MoveFocusRequested](#movefocusrequested)

Le focus du WebView n’a pas changé lors du déclenchement de cet événement.

#### FenêtreParent 

Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.

> public IntPtr [FenêtreParent](#parentwindow)

Le fait de définir la propriété entraînera l’affichage du WebView à la fenêtre nouvellement fournie.

#### ZoomFactor 

Facteur de zoom pour le WebView.

> double [ZoomFactor](#zoomfactor) public

Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page. Le facteur de zoom appliqué par l’hôte en appelant ZoomFactor devient le nouveau zoom par défaut de l’affichage WebView. Ce facteur de zoom s’applique aux différentes navigations et le facteur de zoom est renvoyé lorsque l’utilisateur appuie sur Ctrl + 0. Lorsque le facteur de zoom est modifié par l’utilisateur (ce qui permet à l’application de recevoir ZoomFactorChanged), ce zoom s’applique uniquement à la page active. Tout zoom appliqué à un utilisateur est réservé uniquement à la page active et est réinitialisé sur une navigation. La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée. WebView possède également une plage de facteur de zoom prise en charge interne. Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué. Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.

#### ZoomFactorChanged 

L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change.

> événement public EventHandler< objet > [ZoomFactorChanged](#zoomfactorchanged)

L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom. Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged. WebView associe le dernier facteur de zoom utilisé pour chaque site. Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page. Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement ContentLoading.

#### Fermer 

Ferme le WebView et nettoie l’instance de navigateur sous-jacente.

> public void [Close](#close)()

Le nettoyage de l’instance du navigateur entraîne la libération des ressources du WebView. L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.

Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher. Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.

Close est appelé implicitement lorsque CoreWebView2Controller perd sa référence finale et est détruit. Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application. En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements. L’appel de la fermeture rompt ce cycle en libérant tous les gestionnaires d’événements. Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement l’application WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.

#### MoveFocus 

Déplacer le focus sur le WebView.

> public void [MoveFocus](#movefocus)(raison[CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) )

WebView va mettre le focus et le focus sur l’élément correspondant dans la page hébergée dans le WebView. Pour des raisons de programmation, le focus est défini sur l’élément précédemment prioritaire ou l’élément par défaut s’il n’y a pas d’élément prioritaire auparavant. Pour une raison suivante, le focus est défini sur le premier élément. Pour une raison précédente, le focus est défini sur le dernier élément. Le mode webaffichage peut également mettre le focus sur une interaction utilisateur telle que cliquer sur le WebView ou sur Tab. Pour la fonction de tabulation, l’application peut appeler MoveFocus avec Next ou Previous pour s’aligner sur TAB et Maj + Tab lorsqu’elle décide que le WebView est l’élément tabbable suivant. Par exemple, l’application peut appeler IsDialogMessage dans le cadre de sa boucle de messages pour permettre à la plateforme de gérer automatiquement la tabulation. La plateforme est pivotée sur toutes les fenêtres avec WS_TABSTOP. Lorsque le WebView obtient le focus de IsDialogMessage, il positionne en interne le focus sur le premier ou le dernier élément de Tab et Maj + Tab respectivement.

#### NotifyParentWindowPositionChanged 

Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.

> public void [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Cela est nécessaire pour l’accessibilité et certaines boîtes de dialogue dans WebView pour fonctionner correctement.

#### SetBoundsAndZoomFactor 

Mettez à jour les propriétés de limites et de ZoomFactor en même temps.

> public void [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(encadrements, double ZoomFactor)

Cette opération est atomique du point de vue de l’hôte. Après avoir retourné la fonction, les limites et les propriétés ZoomFactor ont été mises à jour si la fonction est réussie, ou ne sont pas mises à jour en cas d’échec de la fonction. Si les limites et ZoomFactor sont toutes deux mises à jour par la même échelle (c’est-à-dire que les limites et ZoomFactor sont tous deux doublées), la page ne verra aucune modification apportée à Window. innerWidth/innerHeight et le WebView fera apparaître le contenu aux nouvelles tailles et zooms sans rendu intermédiaire. Cette fonction peut également être utilisée pour mettre à jour une seule de ZoomFactor ou de limites en passant la nouvelle valeur pour une et la valeur actuelle pour l’autre.

