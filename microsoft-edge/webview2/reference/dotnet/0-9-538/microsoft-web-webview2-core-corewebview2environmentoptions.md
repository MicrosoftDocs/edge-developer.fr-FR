---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
ms.openlocfilehash: 705e030caba03227749002bad8c9777197839a28
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885561"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Options permettant de créer un environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.
[IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled) | La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.
[Langue](#language) | La langue par défaut avec laquelle le WebView sera exécuté.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Initialise une nouvelle instance de la classe CoreWebView2EnvironmentOptions.

Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.

## Ses

#### AdditionalBrowserArguments 

AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.

> [AdditionalBrowserArguments](#additionalbrowserarguments) de chaîne publique

Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande. Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) . Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur. Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView. Ces commutateurs seront ignorés même en cas de spécification. Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne. Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé. Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées. La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments. Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées. Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée. Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.

#### IsSingleSignOnUsingOSPrimaryAccountEnabled 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.

> public bool [IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled)

La valeur par défaut est Disabled. Les applications de plateforme Windows universelle doivent également déclarer la [fonctionnalité restreinte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO pour que l’authentification unique fonctionne.

#### Langue 

La langue par défaut avec laquelle le WebView sera exécuté.

> [langage](#language) de chaîne publique

Il s’applique aux interfaces utilisateur du navigateur comme le menu contextuel et les boîtes de dialogue. Il s’applique également à l’en-tête HTTP Accept-Language que le WebView envoie aux sites Web. La mise en forme est de l' `language[-country]` endroit où `language` se trouve le code à deux lettres ISO 639 et `country` correspond au code 2 lettres de l’ISO 3166.

#### TargetCompatibleBrowserVersion 

La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.

> [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) de chaîne publique

Par défaut, il s’agit de la version latérale du runtime WebView2 qui correspond à la version du SDK utilisée par l’application. Le format de cette valeur est identique à celui de la propriété BrowserVersionString et des autres valeurs BrowserVersion. Seule la partie version de la valeur BrowserVersion est respectée. Le suffixe de canal, s’il existe, est ignoré. La version des fichiers binaires Edge WebView2 Runtime utilisés est susceptible d’être différente de la TargetCompatibleBrowserVersion spécifiée. Ils sont uniquement compatibles. Vous pouvez vérifier la version réelle sur la propriété BrowserVersionString sur CoreWebView2Environment.

#### CoreWebView2EnvironmentOptions 

Initialise une nouvelle instance de la classe CoreWebView2EnvironmentOptions.

> public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(chaîne additionalBrowserArguments, langage de chaîne, chaîne targetCompatibleBrowserVersion)

##### Parameters
* `additionalBrowserArguments` AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView. 

* `language` La langue par défaut avec laquelle le WebView sera exécuté. 

* `targetCompatibleBrowserVersion` La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.

