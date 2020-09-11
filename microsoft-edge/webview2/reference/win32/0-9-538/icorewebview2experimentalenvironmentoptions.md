---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: ba91056fa6d2e6cf9e7da18202fb3c74d7deb827
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010242"
---
# <span data-ttu-id="c86e1-104">0.9.579-interface ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="c86e1-104">0.9.579 - interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="c86e1-105">Options expérimentales utilisées pour créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="c86e1-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="c86e1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c86e1-106">Summary</span></span>

 <span data-ttu-id="c86e1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c86e1-107">Members</span></span>                        | <span data-ttu-id="c86e1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c86e1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c86e1-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="c86e1-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="c86e1-110">La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.</span><span class="sxs-lookup"><span data-stu-id="c86e1-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="c86e1-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="c86e1-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="c86e1-112">Définissez la propriété IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="c86e1-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="c86e1-113">Une implémentation par défaut est fournie dans WebView2ExperimentalEnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="c86e1-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="c86e1-114">Ses</span><span class="sxs-lookup"><span data-stu-id="c86e1-114">Members</span></span>

#### <span data-ttu-id="c86e1-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="c86e1-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="c86e1-116">La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.</span><span class="sxs-lookup"><span data-stu-id="c86e1-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="c86e1-117">[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)publique HRESULT (bool \* activé)</span><span class="sxs-lookup"><span data-stu-id="c86e1-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c86e1-118">La valeur par défaut est Disabled.</span><span class="sxs-lookup"><span data-stu-id="c86e1-118">Default is disabled.</span></span> <span data-ttu-id="c86e1-119">Les applications de plateforme Windows universelle doivent également déclarer la [fonctionnalité restreinte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO pour que l’authentification unique fonctionne.</span><span class="sxs-lookup"><span data-stu-id="c86e1-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="c86e1-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="c86e1-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="c86e1-121">Définissez la propriété IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="c86e1-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="c86e1-122">[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)publiques HRESULT</span><span class="sxs-lookup"><span data-stu-id="c86e1-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>

