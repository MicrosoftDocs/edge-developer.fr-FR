---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2fdd047068ec761e1fcd3d3031d4c6c911a5b1ef
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752254"
---
# Globals 

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[CompareBrowserVersions](#comparebrowserversions) | Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Crée un environnement WebView2 persistant à l’aide de la version latérale installée.
[CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions) | Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.
[GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring) | Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.

## Ses

#### CompareBrowserVersions 

> public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int * result)

Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.

Il peut être utilisé pour déterminer s’il est possible d’utiliser webview2 ou certaines fonctionnalités de la version. Définit la valeur de result sur-1, 0 ou 1 si la valeur version1 est inférieure ou égale ou supérieure à la valeur version2 respectivement. Renvoie E_INVALIDARG s’il n’y a pas d’analyse des chaînes de version ou si aucun paramètre d’entrée n’a la valeur null. Les données d’entrée peuvent utiliser directement le versionInfo obtenu à partir de GetAvailableCoreWebView2BrowserVersionString, les informations de canal seront ignorées.

#### CreateCoreWebView2Environment 

> public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environment_created_handler)

Crée un environnement WebView2 persistant à l’aide de la version latérale installée.

Cela équivaut à appeler CreateCoreWebView2EnvironmentWithOptions avec nullptr pour browserExecutableFolder, userDataFolder, additionalBrowserArguments. Pour plus d’informations, consultez CreateCoreWebView2EnvironmentWithOptions.

#### CreateCoreWebView2EnvironmentWithOptions 

> public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) * environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environment_created_handler)

Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.

Permet `browserExecutableFolder` de spécifier si les contrôles de WebView2 utilisent une version incorporée de Edge ou la version installée d’Edge qui existe sur un ordinateur client. Pour utiliser une version incorporée de Edge, transmettez le chemin d’accès relatif du dossier qui contient la version incorporée de Edge à `browserExecutableFolder` . Pour obtenir la version incorporée de Edge, copiez le nom du dossier version à partir de la version installée de Edge sur un ordinateur client. Par exemple, copiez le `73.0.52.0` dossier à partir du dossier dans lequel la version Edge 73.0.52.0 a été installée. Assurez-vous que le dossier comporte les fichiers **msedgewebview2.exe** et **msedge.dll** . Pour créer des contrôles WebView2 qui utilisent la version installée de Edge qui existe sur les ordinateurs clients, transmettez une chaîne null ou vide à `browserExecutableFolder` . Dans ce scénario, l’API tente de rechercher une version compatible d’Edge qui est installée sur l’ordinateur client (tout d’abord au niveau de l’ordinateur, puis par utilisateur) en utilisant les préférences de canal sélectionnées. 

L’ordre de recherche de canal par défaut est stable, bêta, dev et Canaries. S’il existe une substitution WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable d’environnement ou une valeur de Registre releaseChannelPreference applicable ayant la valeur 1, l’ordre de recherche de canal est inversé.

userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2. Il peut s’agir d’un chemin d’accès absolu ou d’un chemin de fichier relatif qui est interprété comme relatif au fichier exécutable du processus actuel. Dans le cas contraire, pour les applications UWP, le dossier de données utilisateur par défaut sera le dossier Data App pour le package. dans le cas des applications non UWP, le dossier de données utilisateur par défaut `{Executable File Name}.WebView2` sera créé dans le même répertoire en regard du fichier exécutable de l’application. La création de WebView2 peut échouer si le fichier exécutable s’exécute dans un répertoire dans lequel le processus n’est pas autorisé à créer un nouveau dossier. Lorsque l’application est exécutée, l’application est chargée de nettoyer son dossier de données utilisateur.

Notez que, dans la mesure où le processus de navigateur peut être partagé entre les WebViews, la création de WebView échoue avec HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si les options spécifiées ne correspondent pas aux options des webvues actuellement en cours d’exécution dans le processus de navigateur partagé.

