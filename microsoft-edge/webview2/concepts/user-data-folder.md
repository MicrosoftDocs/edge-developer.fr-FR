---
description: Découvrez comment gérer les dossiers de données utilisateur dans les applications WebView2
title: Gérer le dossier de données utilisateur dans les applications WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, user data folder
ms.openlocfilehash: a6399e59f153d4446946937461e61667f325f4ae
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535889"
---
# <a name="manage-the-user-data-folder"></a>Gérer le dossier de données utilisateur  

Les applications WebView2 interagissent avec les dossiers de données utilisateur pour stocker les données du navigateur, telles que les cookies, les autorisations et les ressources mises en cache.  Chaque instance d’un contrôle WebView2 est associée à un dossier de données utilisateur.  Chaque dossier de données utilisateur est propre à un utilisateur.  

## <a name="best-practices"></a>Meilleures pratiques  

Les dossiers de données utilisateur sont créés automatiquement par WebView2.  Les développeurs WebView2 contrôlent la durée de vie du dossier de données utilisateur.  Si votre application ré-utilise les données utilisateur des sessions d’application, envisagez d’enregistrer les dossiers de données utilisateur, sinon vous pouvez les supprimer.  Prenons les scénarios suivants lorsque vous décidez comment gérer vos dossiers de données utilisateur :  

*   Si le même utilisateur utilise votre application à plusieurs reprises et que le contenu web de l’application s’appuie sur les données de l’utilisateur, enregistrez le dossier de données utilisateur.  Si plusieurs utilisateurs utilisent votre application à plusieurs reprises, créez un dossier de données utilisateur pour chaque nouvel utilisateur et enregistrez le dossier de données utilisateur de chaque utilisateur.
*   Si votre application ne contient pas d’utilisateurs répétés, créez un dossier de données utilisateur pour chaque utilisateur et supprimez le dossier de données utilisateur précédent.  
    
## <a name="create-user-data-folders"></a>Créer des dossiers de données utilisateur  

Pour spécifier l’emplacement du dossier de données utilisateur, incluez le paramètre lorsque vous appelez `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Après la création, les données de navigateur de votre contrôle WebView2 sont stockées dans un sous-foldeur de `userDataFolder` .  `userDataFolder`Lorsqu’il n’est pas spécifié, WebView2 crée des dossiers de données utilisateur aux emplacements par défaut comme suit :  

*   Pour les Windows du Windows Store, le dossier utilisateur par défaut est le sous-dossier du `ApplicationData\LocalFolder` dossier du package.  
*   Pour les applications de bureau existantes, le dossier de données utilisateur par défaut est le chemin d’accès exe de votre application + `.WebView2` .  Au lieu d’utiliser la valeur par défaut, nous vous recommandons de spécifier un dossier de données utilisateur et de le créer dans le même dossier où sont stockées toutes les autres données d’application.  
    
## <a name="delete-user-data-folders"></a>Supprimer des dossiers de données utilisateur  

Votre application devra peut-être supprimer des dossiers de données utilisateur :  

*   Lors de la désinstallation de votre application.  Si vous désinstallez des applications empaquetées Windows store, Windows supprime automatiquement les dossiers de données utilisateur.  
*   Pour nettoyer tout l’historique des données de navigation.  
*   Pour récupérer à partir d’une altération des données.  
*   Pour supprimer les données de session précédentes.  
    
> [!NOTE]
> Les fichiers des dossiers de données utilisateur peuvent toujours être utilisés après la fermeture de l’application WebView2.  Dans ce cas, attendez que le processus du navigateur et tous les processus enfants se quittent avant de supprimer le dossier.  Vous pouvez récupérer l’ID de processus du processus de navigateur à l’aide de la `BrowserProcessId` propriété webView2.  

## <a name="share-user-data-folders"></a>Partager des dossiers de données utilisateur  

Les contrôles WebView2 peuvent partager les mêmes dossiers de données utilisateur pour :  

*   [Optimisez les ressources système](../concepts/process-model.md) en l’exécutant dans un processus de navigateur.  
*   Partagez l’historique du navigateur et les ressources mises en cache.  
    
Prenons les considérations suivantes lors du partage de dossiers de données utilisateur :  

1.  Lorsque vous re-créez des contrôles WebView2 pour mettre à jour les versions du navigateur à l’aide d’événements [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) ou [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\), assurez-vous que les processus de navigateur quittent et ferment les contrôles WebView2 qui partagent le même dossier de données utilisateur.  Pour récupérer l’ID de processus du processus de navigateur, utilisez la `BrowserProcessId` propriété du contrôle WebView2.  
1.  Les contrôles WebView2 qui partagent le même dossier de données utilisateur doivent utiliser les mêmes options pour [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Si ce n’est pas le cas, la création de WebView2 échouera avec `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  
    
Pour isoler différentes parties de votre application ou lorsque le partage de données entre les contrôles WebView2 n’est pas nécessaire, vous pouvez choisir d’utiliser différents dossiers de données utilisateur.  Par exemple, une application peut se composer de deux contrôles WebView2, l’un pour l’affichage d’une annonce et l’autre pour l’affichage du contenu de l’application.  Dans ce scénario, les développeurs peuvent choisir d’utiliser différents dossiers de données utilisateur pour chaque contrôle WebView2.  

> [!NOTE]
> Chaque processus de navigateur WebView2 consomme de la mémoire et de l’espace disque supplémentaires.  Par conséquent, nous vous recommandons de ne pas l’exécution de WebView2s avec un trop grand nombre de dossiers de données utilisateur différents en même temps.  
