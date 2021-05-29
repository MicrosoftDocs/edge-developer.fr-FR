---
description: Découvrez les mises à jour automatiques des extensions dans Microsoft Edge
title: Mettre à jour automatiquement les extensions dans Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: d9901f9c39dabfab111eb7e0c34a3e267a317110
ms.sourcegitcommit: 59d8043e37b89da814f63bc85daf84e0e7167eab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "11586387"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="automatically-update-extensions-in-microsoft-edge"></a><span data-ttu-id="f6f15-104">Mettre à jour automatiquement les extensions dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6f15-104">Automatically update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="f6f15-105">Lorsque vous définissez votre extension pour qu’elle soit automatiquement mise à jour, elle partage les avantages suivants avec les Microsoft Edge lorsque ce dernier est automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-105">When you set your extension to automatically update, your extension shares the following benefits with Microsoft Edge when set to automatically update.</span></span>  

*   <span data-ttu-id="f6f15-106">Incorporer des correctifs de bogue et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f6f15-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="f6f15-107">Ajoutez de nouvelles fonctionnalités ou des améliorations de performances.</span><span class="sxs-lookup"><span data-stu-id="f6f15-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="f6f15-108">Améliorez l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f6f15-108">Improve the user interface.</span></span>  

<span data-ttu-id="f6f15-109">Auparavant, les extensions non stockées étaient pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f6f15-109">Previously, non-store based extensions were supported.</span></span>  <span data-ttu-id="f6f15-110">En outre, vous avez mis à jour les binaires natifs et l’extension en même temps.</span><span class="sxs-lookup"><span data-stu-id="f6f15-110">Also, you updated the native binaries and the extension at the same time.</span></span>  

<span data-ttu-id="f6f15-111">À présent, le magasin Microsoft Edge des extensions héberge vos extensions et vous mettez à jour votre extension à l’aide du même mécanisme que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f6f15-111">Now, the Microsoft Edge Add-ons store hosts your extensions and you update your extension using the same mechanism as Microsoft Edge.</span></span>  <span data-ttu-id="f6f15-112">Vous ne contrôlez pas le mécanisme de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-112">You don't control the update mechanism.</span></span>  <span data-ttu-id="f6f15-113">Soyez prudent lorsque vous mettez à jour les extensions qui ont une dépendance sur les binaires natifs.</span><span class="sxs-lookup"><span data-stu-id="f6f15-113">Be careful when you update extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="f6f15-114">Cet article ne s’applique pas aux extensions que vous publiez à l’aide du tableau [de bord de l’Centre][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] partenaires.</span><span class="sxs-lookup"><span data-stu-id="f6f15-114">This article does not apply to extensions that you publish using the [Partner Center][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] dashboard.</span></span>  <span data-ttu-id="f6f15-115">Vous pouvez utiliser le tableau de bord pour publier des versions mises à jour pour vos utilisateurs et le magasin Microsoft Edge de modules.</span><span class="sxs-lookup"><span data-stu-id="f6f15-115">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="f6f15-116">Pour plus d’informations, [accédez à Mettre à jour ou supprimer votre extension.][ExtensionsPublishUpdateExtension]</span><span class="sxs-lookup"><span data-stu-id="f6f15-116">For more information, navigate to [Update or remove your extension][ExtensionsPublishUpdateExtension].</span></span>  

## <a name="overview"></a><span data-ttu-id="f6f15-117">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f6f15-117">Overview</span></span>  

<span data-ttu-id="f6f15-118">Toutes les quelques heures, Microsoft Edge si chaque extension ou application installée dispose d’une URL de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-118">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="f6f15-119">Pour spécifier une URL de mise à jour pour votre extension, utilisez `update_url` le champ dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="f6f15-119">To specify an update URL for your extension, use the `update_url` field in the manifest.</span></span>  <span data-ttu-id="f6f15-120">Le `update_url` champ dans le manifeste pointe vers un emplacement pour effectuer une vérification de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-120">The `update_url` field in the manifest points to a location to complete an update check.</span></span>  <span data-ttu-id="f6f15-121">Pour chaque `update_url` fichier manifeste, il envoie des demandes pour les fichiers XML de manifeste mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-121">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="f6f15-122">Si le fichier XML de manifeste de mise à jour répertorie une version plus récente que celle installée, Microsoft Edge télécharge et installe la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="f6f15-122">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="f6f15-123">Le même processus fonctionne pour les mises à jour manuelles, où le nouveau fichier doit être signé avec la même clé privée que la `.crx` version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="f6f15-123">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="f6f15-124">Afin de maintenir la confidentialité des utilisateurs, Microsoft Edge n’envoie aucun en-tête avec des demandes de manifeste de mise à jour automatique et ignore les en-têtes dans les réponses à `Cookie` `Set-Cookie` ces demandes.</span><span class="sxs-lookup"><span data-stu-id="f6f15-124">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="f6f15-125">URL de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f6f15-125">Update URL</span></span>  

