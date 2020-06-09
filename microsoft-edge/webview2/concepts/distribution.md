---
description: Options de distribution lors de la publication d’une application à l’aide de Microsoft Edge WebView2
title: Distribution de l’application Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: ec623da0181a4f21c3192652b0d098f922225b0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697923"
---
# Distribution d’applications à l’aide de WebView2 

Le contrôle WebView2 utilise le navigateur Microsoft Edge \ (chrome \). Lors de la distribution de votre application, assurez-vous que le navigateur Edge est installé sur tous les ordinateurs utilisateurs exécutant votre application. Le contrôle WebView2 utilise la version la plus stable du navigateur installée sur un ordinateur. Par exemple, il est possible que vous disposiez de la version stable, bêta, dev et Canaries en même temps, et dans ce cas, les contrôles WebView2 s’exécutent dans le canal stable. Assurez-vous de consulter les notes de publication pour vous assurer que la version du navigateur installée sur vos ordinateurs qui exécutent vos contrôles WebView2 répond à la configuration minimale requise pour la version.

## Feuille de route

Nous sommes conscients que le navigateur Edge peut ne pas être disponible sur tous les ordinateurs des utilisateurs dans lesquels votre application sera exécutée ou si l’installation de votre navigateur Edge au sein de votre organisation risque d’être difficile. Pour vous assurer que votre application s’exécute sur tous les ordinateurs, indépendamment du navigateur Microsoft Edge installé, nous allons libérer Microsoft Edge WebView2 Runtime. Par ailleurs, nous mettons à jour WebView2 pour rechercher la version stable du runtime avant de rechercher des versions préliminaires du navigateur installé.

Les deux options de distribution sont prises en charge à l’aide du WebView2 Runtime: persistant et de la version corrigée.

Les feuilles de distribution seront les modèles de distribution recommandés pour la plupart des développeurs. Dans ce mode, les mises à jour sont transmises automatiquement à l’WebView2 Runtime sans effort supplémentaire de votre application. Le modèle persistant garantit que votre application tire parti des dernières fonctionnalités et des mises à jour de sécurité pour le contenu Web hébergé.

Pour les environnements restreints, un modèle de distribution de version fixe est pris en charge. Dans ce modèle, votre application sélectionne et compresse une version spécifique de WebView2. Les mises à jour apportées à la version WebView ne se produisent pas automatiquement et incombent à l’application. Le modèle de version fixe est utile lorsque vous devez contrôler la version du navigateur et lorsque votre application est mise à jour. 

### Microsoft Edge WebView2 Runtime

Le runtime Microsoft Edge WebView2 va empaqueter les fichiers binaires de navigateur optimisés pour être utilisés par les applications WebView2. Ce service fonctionne autonome ou côte à côte avec un navigateur côté client installé. Pour installer le runtime, de nombreuses applications WebView2 peuvent être exécutées sur l’ordinateur client. L’installation du runtime n’apparaîtra pas sous la forme d’un navigateur pour les utilisateurs finaux et n’aura aucun raccourci sur le bureau, point d’entrée du menu Démarrer ou enregistrement de protocole.

Les applications qui utilisent le runtime WebView2 doivent vérifier que l’installation du runtime est terminée. Pour vous assurer que votre application installe le runtime en tant que dépendance, vous pouvez ajouter le runtime à votre flux d’installation. 
