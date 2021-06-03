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
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a><span data-ttu-id="40ef0-104">Déplacement d’utilisateurs vers Microsoft Edge à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="40ef0-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="40ef0-105">De nombreux sites web modernes ont des conceptions incompatibles avec Internet Explorer \(IE\).</span><span class="sxs-lookup"><span data-stu-id="40ef0-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="40ef0-106">Lorsqu’un utilisateur d’Internet IE visite un site web public incompatible, il peut obtenir un message.</span><span class="sxs-lookup"><span data-stu-id="40ef0-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="40ef0-107">Le message indique que le site web est incompatible avec le navigateur.</span><span class="sxs-lookup"><span data-stu-id="40ef0-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="40ef0-108">Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.</span><span class="sxs-lookup"><span data-stu-id="40ef0-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="40ef0-109">Pour minimiser les interruptions, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="40ef0-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="40ef0-110">Lorsqu’un utilisateur d’Internet Explorer navigue vers un site web incompatible avec Internet Explorer, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40ef0-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="40ef0-111">Pour passer en revue les sites web de la liste, accédez à [Microsoft Edge liste.][MicrosoftEdgeNeededgeV1]</span><span class="sxs-lookup"><span data-stu-id="40ef0-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="40ef0-112">Cet article décrit les concepts suivants.</span><span class="sxs-lookup"><span data-stu-id="40ef0-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="40ef0-113">Pourquoi un site web est ajouté à la liste</span><span class="sxs-lookup"><span data-stu-id="40ef0-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="40ef0-114">Expérience utilisateur pour la redirection</span><span class="sxs-lookup"><span data-stu-id="40ef0-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="40ef0-115">Demander une mise à jour de la liste</span><span class="sxs-lookup"><span data-stu-id="40ef0-115">Request an update to the list</span></span>  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a><span data-ttu-id="40ef0-116">Pourquoi un site web est-il ajouté à la liste de compatibilité d’Internet IE ?</span><span class="sxs-lookup"><span data-stu-id="40ef0-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="40ef0-117">La liste de compatibilité Internet Internet (IE) ajoute un site web uniquement lorsque les actions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="40ef0-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="40ef0-118">Affiche un message à un utilisateur d’Internet Explorer lui suggérant d’utiliser un autre navigateur pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="40ef0-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="40ef0-119">Le propriétaire demande d’ajouter le site web à la liste de compatibilité d’Internet IE.</span><span class="sxs-lookup"><span data-stu-id="40ef0-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <a name="redirection-experience"></a><span data-ttu-id="40ef0-120">Expérience de redirection</span><span class="sxs-lookup"><span data-stu-id="40ef0-120">Redirection experience</span></span>

