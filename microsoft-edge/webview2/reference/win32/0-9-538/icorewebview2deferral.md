---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880121"
---
# <span data-ttu-id="86a63-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="86a63-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="86a63-105">Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.</span><span class="sxs-lookup"><span data-stu-id="86a63-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="86a63-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="86a63-106">Summary</span></span>

 <span data-ttu-id="86a63-107">Ses</span><span class="sxs-lookup"><span data-stu-id="86a63-107">Members</span></span>                        | <span data-ttu-id="86a63-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="86a63-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86a63-109">Complete</span><span class="sxs-lookup"><span data-stu-id="86a63-109">Complete</span></span>](#complete) | <span data-ttu-id="86a63-110">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="86a63-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="86a63-111">Ses</span><span class="sxs-lookup"><span data-stu-id="86a63-111">Members</span></span>

#### <span data-ttu-id="86a63-112">Complete</span><span class="sxs-lookup"><span data-stu-id="86a63-112">Complete</span></span> 

<span data-ttu-id="86a63-113">Termine l’événement différé associé.</span><span class="sxs-lookup"><span data-stu-id="86a63-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="86a63-114">valeur publique HRESULT [achevée](#complete)()</span><span class="sxs-lookup"><span data-stu-id="86a63-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="86a63-115">Complète doit être appelé une seule fois pour chaque Report.</span><span class="sxs-lookup"><span data-stu-id="86a63-115">Complete should only be called once for each deferral taken.</span></span>

