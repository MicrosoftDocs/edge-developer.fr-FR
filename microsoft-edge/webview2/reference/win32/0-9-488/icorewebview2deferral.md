---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653530"
---
# <span data-ttu-id="c9f06-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="c9f06-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="c9f06-105">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="c9f06-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="c9f06-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c9f06-106">Summary</span></span>

 <span data-ttu-id="c9f06-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c9f06-107">Members</span></span>                        | <span data-ttu-id="c9f06-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c9f06-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9f06-109">Complete</span><span class="sxs-lookup"><span data-stu-id="c9f06-109">Complete</span></span>](#complete) | <span data-ttu-id="c9f06-110">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="c9f06-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="c9f06-111">Ses</span><span class="sxs-lookup"><span data-stu-id="c9f06-111">Members</span></span>

#### <span data-ttu-id="c9f06-112">Complete</span><span class="sxs-lookup"><span data-stu-id="c9f06-112">Complete</span></span> 

<span data-ttu-id="c9f06-113">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="c9f06-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="c9f06-114">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="c9f06-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="c9f06-115">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="c9f06-115">Complete should only be called once for each deferral taken.</span></span>

