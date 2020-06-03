---
description: Extensions d’Enterprise documentation pour les extensions de chrome.
title: Hébergement et mise à jour
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: eb1f9921d503d25557fc9efb1517537e7a90f4aa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565448"
---
# <span data-ttu-id="6871b-104">Hébergement et mise à jour du Web Store</span><span class="sxs-lookup"><span data-stu-id="6871b-104">Web Store Hosting and Updating</span></span>  

<span data-ttu-id="6871b-105">La plupart des extensions sont hébergées dans le [catalogue Microsoft Edge Insider (Microsoft Edge Insider)][MicrosoftStoreExtensions] pour protéger au mieux les utilisateurs d’extensions malveillantes.</span><span class="sxs-lookup"><span data-stu-id="6871b-105">Most Extensions are hosted in the [Microsoft Edge Insider Addons catalog \(Microsoft Edge Insider Addons\)][MicrosoftStoreExtensions] to best protect users from malicious Extensions.</span></span>  

## <span data-ttu-id="6871b-106">Diffuser</span><span class="sxs-lookup"><span data-stu-id="6871b-106">Hosting</span></span>  

<span data-ttu-id="6871b-107">Toutes les extensions sont distribuées aux utilisateurs sous forme de fichier ZIP spécial avec le suffixe. CRX.</span><span class="sxs-lookup"><span data-stu-id="6871b-107">All Extensions are distributed to users as a special ZIP file with a .crx suffix.</span></span>  <span data-ttu-id="6871b-108">Les extensions hébergées dans les modules complémentaires Microsoft Edge sont téléchargées en tant que fichiers. zip.</span><span class="sxs-lookup"><span data-stu-id="6871b-108">Extensions hosted in the Microsoft Edge Addons are uploaded as .zip files.</span></span> <span data-ttu-id="6871b-109">Le processus de publication convertit automatiquement le fichier zip en fichier. CRX.</span><span class="sxs-lookup"><span data-stu-id="6871b-109">The publishing process automatically converts the .zip into a .crx file.</span></span>  

<span data-ttu-id="6871b-110">Il existe deux exceptions à la règle d’hébergement des modules complémentaires Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="6871b-110">There are two exceptions to the Microsoft Edge Addons hosting rule:</span></span>  

1.  <span data-ttu-id="6871b-111">Extensions distribuées par le biais de la stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6871b-111">Extensions that are distributed through the Enterprise policy.</span></span>  
1.  <span data-ttu-id="6871b-112">Des répertoires d’extension décompressés à partir d’un ordinateur local en mode développeur.</span><span class="sxs-lookup"><span data-stu-id="6871b-112">Unpacked Extension directories from a local machine while in developer mode.</span></span>  

## <span data-ttu-id="6871b-113">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="6871b-113">Updating</span></span>  

<span data-ttu-id="6871b-114">Le navigateur Microsoft Edge vérifie régulièrement les nouvelles versions des extensions installées et met à jour les mises à jour, sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6871b-114">The Microsoft Edge browser periodically checks for new versions of installed Extensions and updates each without user intervention.</span></span>  

> [!NOTE]
> <span data-ttu-id="6871b-115">Les étapes permettant de mettre à jour une extension sur des modules complémentaires Microsoft Edge sont planifiées.</span><span class="sxs-lookup"><span data-stu-id="6871b-115">Steps to update an Extension on Microsoft Edge Addons are planned be added.</span></span>  

<!-- image links -->

<!-- links -->  

[MicrosoftStoreExtensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensions-compléments Microsoft Edge Insider"  

> [!NOTE]
> <span data-ttu-id="6871b-117">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6871b-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6871b-118">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/hosting).</span><span class="sxs-lookup"><span data-stu-id="6871b-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="6871b-120">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6871b-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  