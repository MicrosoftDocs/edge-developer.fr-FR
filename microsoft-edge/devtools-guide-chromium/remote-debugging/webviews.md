---
description: Commencer à déboguer à distance les webViews dans vos applications Android natives à l’aide Microsoft Edge outils de développement.
title: Prise en main du débogage à distance d’Android WebViews
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 75d948465c62c63c9ccbe0fcd46616819a04e79d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565077"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-remote-debugging-android-webviews"></a><span data-ttu-id="0b249-104">Prise en main du débogage à distance d’Android WebViews</span><span class="sxs-lookup"><span data-stu-id="0b249-104">Get started with remote debugging Android WebViews</span></span>  

<span data-ttu-id="0b249-105">Déboguer des webViews Android dans vos applications Android natives à l’aide Microsoft Edge outils de développement.</span><span class="sxs-lookup"><span data-stu-id="0b249-105">Debug Android WebViews in your native Android apps using Microsoft Edge Developer Tools.</span></span>  

<span data-ttu-id="0b249-106">Sur Android 4.4 \(KitKat\) ou version ultérieure, utilisez DevTools pour déboguer le contenu WebView dans les applications Android natives.</span><span class="sxs-lookup"><span data-stu-id="0b249-106">On Android 4.4 \(KitKat\) or later, use DevTools to debug WebView content in native Android apps.</span></span>  

### <a name="summary"></a><span data-ttu-id="0b249-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="0b249-107">Summary</span></span>  

*   <span data-ttu-id="0b249-108">Activer le débogage Android WebView dans votre application Android native ; déboguer android WebViews dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0b249-108">Turn on Android WebView debugging in your native Android app; debug Android WebViews in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="0b249-109">Pour afficher la liste des webViews Android avec débogage désactivé, accédez à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="0b249-109">To display the list of the Android WebViews with debugging turned on, navigate to `edge://inspect`.</span></span>  
*   <span data-ttu-id="0b249-110">Déboguer android WebViews de la même façon que vous déboguer une page web via le [débogage à distance.][RemoteDebuggingGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="0b249-110">Debug Android WebViews in the same way you debug a webpage through [remote debugging][RemoteDebuggingGettingStarted].</span></span>  

## <a name="configure-android-webviews-to-debug"></a><span data-ttu-id="0b249-111">Configurer android WebViews pour le débogage</span><span class="sxs-lookup"><span data-stu-id="0b249-111">Configure Android WebViews to debug</span></span>  

<span data-ttu-id="0b249-112">Le débogage WebView Android doit être allumé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="0b249-112">Android WebView debugging must be turned on within your app.</span></span>  <span data-ttu-id="0b249-113">Pour activer le débogage Android WebView, exécutez la méthode [statique setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] sur la `WebView` classe.</span><span class="sxs-lookup"><span data-stu-id="0b249-113">To turn on Android WebView debugging, run the [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] static method on the `WebView` class.</span></span>  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

<span data-ttu-id="0b249-114">Le paramètre s’applique à tous les webView Android de l’application.</span><span class="sxs-lookup"><span data-stu-id="0b249-114">The setting applies to all of the Android WebViews of the app.</span></span>  

> [!TIP]
> <span data-ttu-id="0b249-115">Le débogage Android WebView n’est pas affecté par l’état de `debuggable` l’indicateur dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="0b249-115">Android WebView debugging is not affected by the state of the `debuggable` flag in the manifest of the app.</span></span>  <span data-ttu-id="0b249-116">Si vous souhaitez activer le débogage Android WebView uniquement lorsque l’indicateur est , testez l’indicateur lors de `debuggable` `true` l’runtime.</span><span class="sxs-lookup"><span data-stu-id="0b249-116">If you want to turn on Android WebView debugging only when the `debuggable` flag is `true`, test the flag at runtime.</span></span>  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a><span data-ttu-id="0b249-117">Ouvrir un android WebView dans DevTools</span><span class="sxs-lookup"><span data-stu-id="0b249-117">Open an Android WebView in DevTools</span></span>  

<span data-ttu-id="0b249-118">Pour afficher la liste des webViews Android avec débogage qui s’exécutent sur votre appareil, accédez à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="0b249-118">To display a list of the Android WebViews with debugging turned on that run on your device, navigate to `edge://inspect`.</span></span>  

<span data-ttu-id="0b249-119">Pour commencer le débogage, sous Android WebView que vous souhaitez déboguer, choisissez **inspect**.</span><span class="sxs-lookup"><span data-stu-id="0b249-119">To start debugging, under the Android WebView you want to debug, choose **inspect**.</span></span>  <span data-ttu-id="0b249-120">Utilisez DevTools de la même manière que pour un onglet de navigateur distant.</span><span class="sxs-lookup"><span data-stu-id="0b249-120">Use DevTools in the same way that you do a remote browser tab.</span></span>  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a><span data-ttu-id="0b249-121">Résoudre les problèmes</span><span class="sxs-lookup"><span data-stu-id="0b249-121">Troubleshoot</span></span>  

<span data-ttu-id="0b249-122">Vos WebView Android ne sont pas affichés sur la `edge://inspect` page ?</span><span class="sxs-lookup"><span data-stu-id="0b249-122">Your Android WebViews aren't displayed on the `edge://inspect` page?</span></span>  

*   <span data-ttu-id="0b249-123">Vérifiez que le débogage Android WebView est allumé pour votre application.</span><span class="sxs-lookup"><span data-stu-id="0b249-123">Verify that Android WebView debugging is turned on for your app.</span></span>  
*   <span data-ttu-id="0b249-124">Sur votre appareil, ouvrez l’application avec android WebView que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="0b249-124">On your device, open the app with the Android WebView you want to debug.</span></span>  <span data-ttu-id="0b249-125">Ensuite, actualisez `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="0b249-125">Then, refresh `edge://inspect`.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0b249-126">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0b249-126">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Prise en main avec les appareils Android de débogage à distance | Documents Microsoft"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled - WebView | Développeurs Android"  

> [!NOTE]
> <span data-ttu-id="0b249-129">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0b249-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0b249-130">La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="0b249-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="0b249-132">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0b249-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