<span data-ttu-id="f6f15-126">Si vous hébergez votre propre extension ou application, vous devez ajouter le `update_url` champ à votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="f6f15-126">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="f6f15-127">Examinez l’extrait de code suivant pour obtenir un exemple de `update_url` .</span><span class="sxs-lookup"><span data-stu-id="f6f15-127">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="f6f15-128">Manifeste mis à jour</span><span class="sxs-lookup"><span data-stu-id="f6f15-128">Updated manifest</span></span>  

<span data-ttu-id="f6f15-129">Le manifeste mis à jour renvoyé par le serveur doit être un document XML.</span><span class="sxs-lookup"><span data-stu-id="f6f15-129">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="f6f15-130">Examinez l’extrait de code suivant pour obtenir un exemple du fichier manifeste XML mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-130">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="f6f15-131">Le tableau suivant décrit les attributs du fichier manifeste XML mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-131">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="f6f15-132">Attribut</span><span class="sxs-lookup"><span data-stu-id="f6f15-132">Attribute</span></span> | <span data-ttu-id="f6f15-133">Détails</span><span class="sxs-lookup"><span data-stu-id="f6f15-133">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="f6f15-134">L’ID d’extension est généré en fonction d’un hachage de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="f6f15-134">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="f6f15-135">Pour trouver l’ID d’une extension, ouvrez Microsoft Edge et accédez à `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="f6f15-135">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="f6f15-136">URL du `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="f6f15-136">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="f6f15-137">Cette valeur d’attribut est utilisée Microsoft Edge pour déterminer si elle doit télécharger le `.crx` fichier spécifié par `codebase` .</span><span class="sxs-lookup"><span data-stu-id="f6f15-137">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="f6f15-138">Elle doit correspondre à la valeur `version` du fichier `manifest.json` du `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="f6f15-138">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="f6f15-139">Le fichier XML de manifeste de mise à jour peut contenir des informations sur plusieurs extensions en incluant plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="f6f15-139">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="f6f15-140">Test</span><span class="sxs-lookup"><span data-stu-id="f6f15-140">Testing</span></span>  

<span data-ttu-id="f6f15-141">La fréquence de vérification des mises à jour par défaut est de plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="f6f15-141">The default update check frequency is several hours.</span></span>  <span data-ttu-id="f6f15-142">Pour forcer une mise à jour, accédez au bouton Mettre à jour `edge://extensions` **les extensions et choisissez-le maintenant.**</span><span class="sxs-lookup"><span data-stu-id="f6f15-142">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="f6f15-143">Utilisation avancée : paramètres de requête</span><span class="sxs-lookup"><span data-stu-id="f6f15-143">Advanced usage: request parameters</span></span>  

<span data-ttu-id="f6f15-144">Le mécanisme de base est simple.</span><span class="sxs-lookup"><span data-stu-id="f6f15-144">The basic mechanism is simple.</span></span>  <span data-ttu-id="f6f15-145">Pour mettre à jour automatiquement votre extension, effectuez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6f15-145">To automatically update your extension, complete the following actions.</span></span>  

1.  <span data-ttu-id="f6f15-146">Télécharger votre fichier XML statique sur votre serveur web, tel qu’Apache.</span><span class="sxs-lookup"><span data-stu-id="f6f15-146">Upload your static XML file on your web server, such as Apache.</span></span>  
1.  <span data-ttu-id="f6f15-147">Mettez à jour le fichier XML à mesure que vous publiez de nouvelles versions de vos extensions.</span><span class="sxs-lookup"><span data-stu-id="f6f15-147">Update the XML file as you release new versions of your extensions.</span></span>  
    
<span data-ttu-id="f6f15-148">Tirez parti du fait que certains paramètres ajoutés à la demande de manifeste de mise à jour indiquent l’extension `ID` et `version` .</span><span class="sxs-lookup"><span data-stu-id="f6f15-148">Take advantage of the fact that some parameters added to the update manifest request indicate the extension `ID` and `version`.</span></span>  <span data-ttu-id="f6f15-149">Vous pouvez utiliser la même chose pour toutes vos extensions au `update URL` lieu d’un fichier XML statique.</span><span class="sxs-lookup"><span data-stu-id="f6f15-149">You may use the same `update URL` for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="f6f15-150">Pour utiliser la même valeur pour toutes vos extensions, pointez sur une URL qui exécute du code dynamique côté serveur `update URL` pour tester les paramètres.</span><span class="sxs-lookup"><span data-stu-id="f6f15-150">To use the same `update URL` for all your extensions, point to a URL that runs dynamic server-side code to test the parameters.</span></span>  

<span data-ttu-id="f6f15-151">L’exemple suivant illustre le format des paramètres de demande de l’URL de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-151">The following example demonstrates the format of the request parameters of update URL.</span></span>  

```url
?x={extension_data}
```  

