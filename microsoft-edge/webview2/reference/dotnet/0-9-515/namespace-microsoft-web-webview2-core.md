---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e9270705ff6c72167185bddfea6f6f310ebc2e3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877664"
---
# 0.9.515-espace de noms Microsoft. Web. WebView2. Core 

> [!NOTE]
> Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515. Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Format d’image utilisé par la méthode CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Raison du déplacement du focus.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Le type d’une demande d’autorisation.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Réponse à une demande d’autorisation.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Type d’échec de processus utilisé dans la classe CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Type de boîte de dialogue JavaScript utilisée dans la classe CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Valeurs d’état d’erreur pour les navigations Web.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Énum pour les contextes de demande de ressources Web.
CoreWebView2 | WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.
CoreWebView2AcceleratorKeyPressedEventArgs | Arguments d’événement pour l’événement AcceleratorKeyPressed.
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
CoreWebView2ProcessFailedEventArgs | Arguments d’événement pour l’événement ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Arguments d’événement pour l’événement ScriptDialogOpening.
CoreWebView2Settings | Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.
CoreWebView2SourceChangedEventArgs | Arguments d’événement pour l’événement SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Arguments d’événement pour l’événement WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Arguments d’événement pour l’événement WebResourceRequested.
EdgeNotFoundException | Exception levée lorsqu’une installation Edge est manquante.
CoreWebView2PhysicalKeyStatus | Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.

## Ses

#### CoreWebView2CapturePreviewImageFormat 

> énumération [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Png            | Format d’image PNG.
Formats            | Format d’image JPEG.

Format d’image utilisé par la méthode CoreWebView2CapturePreview.

#### CoreWebView2KeyEventKind 

> énumération [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
KeyDown            | Correspond à WM_KEYDOWN de messages de fenêtre.
KeyUp            | Correspond à WM_KEYUP de messages de fenêtre.
SystemKeyDown            | Correspond à WM_SYSKEYDOWN de messages de fenêtre.
SystemKeyUp            | Correspond à WM_SYSKEYUP de messages de fenêtre.

Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.

#### CoreWebView2MoveFocusReason 

> énumération [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Exécuté            | Paramètre de code axé sur le WebView.
Next            | Déplacement du focus en raison d’une touche Tab.
Previous            | Déplacement du focus en partant du haut de l’onglet.

Raison du déplacement du focus.

#### CoreWebView2PermissionKind 

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

Le type d’une demande d’autorisation.

#### CoreWebView2PermissionState 

> énumération [CoreWebView2PermissionState](#corewebview2permissionstate)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Par défaut            | Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.
Autoriser            | Accordez la demande d’autorisation.
Refuser            | Refusez la demande d’autorisation.

Réponse à une demande d’autorisation.

#### CoreWebView2ProcessFailedKind 

> énumération [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
BrowserProcessExited            | Le processus du navigateur s’est arrêté de manière inattendue.
RenderProcessExited            | Le processus de rendu s’est arrêté de manière inattendue.
RenderProcessUnresponsive            | Le processus de rendu ne répond pas.

Type d’échec de processus utilisé dans la classe CoreWebView2ProcessFailedEventHandler.

#### CoreWebView2ScriptDialogKind 

> énumération [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
Alerte            | Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.
Confirmer            | Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.
Demandant            | Une boîte de dialogue appelée via la fonction JavaScript window. prompt.
Beforeunload            | Une boîte de dialogue appelée via la fonction JavaScript window. beforeunload.

Type de boîte de dialogue JavaScript utilisée dans la classe CoreWebView2ScriptDialogOpeningEventHandler.

#### CoreWebView2WebErrorStatus 

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

Valeurs d’état d’erreur pour les navigations Web.

#### CoreWebView2WebResourceContext 

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

Énum pour les contextes de demande de ressources Web.

