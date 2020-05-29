---
description: Apprenez à développer des extensions Microsoft Edge. Ces petits programmes peuvent être utilisés pour ajouter de nouvelles fonctionnalités à Microsoft Edge ou modifier des fonctionnalités existantes.
title: Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
ms.technology: extensions
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 4cc47ba9d927caf7457141f5c8c7eacbb9627b07
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565303"
---
# <span data-ttu-id="1c5e4-105">Extensions Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="1c5e4-105">Microsoft Edge (EdgeHTML) extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="1c5e4-106">Les extensions sont de petits programmes qui peuvent être utilisés pour ajouter de nouvelles fonctionnalités à Microsoft Edge (EdgeHTML) ou pour modifier la fonctionnalité existante.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-106">Extensions are small programs that can be used to add new features to Microsoft Edge (EdgeHTML) or modify the existing functionality.</span></span> <span data-ttu-id="1c5e4-107">Les extensions sont conçues pour améliorer l’utilisation de la navigation quotidienne d’un utilisateur en fournissant une fonctionnalité de niche essentielle pour les audiences ciblées.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-107">Extensions are intended to improve a user’s day-to-day browsing experience by providing niche functionality that is important to targeted audiences.</span></span>

<span data-ttu-id="1c5e4-108">Microsoft Edge (EdgeHTML) prend en charge un nouveau modèle d’extension HTML, JavaScript et CSS.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-108">Microsoft Edge (EdgeHTML) supports a new HTML, JavaScript and CSS based extension model.</span></span> <span data-ttu-id="1c5e4-109">Ce nouveau modèle est compatible chrome, ce qui signifie que les développeurs d’extensions chrome existants pourront migrer leurs extensions vers Microsoft Edge (EdgeHTML) avec les modifications minimales.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-109">This new model is Chrome-compatible which means that existing Chrome extension developers will be able to migrate their extensions to Microsoft Edge (EdgeHTML) with minimal changes.</span></span>

<span data-ttu-id="1c5e4-110">Pour obtenir une vue d’ensemble du parcours de la création d’une extension Microsoft Edge (EdgeHTML) du développement à la publication, consultez le [Guide de mise en route](./getting-started.md).</span><span class="sxs-lookup"><span data-stu-id="1c5e4-110">To get an overview of the end to end journey of creating a Microsoft Edge (EdgeHTML) extension from development to publishing, check out the [Getting started guide](./getting-started.md)!</span></span>


## <span data-ttu-id="1c5e4-111">Articles populaires</span><span class="sxs-lookup"><span data-stu-id="1c5e4-111">Popular articles</span></span>

<table>
  <tr>
    <td><a href = "./api-support/extension-api-roadmap.md"><span data-ttu-id="1c5e4-112">Introduction à l’API d’extension</span><span class="sxs-lookup"><span data-stu-id="1c5e4-112">Extension API roadmap</span></span></a></td>
    <td><span data-ttu-id="1c5e4-113">Découvrez les API prises en charge/en développement pour Windows 10 Insider Preview et les versions publiées publique de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-113">Check out what APIs are supported/in development for Windows 10 Insider Preview and publicly released builds of Microsoft Edge.</span></span></td></p>
<p>  </tr>
  <tr>
    <td><a href = "./api-support/supported-apis.md"><span data-ttu-id="1c5e4-114">API prises en charge</span><span class="sxs-lookup"><span data-stu-id="1c5e4-114">Supported APIs</span></span></a></td>
    <td><span data-ttu-id="1c5e4-115">Obtenez des informations sur nos API prises en charge, notamment les problèmes connus et les incompatibilités chrome.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-115">Get info on our supported APIs including known issues and Chrome incompatibilities.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/creating-an-extension.md"><span data-ttu-id="1c5e4-116">Créer une extension</span><span class="sxs-lookup"><span data-stu-id="1c5e4-116">Creating an extension</span></span></a></td>
    <td><span data-ttu-id="1c5e4-117">Vous débutez dans le développement d’extensions?</span><span class="sxs-lookup"><span data-stu-id="1c5e4-117">New to the world of extension development?</span></span> <span data-ttu-id="1c5e4-118">Testez quelques didacticiels pour être opérationnel.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-118">Try out some tutorials to get up to speed.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/packaging.md"><span data-ttu-id="1c5e4-119">Intégration</span><span class="sxs-lookup"><span data-stu-id="1c5e4-119">Packaging</span></span></a></td>
    <td><span data-ttu-id="1c5e4-120">Découvrez comment empaqueter votre extension une fois que vous avez&#39;le développement fini.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-120">Learn how to package up your extension after you&#39;ve finished development.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/porting-chrome-extensions.md"><span data-ttu-id="1c5e4-121">Portage d’extensions de chrome</span><span class="sxs-lookup"><span data-stu-id="1c5e4-121">Porting Chrome extensions</span></span></a></td>
    <td><span data-ttu-id="1c5e4-122">Avez-vous créé une extension chrome que vous&#39;voir sur Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="1c5e4-122">Created a Chrome extension you&#39;d like to see on Microsoft Edge?</span></span> <span data-ttu-id="1c5e4-123">Découvrez comment le porter à l’aide du kit de connaissances Microsoft Edge extension.</span><span class="sxs-lookup"><span data-stu-id="1c5e4-123">See how to port it with the Microsoft Edge Extension Toolkit.</span></span></td>

  </tr>
</table>
