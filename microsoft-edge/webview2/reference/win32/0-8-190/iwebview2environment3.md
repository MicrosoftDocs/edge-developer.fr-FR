---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886093"
---
# 0.8.355-interface IWebView2Environment3 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

Fonctionnalités supplémentaires implémentées par l’objet Environment.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_NewVersionAvailable](#add_newversionavailable) | L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.
[remove_NewVersionAvailable](#remove_newversionavailable) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.

Pour plus d’informations, consultez l’interface [IWebView2Environment](IWebView2Environment.md) . Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2Environment](IWebView2Environment.md).

## Ses

#### add_NewVersionAvailable 

L’événement NewVersionAvailable se déclenche lors de l’installation d’une nouvelle version du navigateur Edge et peut être utilisée via WebView2.

> [add_NewVersionAvailable](#add_newversionavailable)par le biais du[mot de passe](IWebView2NewVersionAvailableEventHandler.md)

Pour utiliser la version la plus récente du navigateur, vous devez créer un nouveau [IWebView2Environment](IWebView2Environment.md) et [IWebView2WebView](IWebView2WebView.md). L’événement est déclenché uniquement pour la nouvelle version à partir du canal de périphérie d’exécution du code. S’il n’est pas exécuté avec des bords installés, aucun événement n’est déclenché.

Dans la mesure où un dossier de données utilisateur ne peut être utilisé que par un seul processus de navigateur à la fois, si vous souhaitez utiliser le même dossier de données utilisateur dans les webaffichages à l’aide de la nouvelle version du navigateur, vous devez d’abord fermer le [IWebView2Environment](IWebView2Environment.md) et IWebView2WebViews qui utilisent l’ancienne version du navigateur. Vous pouvez également demander à l’utilisateur de redémarrer l’application.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewVersionAvailable 

Supprimez un gestionnaire d’événements préalablement ajouté à add_NewVersionAvailable.

> [remove_NewVersionAvailable](#remove_newversionavailable)par le biais du mot-clé public HRESULT

