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
# 0.9.579-interface ICoreWebView2ExperimentalEnvironmentOptions 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

Options expérimentales utilisées pour créer un environnement WebView2.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled) | La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.
[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled) | Définissez la propriété IsSingleSignOnUsingOSPrimaryAccountEnabled.

Une implémentation par défaut est fournie dans WebView2ExperimentalEnvironmentOptions. h.

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

## Ses

#### get_IsSingleSignOnUsingOSPrimaryAccountEnabled 

La propriété IsSingleSignOnUsingOSPrimaryAccountEnabled est utilisée pour activer l’authentification unique à l’aide d’Azure Active Directory (AAD) via le contrôle WebView en utilisant le compte Windows connecté et l’authentification unique avec les sites Web utilisant le compte Microsoft associé au compte de connexion dans le compte Windows.

> [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)publique HRESULT (bool * activé)

La valeur par défaut est Disabled. Les applications de plateforme Windows universelle doivent également déclarer la [fonctionnalité restreinte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO pour que l’authentification unique fonctionne.

#### put_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Définissez la propriété IsSingleSignOnUsingOSPrimaryAccountEnabled.

> [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)publiques HRESULT

