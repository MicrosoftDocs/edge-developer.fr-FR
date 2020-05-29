---
description: 'Découvrez comment cibler les différents moteurs JavaScript Windows 10. '
title: Ciblage du moteur Microsoft Edge et des moteurs hérités dans les API JsRT Documents Microsoft
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565118"
---
# <span data-ttu-id="ebb51-103">Ciblage du moteur Microsoft Edge et des moteurs hérités dans les API JsRT</span><span class="sxs-lookup"><span data-stu-id="ebb51-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT APIs</span></span>

<span data-ttu-id="ebb51-104">Windows 10 prend en charge deux moteurs JavaScript différents:</span><span class="sxs-lookup"><span data-stu-id="ebb51-104">Windows 10 supports two different JavaScript engines:</span></span>

-   <span data-ttu-id="ebb51-105">L’ancien moteur Chakra (également appelé *moteur hérité* ou jscript9. dll ci-dessous) qui est fourni avec et prend en charge Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="ebb51-105">The old Chakra engine (also called the *legacy engine* or jscript9.dll below) that ships with and supports Internet Explorer 11.</span></span> <span data-ttu-id="ebb51-106">Ce moteur est figé en temps et reste fondamentalement modifié de Win 8.1/IE11 version.</span><span class="sxs-lookup"><span data-stu-id="ebb51-106">This engine is frozen in time and will remain fundamentally unchanged from Win8.1/IE11 release.</span></span>  
  
-   <span data-ttu-id="ebb51-107">Le nouveau moteur Chakra (également appelé *moteur Edge* ou Chakra. dll ci-dessous) qui est fourni avec et prend en charge le nouveau navigateur dans Windows 10 et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ebb51-107">The new Chakra engine (also called the *Edge engine* or chakra.dll below) that ships with and supports the new browser in Windows 10, Microsoft Edge.</span></span> <span data-ttu-id="ebb51-108">Ce moteur sera mis à jour en permanence et sera pris en charge par le moteur [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) «vivre».</span><span class="sxs-lookup"><span data-stu-id="ebb51-108">This engine will be continually updated and will support a "living" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) engine.</span></span> <span data-ttu-id="ebb51-109">Dans le cas d’un moteur Microsoft Edge, il implique que le moteur Microsoft Edge ne transmettra aucune forme de fonctionnalité de script de contrôle de version à accepter.</span><span class="sxs-lookup"><span data-stu-id="ebb51-109">A living Microsoft Edge engine implies that unlike the legacy engine, the Microsoft Edge engine would not carry forward any form of versioning script functionality to opt into.</span></span>  
  
 <span data-ttu-id="ebb51-110">Lors de la création d’une application à l’aide de l’API d’hébergement Runtime JavaScript (JsRT), vous pouvez choisir de cibler le moteur hérité ou le moteur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ebb51-110">When creating an app using the JavaScript Runtime Hosting (JsRT) API, you can choose to target either the legacy or the Microsoft Edge engine.</span></span>  
  
-   <span data-ttu-id="ebb51-111">Si vous devez insister sur la compatibilité descendante de vos applications existantes, ciblez le moteur hérité.</span><span class="sxs-lookup"><span data-stu-id="ebb51-111">If you need to emphasize backward compatibility of your existing applications, target the legacy engine.</span></span>  
  
-   <span data-ttu-id="ebb51-112">Si vous voulez que votre application soit transmise à l’avenir et prenne en charge de nouvelles fonctionnalités JavaScript au fur et à mesure de leur commercialisation (par exemple, ECMAScript 6), ciblez le moteur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ebb51-112">If you want your app to be forward looking and support new JavaScript features as they are released (for example, ECMAScript 6), target the Microsoft Edge engine.</span></span>  
  
 <span data-ttu-id="ebb51-113">Cette rubrique inclut des détails qui décrivent comment cibler les différents moteurs.</span><span class="sxs-lookup"><span data-stu-id="ebb51-113">This topic includes details that describe how to target the different engines.</span></span>  
  
