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
# <span data-ttu-id="1b37b-104">Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1b37b-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="1b37b-105">De nombreux sites Web modernes possèdent des conceptions incompatibles avec Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="1b37b-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="1b37b-106">Lorsqu’un utilisateur d’IE visite un site Web public incompatible, il est possible qu’un message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1b37b-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="1b37b-107">Le message indique que le site Web n’est pas compatible avec le navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b37b-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="1b37b-108">Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.</span><span class="sxs-lookup"><span data-stu-id="1b37b-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="1b37b-109">Pour limiter les perturbations, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b37b-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="1b37b-110">Lorsqu’un utilisateur d’Internet Explorer navigue vers un site Web incompatible avec IE, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b37b-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="1b37b-111">Pour passer en revue les sites Web de la liste, accédez à la [liste Microsoft Edge requis][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="1b37b-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="1b37b-112">Cet article décrit les concepts suivants.</span><span class="sxs-lookup"><span data-stu-id="1b37b-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="1b37b-113">Pourquoi un site Web est ajouté à la liste?</span><span class="sxs-lookup"><span data-stu-id="1b37b-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="1b37b-114">Interface utilisateur pour la redirection</span><span class="sxs-lookup"><span data-stu-id="1b37b-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="1b37b-115">Demander la mise à jour de la liste</span><span class="sxs-lookup"><span data-stu-id="1b37b-115">Request an update to the list</span></span>  
    
## <span data-ttu-id="1b37b-116">Pourquoi un site Web est-il ajouté à la liste de compatibilité Internet?</span><span class="sxs-lookup"><span data-stu-id="1b37b-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="1b37b-117">La liste de compatibilité d’Internet Explorer ajoute uniquement un site Web lorsque les actions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="1b37b-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="1b37b-118">Affiche un message aux fins de compatibilité d’un utilisateur d’un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="1b37b-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="1b37b-119">Demandes de propriétaire pour ajouter le site Web à la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1b37b-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <span data-ttu-id="1b37b-120">Expérience de redirection</span><span class="sxs-lookup"><span data-stu-id="1b37b-120">Redirection experience</span></span>

