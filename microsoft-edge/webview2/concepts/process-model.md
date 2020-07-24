---
description: Modèle de processus
title: Modèle de processus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895545"
---
# Modèle de processus  

WebView2 utilise le même modèle de processus que le navigateur Microsoft Edge.  Pour plus d’informations sur le modèle de processus de navigateur, voir [architecture de navigateur-dans l’interface du navigateur Web moderne][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]. 

Un processus de navigateur est associé aux processus de convertisseur et aux autres processus d’utilitaire, comme décrit dans cet article.  Par ailleurs, dans le cas de WebView2, il existe une application hôte demandant des processus à l’aide de WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processus 1" lightbox="../media/process-model-1.png":::
   Processus 1  
:::image-end:::  

Un processus de navigateur est spécifié par dossier de données utilisateur dans une session utilisateur qui répond à tous les processus de demande WebView2 qui spécifient ce dossier de données utilisateur.  Cela signifie qu’un processus de navigateur est susceptible de traiter plusieurs processus de demande et qu’un processus de requête est susceptible d’utiliser plusieurs processus de navigateur.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processus 2" lightbox="../media/process-model-2.png":::
   Processus 2  
:::image-end:::  

Un processus de navigateur a un certain nombre de processus de rendu associés.  Les processus du navigateur sont créés selon les besoins pour traiter les trames éventuellement multiples dans différentes instances de WebView2.  Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolation de site et du nombre d’origines déconnectées distinctes rendues dans les instances associées de WebView2.  La fonctionnalité navigateur d’isolation du site est décrite dans le contenu précédent.  

`CoreWebView2Environment`Représente un dossier de données utilisateur et un processus de navigateur.  Le `CoreWebView2` ne correspond pas directement à un ensemble de processus, car divers processus de rendu sont utilisés par un WebView2, en fonction de l’isolement du site, comme décrit précédemment.  

Vous pouvez réagir aux blocages et se bloquer dans ces processus de navigateur et de convertisseur à l’aide `ProcessFailed` de l’événement de `CoreWebView2` .  

Vous pouvez arrêter en toute sécurité les processus de navigateur et de convertisseur associés à l’aide `Close` de la méthode de `CoreWebView2Controller` .  

Pour ouvrir la fenêtre Gestionnaire des tâches du navigateur à partir de la fenêtre de **devtools** d’une instance de WebView2, vous pouvez sélectionner `Shift` + `Escape` la barre de titre de la fenêtre devtools, ouvrir le menu contextuel (cliquez avec le bouton droit de la souris \) et choisir `Browser task manager` .  Tous les processus associés au processus de navigation de votre WebView2 sont affichés, y compris les objectifs associés.  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Architecture de navigateur-dans l’interface du navigateur Web moderne (partie 1)"  
