---
description: Utilisez Windows Runtime (WinRT) pour appeler des API Windows natives à partir de votre application JavaScript.
title: Windows Runtime (WinRT) pour JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Windows Runtime, WinRT, PWA, JavaScript
ms.openlocfilehash: e4b6eab4ecfbd26ccda8ef1c6e51a7a30dfaecfc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942211"
---
# Windows Runtime (WinRT) pour JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

[Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \ (ou simplement WinRT \) est l’ensemble d’API natives qui alimentent les applications de [plateforme Windows universelle](/windows/uwp/get-started/universal-application-platform-guide) (UWP) qui s’exécutent sur toutes les [familles d’appareils Windows 10](/uwp/extension-sdks/device-families-overview).  Les API WinRT sont projetées dans plusieurs langues, notamment C#, C++, Visual Basic et JavaScript.  

En tant que développeur Web, vous pouvez demander ces API Windows natives à JavaScript lorsque votre application Web s' [exécute sous la forme d’une application Windows 10 installée](../progressive-web-apps-edgehtml/windows-features.md#set-up-and-run-your-universal-windows-app) (lancée à partir du `wwahost.exe` processus, plutôt que du navigateur.).  De plus, votre site Web sous la forme d’une application Windows 10 pourra également utiliser le contrôle [WebView Microsoft Edge](#webview) pour afficher du contenu Web distant et local et des API [MSApp](#msapp) pour la gestion de BLOB et de flux, entre autres choses.  

Voici les zones d’espaces de noms WinRT de niveau supérieur disponibles pour toutes les applications Windows 10:  

| Espace de noms WinRT | Description |  
|:--- |:--- |  
| [Ai](/uwp/api/windows.AI.MachineLearning.Preview) \ (Preview \) | Contient des classes qui permettent aux applications de charger les modèles d’apprentissage d’ordinateur, de lier les données en tant qu’entrées et d’évaluer les résultats.  |  
| [ApplicationModel](/uwp/api/windows.applicationmodel) | Fournit à une application un accès aux fonctionnalités principales du système et aux informations d’exécution relatives au package d’application, et gère les opérations de suspension.  |  
| [Données](/uwp/api/windows.data.html) | Fournit des classes d’utilitaire pour l’utilisation de divers formats de données, notamment HTML, JSON, PDF, texte et XML.  |  
| [Périphériques](/uwp/api/windows.devices) | Cet espace de noms donne accès aux fournisseurs de périphériques de faible niveau, notamment ADC, GPIO, I2 C, PWM et SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Active les fonctionnalités fondamentales du Windows Runtime, notamment la gestion des opérations asynchrones et l’accès aux magasins de propriétés.  Cet espace de noms définit également les types de valeur courants qui représentent l’URI (Uniform Resource Identifier), les dates et les heures, les mesures 2D et d’autres valeurs de base.  |  
| [Jeux](/uwp/api/windows.gaming.input) |Donne accès à la saisie du contrôleur de jeu, à la barre de jeux, à la surveillance du jeu et à la discussion de jeu.  |  
| [Globalisation](/uwp/api/windows.globalization) | Offre une prise en charge de la globalisation des profils de langue, des régions géographiques et des calendriers internationaux.  |  
| [Graphiques](/uwp/api/windows.graphics) | Fournit des types de données de base contenant des informations sur la façon de dessiner des graphiques.  Ces structures de données sont couramment utilisées pour définir le mode de dessin des surfaces de grande taille lors de l’utilisation de la classe CompositionVirtualDrawingSurface.  |  
| [Gestion](/uwp/api/windows.management) | Fournit des fonctionnalités permettant d’imposer une synchronisation à partir d’un appareil de gestion des périphériques mobiles (GPM) sur le serveur.  Ce protocole de synchronisation GPM est basé sur Open Mobile Alliance-Device Management standard.  |  
| [Support](/uwp/api/windows.media) | Fournit des classes permettant de créer et d’utiliser des éléments multimédias, tels que des photos, des enregistrements audio et vidéo.  |  
| [Réseaux](/uwp/api/windows.networking) | Donne accès aux noms d’hôtes et aux points de terminaison utilisés par les applications réseau.  |  
| [Reçue](/uwp/api/windows.perception) | Contient des classes permettant de percevoir l’environnement de l’utilisateur, ce qui permet aux applications de rechercher et de raison de l’appareil par rapport aux surfaces et aux hologrammes de l’utilisateur.  |  
| [Sécurité](/uwp/api/windows.security.authentication.identity) | Fournit des classes pour l’authentification des utilisateurs, la gestion des informations d’identification, les opérations de chiffrement et les fonctionnalités de protection des données d’entreprise.  |  
| [Services](/uwp/api/windows.services.cortana) | Donne accès à des services Microsoft pour Cortana, cartes, Microsoft Store et le contenu ciblé \ (abonnement \).  |  
| [Stockage](/uwp/api/windows.storage) | Fournit des classes pour la gestion des fichiers, des dossiers et des paramètres d’application.  |  
| [Système](/uwp/api/windows.system) | Active les fonctionnalités système telles que le lancement d’applications, l’obtention d’informations sur un utilisateur et le profilage de la mémoire.  |  
| [Interface utilisateur](/uwp/api/windows.ui) | Fournit une application ayant accès à la fonctionnalité système principale et aux informations d’exécution relatives à l’interface utilisateur.  **Remarque**: les API dans l' `Windows.UI.Xaml` espace de noms ne sont pas disponibles pour les applications JavaScript (qui peuvent utiliser les technologies basées sur des normes Web équivalentes).  |  
| [Web](/uwp/api/windows.web) | Fournit des informations sur les erreurs provenant des opérations de service Web.  |  

Pour plus d’informations sur l’utilisation, voir [utilisation de Windows Runtime en JavaScript](./using-the-windows-runtime-in-javascript.md).  Pour plus d’informations sur l’exécution de votre site Web en tant qu’application Windows, essayez le didacticiel [de personnalisation de Windows](../progressive-web-apps/windows-features.md) .  

## WebView  

Le contrôle [WebView Microsoft Edge](../webview.md) vous permet d’héberger le contenu Web dans votre application Windows 10.  Ce type d’utilisation est semblable à l’utilisation d’un `<iframe>` , mais offre de nombreuses [fonctionnalités et contrôle](../hosting/webview.md#webview-versus-iframe) de l’utilisation.  

## MSApp  

L’objet global [MSApp](./reference/msapp.md) \ ( `window.MSApp` \) fournit des fonctions d’assistance assorties pour les applications Windows 10 basées sur JavaScript, telles que les utilitaires de conversion entre les types d’objets WinRT basés sur le Web et équivalents.  
