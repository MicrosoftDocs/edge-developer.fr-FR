---
title: Représentations DateTime et TimeSpan Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1c51bba74bb7e5182eb25342badcae848eeba339
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942051"
---
# <span data-ttu-id="7f3d5-102">Représentations DateTime et TimeSpan Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="7f3d5-102">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="7f3d5-103">La représentation JavaScript de dates et d’heures est différente de la version Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="7f3d5-103">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="7f3d5-104">La structure [DateTime][UwpWindowsFoundationDatetime] Windows Runtime est représentée dans JavaScript en tant que [Date][MDNDate] contenant un magasin de stockage qui correspond aux `DateTime` données \ (et dont la plage et la précision sont différentes de celles du JavaScript `Date` ).</span><span class="sxs-lookup"><span data-stu-id="7f3d5-104">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="7f3d5-105">Si vous modifiez cet `Date` objet personnalisé, il devient un code JavaScript standard `Date` et perd de la précision.</span><span class="sxs-lookup"><span data-stu-id="7f3d5-105">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="7f3d5-106">`Date`Les valeurs JavaScript peuvent être transmises à un Windows Runtime `DateTime` et sont contrôlées par plages, ce qui peut entraîner des exceptions de marshaling.</span><span class="sxs-lookup"><span data-stu-id="7f3d5-106">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="7f3d5-107">La structure [TimeSpan][UwpWindowsFoundationTimespan] Windows Runtime est convertie en millisecondes et retourné en tant que nombre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7f3d5-107">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="7f3d5-108">Voir également</span><span class="sxs-lookup"><span data-stu-id="7f3d5-108">See also</span></span>  

[<span data-ttu-id="7f3d5-109">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="7f3d5-109">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Struct DateTime | Documents Microsoft"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Structure TimeSpan | Documents Microsoft"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Date | MDN"  
