---
description: Modèle de thread
title: Modèle de thread
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013736"
---
# Modèle de thread 

Le contrôle WebView2 est basé sur le [modèle COM (Component Object Model)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) et doit être exécuté sur un thread de type [thread unique cloisonné (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .

## Sécurité des threads  

WebView2 doit être créé sur un thread d’interface utilisateur.  Particulièrement un thread avec une pompe de messages.  Tous les rappels se produisent sur ce thread et les requêtes dans le WebView2 doivent être effectuées sur ce thread.  Il n’est pas sûr d’utiliser le WebView2 à partir d’un autre thread.  

La seule exception est pour la `Content` propriété de `CoreWebView2WebResourceRequest` .  Le `Content` flux de propriété est lu à partir d’un thread d’arrière-plan.  Le flux doit être une technologie agile ou être créé à partir d’une tâche STA d’arrière-plan pour éviter l’impact sur les performances du thread d’interface utilisateur.  

## Entr  

Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série.  Si vous disposez d’un gestionnaire d’événements et commencez une boucle de messages, aucun gestionnaire d’événements ou aucun rappel d’achèvement ne peut commencer à s’exécuter dans une méthode réentrante.  

## Reports  

Certains événements WebView2 lisent les valeurs définies sur leurs arguments d’événement ou effectuent une action après la fin du gestionnaire d’événements.  Si vous devez également exécuter une opération asynchrone telle qu’un gestionnaire d’événements, vous pouvez utiliser la `GetDeferral` méthode sur les arguments d’événement des événements associés.  L’objet de report retourné garantit que le gestionnaire d’événements n’est pas considéré comme complet tant que la `Complete` méthode de l' `Deferral` est demandée.  

Par exemple, vous pouvez utiliser l' `NewWindowRequested` événement pour fournir une `CoreWebView2` connexion en tant que fenêtre enfant lorsque le gestionnaire d’événements est terminé.  Mais si vous avez besoin de créer la `CoreWebView2` méthode de manière asynchrone, demandez la `GetDeferral` méthode sur le `NewWindowRequestedEventArgs` .  Une fois que vous avez créé le et que vous avez `CoreWebView2` défini la `NewWindow` propriété sur la `NewWindowRequestedEventArgs` requête, l' `Complete` objet est retourné de manière asynchrone `Deferral` à l’aide de la `GetDeferral` méthode.  

<!-- links -->  
