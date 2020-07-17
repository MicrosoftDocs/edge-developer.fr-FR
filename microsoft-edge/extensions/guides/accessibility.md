---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Pour vous assurer que l’icône de votre extension est visible en mode clair et foncé, suivez le Guide d’accessibilité.
title: Accessibilité-extensions (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 60e794467c6d054e390ce61c40559afa3a110c21
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882792"
---
# <span data-ttu-id="f2706-104">Accessibilité-extensions (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f2706-104">Accessibility - Extensions (EdgeHTML)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="f2706-105">Création d’icônes d’extension accessibles pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f2706-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="f2706-106">Les développeurs d’extensions tierces sont invités à utiliser des ressources d’image qui répondent aux exigences strictes en matière d’accessibilité de Microsoft de sorte que les icônes soient clairement visibles pour les thèmes clairs et sombres.</span><span class="sxs-lookup"><span data-stu-id="f2706-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="f2706-107">Nous vous recommandons d’utiliser une 14:1 de rapport entre la couleur d’arrière-plan et la couleur dominante de l’icône.</span><span class="sxs-lookup"><span data-stu-id="f2706-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="f2706-108">Les extensions tierces développées par Microsoft appliquent un traitement visuel «d’adhésif» pour répondre à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="f2706-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="f2706-109">Exemples d’une «vignette»</span><span class="sxs-lookup"><span data-stu-id="f2706-109">Examples of the "stickering"</span></span>

<span data-ttu-id="f2706-110">L’objectif principal de «adhésive» est de rendre l’icône visuellement accessible sur une couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f2706-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="f2706-111">Le rapport couleur recommandé entre le trait blanc et votre icône doit être 14:1 pour prendre en charge les exigences de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="f2706-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="f2706-112">Icône bon</span><span class="sxs-lookup"><span data-stu-id="f2706-112">Good icon</span></span>
<span data-ttu-id="f2706-113">Dans le cas d’une vignette, une icône d’ombre est toujours visible sur une couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f2706-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![image de l’icône visible sur une couleur d’arrière-plan](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="f2706-115">Icône incorrecte</span><span class="sxs-lookup"><span data-stu-id="f2706-115">Bad icon</span></span>
<span data-ttu-id="f2706-116">Sans aucune vignette, une icône peut être mélangée avec l’arrière-plan et devenir impossible à voir.</span><span class="sxs-lookup"><span data-stu-id="f2706-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![image d’une icône fusionnée en arrière-plan noir](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="f2706-118">Icône «autocollant» dans votre extension</span><span class="sxs-lookup"><span data-stu-id="f2706-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="f2706-119">Les cinq étapes suivantes décrivent la méthode de création d’une icône d’extension qui répond aux exigences d’accessibilité de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="f2706-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="f2706-120">Étape1</span><span class="sxs-lookup"><span data-stu-id="f2706-120">Step 1</span></span>                                       | <span data-ttu-id="f2706-121">Étape2</span><span class="sxs-lookup"><span data-stu-id="f2706-121">Step 2</span></span>                                       | <span data-ttu-id="f2706-122">Étape3</span><span class="sxs-lookup"><span data-stu-id="f2706-122">Step 3</span></span>                                                                                 | <span data-ttu-id="f2706-123">Étape4</span><span class="sxs-lookup"><span data-stu-id="f2706-123">Step 4</span></span>                                                                          | <span data-ttu-id="f2706-124">Étape5</span><span class="sxs-lookup"><span data-stu-id="f2706-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="f2706-125">Définissez votre icône dans la grille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f2706-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="f2706-126">Réduisez la taille de votre icône de 2 pixels.</span><span class="sxs-lookup"><span data-stu-id="f2706-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="f2706-127">Copiez votre icône et collez-la sur place.</span><span class="sxs-lookup"><span data-stu-id="f2706-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="f2706-128">Créer un trait extérieur de 2 pixels avec des angles arrondis.</span><span class="sxs-lookup"><span data-stu-id="f2706-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="f2706-129">Dessinez le contour, relâchez le chemin composé et fusionnez les formes restantes.</span><span class="sxs-lookup"><span data-stu-id="f2706-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="f2706-130">Colorez le trait extérieur blanc et l’icône interne comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f2706-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![étape](./../media/accessibility-step1.png) | ![étape2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

