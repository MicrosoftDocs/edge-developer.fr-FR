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
ms.openlocfilehash: c83123876747cb085efd65ff013db87a501b189c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653524"
---
# <span data-ttu-id="7168c-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="7168c-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="7168c-105">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner à cet événement et de vous désabonner.</span><span class="sxs-lookup"><span data-stu-id="7168c-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="7168c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7168c-106">Summary</span></span>

 <span data-ttu-id="7168c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7168c-107">Members</span></span>                        | <span data-ttu-id="7168c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7168c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7168c-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7168c-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="7168c-110">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7168c-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="7168c-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7168c-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="7168c-112">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7168c-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="7168c-113">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="7168c-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="7168c-114">Ses</span><span class="sxs-lookup"><span data-stu-id="7168c-114">Members</span></span>

#### <span data-ttu-id="7168c-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7168c-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7168c-116">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7168c-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="7168c-117">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)par le biais[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="7168c-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7168c-118">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="7168c-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="7168c-119">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="7168c-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="7168c-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7168c-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7168c-121">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7168c-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="7168c-122">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="7168c-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