## <span data-ttu-id="ebb51-114">Cibler votre version préférée</span><span class="sxs-lookup"><span data-stu-id="ebb51-114">Target your preferred version</span></span>  
 <span data-ttu-id="ebb51-115">Lors de la création d’une application, vous pouvez sélectionner la version de JsRT qui prend en charge le moteur Microsoft Edge ou le moteur hérité.</span><span class="sxs-lookup"><span data-stu-id="ebb51-115">When creating an app, you can select the version of the JsRT that supports either the Microsoft Edge engine or the legacy engine.</span></span> <span data-ttu-id="ebb51-116">Vous pouvez choisir la version JsRT en fonction des recommandations ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ebb51-116">You can choose the JsRT version based on the guidelines above.</span></span> <span data-ttu-id="ebb51-117">Pour tenir compte de ces distinctions, les modifications suivantes ont été apportées aux éléments `JsCreateRuntime` `JsCreateContext` et `JsStartDebugging` .</span><span class="sxs-lookup"><span data-stu-id="ebb51-117">To accommodate these distinctions, the following changes have been made to `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging`.</span></span>  
  
 <span data-ttu-id="ebb51-118">Pour `JsCreateRuntime` :</span><span class="sxs-lookup"><span data-stu-id="ebb51-118">For `JsCreateRuntime`:</span></span>  
  
-   <span data-ttu-id="ebb51-119">Lorsque le moteur hérité est ciblé, la `JsRuntimeVersionEdge` valeur d’énumération est déconseillée et un message vous suggère d’utiliser la valeur à la `JsRuntimeVersionInternetExplorer11` place.</span><span class="sxs-lookup"><span data-stu-id="ebb51-119">When targeting the legacy engine, the `JsRuntimeVersionEdge` enumeration value is deprecated, and a message will suggest using the `JsRuntimeVersionInternetExplorer11` value instead.</span></span>  
  
-   <span data-ttu-id="ebb51-120">Lors du ciblage du moteur Microsoft Edge, le paramètre version est omis de la `JsCreateRuntime` fonction.</span><span class="sxs-lookup"><span data-stu-id="ebb51-120">When targeting the Microsoft Edge engine, the version parameter is omitted from the `JsCreateRuntime` function.</span></span>  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 <span data-ttu-id="ebb51-121">Pour `JsCreateContext` et `JsStartDebugging` :</span><span class="sxs-lookup"><span data-stu-id="ebb51-121">For `JsCreateContext` and `JsStartDebugging`:</span></span>  
  
-   <span data-ttu-id="ebb51-122">Lors du ciblage du moteur hérité, l' `IDebugApplication` interface est utilisée pour fournir vos propres méthodes de débogage à distance.</span><span class="sxs-lookup"><span data-stu-id="ebb51-122">When targeting the legacy engine, the `IDebugApplication` interface is used to supply your own non-remote debugging methods.</span></span> <span data-ttu-id="ebb51-123">À des fins de débogage, `JsCreateContext` et les `JsStartDebugging` fonctions prennent `IDebugApplication` en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebb51-123">For debugging purposes, `JsCreateContext` and `JsStartDebugging` functions take `IDebugApplication` as parameter.</span></span>  
  
