---
description: Apprenez à gérer les dossiers de données utilisateur dans les applications WebView2
title: Gestion du dossier des données utilisateur dans les applications WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, dossier de données utilisateur
ms.openlocfilehash: ff11c4e83fa931a97ed1b5c8afa4a30b5c0b5d25
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118988"
---
# Gestion du dossier de données utilisateur  

Les applications WebView2 interagissent avec les dossiers de données utilisateur pour stocker les données du navigateur, telles que les cookies, les autorisations et les ressources mises en cache.  Chaque instance d’un contrôle WebView2 est associée à un dossier de données utilisateur.  Chaque dossier de données utilisateur est propre à un utilisateur.  

## Meilleures pratiques  

Les dossiers de données utilisateurs sont créés automatiquement par WebView2.  Les développeurs WebView2 contrôlent la durée de vie du dossier des données utilisateur.  Si votre application réutilise les données utilisateur des sessions d’application, envisagez d’enregistrer les dossiers de données des utilisateurs, sinon vous pouvez les supprimer.  Prenez en compte les scénarios suivants lorsque vous décidez comment gérer vos dossiers de données utilisateur:  

*   Si le même utilisateur utilise votre application de manière répétée et que le contenu Web de l’application repose sur les données de l’utilisateur, enregistrez le dossier des données utilisateur.  Si plusieurs utilisateurs utilisent votre application de manière répétée, créez un nouveau dossier de données utilisateur pour chaque nouvel utilisateur, puis enregistrez le dossier des données utilisateur de chaque utilisateur.
*   Si votre application n’a pas de répétition d’utilisateurs, créez un nouveau dossier de données utilisateur pour chaque utilisateur, puis supprimez le dossier des données utilisateur précédent.  

## Créer des dossiers de données utilisateur  

Pour spécifier l’emplacement du dossier de données de l’utilisateur, incluez le `userDataFolder` paramètre lors de l’appel à [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.net \).  Après la création, les données de navigateur de votre contrôle WebView2 sont stockées dans un sous-dossier de `userDataFolder` .  Lorsque `userDataFolder` n’est pas spécifié, WebView2 crée des dossiers de données utilisateur aux emplacements par défaut comme suit:  

*   Pour les applications du Windows Store empaquetées, le dossier utilisateur par défaut est le sous `ApplicationData\LocalFolder` -dossier du dossier du package.  
*   Pour les applications de bureau existantes, le dossier de données utilisateur par défaut est le chemin d’accès exe de votre application + `.WebView2` .  Au lieu d’utiliser la valeur par défaut, il est recommandé de spécifier un dossier de données utilisateur et de le créer dans le même dossier que celui où sont stockées toutes les autres données d’application.  

## Supprimer des dossiers de données utilisateur  

Il est possible que votre application ait besoin de supprimer les dossiers de données des utilisateurs:  

*   Lors de la désinstallation de votre application.  Si vous désinstallez les applications du Windows Store empaquetées, Windows supprime automatiquement les dossiers de données utilisateur.  
*   Pour nettoyer l’historique de vos données de navigation.  
*   Pour récupérer des données endommagées.  
*   Pour supprimer les données de la session précédente.  

> [!NOTE]
> Les fichiers dans les dossiers de données utilisateur sont peut-être toujours en cours d’utilisation après la fermeture de l’application WebView2.  Dans ce cas, attendez la fin du processus de navigateur et de tous les processus enfants avant de supprimer le dossier.  Vous pouvez récupérer l’ID de processus du processus du navigateur à l’aide `BrowserProcessId` de la propriété de WebView2.  

## Partager des dossiers de données utilisateur  

Les contrôles WebView2 risquent de partager les mêmes dossiers de données utilisateur pour:  

*   [Optimisez les ressources système](../concepts/process-model.md) en les exécutant dans un seul processus de navigateur.  
*   Partager l’historique du navigateur et les ressources mises en cache.  

Prenez en considération les points suivants lors du partage de dossiers de données utilisateur:  

1.  Lors de la recréation de contrôles WebView2 pour mettre à jour des versions de navigateur à l’aide d' [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \ (Win32 \) ou de [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \ (.net \), assurez-vous que les processus de navigateur ferment et ferment WebView2 contrôles qui partagent le même dossier de données utilisateur.  Pour récupérer l’ID de processus du processus du navigateur, utilisez la `BrowserProcessId` propriété du contrôle WebView2.  

2.  Les contrôles WebView2 qui partagent le même dossier de données utilisateur doivent utiliser les mêmes options pour [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.net \).  Si ce n’est pas le cas, la création de WebView2 échoue avec `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  

Pour isoler différentes parties de votre application ou lorsque vous n’avez pas besoin de partager des données entre des contrôles WebView2, vous pouvez choisir d’utiliser différents dossiers de données utilisateur.  Par exemple, une application est composée de deux contrôles WebView2, l’un pour afficher une publicité et l’autre pour l’affichage du contenu de l’application.  Dans ce scénario, les développeurs peuvent choisir d’utiliser différents dossiers de données utilisateur pour chaque contrôle WebView2.  

> [!NOTE]
> Chaque processus de navigateur WebView2 utilise une mémoire et un espace disque supplémentaires.  Par conséquent, nous vous conseillons de ne pas exécuter WebView2s avec un trop grand nombre de dossiers de données utilisateur en même temps.  
