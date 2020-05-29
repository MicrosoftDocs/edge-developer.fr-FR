---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Repères pour les fonctionnalités du navigateur dans Microsoft Edge.
title: Guide du développement-navigateur
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/28/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: e7b13b18048e0a703ca5e2a0e5b52712f41c2101
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564704"
---
# <span data-ttu-id="2135c-104">Fonctionnalités du navigateur</span><span class="sxs-lookup"><span data-stu-id="2135c-104">Browser features</span></span>

## <span data-ttu-id="2135c-105">Stratégies de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="2135c-105">Autoplay policies</span></span>

 <span data-ttu-id="2135c-106">Microsoft Edge offre aux utilisateurs la possibilité de personnaliser leurs préférences de navigation sur les sites Web qui entourent le son par lecture automatique afin de réduire le nombre de distractions sur le Web et de économiser la bande passante.</span><span class="sxs-lookup"><span data-stu-id="2135c-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="2135c-107">Les utilisateurs peuvent personnaliser le comportement multimédia avec les contrôles de lecture automatique globaux et par site.</span><span class="sxs-lookup"><span data-stu-id="2135c-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span> <span data-ttu-id="2135c-108">Par ailleurs, Microsoft Edge supprime automatiquement la lecture automatique de contenus multimédias dans les onglets d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2135c-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="2135c-109">Pour plus d’informations sur l’utilisation du contenu multimédia hébergé sur votre site, voir [stratégies de lecture automatique](./browser-features/autoplay-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="2135c-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>

## <span data-ttu-id="2135c-110">Flash</span><span class="sxs-lookup"><span data-stu-id="2135c-110">Flash</span></span>
<span data-ttu-id="2135c-111">Si flash est utilisé sur votre page mais que l’utilisateur ne l’a pas activé, Microsoft Edge affichera en principe une icône de pièce de puzzle dans la barre d’adresse.</span><span class="sxs-lookup"><span data-stu-id="2135c-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span> <span data-ttu-id="2135c-112">Si vous ajoutez dynamiquement le contrôle instantané après le chargement de la page, l’icône de puzzle peut ne pas s’afficher, auquel cas vous voudrez [tester si flash est chargé et fournir une version de secours harmonieuse](./browser-features/flash.md) en cas d’absence.</span><span class="sxs-lookup"><span data-stu-id="2135c-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>

## <span data-ttu-id="2135c-113">Mode Lecture</span><span class="sxs-lookup"><span data-stu-id="2135c-113">Reading view</span></span>
<span data-ttu-id="2135c-114">Microsoft Edge fournit un [mode lecture](./browser-features/reading-view.md) pour une connaissance plus rationalisée et plus agréable de la lecture de pages Web, sans la distraction de contenus non liés ou secondaires sur la page.</span><span class="sxs-lookup"><span data-stu-id="2135c-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span> <span data-ttu-id="2135c-115">Vous trouverez ci-dessous des conseils pour garantir une meilleure utilisation du mode lecture sur votre site, ainsi que des instructions pour l’utilisation du mode lecture sur votre site.</span><span class="sxs-lookup"><span data-stu-id="2135c-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>

## <span data-ttu-id="2135c-116">Découverte du fournisseur de recherche</span><span class="sxs-lookup"><span data-stu-id="2135c-116">Search provider discovery</span></span>

<span data-ttu-id="2135c-117">L’intégration de recherche complète est intégrée à la barre d’adresses Microsoft Edge, y compris aux suggestions de recherche, aux résultats provenant du Web, à votre historique de navigation et aux favoris.</span><span class="sxs-lookup"><span data-stu-id="2135c-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="2135c-118">Vous [trouverez ci-dessous des informations supplémentaires pour les fournisseurs de recherche](./browser-features/search-provider-discovery.md) qui souhaitent obtenir une assistance technique pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2135c-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>
