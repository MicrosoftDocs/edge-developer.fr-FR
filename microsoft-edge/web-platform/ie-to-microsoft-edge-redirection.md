---
description: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
title: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
author: MSEdgeTeam
ms.date: 11/04/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web, Internet Explorer
ms.openlocfilehash: 48f0f4121fb444d80603dcbb408397679c64753d
ms.sourcegitcommit: 7b4441b7656c8317139650f904b70cc87797d37e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154330"
---
# Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer 

De nombreux sites Web modernes possèdent des conceptions incompatibles avec Internet Explorer \ (IE \).  Lorsqu’un utilisateur d’IE visite un site Web public incompatible, il est possible qu’un message s’affiche.  Le message indique que le site Web n’est pas compatible avec le navigateur.  Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.  Pour limiter les perturbations, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.  Lorsqu’un utilisateur d’Internet Explorer navigue vers un site Web incompatible avec IE, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.  Pour passer en revue les sites Web de la liste, accédez à la [liste Microsoft Edge requis][MicrosoftEdgeNeededgeV1].

Cet article décrit les concepts suivants.  

*   Interface utilisateur pour la redirection  
*   Comment ajouter votre site Web à la liste de compatibilité d’Internet Explorer  
*   Suppression de votre site Web de la liste de compatibilité d’Internet Explorer  
    
## Pourquoi un site Web est-il ajouté à la liste de compatibilité Internet?  

La liste de compatibilité d’Internet Explorer ajoute uniquement un site Web lorsque les actions suivantes se produisent.  

*   Affiche un message aux fins de compatibilité d’un utilisateur d’un autre navigateur.  
*   Demandes de propriétaire pour ajouter le site Web à la liste de compatibilité d’Internet Explorer.  
    
## Mettre à jour la liste de compatibilité d’Internet Explorer  

La liste de compatibilité Internet est un fichier XML sur [Microsoft.com][MicrosoftOfficialHome].  La liste est régulièrement mise à jour en réponse aux demandes des développeurs de sites Web et d’utilisateurs qui ont été ajoutées ou supprimées.  Les mises à jour apportées à la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.  

Envoyez les informations suivantes à [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site Web soit ajouté ou supprimé de la liste de compatibilité d’Internet Explorer.    

*   Nom du propriétaire  
*   Titre de l’entreprise  
*   Adresse électronique  
*   Nom de la société  
*   Adresse postale  
*   Adresse du site Web  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un e-mail à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil Microsoft Official"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Vous avez besoin de la liste Microsoft Edge v1 XML | Microsoft Edge"  
