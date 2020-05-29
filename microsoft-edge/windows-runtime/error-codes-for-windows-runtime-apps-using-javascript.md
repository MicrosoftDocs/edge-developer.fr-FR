---
title: Codes d’erreur pour les applications Windows Runtime en JavaScript
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
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
manager: ''
ms.openlocfilehash: 7aad8577d79bc5612f526e4e2bf1ceb0f2c2929a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566657"
---
# Codes d’erreur pour les applications Windows Runtime en JavaScript  

Voici les codes d’erreur qui s’affichent dans la console Microsoft Visual Studio lorsque vous développez des applications Windows Runtime en JavaScript.  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9601: "Impossible de charger *remoteURI*.  Une application ne peut pas charger du contenu Web distant dans le contexte local.» | Pour plus d’informations sur ce qui est autorisé dans le contexte Web, voir [fonctionnalités et restrictions par contexte][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "'JavaScript: 'est une valeur d’attribut non valide et sera ignorée.  N’utilisez pas d’URI «JavaScript:» dans le contexte local.» | Pour des raisons de sécurité, vous ne pouvez pas utiliser des URI’JavaScript: 'dans le contexte local.  Pour plus d’informations sur ce qui est autorisé dans le contexte local, voir [fonctionnalités et restrictions par contexte][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "Impossible de charger le plug-in ActiveX ayant l’ID de classe *ClassID*.  Les applications ne peuvent pas charger de contrôles ActiveX.» | Les applications Windows Runtime utilisant JavaScript ne prennent pas en charge Microsoft ActiveXcontrols personnalisé.  Si vous avez besoin d’un contrôle d’interface utilisateur, utilisez un contrôle Web standard, une bibliothèque de contrôles ou créez votre propre contrôle personnalisé.  Si vous devez exécuter une logique personnalisée, créez plutôt un objet Windows Runtime personnalisé.  Pour plus d’informations sur les autres différences HTML, CSS et JavaScript, voir [fonctionnalités html, CSS et JavaScript et différences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: «vous ne pouvez pas accéder à l' *URI* car il utilise un codage de caractères non valide.  Une application peut accéder uniquement aux fichiers codés en UTF8.» | Tout le code HTML, JavaScript et CSS accédé par un Windows Runtime doit être encodé en tant que format UTF-8 (Unicode Transformation Format).  Pour plus d’informations sur les autres différences HTML, CSS et JavaScript, voir [fonctionnalités html, CSS et JavaScript et différences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: «vous ne pouvez pas accéder à *targetURI* depuis *sourceURI* , car l’URI de destination se trouve dans une zone de sécurité plus élevée.  Vous ne pouvez pas naviguer à partir d’une zone avec un niveau de sécurité inférieur vers une zone avec une sécurité plus élevée, sauf si vous naviguez jusqu’à un URI de contexte local à partir d’un URI de contexte Web et que vous avez inscrit l’URI de contexte local avec la méthode MSApp. addPublicLocalApplicationUri. " | Pour plus d’informations, voir [MSApp. addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "Impossible de charger l' *URI* , car il utilise une connexion http et l’élément méta MS-https-connections uniquement est présent.  Seules les connexions HTTPs sont autorisées lorsque vous utilisez l’élément méta MS-https-connections-only.  Utiliser une connexion HTTPs ou, si vous n’avez pas besoin d’une connexion sécurisée, supprimez l’élément méta. | Pour plus d’informations, reportez-vous [à la rubrique exiger une connexion HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: «l’application ne peut pas lancer l’URI sur l' *URI* en raison de l’erreur suivante: *failureCode*». | Un fichier manquant ou non valide est le cause courante de cette erreur.  |  
| APPHOST9608: «l’application n’a pas pu accéder à la page «à propos de:» en raison de l’erreur suivante: *codeerreur*.» |  |  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9610: «l’application a détecté une erreur lors de la préparation de la navigation vers une page d’erreur personnalisée: *codeerreur*». |  |  
| APPHOST9611: «l’application n’a pas pu accéder à une page d’erreur personnalisée en raison de l’erreur suivante: *codeerreur*.» |  |  
| APPHOST9613: «l’application n’a pas pu accéder à l' *URI* en raison de l’erreur suivante: *codeerreur*.» |  |  
| APPHOST9614: «un document dans un IFRAME a demandé le mode de document *requestedDocMode* , mais le système applique le mode de document *currentDocMode* .  L’iframe utilise le mode de document *currentDocMode* . | Pour plus d’informations sur l’affichage de contenu Web distant, voir [comment créer un lien vers des pages Web externes][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: «l’application ne peut pas télécharger le fichier sur *URI* , car il a été appelé par programme en dehors du contexte local.» | Se produit lorsque le contenu du contexte Web essaie de télécharger un fichier par programme.  |  
| APPHOST9616: "cet URI ne peut pas utiliser les API de géolocalisation.  Les API de géolocalisation peuvent être appelées uniquement à partir d’un URI qui fait partie du package ou qui est inclus dans l’élément ApplicationContentUris du manifeste.» | Pour plus d’informations sur ce qui est autorisé dans le contexte Web, voir [fonctionnalités et restrictions par contexte][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: «cet URI ne peut pas utiliser les API du presse-papiers.  Les API du presse-papiers peuvent être appelées uniquement à partir d’un URI qui fait partie du package ou qui est inclus dans l’élément ApplicationContentUris du manifeste.» | Pour plus d’informations sur ce qui est autorisé dans le contexte Web, voir [fonctionnalités et restrictions par contexte][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: «cet URI ne peut pas utiliser Window. Close.  La méthode Window. Close peut être appelée uniquement à partir du contenu empaqueté chargé avec un schéma d’URI MS-Appx.» | Pour plus d’informations sur ce qui est autorisé dans le contexte Web, voir [fonctionnalités et restrictions par contexte][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: «l’application ne peut pas accéder à l' *URI* , car une page du contexte Web ne peut pas être le document de niveau supérieur de l’application.  Il est préférable de charger la page dans un IFRAME.» | Vous ne pouvez pas parcourir votre page de niveau supérieur vers une page Web distante, mais votre application peut afficher une page Web dans un [IFRAME][MDNIframe].  Pour plus d’informations sur l’affichage de contenu Web distant, voir [comment créer un lien vers des pages Web externes][PreviousVersionsWindowsAppsHh780594].  |  

| Erreur | Remarques |  
|:--- |:--- |  
| APPHOST9620: «cette application a été fermée, car elle a utilisé une connexion HTTP et l’élément méta MS-https-connections uniquement est présent.  Seules les connexions HTTPs sont autorisées lorsque vous utilisez l’élément méta MS-https-connections-only.  Utiliser une connexion HTTPs ou, si vous n’avez pas besoin d’une connexion sécurisée, supprimez l’élément méta. | Pour plus d’informations, reportez-vous [à la rubrique exiger une connexion HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: «l’application n’a pas pu résoudre l' *URL* en raison de l’erreur suivante: *codeerreur*.» | La cause courante de cette erreur est un fichier manquant.  |  
| APPHOST9624: «l’application ne peut pas utiliser le script pour charger l’URL d' *URL* , car l’URL lance une autre application.  Seule l’action directe de l’utilisateur peut lancer une autre application.» | Les applications ne peuvent pas lancer d’autres applications directement.  Les autres applications peuvent être lancées par l’utilisateur lorsque l’application implémente certains contrats.  Pour plus d’informations, voir [Contrats et extensions d’application][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: «une référence directe à un fichier de ressources `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` a été détectée.  Cette référence entraîne des échecs lorsqu’elle est utilisée en dehors de l’environnement de débogage. | En raison du chemin d’accès du fichier `logo.scale-140.png` , ce fichier PNG est considéré comme une ressource localisée, ce qui provoque l’erreur dans ces ressources localisées qui ne peuvent pas être référencées directement.  Voir [globalisation de votre application (html)][PreviousVersionsWindowsAppsHh465006] si vous envisagez d’utiliser ce fichier en tant que ressource de langue.  Dans le cas contraire, essayez de renommer le répertoire posant problème.  |  

## Voir aussi  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Utilisation de Windows Runtime en JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe de géolocalisation"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "méthode addPublicLocalApplicationUri"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Comment exiger une connexion HTTPs (HTML)"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contrats et extensions d’application (applications Windows Runtime)"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalisation de votre application (HTML)"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Fonctionnalités et restrictions par contexte (HTML)"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Fonctionnalités HTML, CSS et JavaScript et différences (HTML)"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Créer un lien vers des pages Web externes (HTML)"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: élément de cadre inséré | MDN"  
