---
description: Héberger et publier des extensions dans l’entreprise pour Microsoft Edge (Chromium).
title: Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327686"
---
# <span data-ttu-id="2d72f-104">Publier et mettre à jour des extensions dans le magasin de modules extensions Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2d72f-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="2d72f-105">La plupart des extensions sont publiées dans le magasin des [extensions Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] pour protéger les utilisateurs contre les extensions malveillantes.</span><span class="sxs-lookup"><span data-stu-id="2d72f-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <span data-ttu-id="2d72f-106">Options de publication des extensions</span><span class="sxs-lookup"><span data-stu-id="2d72f-106">Publish options for extensions</span></span>  

<span data-ttu-id="2d72f-107">Toutes les extensions sont distribuées aux utilisateurs en tant que fichier d’archive \( `.zip` \) spécial avec `.crx` un suffixe.</span><span class="sxs-lookup"><span data-stu-id="2d72f-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="2d72f-108">Les extensions publiées dans le magasin des extensions Microsoft Edge sont téléchargées en tant que `.zip` fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d72f-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="2d72f-109">Le processus de publication convertit automatiquement le `.zip` fichier en `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="2d72f-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="2d72f-110">Les deux scénarios suivants n’exigent pas que vous publiiez votre extension dans le magasin de modules extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2d72f-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="2d72f-111">Extensions distribuées à l’aide de la stratégie Entreprise.</span><span class="sxs-lookup"><span data-stu-id="2d72f-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="2d72f-112">Utilisation de répertoires d’extension décompressés sur un ordinateur local lorsque Microsoft Edge est en mode développeur.</span><span class="sxs-lookup"><span data-stu-id="2d72f-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <span data-ttu-id="2d72f-113">Mises à jour des extensions</span><span class="sxs-lookup"><span data-stu-id="2d72f-113">Updates to extensions</span></span>

<span data-ttu-id="2d72f-114">Le navigateur Microsoft Edge recherche régulièrement les nouvelles versions des extensions installées et les mises à jour sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d72f-114">The Microsoft Edge browser periodically checks for new versions of installed extensions and updates each without user intervention.</span></span>  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensions - Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> <span data-ttu-id="2d72f-116">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2d72f-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2d72f-117">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="2d72f-117">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2d72f-119">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2d72f-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
