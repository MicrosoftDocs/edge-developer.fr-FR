---
description: Apprenez à développer des applications WebView2 sécurisées
title: Recommandations en matière de développement d’applications WebView2 sécurisées
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, sécurité
ms.openlocfilehash: f30163954f1906f71afa520b87d58c7647a5250a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894304"
---
# <span data-ttu-id="12ed6-104">Recommandations en matière de développement d’applications WebView2 sécurisées</span><span class="sxs-lookup"><span data-stu-id="12ed6-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="12ed6-105">Le [contrôle WebView2][Webview2Main] permet aux développeurs d’héberger du contenu Web dans les applications natives.</span><span class="sxs-lookup"><span data-stu-id="12ed6-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="12ed6-106">En cas d’utilisation correcte, le contenu Web d’hébergement offre plusieurs avantages, comme l’utilisation de l’interface utilisateur Web, l’accès aux fonctionnalités de la plateforme Web, le partage de code multiplateforme, etc.</span><span class="sxs-lookup"><span data-stu-id="12ed6-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="12ed6-107">Pour éviter toute vulnérabilité pouvant découler de l’hébergement de contenu Web, veillez à concevoir votre application WebView2 pour surveiller étroitement les interactions entre le contenu Web et l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="12ed6-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="12ed6-108">Considérer tout le contenu Web comme non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="12ed6-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="12ed6-109">Validez les messages Web et les paramètres d’objet de l’hôte avant d’utiliser chacun d’eux, car les messages et les paramètres Web peuvent être incorrects (ou involontairement) et provoquer une inadvertance du comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="12ed6-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="12ed6-110">Vérifiez toujours l’origine du document exécuté dans WebView2 et évaluez la fiabilité du contenu.</span><span class="sxs-lookup"><span data-stu-id="12ed6-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="12ed6-111">Concevez des messages Web et des interactions d’objets hôtes spécifiques au lieu d’utiliser des proxys génériques.</span><span class="sxs-lookup"><span data-stu-id="12ed6-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="12ed6-112">Définissez les options suivantes pour limiter les fonctionnalités de contenu Web en modifiant [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span><span class="sxs-lookup"><span data-stu-id="12ed6-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="12ed6-113">Définissez `AreHostObjectsAllowed` la valeur sur `false` , si vous ne pensez pas que le contenu Web accède aux objets hôtes.</span><span class="sxs-lookup"><span data-stu-id="12ed6-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="12ed6-114">Définissez `IsWebMessageEnabled` la valeur sur `false` , si vous ne souhaitez pas que le contenu Web publie des messages Web dans votre application native.</span><span class="sxs-lookup"><span data-stu-id="12ed6-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="12ed6-115">Définissez `IsScriptEnabled` sur `false` , si vous ne pensez pas que le contenu Web doit exécuter des scripts (par exemple, lors de l’affichage d’un contenu HTML statique).</span><span class="sxs-lookup"><span data-stu-id="12ed6-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="12ed6-116">Définissez `AreDefaultScriptDialogsEnabled` sur `false` , si vous ne souhaitez pas que le contenu Web s’affiche ou ne s’affiche pas `alert` `prompt` .</span><span class="sxs-lookup"><span data-stu-id="12ed6-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="12ed6-117">Dans les étapes suivantes, utilisez les `NavigationStarting` `FrameNavigationStarting` événements et pour mettre à jour les paramètres en fonction de l’origine de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="12ed6-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="12ed6-118">Pour empêcher votre application de naviguer vers certaines pages, utilisez les événements pour vérifier et bloquer la navigation de la page ou du frame.</span><span class="sxs-lookup"><span data-stu-id="12ed6-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="12ed6-119">Lorsque vous naviguez vers une nouvelle page, il est possible que vous deviez ajuster les valeurs de propriétés sur [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] , comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="12ed6-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="12ed6-120">Lorsque vous naviguez vers un nouveau document, utilisez l' `ContentLoading` événement pour supprimer les objets hôtes exposés à l’aide de `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="12ed6-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[Webview2ReferenceWin3209538Icorewebview2settings]: ../reference/win32/0-9-538/icorewebview2settings.md "interface ICoreWebView2Settings | Documents Microsoft"  

[Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings | Documents Microsoft"  