environment_created_handler est le résultat du gestionnaire à l’opération asynchrone qui contient le WebView2Environment qui a été créé.

Le browserExecutableFolder, userDataFolder et additionalBrowserArguments du environmentOptions peut être substitué par les valeurs spécifiées dans les variables d’environnement ou dans le registre.

Lors de la création d’un WebView2Environment, les variables d’environnement suivantes sont activées:

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

S’il existe une variable d’environnement de substitution, nous utilisons les valeurs browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithOptions.

Bien qu’il ne soit pas nécessaire de remplacer strictement, il existe d’autres variables d’environnement qui peuvent être définies:

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Dans le cas d’une valeur non vide, cela indique que le WebView est démarré sous un débogueur de script. Dans ce cas, le WebView lancera une `Page.waitForDebugger` commande CDP qui entraînera l’exécution du script à l’intérieur du WebView sur le lancement, jusqu’à ce qu’un débogueur publie une `Runtime.runIfWaitingForDebugger` commande CDP correspondante pour reprendre l’exécution. Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Dans le cas d’une valeur non vide, cela signifie que l’application WebView est lancée sous un débogueur de script qui prend également en charge les applications hébergées sur plusieurs vues Web. La valeur est utilisée comme identificateur pour un canal nommé qui sera ouvert et écrit lors de la création d’un nouveau WebView par l’application hôte. La charge utile correspond à celle de la cible JSON du débogage à distance et peut être utilisée par le débogueur externe pour être attachée à une instance WebView spécifique. Le format du canal créé par le débogueur doit être `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` le suivant:

* `{app_name}` est le nom de fichier exe de l’application hôte, par exemple WebView2Example.exe

* `{pipe_name}` est la valeur définie pour WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Pour activer le débogage des cibles identifiées par le JSON, vous devez également définir la variable d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS à envoyer `--remote-debugging-port={port_num}` :

* `{port_num}` correspond au port sur lequel est lié le serveur CDP.

N’ayez pas à faire en sorte que la définition des variables d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS et WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER entraîne l’affichage des webvues hébergées dans votre application et de leur contenu aux applications tierces, telles que les débogueurs.

Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.

S’il n’existe aucune de ces variables d’environnement, le Registre est examiné suivant. Les clés de Registre suivantes sont activées:

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

Dans le cas improbable où certaines instances de WebView sont ouvertes lors d’une mise à jour de navigateur, nous pouvons dès lors bloquer la suppression de anciens navigateurs de bord. Pour éviter de manquer d’espace disque, une nouvelle création d’affichage WebView échoue avec l’erreur suivante s’il détecte qu’il existe de nombreuses versions antérieures.

```
ERROR_DISK_FULL
```

Le nombre maximal de versions Edge autorisées par défaut est 20.

Il est possible d’écraser le nombre maximal de versions latérales antérieures autorisées avec la valeur de la variable d’environnement suivante.

```
WEBVIEW2_MAX_INSTANCES
```

Si WebView dépend d’une périphérie installée et qu’elle est désinstallée, tout création ultérieure échoue avec l’erreur suivante

```
ERROR_PRODUCT_UNINSTALLED
```

Tout d’abord, nous allons vérifier avec root, puis HKCU. AppId est d’abord défini sur l’ID de modèle utilisateur de l’application du processus de l’appelant, s’il n’y a pas de clé de Registre correspondante, l’AppId est défini sur le nom exécutable du processus de l’appelant, ou si ce n’est pas une clé de Registre, ' * '. S’il existe une clé de registre de remplacement, nous utilisons les valeurs de Registre browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithOptions.

#### GetAvailableCoreWebView2BrowserVersionString 

> public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr * VERSIONINFO)

Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.

Les noms de canaux sont Beta, dev et Canaries. S’il existe un remplacement pour le browserExecutableFolder ou l’option de canal, la substitution est utilisée. S’il n’y a pas de remplacement, le paramètre transmis à GetAvailableCoreWebView2BrowserVersionString est utilisé.
