---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 4c2c859525753a386134b2ae0145f4fdca4c37ae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653331"
---
# <span data-ttu-id="c9102-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="c9102-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

> [!NOTE]
> <span data-ttu-id="c9102-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c9102-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c9102-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c9102-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="c9102-107">Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner et de unsubsribe à partir de cet événement.</span><span class="sxs-lookup"><span data-stu-id="c9102-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubsribe from that event.</span></span>

## <span data-ttu-id="c9102-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c9102-108">Summary</span></span>

 <span data-ttu-id="c9102-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c9102-109">Members</span></span>                        | <span data-ttu-id="c9102-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c9102-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9102-111">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c9102-111">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="c9102-112">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="c9102-112">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="c9102-113">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c9102-113">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="c9102-114">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="c9102-114">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="c9102-115">Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="c9102-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="c9102-116">Ses</span><span class="sxs-lookup"><span data-stu-id="c9102-116">Members</span></span>

#### <span data-ttu-id="c9102-117">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c9102-117">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="c9102-118">S’abonner à un événement DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="c9102-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="c9102-119">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)par le biais[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c9102-119">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="c9102-120">La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché.</span><span class="sxs-lookup"><span data-stu-id="c9102-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="c9102-121">Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="c9102-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="c9102-122">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c9102-122">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="c9102-123">Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="c9102-123">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="c9102-124">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c9102-124">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

