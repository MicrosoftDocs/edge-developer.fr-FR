---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4ba0299f3afbc6fc2846481f52c1000cd338ecd8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885785"
---
# <span data-ttu-id="a99cb-104">0.8.355-interface IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="a99cb-104">0.8.355 - interface IWebView2Settings2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="a99cb-105">Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.</span><span class="sxs-lookup"><span data-stu-id="a99cb-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="a99cb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a99cb-106">Summary</span></span>

 <span data-ttu-id="a99cb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a99cb-107">Members</span></span>                        | <span data-ttu-id="a99cb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a99cb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a99cb-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a99cb-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="a99cb-110">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a99cb-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="a99cb-111">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a99cb-111">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="a99cb-112">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="a99cb-112">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="a99cb-113">Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="a99cb-113">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="a99cb-114">Ses</span><span class="sxs-lookup"><span data-stu-id="a99cb-114">Members</span></span>

#### <span data-ttu-id="a99cb-115">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a99cb-115">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="a99cb-116">La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.</span><span class="sxs-lookup"><span data-stu-id="a99cb-116">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="a99cb-117">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="a99cb-117">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="a99cb-118">Par défaut, la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a99cb-118">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="a99cb-119">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="a99cb-119">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="a99cb-120">Définissez la propriété AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="a99cb-120">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="a99cb-121">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="a99cb-121">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

