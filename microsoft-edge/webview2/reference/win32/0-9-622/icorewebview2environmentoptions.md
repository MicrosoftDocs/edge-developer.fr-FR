---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011983"
---
# <span data-ttu-id="db494-104">interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="db494-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="db494-105">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="db494-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="db494-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="db494-106">Summary</span></span>

 <span data-ttu-id="db494-107">Ses</span><span class="sxs-lookup"><span data-stu-id="db494-107">Members</span></span>                        | <span data-ttu-id="db494-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="db494-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="db494-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="db494-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="db494-110">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="db494-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="db494-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="db494-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#get_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="db494-112">La propriété AllowSingleSignOnUsingOSPrimaryAccount est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.</span><span class="sxs-lookup"><span data-stu-id="db494-112">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="db494-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="db494-113">get_Language</span></span>](#get_language) | <span data-ttu-id="db494-114">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="db494-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="db494-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="db494-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="db494-116">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="db494-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="db494-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="db494-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="db494-118">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="db494-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="db494-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="db494-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#put_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="db494-120">Définissez la propriété AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="db494-120">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>
[<span data-ttu-id="db494-121">put_Language</span><span class="sxs-lookup"><span data-stu-id="db494-121">put_Language</span></span>](#put_language) | <span data-ttu-id="db494-122">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="db494-122">Set the Language property.</span></span>
[<span data-ttu-id="db494-123">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="db494-123">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="db494-124">Définissez la propriété TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="db494-124">Set the TargetCompatibleBrowserVersion property.</span></span>

<span data-ttu-id="db494-125">Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="db494-125">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="db494-126">Ses</span><span class="sxs-lookup"><span data-stu-id="db494-126">Members</span></span>

#### <span data-ttu-id="db494-127">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="db494-127">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="db494-128">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="db494-128">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="db494-129">valeur publique HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="db494-129">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="db494-130">Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="db494-130">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="db494-131">Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="db494-131">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="db494-132">Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur.</span><span class="sxs-lookup"><span data-stu-id="db494-132">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="db494-133">Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="db494-133">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="db494-134">Ces commutateurs seront ignorés même en cas de spécification.</span><span class="sxs-lookup"><span data-stu-id="db494-134">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="db494-135">Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne.</span><span class="sxs-lookup"><span data-stu-id="db494-135">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="db494-136">Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé.</span><span class="sxs-lookup"><span data-stu-id="db494-136">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="db494-137">Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées.</span><span class="sxs-lookup"><span data-stu-id="db494-137">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="db494-138">La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="db494-138">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="db494-139">Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées.</span><span class="sxs-lookup"><span data-stu-id="db494-139">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="db494-140">Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="db494-140">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="db494-141">Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="db494-141">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="db494-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="db494-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="db494-143">La propriété AllowSingleSignOnUsingOSPrimaryAccount est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.</span><span class="sxs-lookup"><span data-stu-id="db494-143">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="db494-144">[get_AllowSingleSignOnUsingOSPrimaryAccounts](#get_allowsinglesignonusingosprimaryaccount)par l’autorisation public HRESULT</span><span class="sxs-lookup"><span data-stu-id="db494-144">public HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(BOOL \* allow)</span></span>

<span data-ttu-id="db494-145">La valeur par défaut est Disabled.</span><span class="sxs-lookup"><span data-stu-id="db494-145">Default is disabled.</span></span> <span data-ttu-id="db494-146">Les applications de plateforme Windows universelle doivent également déclarer la [fonctionnalité restreinte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO pour que l’authentification unique fonctionne.</span><span class="sxs-lookup"><span data-stu-id="db494-146">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="db494-147">get_Language</span><span class="sxs-lookup"><span data-stu-id="db494-147">get_Language</span></span> 

<span data-ttu-id="db494-148">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="db494-148">The default language that WebView will run with.</span></span>

> <span data-ttu-id="db494-149">valeur publique HRESULT [get_Language](#get_language)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="db494-149">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="db494-150">Il s’applique aux interfaces utilisateur du navigateur comme le menu contextuel et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="db494-150">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="db494-151">Il s’applique également à l’en-tête HTTP Accept-Language que le WebView envoie aux sites Web.</span><span class="sxs-lookup"><span data-stu-id="db494-151">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="db494-152">La mise en forme est de l' `language[-country]` endroit où `language` se trouve le code à deux lettres ISO 639 et `country` correspond au code 2 lettres de l’ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="db494-152">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="db494-153">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="db494-153">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="db494-154">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="db494-154">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="db494-155">valeur publique HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span><span class="sxs-lookup"><span data-stu-id="db494-155">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="db494-156">Par défaut, il s’agit de la version latérale du runtime WebView2 qui correspond à la version du SDK utilisée par l’application.</span><span class="sxs-lookup"><span data-stu-id="db494-156">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="db494-157">Le format de cette valeur est identique à celui de la propriété BrowserVersionString et des autres valeurs BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="db494-157">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="db494-158">Seule la partie version de la valeur BrowserVersion est respectée.</span><span class="sxs-lookup"><span data-stu-id="db494-158">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="db494-159">Le suffixe de canal, s’il existe, est ignoré.</span><span class="sxs-lookup"><span data-stu-id="db494-159">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="db494-160">La version des fichiers binaires Edge WebView2 Runtime utilisés est susceptible d’être différente de la TargetCompatibleBrowserVersion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="db494-160">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="db494-161">Ils sont uniquement compatibles.</span><span class="sxs-lookup"><span data-stu-id="db494-161">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="db494-162">Vous pouvez vérifier la version réelle sur la propriété BrowserVersionString sur ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="db494-162">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="db494-163">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="db494-163">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="db494-164">Définissez la propriété AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="db494-164">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="db494-165">valeur publique HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="db494-165">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="db494-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="db494-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="db494-167">Définissez la propriété AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="db494-167">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>

> <span data-ttu-id="db494-168">[put_AllowSingleSignOnUsingOSPrimaryAccounts](#put_allowsinglesignonusingosprimaryaccount)par l’autorisation public HRESULT</span><span class="sxs-lookup"><span data-stu-id="db494-168">public HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(BOOL allow)</span></span>

#### <span data-ttu-id="db494-169">put_Language</span><span class="sxs-lookup"><span data-stu-id="db494-169">put_Language</span></span> 

<span data-ttu-id="db494-170">Définissez la propriété Language.</span><span class="sxs-lookup"><span data-stu-id="db494-170">Set the Language property.</span></span>

> <span data-ttu-id="db494-171">valeur publique HRESULT [put_Language](#put_language)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="db494-171">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="db494-172">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="db494-172">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="db494-173">Définissez la propriété TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="db494-173">Set the TargetCompatibleBrowserVersion property.</span></span>

> <span data-ttu-id="db494-174">valeur publique HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valeur LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="db494-174">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