<span data-ttu-id="f6f15-152">Dans cet exemple, il s’agit d’une chaîne codée au format `{extension_data}` URL qui utilise le format suivant.</span><span class="sxs-lookup"><span data-stu-id="f6f15-152">In this example, `{extension_data}` is a URL-encoded string that uses the following format.</span></span>  

```url
id={id}&v={version}
```  

<span data-ttu-id="f6f15-153">Par exemple, les deux extensions suivantes pointent vers la même URL de mise à `http://contoso.com/extension_updates.php` jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-153">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*   <span data-ttu-id="f6f15-154">Extension 1</span><span class="sxs-lookup"><span data-stu-id="f6f15-154">Extension 1</span></span>  
    *   <span data-ttu-id="f6f15-155">ID:</span><span class="sxs-lookup"><span data-stu-id="f6f15-155">ID:</span></span> `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   <span data-ttu-id="f6f15-156">URL de mise à jour :</span><span class="sxs-lookup"><span data-stu-id="f6f15-156">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="f6f15-157">Version:</span><span class="sxs-lookup"><span data-stu-id="f6f15-157">Version:</span></span> `1.1`  
*   <span data-ttu-id="f6f15-158">Extension 2</span><span class="sxs-lookup"><span data-stu-id="f6f15-158">Extension 2</span></span>  
    *   <span data-ttu-id="f6f15-159">ID:</span><span class="sxs-lookup"><span data-stu-id="f6f15-159">ID:</span></span> `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   <span data-ttu-id="f6f15-160">URL de mise à jour :</span><span class="sxs-lookup"><span data-stu-id="f6f15-160">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="f6f15-161">Version:</span><span class="sxs-lookup"><span data-stu-id="f6f15-161">Version:</span></span> `0.4`  


<span data-ttu-id="f6f15-162">Voici les demandes de mise à jour de chaque extension.</span><span class="sxs-lookup"><span data-stu-id="f6f15-162">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="f6f15-163">Vous pouvez également ré lister plusieurs extensions dans une seule demande pour chaque URL de mise à jour unique.</span><span class="sxs-lookup"><span data-stu-id="f6f15-163">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="f6f15-164">L’exemple suivant fusionne les demandes précédentes en une seule requête.</span><span class="sxs-lookup"><span data-stu-id="f6f15-164">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="f6f15-165">Si vous envoyez une seule demande et que le nombre d’extensions installées qui utilisent la même URL de mise à jour est trop long, la vérification de mise à jour envoie davantage de `GET` demandes.</span><span class="sxs-lookup"><span data-stu-id="f6f15-165">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="f6f15-166">Une `GET` URL de demande est trop longue si elle fait environ 2 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="f6f15-166">A `GET` request URL is too long if it's approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="f6f15-167">À l’avenir, une `POST` seule demande peut remplacer plusieurs `GET` demandes.</span><span class="sxs-lookup"><span data-stu-id="f6f15-167">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="f6f15-168">La `POST` demande peut contenir les paramètres de la demande dans le `POST` corps.</span><span class="sxs-lookup"><span data-stu-id="f6f15-168">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="f6f15-169">Utilisation avancée : version minimale du navigateur</span><span class="sxs-lookup"><span data-stu-id="f6f15-169">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="f6f15-170">À mesure que de nouvelles API sont publiées pour le système d’extensions Microsoft Edge, vous pouvez publier une version mise à jour de votre extension ou application qui fonctionne uniquement avec les versions Microsoft Edge plus récentes.</span><span class="sxs-lookup"><span data-stu-id="f6f15-170">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="f6f15-171">Lorsque Microsoft Edge mise à jour automatique, la mise à jour de la plupart de vos utilisateurs vers cette nouvelle version peut prendre quelques jours.</span><span class="sxs-lookup"><span data-stu-id="f6f15-171">When Microsoft Edge is automatically updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="f6f15-172">Pour vous assurer qu’une mise à jour spécifique s’applique uniquement Microsoft Edge versions actuelles ou plus récentes qu’une version spécifique, ajoutez l’attribut dans votre manifeste `prodversionmin` de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f6f15-172">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="f6f15-173">Dans l’extrait de code suivant, la valeur d’attribut de spécifie que votre application est automatiquement mise à jour vers la version uniquement lorsque l’utilisateur exécute une Microsoft Edge ou `prodversionmin` `3.0.193.0` une version plus `2.0` `3.0.193.0` récente.</span><span class="sxs-lookup"><span data-stu-id="f6f15-173">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app automatically updated to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Mettre à jour ou supprimer votre extension | Documents Microsoft"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> <span data-ttu-id="f6f15-176">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6f15-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f6f15-177">La page d’origine se trouve [ici.](https://developer.chrome.com/docs/apps/autoupdate)</span><span class="sxs-lookup"><span data-stu-id="f6f15-177">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="f6f15-179">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6f15-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
