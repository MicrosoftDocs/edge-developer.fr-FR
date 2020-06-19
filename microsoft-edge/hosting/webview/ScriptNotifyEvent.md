---
description: Représente une chaîne de notification transmise à partir du contenu WebView vers l’application.
title: Objet ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752009"
---
# <span data-ttu-id="91309-104">Objet ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="91309-104">ScriptNotifyEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="91309-105">Objet qui représente un événement déclenché lorsque le contenu contenu dans le [WebView](../webview.md) transmet une chaîne à l’application en utilisant JavaScript.</span><span class="sxs-lookup"><span data-stu-id="91309-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>  

## <span data-ttu-id="91309-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91309-106">Properties</span></span>  

### <span data-ttu-id="91309-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="91309-107">callingUri</span></span>  

<span data-ttu-id="91309-108">Obtient l’URI (Uniform Resource Identifier) de la page qui contient le script qui a déclenché l' **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="91309-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>  

<span data-ttu-id="91309-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="91309-109">This property is read-only.</span></span>  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### <span data-ttu-id="91309-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="91309-110">Property value</span></span>  

<span data-ttu-id="91309-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="91309-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="91309-112">value</span><span class="sxs-lookup"><span data-stu-id="91309-112">value</span></span>  

<span data-ttu-id="91309-113">Nom de la méthode transmis à l’application.</span><span class="sxs-lookup"><span data-stu-id="91309-113">The method name as passed to the application.</span></span>  

<span data-ttu-id="91309-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="91309-114">This property is read-only.</span></span>  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### <span data-ttu-id="91309-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="91309-115">Property value</span></span>  

<span data-ttu-id="91309-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="91309-116">Type: **DOMString**</span></span>  
