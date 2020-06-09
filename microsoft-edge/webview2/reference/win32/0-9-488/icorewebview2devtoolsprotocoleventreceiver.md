---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 760919ba215f725cac10ad03d278d0a3e994286e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698056"
---
# <span data-ttu-id="f41dd-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="f41dd-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

> [!NOTE]
> <span data-ttu-id="f41dd-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f41dd-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f41dd-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f41dd-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="f41dd-107">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="f41dd-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="f41dd-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f41dd-108">Summary</span></span>

 <span data-ttu-id="f41dd-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f41dd-109">Members</span></span>                        | <span data-ttu-id="f41dd-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f41dd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f41dd-111">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f41dd-111">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="f41dd-112">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f41dd-112">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="f41dd-113">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f41dd-113">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="f41dd-114">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="f41dd-114">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="f41dd-115">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="f41dd-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="f41dd-116">Ses</span><span class="sxs-lookup"><span data-stu-id="f41dd-116">Members</span></span>

#### <span data-ttu-id="f41dd-117">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f41dd-117">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="f41dd-118">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="f41dd-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="f41dd-119">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)par le biais[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f41dd-119">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f41dd-120">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="f41dd-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="f41dd-121">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="f41dd-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="f41dd-122">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="f41dd-122">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="f41dd-123">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="f41dd-123">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="f41dd-124">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f41dd-124">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