<span data-ttu-id="40ef0-121">Lors de la redirection vers Microsoft Edge, la boîte de dialogue à une seule fois s’affiche dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="40ef0-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="40ef0-122">La boîte de dialogue fournit à l’utilisateur les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="40ef0-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="40ef0-123">Il explique pourquoi le site web est redirigé.</span><span class="sxs-lookup"><span data-stu-id="40ef0-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="40ef0-124">Il invite l’utilisateur à consentir à copier les données de navigation et les préférences d’Internet Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40ef0-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="40ef0-125">Les données de navigation suivantes sont importées.</span><span class="sxs-lookup"><span data-stu-id="40ef0-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="40ef0-126">Favoris</span><span class="sxs-lookup"><span data-stu-id="40ef0-126">Favorites</span></span>  
      *   <span data-ttu-id="40ef0-127">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="40ef0-127">Passwords</span></span>  
      *   <span data-ttu-id="40ef0-128">Moteurs de recherche</span><span class="sxs-lookup"><span data-stu-id="40ef0-128">Search engines</span></span>  
      *   <span data-ttu-id="40ef0-129">Ouvrir les onglets</span><span class="sxs-lookup"><span data-stu-id="40ef0-129">Open tabs</span></span>  
      *   <span data-ttu-id="40ef0-130">Historique</span><span class="sxs-lookup"><span data-stu-id="40ef0-130">History</span></span>  
      *   <span data-ttu-id="40ef0-131">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40ef0-131">Settings</span></span>  
      *   <span data-ttu-id="40ef0-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="40ef0-132">Cookies</span></span>  
      *   <span data-ttu-id="40ef0-133">Page d’accueil</span><span class="sxs-lookup"><span data-stu-id="40ef0-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notification de navigation et invite à importer des données et des préférences" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="40ef0-135">Notification de navigation et invite à importer des données et des préférences</span><span class="sxs-lookup"><span data-stu-id="40ef0-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="40ef0-136">Si l’utilisateur ne donne pas son consentement en choisissant la case à cocher \*\*\*\* Toujours mettre en avant mes données et préférences de navigation à partir d’Internet **Explorer,** l’utilisateur peut choisir Continuer la navigation pour poursuivre la session de   navigation.</span><span class="sxs-lookup"><span data-stu-id="40ef0-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="40ef0-137">Enfin, une bannière d’incompatibilité de site web s’affiche sous la barre d’adresse pour chaque redirection.</span><span class="sxs-lookup"><span data-stu-id="40ef0-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="40ef0-138">Un exemple de bannière d’incompatibilité de site web est affiché dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="40ef0-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notification sur les sites modernes et invite à définir Microsoft Edge navigateur par défaut ou explorer Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="40ef0-140">Notification sur les sites modernes et invite à définir Microsoft Edge navigateur par défaut ou explorer Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40ef0-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="40ef0-141">La bannière d’incompatibilité du site web fournit les détails suivants à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="40ef0-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="40ef0-142">Recommande à l’utilisateur de basculer vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40ef0-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="40ef0-143">Offre de définir Microsoft Edge comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="40ef0-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="40ef0-144">Permet à l’utilisateur d’explorer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40ef0-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="40ef0-145">Lorsqu’un site web est redirigé d’Internet Explorer vers Microsoft Edge, l’une des actions suivantes se produit.</span><span class="sxs-lookup"><span data-stu-id="40ef0-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="40ef0-146">Si l’onglet IE actif n’avait aucun contenu préalable, il est fermé.</span><span class="sxs-lookup"><span data-stu-id="40ef0-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="40ef0-147">Si l’onglet Internet Explorer actif avait un contenu antérieur, il navigue vers la page de support Microsoft qui explique pourquoi le site web a été [redirigé vers Microsoft Edge.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]</span><span class="sxs-lookup"><span data-stu-id="40ef0-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="40ef0-148">Après une redirection, les utilisateurs peuvent continuer à utiliser Internet IE pour les sites web qui ne sont pas répertoriés dans la liste de compatibilité d’Internet Internet.</span><span class="sxs-lookup"><span data-stu-id="40ef0-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <a name="request-an-update-to-the-ie-compatibility-list"></a><span data-ttu-id="40ef0-149">Demander une mise à jour de la liste de compatibilité d’IE</span><span class="sxs-lookup"><span data-stu-id="40ef0-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="40ef0-150">La liste de compatibilité d’IE est un fichier XML sur [microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="40ef0-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="40ef0-151">La liste est régulièrement mise à jour en réponse aux demandes des utilisateurs et des développeurs de sites web pour ajouter ou supprimer des sites web.</span><span class="sxs-lookup"><span data-stu-id="40ef0-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="40ef0-152">Les mises à jour de la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="40ef0-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="40ef0-153">Envoyez les informations suivantes [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site web soit ajouté ou supprimé de la liste de compatibilité d’Internet IE.</span><span class="sxs-lookup"><span data-stu-id="40ef0-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="40ef0-154">Nom du propriétaire</span><span class="sxs-lookup"><span data-stu-id="40ef0-154">Owner name</span></span>  
*   <span data-ttu-id="40ef0-155">Titre de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="40ef0-155">Corporate title</span></span>  
*   <span data-ttu-id="40ef0-156">Adresse électronique</span><span class="sxs-lookup"><span data-stu-id="40ef0-156">Email address</span></span>  
*   <span data-ttu-id="40ef0-157">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="40ef0-157">Company name</span></span>  
*   <span data-ttu-id="40ef0-158">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="40ef0-158">Street address</span></span>  
*   <span data-ttu-id="40ef0-159">Adresse du site web</span><span class="sxs-lookup"><span data-stu-id="40ef0-159">Website address</span></span>  
    
<span data-ttu-id="40ef0-160">La liste de compatibilité d’IE est mise à jour au cours d’une semaine.</span><span class="sxs-lookup"><span data-stu-id="40ef0-160">The IE compatibility list is updated within a week.</span></span>

> [!NOTE]
> <span data-ttu-id="40ef0-161">La liste de compatibilité d’Internet IE est conçue pour fonctionner uniquement avec des sites publics.</span><span class="sxs-lookup"><span data-stu-id="40ef0-161">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un courrier électronique à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil officiel Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Besoin Microsoft Edge liste xml v1 | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Le site web que vous tentiez d’atteindre ne fonctionne pas avec Internet Explorer | Microsoft Office Prise en charge"  
