---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1cac030b27164222bd1c11240cf4a92aee91ff01
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880674"
---
# <span data-ttu-id="d2bd3-104">0.9.515-interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="d2bd3-104">0.9.515 - interface ICoreWebView2EnvironmentOptions</span></span> 

> [!NOTE]
> <span data-ttu-id="d2bd3-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d2bd3-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="d2bd3-107">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="d2bd3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d2bd3-108">Summary</span></span>

 <span data-ttu-id="d2bd3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d2bd3-109">Members</span></span>                        | <span data-ttu-id="d2bd3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d2bd3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2bd3-111">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="d2bd3-111">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="d2bd3-112">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="d2bd3-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="d2bd3-113">get_Language</span></span>](#get_language) | <span data-ttu-id="d2bd3-114">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="d2bd3-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="d2bd3-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="d2bd3-116">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="d2bd3-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="d2bd3-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="d2bd3-118">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="d2bd3-119">put_Language</span><span class="sxs-lookup"><span data-stu-id="d2bd3-119">put_Language</span></span>](#put_language) | <span data-ttu-id="d2bd3-120">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-120">Set the Language property.</span></span>
[<span data-ttu-id="d2bd3-121">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="d2bd3-121">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="d2bd3-122">Définissez TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-122">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="d2bd3-123">Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-123">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="d2bd3-124">Ses</span><span class="sxs-lookup"><span data-stu-id="d2bd3-124">Members</span></span>

#### <span data-ttu-id="d2bd3-125">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="d2bd3-125">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="d2bd3-126">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-126">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="d2bd3-127">valeur publique HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-127">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="d2bd3-128">Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-128">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="d2bd3-129">Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="d2bd3-129">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="d2bd3-130">Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-130">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="d2bd3-131">Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-131">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="d2bd3-132">Ces commutateurs seront ignorés même en cas de spécification.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-132">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="d2bd3-133">Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-133">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="d2bd3-134">Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-134">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="d2bd3-135">Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-135">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="d2bd3-136">La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-136">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="d2bd3-137">Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-137">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="d2bd3-138">Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-138">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="d2bd3-139">Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-139">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="d2bd3-140">get_Language</span><span class="sxs-lookup"><span data-stu-id="d2bd3-140">get_Language</span></span> 

<span data-ttu-id="d2bd3-141">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-141">The default language that WebView will run with.</span></span>

> <span data-ttu-id="d2bd3-142">valeur publique HRESULT [get_Language](#get_language)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-142">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="d2bd3-143">Il s’applique aux interfaces utilisateur du navigateur comme le menu contextuel et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-143">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="d2bd3-144">Il s’applique également à l’en-tête HTTP Accept-Language que le WebView envoie aux sites Web.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-144">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="d2bd3-145">La mise en forme est de l' `language[-country]` endroit où `language` se trouve le code à deux lettres ISO 639 et `country` correspond au code 2 lettres de l’ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-145">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="d2bd3-146">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="d2bd3-146">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="d2bd3-147">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-147">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="d2bd3-148">valeur publique HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-148">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="d2bd3-149">Par défaut, il s’agit de la version latérale du runtime WebView2 qui correspond à la version du SDK utilisée par l’application.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-149">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="d2bd3-150">Le format de cette valeur est identique à celui de la propriété BrowserVersionString et des autres valeurs BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-150">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="d2bd3-151">Seule la partie version de la valeur BrowserVersion est respectée.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-151">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="d2bd3-152">Le suffixe de canal, s’il existe, est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-152">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="d2bd3-153">La version des fichiers binaires Edge WebView2 Runtime utilisés est susceptible d’être différente de la TargetCompatibleBrowserVersion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-153">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="d2bd3-154">Ils sont uniquement compatibles.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-154">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="d2bd3-155">Vous pouvez vérifier la version réelle sur la propriété BrowserVersionString sur ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-155">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="d2bd3-156">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="d2bd3-156">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="d2bd3-157">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-157">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="d2bd3-158">valeur publique HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-158">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="d2bd3-159">put_Language</span><span class="sxs-lookup"><span data-stu-id="d2bd3-159">put_Language</span></span> 

<span data-ttu-id="d2bd3-160">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-160">Set the Language property.</span></span>

> <span data-ttu-id="d2bd3-161">valeur publique HRESULT [put_Language](#put_language)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-161">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="d2bd3-162">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="d2bd3-162">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="d2bd3-163">Définissez TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="d2bd3-163">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="d2bd3-164">valeur publique HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d2bd3-164">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

