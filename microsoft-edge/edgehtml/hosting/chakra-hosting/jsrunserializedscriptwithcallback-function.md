---
description: Exécute un script sérialisé. Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.
title: Fonction JsRunSerializedScriptWithCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233470"
---
# <span data-ttu-id="354ac-104">JsRunSerializedScriptWithCallback Function</span><span class="sxs-lookup"><span data-stu-id="354ac-104">JsRunSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="354ac-105">Exécute un script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="354ac-105">Runs a serialized script.</span></span> <span data-ttu-id="354ac-106">Offre la possibilité de charger les sources de scripts uniquement si vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="354ac-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="354ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="354ac-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="354ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="354ac-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="354ac-109">Rappel appelé lorsque le code source du script doit être chargé.</span><span class="sxs-lookup"><span data-stu-id="354ac-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="354ac-110">Rappel appelé lorsque le script sérialisé et le code source ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="354ac-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="354ac-111">Script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="354ac-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="354ac-112">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="354ac-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="354ac-113">Ce contexte est transmis à scriptLoadCallback et scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="354ac-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="354ac-114">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="354ac-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="354ac-115">Résultat de l’exécution du script, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="354ac-115">The result of running the script, if any.</span></span> <span data-ttu-id="354ac-116">Ce paramètre peut être null.</span><span class="sxs-lookup"><span data-stu-id="354ac-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="354ac-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="354ac-117">Return Value</span></span>  
 <span data-ttu-id="354ac-118">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="354ac-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="354ac-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="354ac-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="354ac-120">Cette API n’est pas encore disponible pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="354ac-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="354ac-121">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="354ac-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="354ac-122">Le runtime sera maintenu sur la mémoire tampon jusqu’à ce que toutes les instances de toutes les fonctions créées à partir de la mémoire tampon soient récupérées par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="354ac-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="354ac-123">Il appelle alors scriptUnloadCallback pour indiquer à l’appelant qu’il est en sécurité.</span><span class="sxs-lookup"><span data-stu-id="354ac-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="354ac-124">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="354ac-124">Requirements</span></span>  
 <span data-ttu-id="354ac-125">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="354ac-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="354ac-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="354ac-126">See Also</span></span>  
 [<span data-ttu-id="354ac-127">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="354ac-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
