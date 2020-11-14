---
description: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
title: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web, Internet Explorer
ms.openlocfilehash: 872bd5ec52f471e4958ef7354c046ec30f1ba72e
ms.sourcegitcommit: 62258ce0ef469948ca8af42141d02aa9719243f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168362"
---
# Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer  

De nombreux sites Web modernes possèdent des conceptions incompatibles avec Internet Explorer \ (IE \).  Lorsqu’un utilisateur d’IE visite un site Web public incompatible, il est possible qu’un message s’affiche.  Le message indique que le site Web n’est pas compatible avec le navigateur.  Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.  Pour limiter les perturbations, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.  Lorsqu’un utilisateur d’Internet Explorer navigue vers un site Web incompatible avec IE, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.  Pour passer en revue les sites Web de la liste, accédez à la [liste Microsoft Edge requis][MicrosoftEdgeNeededgeV1].

Cet article décrit les concepts suivants.  

*   Pourquoi un site Web est ajouté à la liste?  
*   Interface utilisateur pour la redirection  
*   Demander la mise à jour de la liste  
    
## Pourquoi un site Web est-il ajouté à la liste de compatibilité Internet?  

La liste de compatibilité d’Internet Explorer ajoute uniquement un site Web lorsque les actions suivantes se produisent.  

*   Affiche un message aux fins de compatibilité d’un utilisateur d’un autre navigateur.  
*   Demandes de propriétaire pour ajouter le site Web à la liste de compatibilité d’Internet Explorer.  

## Expérience de redirection

Lorsque vous redirigez vers Microsoft Edge, l’utilisateur affiche la boîte de dialogue ponctuelle suivante.  La boîte de dialogue fournit à l’utilisateur les informations suivantes.  

*   Il explique pourquoi le site Web est redirigé.  
*   Le système demande à l’utilisateur l’autorisation de copier les données de navigation et les préférences d’Internet Explorer dans Microsoft Edge.  

:::row:::
   :::column span="":::
      Les données de navigation suivantes sont importées.  
      
      *   Favoris  
      *   Mots de passe  
      *   Moteurs de recherche  
      *   Ouvrir les onglets  
      *   Historique  
      *   Paramètres  
      *   Cookies  
      *   Page d’accueil  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notification de navigation et invite d’importation de données et préférences" lightbox="../media/neededge-dialog1.msft.png":::
         Notification de navigation et invite d’importation de données et préférences  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Si l’utilisateur n’est pas en mesure d’accepter en activant la case à cocher **toujours faire basculer les données et préférences de navigation d’Internet Explorer** , il est possible que l’utilisateur sélectionne **poursuivre la navigation**   pour continuer la session de navigation.  

Enfin, une bannière d’incompatibilité de site Web s’affiche sous la barre d’adresse pour chaque redirection.  Un exemple de bannière d’incompatibilité de site Web s’affiche dans la figure ci-dessous.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notification sur les sites modernes et invite à définir Microsoft Edge comme navigateur par défaut ou découvrir Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notification sur les sites modernes et invite à définir Microsoft Edge comme navigateur par défaut ou découvrir Microsoft Edge  
:::image-end:::

La bannière d’incompatibilité de site Web fournit les informations suivantes à l’utilisateur.  

*   Recommande aux utilisateurs de basculer vers Microsoft Edge.  
*   Propose de définir Microsoft Edge comme navigateur par défaut.  
*   Offre à l’utilisateur la possibilité d’explorer Microsoft Edge.    
    
Lorsqu’un site Web est redirigé d’Internet Explorer vers Microsoft Edge, l’une des actions suivantes se produit.

*   Si l’onglet IE actif ne contenait aucun contenu antérieur, il est fermé.  
*   Si l’onglet IE actif comporte du contenu antérieur, il accède à la [page du support Microsoft qui explique pourquoi le site Web a été redirigé vers Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].  

> [!NOTE]
> Après une redirection, les utilisateurs peuvent continuer à utiliser Internet Explorer pour les sites Web qui ne figurent pas dans la liste de compatibilité d’Internet Explorer.  

## Demander une mise à jour de la liste de compatibilité d’Internet Explorer  

La liste de compatibilité Internet est un fichier XML sur [Microsoft.com][MicrosoftOfficialHome].  La liste est régulièrement mise à jour en réponse aux demandes des développeurs de sites Web et d’utilisateurs qui ont été ajoutées ou supprimées.  Les mises à jour apportées à la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.  

Envoyez les informations suivantes à [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site Web soit ajouté ou supprimé de la liste de compatibilité d’Internet Explorer.    

*   Nom du propriétaire  
*   Titre de l’entreprise  
*   Adresse électronique  
*   Nom de la société  
*   Adresse postale  
*   Adresse du site Web  
    
> [!NOTE]
> La liste de compatibilité d’Internet Explorer est conçue pour fonctionner uniquement avec des sites publics.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un e-mail à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil Microsoft Official"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Vous avez besoin de la liste Microsoft Edge v1 XML | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Le site Web que vous essayez de joindre ne fonctionne pas avec Internet Explorer | Support Microsoft Office"  