<span data-ttu-id="1b37b-121">Lorsque vous redirigez vers Microsoft Edge, l’utilisateur affiche la boîte de dialogue ponctuelle suivante.</span><span class="sxs-lookup"><span data-stu-id="1b37b-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="1b37b-122">La boîte de dialogue fournit à l’utilisateur les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b37b-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="1b37b-123">Il explique pourquoi le site Web est redirigé.</span><span class="sxs-lookup"><span data-stu-id="1b37b-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="1b37b-124">Le système demande à l’utilisateur l’autorisation de copier les données de navigation et les préférences d’Internet Explorer dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b37b-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1b37b-125">Les données de navigation suivantes sont importées.</span><span class="sxs-lookup"><span data-stu-id="1b37b-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="1b37b-126">Favoris</span><span class="sxs-lookup"><span data-stu-id="1b37b-126">Favorites</span></span>  
      *   <span data-ttu-id="1b37b-127">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="1b37b-127">Passwords</span></span>  
      *   <span data-ttu-id="1b37b-128">Moteurs de recherche</span><span class="sxs-lookup"><span data-stu-id="1b37b-128">Search engines</span></span>  
      *   <span data-ttu-id="1b37b-129">Ouvrir les onglets</span><span class="sxs-lookup"><span data-stu-id="1b37b-129">Open tabs</span></span>  
      *   <span data-ttu-id="1b37b-130">Historique</span><span class="sxs-lookup"><span data-stu-id="1b37b-130">History</span></span>  
      *   <span data-ttu-id="1b37b-131">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b37b-131">Settings</span></span>  
      *   <span data-ttu-id="1b37b-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="1b37b-132">Cookies</span></span>  
      *   <span data-ttu-id="1b37b-133">Page d’accueil</span><span class="sxs-lookup"><span data-stu-id="1b37b-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notification de navigation et invite d’importation de données et préférences" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="1b37b-135">Notification de navigation et invite d’importation de données et préférences</span><span class="sxs-lookup"><span data-stu-id="1b37b-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="1b37b-136">Si l’utilisateur n’est pas en mesure d’accepter en activant la case à cocher **toujours faire basculer les données et préférences de navigation d’Internet Explorer** , il est possible que l’utilisateur sélectionne **poursuivre la navigation**   pour continuer la session de navigation.</span><span class="sxs-lookup"><span data-stu-id="1b37b-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="1b37b-137">Enfin, une bannière d’incompatibilité de site Web s’affiche sous la barre d’adresse pour chaque redirection.</span><span class="sxs-lookup"><span data-stu-id="1b37b-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="1b37b-138">Un exemple de bannière d’incompatibilité de site Web s’affiche dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1b37b-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notification sur les sites modernes et invite à définir Microsoft Edge comme navigateur par défaut ou découvrir Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="1b37b-140">Notification sur les sites modernes et invite à définir Microsoft Edge comme navigateur par défaut ou découvrir Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b37b-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="1b37b-141">La bannière d’incompatibilité de site Web fournit les informations suivantes à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b37b-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="1b37b-142">Recommande aux utilisateurs de basculer vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b37b-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="1b37b-143">Propose de définir Microsoft Edge comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b37b-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="1b37b-144">Offre à l’utilisateur la possibilité d’explorer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1b37b-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="1b37b-145">Lorsqu’un site Web est redirigé d’Internet Explorer vers Microsoft Edge, l’une des actions suivantes se produit.</span><span class="sxs-lookup"><span data-stu-id="1b37b-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="1b37b-146">Si l’onglet IE actif ne contenait aucun contenu antérieur, il est fermé.</span><span class="sxs-lookup"><span data-stu-id="1b37b-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="1b37b-147">Si l’onglet IE actif comporte du contenu antérieur, il accède à la [page du support Microsoft qui explique pourquoi le site Web a été redirigé vers Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span><span class="sxs-lookup"><span data-stu-id="1b37b-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="1b37b-148">Après une redirection, les utilisateurs peuvent continuer à utiliser Internet Explorer pour les sites Web qui ne figurent pas dans la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1b37b-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <span data-ttu-id="1b37b-149">Demander une mise à jour de la liste de compatibilité d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1b37b-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="1b37b-150">La liste de compatibilité Internet est un fichier XML sur [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="1b37b-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="1b37b-151">La liste est régulièrement mise à jour en réponse aux demandes des développeurs de sites Web et d’utilisateurs qui ont été ajoutées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="1b37b-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="1b37b-152">Les mises à jour apportées à la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b37b-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="1b37b-153">Envoyez les informations suivantes à [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site Web soit ajouté ou supprimé de la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1b37b-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="1b37b-154">Nom du propriétaire</span><span class="sxs-lookup"><span data-stu-id="1b37b-154">Owner name</span></span>  
*   <span data-ttu-id="1b37b-155">Titre de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="1b37b-155">Corporate title</span></span>  
*   <span data-ttu-id="1b37b-156">Adresse électronique</span><span class="sxs-lookup"><span data-stu-id="1b37b-156">Email address</span></span>  
*   <span data-ttu-id="1b37b-157">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="1b37b-157">Company name</span></span>  
*   <span data-ttu-id="1b37b-158">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="1b37b-158">Street address</span></span>  
*   <span data-ttu-id="1b37b-159">Adresse du site Web</span><span class="sxs-lookup"><span data-stu-id="1b37b-159">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="1b37b-160">La liste de compatibilité d’Internet Explorer est conçue pour fonctionner uniquement avec des sites publics.</span><span class="sxs-lookup"><span data-stu-id="1b37b-160">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un e-mail à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil Microsoft Official"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Vous avez besoin de la liste Microsoft Edge v1 XML | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Le site Web que vous essayez de joindre ne fonctionne pas avec Internet Explorer | Support Microsoft Office"  
