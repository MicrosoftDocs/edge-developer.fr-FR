---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core
ms.openlocfilehash: e45cb4c6a6fdd01680abc59691a0e0c34a64af15
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881192"
---
# Microsoft.Web.WebView2.Core namespace 

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Format d’image utilisé par la méthode CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.
[CoreWebView2MouseEventKind](#corewebview2mouseeventkind) | Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.
[CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys) | Touches virtuelles d’événement de souris associées à un CoreWebView2MouseEventKind pour SendMouseInput.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Raison du déplacement du focus.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Le type d’une demande d’autorisation.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Réponse à une demande d’autorisation.
[CoreWebView2PointerEventKind](#corewebview2pointereventkind) | Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Type d’échec de processus utilisé dans la classe CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Type de boîte de dialogue JavaScript utilisée dans la classe CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Valeurs d’état d’erreur pour les navigations Web.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Énum pour les contextes de demande de ressources Web.
CoreWebView2 | WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.
CoreWebView2AcceleratorKeyPressedEventArgs | Arguments d’événement pour l’événement AcceleratorKeyPressed.
CoreWebView2CompositionController | Cette classe est une extension de la classe CoreWebView2Controller pour prendre en charge l’hébergement visuel.
CoreWebView2ContentLoadingEventArgs | Arguments d’événement pour l’événement ContentLoading.
CoreWebView2Controller | Cette classe est le propriétaire de l’objet CoreWebView2 et prend en charge le redimensionnement, l’affichage et le masquage, le focus, ainsi que d’autres fonctionnalités relatives à la fenêtre et à la composition.
CoreWebView2Deferral | Cette classe est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Arguments d’événement pour l’événement DevToolsProtocolEventReceived.
CoreWebView2DevToolsProtocolEventReceiver | Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.
CoreWebView2Environment | Il s’agit de l’environnement WebView2.
CoreWebView2EnvironmentOptions | Options permettant de créer un environnement WebView2.
CoreWebView2MoveFocusRequestedEventArgs | Arguments d’événement pour l’événement MoveFocusRequested.
CoreWebView2NavigationCompletedEventArgs | Arguments d’événement pour l’événement NavigationCompleted.
CoreWebView2NavigationStartingEventArgs | Arguments d’événement pour l’événement NavigationStarting.
CoreWebView2NewWindowRequestedEventArgs | Arguments d’événement pour l’événement NewWindowRequested.
CoreWebView2PermissionRequestedEventArgs | Arguments d’événement pour l’événement PermissionRequested.
CoreWebView2PointerInfo | Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.
CoreWebView2ProcessFailedEventArgs | Arguments d’événement pour l’événement ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Arguments d’événement pour l’événement ScriptDialogOpening.
CoreWebView2Settings | Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.
CoreWebView2SourceChangedEventArgs | Arguments d’événement pour l’événement SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Arguments d’événement pour l’événement WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Arguments d’événement pour l’événement WebResourceRequested.
CoreWebView2WindowFeatures | Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.
EdgeNotFoundException | Exception levée lorsqu’une installation Edge est manquante.
CoreWebView2Matrix4x4 | Cette transformation est utilisée pour calculer les coordonnées correctes lors de l’appel de CreateCoreWebView2PointerInfoFromPointerId.
CoreWebView2PhysicalKeyStatus | Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.

## Ses

#### CoreWebView2CapturePreviewImageFormat 

Format d’image utilisé par la méthode CoreWebView2CapturePreview.

> énumération [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Png            | Format d’image PNG.
Formats            | Format d’image JPEG.

#### CoreWebView2KeyEventKind 

Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.

> énumération [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
KeyDown            | Correspond à WM_KEYDOWN de messages de fenêtre.
KeyUp            | Correspond à WM_KEYUP de messages de fenêtre.
SystemKeyDown            | Correspond à WM_SYSKEYDOWN de messages de fenêtre.
SystemKeyUp            | Correspond à WM_SYSKEYUP de messages de fenêtre.

#### CoreWebView2MouseEventKind 

> [!NOTE]
> Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).

Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.

> énumération [CoreWebView2MouseEventKind](#corewebview2mouseeventkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
HorizontalWheel            | Événement de défilement de la molette horizontale de la souris, WM_MOUSEHWHEEL.
LeftButtonDoubleClick            | Double-cliquez sur le bouton gauche de la souris, WM_LBUTTONDBLCLK.
LeftButtonDown            | Bouton gauche de la souris, WM_LBUTTONDOWN.
LeftButtonUp            | Bouton gauche de la souris, WM_LBUTTONUP.
Remplissez            | Événement de départ de la souris, WM_MOUSELEAVE.
MiddleButtonDoubleClick            | Bouton du milieu cliquez deux fois sur événement de souris, WM_MBUTTONDBLCLK.
MiddleButtonDown            | Bouton du milieu de la souris, WM_MBUTTONDOWN.
MiddleButtonUp            | Bouton du milieu de la souris, WM_MBUTTONUP.
Déplacement            | Événement de déplacement de la souris, WM_MOUSEMOVE.
RightButtonDoubleClick            | Cliquez deux fois sur le bouton droit de la souris, WM_RBUTTONDBLCLK.
RightButtonDown            | Bouton droit de la souris, WM_RBUTTONDOWN.
RightButtonUp            | Cliquez sur le bouton droit de la souris, WM_RBUTTONUP.
Molette            | Événement de défilement de la roulette de la souris, WM_MOUSEWHEEL.
XButtonDoubleClick            | Premier ou deuxième bouton X Cliquez deux fois sur événement de souris, WM_XBUTTONDBLCLK.
XButtonDown            | Premier ou deuxième X boutons de la souris, WM_XBUTTONDOWN.
XButtonUp            | Premier ou deuxième X boutons vers le haut, WM_XBUTTONUP.

#### CoreWebView2MouseEventVirtualKeys 

> [!NOTE]
> Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).

Touches virtuelles d’événement de souris associées à un CoreWebView2MouseEventKind pour SendMouseInput.

> énumération [CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
None            | Aucune touche supplémentaire enfoncée.
LeftButton            | Le bouton gauche de la souris est enfoncé, MK_LBUTTON.
RightButton            | Le bouton droit de la souris est en bas, MK_RBUTTON.
Maj            | La touche Maj est enfoncée, MK_SHIFT.
Contrôle            | Touche CTRL enfoncée, MK_CONTROL.
MiddleButton            | Le bouton du milieu de la souris est en bas, MK_MBUTTON.
XButton1            | Le premier bouton X est en bas, MK_XBUTTON1.
XButton2            | Le deuxième bouton X est en bas, MK_XBUTTON2.

#### CoreWebView2MoveFocusReason 

Raison du déplacement du focus.

> énumération [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Exécuté            | Paramètre de code axé sur le WebView.
Next            | Déplacement du focus en raison d’une touche Tab.
Previous            | Déplacement du focus en partant du haut de l’onglet.

#### CoreWebView2PermissionKind 

Le type d’une demande d’autorisation.

> énumération [CoreWebView2PermissionKind](#corewebview2permissionkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
UnknownPermission            | Autorisation inconnue.
Micro            | Autorisation de capture audio.
Appareil photo            | Autorisation de capture vidéo.
Géolocalisation            | Autorisation d’accès à la géolocalisation.
Notifications            | Autorisation d’envoyer des notifications Web.
OtherSensors            | Autorisation d’accès au capteur générique.
ClipboardRead            | Autorisation de lecture du presse-papiers système sans mouvement utilisateur.

#### CoreWebView2PermissionState 

Réponse à une demande d’autorisation.

> énumération [CoreWebView2PermissionState](#corewebview2permissionstate)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Par défaut            | Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.
Autoriser            | Accordez la demande d’autorisation.
Refuser            | Refusez la demande d’autorisation.

#### CoreWebView2PointerEventKind 

> [!NOTE]
> Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).

Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.

> énumération [CoreWebView2PointerEventKind](#corewebview2pointereventkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Activer            | Correspond à WM_POINTERACTIVATE.
Vers le bas            | Correspond à WM_POINTERDOWN.
Entrée            | Correspond à WM_POINTERENTER.
Remplissez            | Correspond à WM_POINTERLEAVE.
Vers le haut            | Correspond à WM_POINTERUP.
Update            | Correspond à WM_POINTERUPDATE.

#### CoreWebView2ProcessFailedKind 

Type d’échec de processus utilisé dans la classe CoreWebView2ProcessFailedEventHandler.

> énumération [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
BrowserProcessExited            | Le processus du navigateur s’est arrêté de manière inattendue.
RenderProcessExited            | Le processus de rendu s’est arrêté de manière inattendue.
RenderProcessUnresponsive            | Le processus de rendu ne répond pas.

#### CoreWebView2ScriptDialogKind 

Type de boîte de dialogue JavaScript utilisée dans la classe CoreWebView2ScriptDialogOpeningEventHandler.

> énumération [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Alerte            | Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.
Confirmer            | Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.
Demandant            | Une boîte de dialogue appelée via la fonction JavaScript window. prompt.
Beforeunload            | Une boîte de dialogue appelée via la fonction JavaScript window. beforeunload.

#### CoreWebView2WebErrorStatus 

Valeurs d’état d’erreur pour les navigations Web.

> énumération [CoreWebView2WebErrorStatus](#corewebview2weberrorstatus)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Inconnu            | Une erreur inconnue s’est produite.
CertificateCommonNameIsIncorrect            | Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.
CertificateExpired            | Le certificat SSL a expiré.
ClientCertificateContainsErrors            | Le certificat client SSL comporte des erreurs.
CertificateRevoked            | Le certificat SSL a été révoqué.
CertificateIsInvalid            | Le certificat SSL n’est pas valide &ndash; cela peut signifier que le certificat ne correspond pas aux codes confidentiels de clé publique du nom d’hôte. le certificat est signé par une autorité non approuvée ou à l’aide d’un algorithme de signature faible, le certificat ayant revendiqué des noms DNS enfreignant les contraintes de nom, le certificat contient une clé faible, la période de validité du certificat est trop longue, l’absence de données de révocation ou du mécanisme de révocation, le [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)nom d’hôte non unique, l’absence de données de transparence de
ServerUnreachable            | L’hôte n’est pas joignable.
Délai d’expiration dépassé            | La connexion a expiré.
ErrorHttpInvalidServerResponse            | Le serveur a renvoyé une réponse non valide ou non reconnue.
ConnectionAborted            | La connexion a été annulée.
ConnectionReset            | La connexion a été réinitialisée.
Déconnecté            | La connexion Internet a été interrompue.
CannotConnect            | Connexion impossible à la destination.
HostNameNotResolved            | Impossible de résoudre le nom d’hôte fourni.
OperationCanceled            | L’opération a été annulée.
RedirectFailed            | Échec de la redirection de la requête.
UnexpectedError            | Une erreur inattendue s’est produite.

#### CoreWebView2WebResourceContext 

Énum pour les contextes de demande de ressources Web.

> énumération [CoreWebView2WebResourceContext](#corewebview2webresourcecontext)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Tous            | Toutes les ressources.
Document            | Ressources de documents.
Style            | Des ressources CSS;
Image            | Ressources d’image.
Support            | Autres ressources multimédias telles que les vidéos.
Police            | Ressources de police.
Script            | Ressources de script.
XmlHttpRequest            | Requêtes HTTP XML.
Recherche            | Extraire la communication de l’API.
TextTrack            | Ressources TextTrack.
EventSource            | Communication API EventSource.
Websocket            | Communication de l’API WebSocket.
Manifeste            | Manifestes de l’application Web.
SignedExchange            | Échange HTTP signé.
Test ping            | Demandes ping.
CspViolationReport            | Rapports de violation des CSP.
Other            | Autres ressources.

