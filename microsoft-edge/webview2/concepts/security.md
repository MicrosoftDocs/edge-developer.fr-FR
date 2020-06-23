---
description: Apprenez à développer des applications WebView2 sécurisées
title: Recommandations en matière de développement d’applications WebView2 sécurisées
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, sécurité
ms.openlocfilehash: e71dbe9ad98b7156d8888da074e30a96683469d5
ms.sourcegitcommit: e49b86082da884299fdd485d3311d63a7688c0d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2020
ms.locfileid: "10755395"
---
# Recommandations en matière de développement d’applications WebView2 sécurisées

Le [contrôle WebView2](https://docs.microsoft.com/microsoft-edge/webview2/) permet aux développeurs d’héberger du contenu Web dans leurs applications natives. En cas d’utilisation correcte, le contenu Web d’hébergement offre plusieurs avantages, comme l’utilisation de l’interface utilisateur Web, l’accès aux fonctionnalités de la plateforme Web, le partage de code multiplateforme, etc. Pour éviter toute vulnérabilité pouvant découler de l’hébergement de contenu Web, veillez à concevoir votre application WebView2 pour surveiller étroitement les interactions entre le contenu Web et l’application hôte. 

1. Considérer tout le contenu Web comme non sécurisé
    - Validez les messages Web et les paramètres d’objet hôtes avant de les utiliser, car les messages et les paramètres Web peuvent être mal formés (involontairement ou malveillants) et provoquer une inadvertance du comportement de l’application.
    - Vérifiez toujours l’origine du document exécuté dans WebView2 et évaluez la fiabilité du contenu. 

2. Concevez des messages Web et des interactions d’objets hôtes spécifiques au lieu d’utiliser des proxys génériques.

3. Restreignez la fonctionnalité de contenu Web en modifiant [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) ou [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) en procédant comme suit:
    - Définissez `AreHostObjectsAllowed` la valeur sur `false` , si vous ne pensez pas que le contenu Web accède aux objets hôtes.
    - Définissez `IsWebMessageEnabled` la valeur sur `false` , si vous ne pensez pas que le contenu Web publie des messages Web dans votre application native. 
    - Définissez `IsScriptEnabled` sur `false` , si vous ne pensez pas que le contenu Web doit exécuter des scripts (par exemple, lors de l’affichage de contenu HTML statique).
    - Définissez `AreDefaultScriptDialogsEnabled` sur `false` , si vous ne pensez pas que le contenu Web s’affiche ou ne s’affiche pas `alert` `prompt` .

4.  Utilisez les `NavigationStarting` `FrameNavigationStarting` événements et pour mettre à jour les paramètres en fonction de l’origine de la nouvelle page comme suit:
    1.  Pour éviter que votre application ne navigue vers certaines pages, utilisez ces événements pour vérifier et bloquer la navigation par page ou cadre. 
    2.  Lorsque vous naviguez vers une nouvelle page, il est possible que vous deviez ajuster les valeurs de propriétés sur [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) ou [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) 'comme décrit ci-dessus.

5. Lorsque vous naviguez vers un nouveau document, utilisez l' `ContentLoading` événement pour supprimer les objets hôtes exposés à l’aide de `RemoveHostObjectFromScript` . 