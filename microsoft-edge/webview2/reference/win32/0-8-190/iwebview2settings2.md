---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: cb317e9078e48ed14091eb2eda6ff9d59a19c6ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653399"
---
# <span data-ttu-id="4e8c3-104">interface IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="4e8c3-104">interface IWebView2Settings2</span></span> 

> [!NOTE]
> <span data-ttu-id="4e8c3-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="4e8c3-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="4e8c3-107">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="4e8c3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4e8c3-108">Summary</span></span>

 <span data-ttu-id="4e8c3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4e8c3-109">Members</span></span>                        | <span data-ttu-id="4e8c3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4e8c3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e8c3-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4e8c3-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="4e8c3-112">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="4e8c3-113">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4e8c3-113">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="4e8c3-114">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-114">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="4e8c3-115">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-115">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="4e8c3-116">Ses</span><span class="sxs-lookup"><span data-stu-id="4e8c3-116">Members</span></span>

#### <span data-ttu-id="4e8c3-117">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4e8c3-117">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="4e8c3-118">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-118">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="4e8c3-119">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="4e8c3-119">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="4e8c3-120">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-120">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="4e8c3-121">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="4e8c3-121">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="4e8c3-122">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="4e8c3-122">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="4e8c3-123">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="4e8c3-123">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

