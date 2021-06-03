---
description: Déplacement d’utilisateurs vers Microsoft Edge à partir d’Internet Explorer
title: Déplacement d’utilisateurs vers Microsoft Edge à partir d’Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: microsoft Edge, compatibilité, plateforme web, Internet Explorer
ms.openlocfilehash: c2106955ed79bd28dc1f847dee220944bb014689
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461135"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a>Déplacement d’utilisateurs vers Microsoft Edge à partir d’Internet Explorer  

De nombreux sites web modernes ont des conceptions incompatibles avec Internet Explorer \(IE\).  Lorsqu’un utilisateur d’Internet IE visite un site web public incompatible, il peut obtenir un message.  Le message indique que le site web est incompatible avec le navigateur.  Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.  Pour minimiser les interruptions, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.  Lorsqu’un utilisateur d’Internet Explorer navigue vers un site web incompatible avec Internet Explorer, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.  Pour passer en revue les sites web de la liste, accédez à [Microsoft Edge liste.][MicrosoftEdgeNeededgeV1]

Cet article décrit les concepts suivants.  

*   Pourquoi un site web est ajouté à la liste  
*   Expérience utilisateur pour la redirection  
*   Demander une mise à jour de la liste  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a>Pourquoi un site web est-il ajouté à la liste de compatibilité d’Internet IE ?  

La liste de compatibilité Internet Internet (IE) ajoute un site web uniquement lorsque les actions suivantes se produisent.  

*   Affiche un message à un utilisateur d’Internet Explorer lui suggérant d’utiliser un autre navigateur pour des raisons de compatibilité.  
*   Le propriétaire demande d’ajouter le site web à la liste de compatibilité d’Internet IE.  

## <a name="redirection-experience"></a>Expérience de redirection

Lors de la redirection vers Microsoft Edge, la boîte de dialogue à une seule fois s’affiche dans la capture d’écran suivante.  La boîte de dialogue fournit à l’utilisateur les informations suivantes.  

*   Il explique pourquoi le site web est redirigé.  
*   Il invite l’utilisateur à consentir à copier les données de navigation et les préférences d’Internet Microsoft Edge.  

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
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notification de navigation et invite à importer des données et des préférences" lightbox="../media/neededge-dialog1.msft.png":::
         Notification de navigation et invite à importer des données et des préférences  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Si l’utilisateur ne donne pas son consentement en choisissant la case à cocher **** Toujours mettre en avant mes données et préférences de navigation à partir d’Internet **Explorer,** l’utilisateur peut choisir Continuer la navigation pour poursuivre la session de   navigation.  

Enfin, une bannière d’incompatibilité de site web s’affiche sous la barre d’adresse pour chaque redirection.  Un exemple de bannière d’incompatibilité de site web est affiché dans la figure suivante.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notification sur les sites modernes et invite à définir Microsoft Edge navigateur par défaut ou explorer Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notification sur les sites modernes et invite à définir Microsoft Edge navigateur par défaut ou explorer Microsoft Edge  
:::image-end:::

La bannière d’incompatibilité du site web fournit les détails suivants à l’utilisateur.  

*   Recommande à l’utilisateur de basculer vers Microsoft Edge.  
*   Offre de définir Microsoft Edge comme navigateur par défaut.  
*   Permet à l’utilisateur d’explorer Microsoft Edge.    
    
Lorsqu’un site web est redirigé d’Internet Explorer vers Microsoft Edge, l’une des actions suivantes se produit.

*   Si l’onglet IE actif n’avait aucun contenu préalable, il est fermé.  
*   Si l’onglet Internet Explorer actif avait un contenu antérieur, il navigue vers la page de support Microsoft qui explique pourquoi le site web a été [redirigé vers Microsoft Edge.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]  

> [!NOTE]
> Après une redirection, les utilisateurs peuvent continuer à utiliser Internet IE pour les sites web qui ne sont pas répertoriés dans la liste de compatibilité d’Internet Internet.  

## <a name="request-an-update-to-the-ie-compatibility-list"></a>Demander une mise à jour de la liste de compatibilité d’IE  

La liste de compatibilité d’IE est un fichier XML sur [microsoft.com][MicrosoftOfficialHome].  La liste est régulièrement mise à jour en réponse aux demandes des utilisateurs et des développeurs de sites web pour ajouter ou supprimer des sites web.  Les mises à jour de la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.  

Envoyez les informations suivantes [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site web soit ajouté ou supprimé de la liste de compatibilité d’Internet IE.    

*   Nom du propriétaire  
*   Titre de l’entreprise  
*   Adresse électronique  
*   Nom de la société  
*   Adresse postale  
*   Adresse du site web  
    
La liste de compatibilité d’IE est mise à jour au cours d’une semaine.

> [!NOTE]
> La liste de compatibilité d’Internet IE est conçue pour fonctionner uniquement avec des sites publics.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un courrier électronique à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil officiel Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Besoin Microsoft Edge liste xml v1 | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Le site web que vous tentiez d’atteindre ne fonctionne pas avec Internet Explorer | Microsoft Office Prise en charge"  