-   <span data-ttu-id="ebb51-124">Lorsque le moteur Microsoft Edge est ciblé, l' `IDebugApplication` interface est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ebb51-124">When targeting the Microsoft Edge engine, the `IDebugApplication` interface is deprecated.</span></span> <span data-ttu-id="ebb51-125">Le moteur Chakra prend en charge la fonctionnalité de débogage native et de script avec le débogueur Visual Studio sans nécessiter l’implémentation de l' `IDebugApplication` utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebb51-125">The Chakra engine enables native and script debugging capability with Visual Studio debugger without requiring an implementation of `IDebugApplication` from user.</span></span> <span data-ttu-id="ebb51-126">L’interface n’est plus un paramètre pour `JsCreateContext` and `JsStartDebugging` en conséquence.</span><span class="sxs-lookup"><span data-stu-id="ebb51-126">The interface is no longer a parameter for `JsCreateContext` and `JsStartDebugging` as a result.</span></span>  
  
 <span data-ttu-id="ebb51-127">Les signatures des API précédentes du moteur hérité sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="ebb51-127">The signatures for the preceding APIs in the legacy engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 <span data-ttu-id="ebb51-128">Les signatures des API précédentes du moteur Microsoft Edge sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="ebb51-128">The signatures for the preceding APIs in the Microsoft Edge engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## <span data-ttu-id="ebb51-129">Compiler pour votre version préférée à l’aide de Visual C++</span><span class="sxs-lookup"><span data-stu-id="ebb51-129">Compile for your preferred version using Visual C++</span></span>  
 <span data-ttu-id="ebb51-130">Lors de l’utilisation de Visual C++, importez l’API JsRT en incluant l’en-tête JsRT. h et assurez-vous que JsRT. lib est inclus dans la liste des fichiers en entrée de l’éditeur de liens:</span><span class="sxs-lookup"><span data-stu-id="ebb51-130">When using Visual C++, import the JsRT API by including the jsrt.h header, and ensure that jsrt.lib is included in your linker input files list:</span></span>  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Ajout de jsrt. lib en tant que fichier d’entrée de l’éditeur de liens](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 <span data-ttu-id="ebb51-132">Si vous souhaitez cibler les fichiers binaires du moteur Microsoft Edge, vous devez définir la macro `USE_EDGEMODE_JSRT` avant d’inclure jsrt. h et au lieu de lier jsrt. lib, vous devez créer un lien vers chakrart. lib:</span><span class="sxs-lookup"><span data-stu-id="ebb51-132">If you want to target the Microsoft Edge engine binaries, you need to define the macro `USE_EDGEMODE_JSRT` before including jsrt.h, and instead of linking against jsrt.lib, you should link against chakrart.lib:</span></span>  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Ajout de chakrart. lib en tant que fichier d’entrée de l’éditeur de liens](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 <span data-ttu-id="ebb51-134">Si vous commencez à utiliser une nouvelle application, vous êtes maintenant prêt à commencer à écrire du code à l’aide de l’API JsRT.</span><span class="sxs-lookup"><span data-stu-id="ebb51-134">If you're starting with a new application, you are now ready to start writing code against the JsRT API.</span></span>  
  
## <span data-ttu-id="ebb51-135">Compiler pour votre version préférée à l’aide de .NET</span><span class="sxs-lookup"><span data-stu-id="ebb51-135">Compile for your preferred version using .NET</span></span>  
 <span data-ttu-id="ebb51-136">Si vous utilisez .NET et P/Invoke, vous devez modifier vos déclarations d’API JsRT [DllImport] pour importer Chakra. dll au lieu de jscript9. dll.</span><span class="sxs-lookup"><span data-stu-id="ebb51-136">If you're using .NET and P/Invoke, you must change your JsRT API [DllImport] declarations to import chakra.dll instead of jscript9.dll.</span></span> <span data-ttu-id="ebb51-137">Par ailleurs, vous pouvez modifier la définition de `JsCreateRuntime` pour supprimer le `JsRuntimeVersion` paramètre et la définition de `JsCreateContext` et `JsStartDebugging` pour supprimer le `IDebugApplication` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebb51-137">In addition, change the definition of `JsCreateRuntime` to remove the `JsRuntimeVersion` parameter and the definition of `JsCreateContext` and `JsStartDebugging` to remove the `IDebugApplication` parameter.</span></span>  
  
 <span data-ttu-id="ebb51-138">Pour le moteur hérité, utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="ebb51-138">For the legacy engine, use the following code.</span></span>  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 <span data-ttu-id="ebb51-139">Pour le moteur Microsoft Edge, utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="ebb51-139">For the Microsoft Edge engine, use the following code.</span></span>  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  <span data-ttu-id="ebb51-140">Si vous marshalez manuellement le pointeur de fonction (par exemple, via LoadLibrary/GetProcAddress), il est important que vous ne mélangez pas les déclarations de la méthode ou que vous ne Réequilibrez pas la pile, ce qui se traduit par un comportement inattendable, par exemple, le blocage de votre application.</span><span class="sxs-lookup"><span data-stu-id="ebb51-140">If you are manually marshaling the function pointer (such as via LoadLibrary/GetProcAddress), it is critical that you do not mix the declarations of the method, or else you will unbalance the stack, which will result in unpredictable behavior such as causing your app to crash.</span></span> <span data-ttu-id="ebb51-141">Le même problème se produit si vous effectuez une opération de recherche et remplacement globale d’instances de jscript9. dll dans votre code d’importation, car vous manquez le `version` paramètre ignoré.</span><span class="sxs-lookup"><span data-stu-id="ebb51-141">The same problem will occur if you perform a global search-and-replace of instances of jscript9.dll in your import code, because you'll miss the `version` parameter being dropped.</span></span>  
  
## <span data-ttu-id="ebb51-142">Résumé</span><span class="sxs-lookup"><span data-stu-id="ebb51-142">Summary</span></span>  
 <span data-ttu-id="ebb51-143">Dans Windows 10, les API d’hébergement du runtime JavaScript sont divisées en deux.</span><span class="sxs-lookup"><span data-stu-id="ebb51-143">In Windows 10, the JavaScript Runtime Hosting APIs are splitting into two.</span></span> <span data-ttu-id="ebb51-144">Ces API prennent désormais en charge un moteur Microsoft Edge, dont les fonctionnalités de langue seront alignées avec le moteur Microsoft Edge «vivant» dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ebb51-144">These APIs now support a "living" Microsoft Edge engine, whose language capabilities will be aligned with the "living" Microsoft Edge engine in the Microsoft Edge.</span></span> <span data-ttu-id="ebb51-145">Vous pouvez tirer parti de ces fonctionnalités à partir de vos applications de bureau ou du Windows Store afin de créer des méthodes passionnantes pour étendre votre application et exploiter les compétences Web modernes de votre base de code existante.</span><span class="sxs-lookup"><span data-stu-id="ebb51-145">You can leverage these capabilities from your desktop or Store apps to create new and exciting ways to extend your application and to leverage modern Web skills in your existing code base.</span></span> <span data-ttu-id="ebb51-146">Toutefois, étant donné qu’il existe de subtils différences entre les versions précédentes, vous devez tenir compte des points suivants lorsque vous ciblez le moteur Edge ou hérité.</span><span class="sxs-lookup"><span data-stu-id="ebb51-146">However, because there are subtle differences between previous versions, you must be aware of the following points when targeting the Edge or legacy engine.</span></span>  
  
-   <span data-ttu-id="ebb51-147">Votre application ne peut prendre en charge qu’une seule version de JsRT par processus.</span><span class="sxs-lookup"><span data-stu-id="ebb51-147">Your app can support only one version of JsRT per process.</span></span>  
  
     <span data-ttu-id="ebb51-148">Par exemple, vous ne pouvez pas créer d’exécutable du moteur Microsoft Edge, puis le runtime du moteur hérité et attendre qu’ils s’exécutent correctement dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="ebb51-148">For example, you can't create a Microsoft Edge engine runtime and then a legacy engine runtime and expect them to run correctly in the same process.</span></span> <span data-ttu-id="ebb51-149">Ceci n’est pas pris en charge et peut entraîner un comportement non documenté, par exemple l’impossibilité de charger la deuxième DLL.</span><span class="sxs-lookup"><span data-stu-id="ebb51-149">This is unsupported and may result in undocumented behavior, such as failure to load the second DLL.</span></span>  
  
-   <span data-ttu-id="ebb51-150">Dans le cadre du ciblage du moteur Microsoft Edge, votre application peut acquérir de nouvelles fonctionnalités de manière inattendue lorsque la plateforme sous-jacente est mise à jour automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ebb51-150">When targeting the Microsoft Edge engine, your app may unexpectedly acquire new features when the underlying platform is automatically updated.</span></span>  
  
     <span data-ttu-id="ebb51-151">Par exemple, le mode Internet Explorer 11 de l’ancien Runtime prend en charge les déclarations de variables de portée bloc, par exemple `let` et `const` .</span><span class="sxs-lookup"><span data-stu-id="ebb51-151">For example, the Internet Explorer 11 mode of the legacy runtime supports block-scoping variable declarations such as `let` and `const`.</span></span> <span data-ttu-id="ebb51-152">Si le comportement du contrôle de version automatique du moteur Microsoft Edge a été le même que celui de la norme auparavant, le code qui fonctionnait dans le mode Internet Explorer 10, qui ne disposait pas de règles de blocs-notes, a pu démarrer une erreur lors de la mise à niveau automatique de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ebb51-152">If the Microsoft Edge engine automatic versioning behavior had been the standard previously, code that had worked in Internet Explorer 10 mode, which did not have block-scoping rules, may have started failing when the platform had automatically upgraded.</span></span> <span data-ttu-id="ebb51-153">Cela doit être une considération lors du choix du modèle d’exécution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ebb51-153">This must be a consideration when choosing which runtime model to use.</span></span> <span data-ttu-id="ebb51-154">Même si vous pensez que vous devez cibler le moteur Microsoft Edge, dans la mesure du possible, vous devez utiliser une structure de code JavaScript qui peut devenir non valide à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ebb51-154">While we believe you should target the Microsoft Edge engine whenever possible, you must be careful about using JavaScript code structures that may become invalid in the future.</span></span>  
  
-   <span data-ttu-id="ebb51-155">JsRT pour le Windows Store prend uniquement en charge le moteur Microsoft Edge (Chakra. dll).</span><span class="sxs-lookup"><span data-stu-id="ebb51-155">JsRT for the Windows Store only supports the Microsoft Edge engine (chakra.dll).</span></span> <span data-ttu-id="ebb51-156">Les applications qui essaient de lier une API JsRT dans jscript9. dll ne pourront pas être certifiées.</span><span class="sxs-lookup"><span data-stu-id="ebb51-156">Apps attempting to link against any JsRT API in jscript9.dll will fail certification.</span></span>  
  
-   <span data-ttu-id="ebb51-157">Il est important de ne pas confondre la déclaration de `JsCreateRuntime` , `JsCreateContext` , et `JsStartDebugging` entre jscript9. dll et Chakra. dll, car cela entraînera un interéquilibrage de la pile.</span><span class="sxs-lookup"><span data-stu-id="ebb51-157">It is critical that you do not confuse the declaration of `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging` between jscript9.dll and chakra.dll, because it will result in imbalancing the stack.</span></span>  
  
     <span data-ttu-id="ebb51-158">Lorsque vous utilisez C et C++, vous recevez une erreur de l’éditeur de liens si vous essayez d’utiliser la déclaration incorrecte, tant que vous n’avez pas besoin d’appeler, `LoadLibrary` puis `GetProcAddress` .</span><span class="sxs-lookup"><span data-stu-id="ebb51-158">When using C and C++, you will receive a linker error if you try to use the wrong declaration, as long as you're not doing something like calling `LoadLibrary` and then `GetProcAddress`.</span></span> <span data-ttu-id="ebb51-159">Il est possible que les développeurs .NET ne trouvent pas ce problème facilement et vérifient donc votre code lors de l’utilisation de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ebb51-159">.NET developers may not find this problem as easily, so double-check your code when using this feature.</span></span>  
  
## <span data-ttu-id="ebb51-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebb51-160">See Also</span></span>  
 [<span data-ttu-id="ebb51-161">Hébergement Runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="ebb51-161">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
 