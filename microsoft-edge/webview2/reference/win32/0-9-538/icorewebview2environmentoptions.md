---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 3de9cd454f693179a0d1dc63e6ccb1332f80c875
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698638"
---
# <span data-ttu-id="b1323-104">interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="b1323-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="b1323-105">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="b1323-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="b1323-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b1323-106">Summary</span></span>

 <span data-ttu-id="b1323-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b1323-107">Members</span></span>                        | <span data-ttu-id="b1323-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b1323-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1323-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b1323-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="b1323-110">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="b1323-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="b1323-111">get_Language</span><span class="sxs-lookup"><span data-stu-id="b1323-111">get_Language</span></span>](#get_language) | <span data-ttu-id="b1323-112">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="b1323-112">The default language that WebView will run with.</span></span>
[<span data-ttu-id="b1323-113">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b1323-113">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="b1323-114">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b1323-114">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="b1323-115">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b1323-115">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="b1323-116">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="b1323-116">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="b1323-117">put_Language</span><span class="sxs-lookup"><span data-stu-id="b1323-117">put_Language</span></span>](#put_language) | <span data-ttu-id="b1323-118">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="b1323-118">Set the Language property.</span></span>
[<span data-ttu-id="b1323-119">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b1323-119">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="b1323-120">Définissez TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b1323-120">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="b1323-121">Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="b1323-121">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="b1323-122">Ses</span><span class="sxs-lookup"><span data-stu-id="b1323-122">Members</span></span>

#### <span data-ttu-id="b1323-123">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b1323-123">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b1323-124">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="b1323-124">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="b1323-125">valeur publique HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="b1323-125">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="b1323-126">Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b1323-126">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="b1323-127">Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="b1323-127">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="b1323-128">Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur.</span><span class="sxs-lookup"><span data-stu-id="b1323-128">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="b1323-129">Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="b1323-129">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="b1323-130">Ces commutateurs seront ignorés même en cas de spécification.</span><span class="sxs-lookup"><span data-stu-id="b1323-130">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="b1323-131">Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne.</span><span class="sxs-lookup"><span data-stu-id="b1323-131">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="b1323-132">Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé.</span><span class="sxs-lookup"><span data-stu-id="b1323-132">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="b1323-133">Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées.</span><span class="sxs-lookup"><span data-stu-id="b1323-133">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="b1323-134">La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="b1323-134">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="b1323-135">Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées.</span><span class="sxs-lookup"><span data-stu-id="b1323-135">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="b1323-136">Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="b1323-136">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="b1323-137">Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b1323-137">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="b1323-138">get_Language</span><span class="sxs-lookup"><span data-stu-id="b1323-138">get_Language</span></span> 

<span data-ttu-id="b1323-139">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="b1323-139">The default language that WebView will run with.</span></span>

> <span data-ttu-id="b1323-140">valeur publique HRESULT [get_Language](#get_language)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="b1323-140">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="b1323-141">Il s’applique aux interfaces utilisateur du navigateur comme le menu contextuel et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b1323-141">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="b1323-142">Il s’applique également à l’en-tête HTTP Accept-Language que le WebView envoie aux sites Web.</span><span class="sxs-lookup"><span data-stu-id="b1323-142">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="b1323-143">La mise en forme est de l' `language[-country]` endroit où `language` se trouve le code à deux lettres ISO 639 et `country` correspond au code 2 lettres de l’ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="b1323-143">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="b1323-144">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b1323-144">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b1323-145">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b1323-145">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="b1323-146">valeur publique HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="b1323-146">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="b1323-147">Par défaut, il s’agit de la version latérale du runtime WebView2 qui correspond à la version du SDK utilisée par l’application.</span><span class="sxs-lookup"><span data-stu-id="b1323-147">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="b1323-148">Le format de cette valeur est identique à celui de la propriété BrowserVersionString et des autres valeurs BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b1323-148">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="b1323-149">Seule la partie version de la valeur BrowserVersion est respectée.</span><span class="sxs-lookup"><span data-stu-id="b1323-149">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="b1323-150">Le suffixe de canal, s’il existe, est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b1323-150">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="b1323-151">La version des fichiers binaires Edge WebView2 Runtime utilisés est susceptible d’être différente de la TargetCompatibleBrowserVersion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1323-151">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="b1323-152">Ils sont uniquement compatibles.</span><span class="sxs-lookup"><span data-stu-id="b1323-152">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="b1323-153">Vous pouvez vérifier la version réelle sur la propriété BrowserVersionString sur ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="b1323-153">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="b1323-154">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b1323-154">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b1323-155">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="b1323-155">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="b1323-156">valeur publique HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b1323-156">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b1323-157">put_Language</span><span class="sxs-lookup"><span data-stu-id="b1323-157">put_Language</span></span> 

<span data-ttu-id="b1323-158">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="b1323-158">Set the Language property.</span></span>

> <span data-ttu-id="b1323-159">valeur publique HRESULT [put_Language](#put_language)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b1323-159">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b1323-160">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b1323-160">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b1323-161">Définissez TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b1323-161">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="b1323-162">valeur publique HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b1323-162">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

