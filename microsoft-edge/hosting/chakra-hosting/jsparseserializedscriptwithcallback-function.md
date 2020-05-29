---
description: Analyse un script sérialisé et retourne une fonction qui représente le script. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.
title: Fonction JsParseSerializedScriptWithCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566280"
---
# <span data-ttu-id="82919-104">Fonction JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="82919-104">JsParseSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="82919-105">Analyse un script sérialisé et retourne une fonction qui représente le script.</span><span class="sxs-lookup"><span data-stu-id="82919-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="82919-106">Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="82919-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="82919-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82919-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="82919-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82919-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="82919-109">Rappel appelé lorsque le code source du script doit être chargé.</span><span class="sxs-lookup"><span data-stu-id="82919-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="82919-110">Rappel appelé lorsque le script sérialisé et le code source ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="82919-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="82919-111">Script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="82919-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="82919-112">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="82919-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="82919-113">Ce contexte est transmis à scriptLoadCallback et scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="82919-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="82919-114">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="82919-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="82919-115">Fonction qui représente le code de script.</span><span class="sxs-lookup"><span data-stu-id="82919-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="82919-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="82919-116">Return Value</span></span>  
 <span data-ttu-id="82919-117">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="82919-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="82919-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="82919-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="82919-119">Cette API n’est pas encore disponible pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="82919-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="82919-120">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="82919-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="82919-121">Le runtime sera maintenu sur la mémoire tampon jusqu’à ce que toutes les instances de toutes les fonctions créées à partir de la mémoire tampon soient récupérées par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="82919-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="82919-122">Il appelle alors scriptUnloadCallback pour indiquer à l’appelant qu’il est en sécurité.</span><span class="sxs-lookup"><span data-stu-id="82919-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="82919-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82919-123">Requirements</span></span>  
 <span data-ttu-id="82919-124">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="82919-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="82919-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82919-125">See Also</span></span>  
 [<span data-ttu-id="82919-126">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="82919-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)