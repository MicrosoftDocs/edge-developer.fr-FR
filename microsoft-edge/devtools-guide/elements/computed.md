---
description: Utiliser le volet calculé pour comprendre la manière dont votre CSS effectue une cascade et des calculs sur des éléments de page
title: DevTools-éléments calculés
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/10/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, CSS, valeur calculée, zone modèle
ms.custom: seodec18
ms.openlocfilehash: c7b1b7c86f30e6947442c9b3d0e8856074ce4c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566348"
---
# <span data-ttu-id="43b7f-104">Calculée</span><span class="sxs-lookup"><span data-stu-id="43b7f-104">Computed</span></span>

<span data-ttu-id="43b7f-105">Regardez un diagramme de modèle de cadre (Width, Padding, bordure, marge et valeurs de décalage) de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="43b7f-105">See a box model diagram (width, padding, border, margin and offset values) of the selected element.</span></span> <span data-ttu-id="43b7f-106">Si vous activez l’outil de **mise en surbrillance des éléments** ( `Ctrl+Shift+L` ), les mêmes régions de couleur que vous avez affichées dans le diagramme (pour Width, Padding, etc.) qui s’affichent à l’écran.</span><span class="sxs-lookup"><span data-stu-id="43b7f-106">If you turn on the **Element highlighting** tool (`Ctrl+Shift+L`), the same colored regions in the diagram (for width, padding, etc.) that will overlay the rendered element when you select it on the page.</span></span> <span data-ttu-id="43b7f-107">Vous pouvez modifier n’importe quelle valeur dans le diagramme en cliquant dessus.</span><span class="sxs-lookup"><span data-stu-id="43b7f-107">You can edit any value in the diagram by clicking it.</span></span> 

<span data-ttu-id="43b7f-108">Le diagramme de modèle de cadre est une liste filtrable et éditable de propriétés de style calculées.</span><span class="sxs-lookup"><span data-stu-id="43b7f-108">Below the box model diagram is a filterable and editable list of computed style properties.</span></span> <span data-ttu-id="43b7f-109">La désactivation d’une propriété active active la propriété Next dans la cascade, s’il en existe une.</span><span class="sxs-lookup"><span data-stu-id="43b7f-109">Turning off a currently active property activates the next property in the cascade, if one exists.</span></span> <span data-ttu-id="43b7f-110">Vous pouvez afficher vos modifications dans le volet [**modifications**](./changes.md) .</span><span class="sxs-lookup"><span data-stu-id="43b7f-110">You can view your changes in the [**Changes**](./changes.md) pane.</span></span>

<span data-ttu-id="43b7f-111">Le bouton **afficher uniquement les styles utilisateur** est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="43b7f-111">The **Display user styles only** button is on by default.</span></span> <span data-ttu-id="43b7f-112">La pression sur le bouton inclut les styles de la *feuille de calcul par défaut* de Microsoft Edge dans la liste styles calculés.</span><span class="sxs-lookup"><span data-stu-id="43b7f-112">Depressing the button will include styles from the *default stylesheet* of Microsoft Edge in the computed styles list.</span></span>

![Volet calculé](../media/elements_computed.png)