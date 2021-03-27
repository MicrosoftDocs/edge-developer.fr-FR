---
description: Héberger et publier des extensions dans l’entreprise pour Microsoft Edge (Chromium).
title: Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461219"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a><span data-ttu-id="927b9-104">Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="927b9-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="927b9-105">La plupart des extensions sont publiées dans le magasin des [extensions Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] pour protéger les utilisateurs contre les extensions malveillantes.</span><span class="sxs-lookup"><span data-stu-id="927b9-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <a name="publish-options-for-extensions"></a><span data-ttu-id="927b9-106">Options de publication des extensions</span><span class="sxs-lookup"><span data-stu-id="927b9-106">Publish options for extensions</span></span>  

<span data-ttu-id="927b9-107">Toutes les extensions sont distribuées aux utilisateurs en tant que fichier d’archive \( `.zip` \) spécial avec `.crx` un suffixe.</span><span class="sxs-lookup"><span data-stu-id="927b9-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="927b9-108">Les extensions publiées dans le magasin des extensions Microsoft Edge sont téléchargées en tant que `.zip` fichiers.</span><span class="sxs-lookup"><span data-stu-id="927b9-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="927b9-109">Le processus de publication convertit automatiquement le `.zip` fichier en `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="927b9-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="927b9-110">Les deux scénarios suivants ne vous obligent pas à publier votre extension dans le magasin de modules extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="927b9-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="927b9-111">Extensions distribuées à l’aide de la stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="927b9-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="927b9-112">Utilisation de répertoires d’extension décompressés sur un ordinateur local lorsque Microsoft Edge est en mode développeur.</span><span class="sxs-lookup"><span data-stu-id="927b9-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <a name="updates-to-extensions"></a><span data-ttu-id="927b9-113">Mises à jour des extensions</span><span class="sxs-lookup"><span data-stu-id="927b9-113">Updates to extensions</span></span>

<span data-ttu-id="927b9-114">Le navigateur Microsoft Edge recherche automatiquement les nouvelles versions des extensions installées.</span><span class="sxs-lookup"><span data-stu-id="927b9-114">The Microsoft Edge browser automatically checks for new versions of installed Extensions.</span></span> <span data-ttu-id="927b9-115">Les mises à jour sont installées sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="927b9-115">Updates are installed without user intervention.</span></span>  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensions - Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> <span data-ttu-id="927b9-117">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="927b9-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="927b9-118">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="927b9-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="927b9-120">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="927b9-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
