---
description: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
title: Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer
author: MSEdgeTeam
ms.date: 11/06/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web, Internet Explorer
ms.openlocfilehash: 2e1488359e405247e290ad8f6300c480a7e20af6
ms.sourcegitcommit: 6ef48c8cda392c6bf8217cff5f696ac620d10739
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163210"
---
# <span data-ttu-id="b3e82-104">Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b3e82-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="b3e82-105">De nombreux sites Web modernes possèdent des conceptions incompatibles avec Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="b3e82-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="b3e82-106">Lorsqu’un utilisateur d’IE visite un site Web public incompatible, il est possible qu’un message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b3e82-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="b3e82-107">Le message indique que le site Web n’est pas compatible avec le navigateur.</span><span class="sxs-lookup"><span data-stu-id="b3e82-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="b3e82-108">Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.</span><span class="sxs-lookup"><span data-stu-id="b3e82-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="b3e82-109">Pour limiter les perturbations, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3e82-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="b3e82-110">Lorsqu’un utilisateur d’Internet Explorer navigue vers un site Web incompatible avec IE, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b3e82-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="b3e82-111">Pour passer en revue les sites Web de la liste, accédez à la [liste Microsoft Edge requis][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="b3e82-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="b3e82-112">Cet article décrit les concepts suivants.</span><span class="sxs-lookup"><span data-stu-id="b3e82-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="b3e82-113">Interface utilisateur pour la redirection</span><span class="sxs-lookup"><span data-stu-id="b3e82-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="b3e82-114">Comment demander une mise à jour à la liste</span><span class="sxs-lookup"><span data-stu-id="b3e82-114">How to request an update to the list</span></span>  
    
## <span data-ttu-id="b3e82-115">Pourquoi un site Web est-il ajouté à la liste de compatibilité Internet?</span><span class="sxs-lookup"><span data-stu-id="b3e82-115">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="b3e82-116">La liste de compatibilité d’Internet Explorer ajoute uniquement un site Web lorsque les actions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="b3e82-116">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="b3e82-117">Affiche un message aux fins de compatibilité d’un utilisateur d’un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b3e82-117">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="b3e82-118">Demandes de propriétaire pour ajouter le site Web à la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b3e82-118">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="b3e82-119">Mettre à jour la liste de compatibilité d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b3e82-119">Update the IE compatibility list</span></span>  

<span data-ttu-id="b3e82-120">La liste de compatibilité Internet est un fichier XML sur [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="b3e82-120">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="b3e82-121">La liste est régulièrement mise à jour en réponse aux demandes des développeurs de sites Web et d’utilisateurs qui ont été ajoutées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="b3e82-121">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="b3e82-122">Les mises à jour apportées à la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3e82-122">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="b3e82-123">Envoyez les informations suivantes à [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site Web soit ajouté ou supprimé de la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b3e82-123">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="b3e82-124">Nom du propriétaire</span><span class="sxs-lookup"><span data-stu-id="b3e82-124">Owner name</span></span>  
*   <span data-ttu-id="b3e82-125">Titre de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="b3e82-125">Corporate title</span></span>  
*   <span data-ttu-id="b3e82-126">Adresse électronique</span><span class="sxs-lookup"><span data-stu-id="b3e82-126">Email address</span></span>  
*   <span data-ttu-id="b3e82-127">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="b3e82-127">Company name</span></span>  
*   <span data-ttu-id="b3e82-128">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="b3e82-128">Street address</span></span>  
*   <span data-ttu-id="b3e82-129">Adresse du site Web</span><span class="sxs-lookup"><span data-stu-id="b3e82-129">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b3e82-130">La liste de compatibilité d’Internet Explorer est conçue pour fonctionner uniquement avec des sites publics.</span><span class="sxs-lookup"><span data-stu-id="b3e82-130">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un e-mail à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil Microsoft Official"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Vous avez besoin de la liste Microsoft Edge v1 XML | Microsoft Edge"  
