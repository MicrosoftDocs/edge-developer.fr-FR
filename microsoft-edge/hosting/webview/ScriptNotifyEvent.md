---
description: Représente une chaîne de notification transmise à partir du contenu WebView vers l’application.
title: Objet ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564626"
---
# <span data-ttu-id="8634f-104">Objet ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="8634f-104">ScriptNotifyEvent object</span></span>

<span data-ttu-id="8634f-105">Objet qui représente un événement déclenché lorsque le contenu contenu dans le [WebView](../webview.md) transmet une chaîne à l’application en utilisant JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8634f-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>

## <span data-ttu-id="8634f-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8634f-106">Properties</span></span>
    
### <span data-ttu-id="8634f-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="8634f-107">callingUri</span></span>

<span data-ttu-id="8634f-108">Obtient l’URI (Uniform Resource Identifier) de la page qui contient le script qui a déclenché l' **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="8634f-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>

<span data-ttu-id="8634f-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8634f-109">This property is read-only.</span></span>

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### <span data-ttu-id="8634f-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="8634f-110">Property value</span></span>
<span data-ttu-id="8634f-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8634f-111">Type: **DOMString**</span></span>

### <span data-ttu-id="8634f-112">value</span><span class="sxs-lookup"><span data-stu-id="8634f-112">value</span></span>

<span data-ttu-id="8634f-113">Nom de la méthode transmis à l’application.</span><span class="sxs-lookup"><span data-stu-id="8634f-113">The method name as passed to the application.</span></span>

<span data-ttu-id="8634f-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8634f-114">This property is read-only.</span></span>

```js
var value = ScriptNotifyEvent.value;
```

#### <span data-ttu-id="8634f-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="8634f-115">Property value</span></span>
<span data-ttu-id="8634f-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8634f-116">Type: **DOMString**</span></span>