---
description: Représentations DateTime et TimeSpan Windows Runtime
title: Représentations DateTime et TimeSpan Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c2627826755f041a440112c3390ecb17d1f703ce
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398125"
---
# <a name="windows-runtime-datetime-and-timespan-representations"></a><span data-ttu-id="8b609-103">Représentations DateTime et TimeSpan Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="8b609-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="8b609-104">La représentation JavaScript des dates et heures est différente de la version Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="8b609-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="8b609-105">La structure [DateTime][UwpWindowsFoundationDatetime] Windows Runtime est représentée en JavaScript sous la forme d’une [date][MDNDate] avec un magasin de données qui correspond aux données \(et présente une plage et une précision différentes de celle du `DateTime` javascript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="8b609-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="8b609-106">Si vous modifiez cet `Date` objet personnalisé, il devient un JavaScript standard et `Date` perd sa précision.</span><span class="sxs-lookup"><span data-stu-id="8b609-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="8b609-107">Les valeurs JavaScript peuvent être transmises à Windows Runtime et seront vérifiées par plage, ce qui peut entraîner le `Date` `DateTime` marshaling des exceptions.</span><span class="sxs-lookup"><span data-stu-id="8b609-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

<span data-ttu-id="8b609-108">La structure [TimeSpan Windows][UwpWindowsFoundationTimespan] Runtime est convertie en millisecondes et renvoyée sous forme de nombre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8b609-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b609-109">Voir également</span><span class="sxs-lookup"><span data-stu-id="8b609-109">See also</span></span>  

[<span data-ttu-id="8b609-110">Utilisation de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="8b609-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Documents Microsoft"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "| Documents Microsoft"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Date | MDN"  
