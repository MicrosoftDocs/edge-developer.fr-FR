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
# <span data-ttu-id="f9daa-104">Déplacer des utilisateurs vers Microsoft Edge à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9daa-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="f9daa-105">De nombreux sites Web modernes possèdent des conceptions incompatibles avec Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="f9daa-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="f9daa-106">Lorsqu’un utilisateur d’IE visite un site Web public incompatible, il est possible qu’un message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f9daa-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="f9daa-107">Le message indique que le site Web n’est pas compatible avec le navigateur.</span><span class="sxs-lookup"><span data-stu-id="f9daa-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="f9daa-108">Une fois le message affiché, l’utilisateur est censé basculer manuellement vers un navigateur moderne.</span><span class="sxs-lookup"><span data-stu-id="f9daa-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="f9daa-109">Pour limiter les perturbations, à partir de la version 84, Microsoft Edge prend en charge une nouvelle fonctionnalité qui redirige automatiquement les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f9daa-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="f9daa-110">Lorsqu’un utilisateur d’Internet Explorer navigue vers un site Web incompatible avec IE, Windows redirige automatiquement l’utilisateur vers Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f9daa-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="f9daa-111">Pour passer en revue les sites Web de la liste, accédez à la [liste Microsoft Edge requis][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="f9daa-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="f9daa-112">Cet article décrit les concepts suivants.</span><span class="sxs-lookup"><span data-stu-id="f9daa-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="f9daa-113">Interface utilisateur pour la redirection</span><span class="sxs-lookup"><span data-stu-id="f9daa-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="f9daa-114">Comment ajouter votre site Web à la liste de compatibilité d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9daa-114">How to add your website to the IE compatibility list</span></span>  
*   <span data-ttu-id="f9daa-115">Suppression de votre site Web de la liste de compatibilité d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9daa-115">How to remove your website from the IE compatibility list</span></span>  
    
## <span data-ttu-id="f9daa-116">Pourquoi un site Web est-il ajouté à la liste de compatibilité Internet?</span><span class="sxs-lookup"><span data-stu-id="f9daa-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="f9daa-117">La liste de compatibilité d’Internet Explorer ajoute uniquement un site Web lorsque les actions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="f9daa-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="f9daa-118">Affiche un message aux fins de compatibilité d’un utilisateur d’un autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="f9daa-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="f9daa-119">Demandes de propriétaire pour ajouter le site Web à la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f9daa-119">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="f9daa-120">Mettre à jour la liste de compatibilité d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9daa-120">Update the IE compatibility list</span></span>  

<span data-ttu-id="f9daa-121">La liste de compatibilité Internet est un fichier XML sur [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="f9daa-121">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="f9daa-122">La liste est régulièrement mise à jour en réponse aux demandes des développeurs de sites Web et d’utilisateurs qui ont été ajoutées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="f9daa-122">The list is regularly updated in response to user's and website developers requests to have websites added or removed.</span></span>  <span data-ttu-id="f9daa-123">Les mises à jour apportées à la liste sont automatiquement téléchargées sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f9daa-123">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="f9daa-124">Envoyez les informations suivantes à [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] pour que votre site Web soit ajouté ou supprimé de la liste de compatibilité d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f9daa-124">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="f9daa-125">Nom du propriétaire</span><span class="sxs-lookup"><span data-stu-id="f9daa-125">Owner name</span></span>  
*   <span data-ttu-id="f9daa-126">Titre de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="f9daa-126">Corporate title</span></span>  
*   <span data-ttu-id="f9daa-127">Adresse électronique</span><span class="sxs-lookup"><span data-stu-id="f9daa-127">Email address</span></span>  
*   <span data-ttu-id="f9daa-128">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="f9daa-128">Company name</span></span>  
*   <span data-ttu-id="f9daa-129">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="f9daa-129">Street address</span></span>  
*   <span data-ttu-id="f9daa-130">Adresse du site Web</span><span class="sxs-lookup"><span data-stu-id="f9daa-130">Website address</span></span>  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envoyer un e-mail à ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Accueil Microsoft Official"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Vous avez besoin de la liste Microsoft Edge v1 XML | Microsoft Edge"  
