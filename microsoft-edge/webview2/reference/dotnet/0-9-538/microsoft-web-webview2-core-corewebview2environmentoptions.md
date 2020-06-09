---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 7bade615e2783631901b6e5146a636d824f909c1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698605"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions 

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Options permettant de créer un environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.
[Langue](#language) | La langue par défaut avec laquelle le WebView sera exécuté.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Initialise une nouvelle instance de la classe CoreWebView2EnvironmentOptions.

Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.

## Ses

#### AdditionalBrowserArguments 

AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.

> [AdditionalBrowserArguments](#additionalbrowserarguments) de chaîne publique

Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande. Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) . Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur. Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView. Ces commutateurs seront ignorés même en cas de spécification. Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne. Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé. Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées. La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments. Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées. Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée. Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.

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

