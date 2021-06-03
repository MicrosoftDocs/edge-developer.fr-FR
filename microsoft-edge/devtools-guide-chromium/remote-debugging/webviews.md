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
# <a name="get-started-with-remote-debugging-android-webviews"></a>Prise en main du débogage à distance d’Android WebViews  

Déboguer des webViews Android dans vos applications Android natives à l’aide Microsoft Edge outils de développement.  

Sur Android 4.4 \(KitKat\) ou version ultérieure, utilisez DevTools pour déboguer le contenu WebView dans les applications Android natives.  

### <a name="summary"></a>Résumé  

*   Activer le débogage Android WebView dans votre application Android native ; déboguer android WebViews dans Microsoft Edge DevTools.  
*   Pour afficher la liste des webViews Android avec débogage désactivé, accédez à `edge://inspect` .  
*   Déboguer android WebViews de la même façon que vous déboguer une page web via le [débogage à distance][RemoteDebuggingGettingStarted].  

## <a name="configure-android-webviews-to-debug"></a>Configurer android WebViews pour le débogage  

Le débogage WebView Android doit être allumé dans votre application.  Pour activer le débogage Android WebView, exécutez la méthode [statique setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] sur la `WebView` classe.  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

Le paramètre s’applique à tous les webView Android de l’application.  

> [!TIP]
> Le débogage WebView Android n’est pas affecté par l’état de `debuggable` l’indicateur dans le manifeste de l’application.  Si vous souhaitez activer le débogage Android WebView uniquement lorsque l’indicateur est , testez l’indicateur lors de `debuggable` `true` l’runtime.  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a>Ouvrir un android WebView dans DevTools  

Pour afficher la liste des webViews Android avec débogage qui s’exécutent sur votre appareil, accédez à `edge://inspect` .  

Pour commencer le débogage, sous Android WebView que vous souhaitez déboguer, choisissez **inspect**.  Utilisez DevTools de la même manière que pour un onglet de navigateur distant.  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a>Résoudre les problèmes  

Vos WebView Android ne sont pas affichés sur la `edge://inspect` page ?  

*   Vérifiez que le débogage Android WebView est allumé pour votre application.  
*   Sur votre appareil, ouvrez l’application avec android WebView que vous souhaitez déboguer.  Ensuite, actualisez `edge://inspect` .  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Prise en main avec les appareils Android de débogage à distance | Documents Microsoft"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled - WebView | Développeurs Android"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
