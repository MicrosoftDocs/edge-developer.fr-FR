---
description: En savoir plus sur les nouveautés à venir pour WebView2
title: Introduction à la WebView 2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: dcc9a92ee4db4c41a024aee565dfafe22b185e2a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698175"
---
# <span data-ttu-id="cab96-104">Introduction à Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="cab96-104">Microsoft Edge WebView2 roadmap</span></span>

##### <span data-ttu-id="cab96-105">Dernière mise à jour: 2020</span><span class="sxs-lookup"><span data-stu-id="cab96-105">Last Updated: May 2020</span></span>

<span data-ttu-id="cab96-106">Le contrôle WebView2 permet aux développeurs d’incorporer des technologies Web dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="cab96-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span> <span data-ttu-id="cab96-107">Ce document présente la procédure prospective pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="cab96-107">This document outlines the prospective roadmap for WebView2.</span></span> 

> [!NOTE]
> <span data-ttu-id="cab96-108">WebView2 est en cours de développement actif et la présentation continue à évoluer en fonction des variations du marché et des commentaires des clients. Veuillez noter que les plans décrits ici ne sont pas exhaustifs et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="cab96-108">WebView2 is under active development and the roadmap will continue to evolve based on market changes and customer feedback, so please note that the plans outlined here aren't exhaustive and are subject to change.</span></span> 

<span data-ttu-id="cab96-109">Si vous avez des inquiétudes ou des questions concernant la présentation, Merci de laisser votre avis dans le [référentiel samples de commentaires](https://github.com/MicrosoftEdge/WebViewFeedback).</span><span class="sxs-lookup"><span data-stu-id="cab96-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span></span>

<span data-ttu-id="cab96-110">L’équipe WebView2 dispose de quelques efforts importants:</span><span class="sxs-lookup"><span data-stu-id="cab96-110">The WebView2 team has a few major efforts underway:</span></span>

1.  <span data-ttu-id="cab96-111">Programme d’installation d’WebView2 Runtime (4e trimestre 2020)</span><span class="sxs-lookup"><span data-stu-id="cab96-111">WebView2 Runtime Installer (Q4 2020)</span></span>
2.  <span data-ttu-id="cab96-112">Version fixe (4e trim 2020)</span><span class="sxs-lookup"><span data-stu-id="cab96-112">Fixed Version (Q4 2020)</span></span>
3.  <span data-ttu-id="cab96-113">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="cab96-113">General Availability</span></span> 
    *   <span data-ttu-id="cab96-114">Win32 C/C++ (4e trim 2020)</span><span class="sxs-lookup"><span data-stu-id="cab96-114">Win32 C/C++ (Q4 2020)</span></span>
    *   <span data-ttu-id="cab96-115">.NET (4E TRIM 2020)</span><span class="sxs-lookup"><span data-stu-id="cab96-115">.NET (Q4 2020)</span></span>
    *   [<span data-ttu-id="cab96-116">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="cab96-116">WinUI 3.0</span></span>](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## <span data-ttu-id="cab96-117">Programme d’installation de & WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="cab96-117">WebView2 Runtime & Installer</span></span>

<span data-ttu-id="cab96-118">Le modèle [de distribution de](./concepts/distribution.md#microsoft-edge-webview2-runtime) WebView2 à l’aide de l’installation de WebView2 Runtime sur l’ordinateur de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cab96-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) distribution model will allow you to target or chain install the WebView2 Runtime onto your user's machine.</span></span> <span data-ttu-id="cab96-119">Une préversion de la version d’évaluation et du programme d’installation de WebView2 est censée être disponible pour les 2020 et la disponibilité du 4e trimestre 2020.</span><span class="sxs-lookup"><span data-stu-id="cab96-119">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>

## <span data-ttu-id="cab96-120">Version corrigée</span><span class="sxs-lookup"><span data-stu-id="cab96-120">Fixed version</span></span>

<span data-ttu-id="cab96-121">WebView2 modèle de distribution [fixe](./concepts/distribution.md#roadmap) vous permet d’empaqueter les fichiers binaires Microsoft Edge dans votre application native.</span><span class="sxs-lookup"><span data-stu-id="cab96-121">WebView2 [Fixed](./concepts/distribution.md#roadmap) distribution model allows you to package the Microsoft Edge binaries inside your native application.</span></span> <span data-ttu-id="cab96-122">Le processus d’ingénierie est actuellement en cours d’une préversion prévue pour être prêt à la fin du 3e trimestre 2020 et de la disponibilité du 4e trimestre 2020.</span><span class="sxs-lookup"><span data-stu-id="cab96-122">Engineering work is currently under way with a preview anticipated to be ready towards the end of  Q3 2020 and GA Q4 2020.</span></span>

## <span data-ttu-id="cab96-123">Disponibilité générale</span><span class="sxs-lookup"><span data-stu-id="cab96-123">General availability</span></span> 

### <span data-ttu-id="cab96-124">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="cab96-124">Win32 C/C++</span></span>

<span data-ttu-id="cab96-125">Le kit de développement logiciel (SDK) C/C++ Win32 est censé se produire dans le 4e trimestre 2020, juste après le runtime WebView2 et le programme d’installation GA.</span><span class="sxs-lookup"><span data-stu-id="cab96-125">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>

### <span data-ttu-id="cab96-126">.NET</span><span class="sxs-lookup"><span data-stu-id="cab96-126">.NET</span></span>

<span data-ttu-id="cab96-127">Le kit de développement logiciel (SDK) .NET englobe le SDK C/C++ Win32.</span><span class="sxs-lookup"><span data-stu-id="cab96-127">The .NET SDK wraps the Win32 C/C++ SDK.</span></span> <span data-ttu-id="cab96-128">Le kit de développement logiciel (SDK) .NET est censé se produire sous la version de Win32 C/C++ GA du 4e trimestre 2020.</span><span class="sxs-lookup"><span data-stu-id="cab96-128">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>

### <span data-ttu-id="cab96-129">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="cab96-129">WinUI 3.0</span></span>

<span data-ttu-id="cab96-130">Vous pouvez mettre WebView2 vers des applications UWP via [Win UI 3,0](/uwp/toolkits/winui3/), actuellement en alpha.</span><span class="sxs-lookup"><span data-stu-id="cab96-130">You can bring WebView2 to UWP applications through [Win UI 3.0](/uwp/toolkits/winui3/), currently in alpha.</span></span> <span data-ttu-id="cab96-131">Extraire l’introduction à la bibliothèque de l' [interface utilisateur Windows](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) pour rester à jour.</span><span class="sxs-lookup"><span data-stu-id="cab96-131">Checkout the [Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) to keep up to date.</span></span>  
