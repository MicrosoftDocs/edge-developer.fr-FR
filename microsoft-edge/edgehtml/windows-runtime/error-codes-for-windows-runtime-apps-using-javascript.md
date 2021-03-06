---
description: Codes d’erreur pour les applications Windows Runtime utilisant JavaScript
title: Codes d’erreur pour les applications Windows Runtime utilisant JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e7241d675a6f488e70eefb20c40149683f965c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398489"
---
# <a name="error-codes-for-windows-runtime-apps-using-javascript"></a>Codes d’erreur pour les applications Windows Runtime utilisant JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Voici les codes d’erreur affichés par la console Microsoft Visual Studio lors du développement d’applications Windows Runtime à l’aide de JavaScript.  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9601: «Can’t load *remoteURI*.  Une application ne peut pas charger de contenu web distant dans le contexte local. » | Pour plus d’informations sur ce qui est autorisé dans le contexte web, voir [Fonctionnalités et restrictions par contexte.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9602: «'javascript:' is an invalid attribute value and will be ignored.  N’utilisez pas d' URIs « javascript: » dans le contexte local. » | Pour des raisons de sécurité, vous ne pouvez pas utiliser les URL « javascript: » dans le contexte local.  Pour plus d’informations sur ce qui est autorisé dans le contexte local, voir [Fonctionnalités et restrictions par contexte.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9603 : « Can’t load the ActiveX plug-in that has the class ID *classID*.  Les applications ne peuvent pas charger ActiveX contrôles. » | Les applications Windows Runtime utilisant JavaScript ne permettent pas de personnaliser Microsoft ActiveXcontrols.  Si vous avez besoin d’un contrôle d’interface utilisateur, utilisez un contrôle web standard, une bibliothèque de contrôles ou créez votre propre contrôle personnalisé.  Si vous devez effectuer une logique personnalisée, créez plutôt un objet Windows Runtime personnalisé.  Pour plus d’informations sur les autres différences HTML, CSS et JavaScript, voir [html, CSS et JavaScript fonctionnalités et différences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: «Can’t navigate to *uri* because it uses an invalid character encoding.  Une application peut accéder uniquement aux fichiers codés en UTF8. » | Tous les fichiers HTML, JavaScript et CSS accessibles par Windows Runtime doivent être codés au format UTF-8 (Unicode Transformation Format) 8 bits.  Pour plus d’informations sur les autres différences HTML, CSS et JavaScript, voir [html, CSS et JavaScript fonctionnalités et différences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605 : « Can’t navigate to *targetURI* from *sourceURI* because the destination URI is in a higher security zone.  Vous ne pouvez pas naviguer d’une zone avec une sécurité inférieure à une zone avec une sécurité plus élevée, sauf si vous naviguez vers un URI de contexte local à partir d’un URI de contexte web et que vous avez inscrit l’URI de contexte local à l’aide de la méthode MSApp.addPublicLocalApplicationUri. » | Pour plus d’informations, [voir MSApp.addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: «Can’t load *uri* because it uses an HTTP connection and the ms-https-connections-only meta element is present.  Seules les connexions HTTPS sont autorisées lorsque vous utilisez l’élément meta ms-https-connections-only.  Utilisez une connexion HTTPS ou, si vous n’avez pas besoin d’une connexion sécurisée, supprimez l’élément meta. » | Pour plus d’informations, [voir Comment exiger une connexion HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607 : « L’application ne peut pas lancer l’URI à *l’URI* en raison de cette erreur *: failureCode*. » | Une ressource manquante ou un fichier non valide sont des causes courantes de cette erreur.  |  
| APPHOST9608 : « L’application n’a pas pu accéder à la page about:blank en raison de cette erreur : *errorCode*. » |  |  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9610 : « L’application a trouvé une erreur lors de la préparation pour accéder à une page d’erreur personnalisée : *errorCode*. » |  |  
| APPHOST9611 : « L’application n’a pas pu accéder à une page d’erreur personnalisée en raison de cette erreur : *errorCode*. » |  |  
| APPHOST9613 : « L’application n’a pas pu accéder à *l’uri*  en raison de cette erreur : *errorCode*. » |  |  
| APPHOST9614 : « Un document dans un iframe a demandé le mode doc *requestedDocMode,* mais le système applique le mode doc *currentDocMode.*  L’iframe utilise le mode doc *currentDocMode.* » | Pour plus d’informations sur l’affichage de contenu web distant, voir [Comment lier des pages web externes.][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615 : « L’application ne peut pas télécharger le fichier à *l’URI,* car il a été appelé par programmation en dehors du contexte local. » | Se produit lorsque le contenu du contexte web tente de télécharger un fichier par programmation.  |  
| APPHOST9616 : « Cet URI ne peut pas utiliser les API de géolocalisation.  Les API de géolocalisation peuvent être invoquées uniquement à partir d’un URI qui fait partie du package ou qui est inclus dans l’élément ApplicationContentUris du manifeste. » | Pour plus d’informations sur ce qui est autorisé dans le contexte web, voir [Fonctionnalités et restrictions par contexte.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9617 : « Cet URI ne peut pas utiliser les API du Presse-papiers.  Les API du Presse-papiers peuvent être invoquées uniquement à partir d’un URI qui fait partie du package ou qui est inclus dans l’élément ApplicationContentUris du manifeste. » | Pour plus d’informations sur ce qui est autorisé dans le contexte web, voir [Fonctionnalités et restrictions par contexte.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9618: «Cet URI ne peut pas utiliser window.close.  La méthode window.close peut être invoquée uniquement à partir du contenu empaqueté qui a été chargé avec un schéma d’URI ms-appx. » | Pour plus d’informations sur ce qui est autorisé dans le contexte web, voir [Fonctionnalités et restrictions par contexte.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9619 : « L’application ne peut pas accéder à *l’URI,* car une page dans le contexte web ne peut pas être le document de niveau supérieur de l’application.  Chargez plutôt la page dans un iframe. » | Vous ne pouvez pas naviguer dans votre page de niveau supérieur vers une page web distante, mais votre application peut afficher une page web dans [un iframe.][MDNIframe]  Pour plus d’informations sur l’affichage de contenu web distant, voir [Comment lier des pages web externes.][PreviousVersionsWindowsAppsHh780594]  |  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9620 : « Cette application a été fermée car elle utilisait une connexion HTTP et l’élément meta ms-https-connections-only est présent.  Seules les connexions HTTPS sont autorisées lorsque vous utilisez l’élément meta ms-https-connections-only.  Utilisez une connexion HTTPS ou, si vous n’avez pas besoin d’une connexion sécurisée, supprimez l’élément meta. » | Pour plus d’informations, [voir Comment exiger une connexion HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623 : « L’application n’a pas pu résoudre *l’URL* en raison de cette erreur : *errorCode*. » | Une cause courante de cette erreur est un fichier manquant.  |  
| APPHOST9624 : « L’application ne peut pas utiliser de script pour charger *l’URL,* car l’URL lance une autre application.  Seule l’interaction directe de l’utilisateur peut lancer une autre application. » | Les applications ne peuvent pas lancer d’autres applications directement.  D’autres applications peuvent être lancées par l’utilisateur lorsque l’application implémente certains contrats.  Pour plus d’informations, voir [Contrats et extensions d’application][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626 : « Une référence directe au fichier de ressources `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` a été détectée.  Cette référence provoque des échecs lorsqu’elle est utilisée en dehors de l’environnement de débogage. » | En raison du chemin d’accès au fichier, ce fichier PNG est traité comme une ressource localisée, ce qui provoque l’erreur dans le fait que les ressources localisées ne peuvent pas être `logo.scale-140.png` référencés directement.  Voir [Globalisation de votre application (HTML)][PreviousVersionsWindowsAppsHh465006] si vous avez l’intention d’utiliser ce fichier comme ressource de langue.  Sinon, essayez de renommer le répertoire problématique.  |  

## <a name="see-also"></a>Voir également  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Documents Microsoft"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "AddPublicLocalApplicationUri, méthode | Documents Microsoft"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Comment exiger une connexion HTTPS (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contrats et extensions d’application (applications Windows Runtime) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalisation de votre application (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Fonctionnalités et restrictions par contexte (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Fonctionnalités html, CSS et JavaScript et différences (HTML) | Documents Microsoft"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Comment lier des pages web externes (HTML) | Documents Microsoft"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe> : l’élément Inline Frame | MDN"  
