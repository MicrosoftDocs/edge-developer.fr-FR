---
description: En savoir plus sur les mises à jour automatiques des extensions dans Microsoft Edge
title: Mise à jour automatique des extensions dans Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461513"
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
# <a name="auto-update-extensions-in-microsoft-edge"></a><span data-ttu-id="3f100-104">Mise à jour automatique des extensions dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3f100-104">Auto-update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="3f100-105">La mise à jour automatique des extensions offre les mêmes avantages que la mise à jour automatique de Microsoft Edge :</span><span class="sxs-lookup"><span data-stu-id="3f100-105">Automatically updating extensions share some of the same benefits as automatically updating Microsoft Edge:</span></span>   

*   <span data-ttu-id="3f100-106">Incorporer des correctifs de bogue et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3f100-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="3f100-107">Ajoutez de nouvelles fonctionnalités ou améliorations de performances.</span><span class="sxs-lookup"><span data-stu-id="3f100-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="3f100-108">Améliorez l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f100-108">Improve the user interface.</span></span>  

<span data-ttu-id="3f100-109">Auparavant, lorsque les extensions non stockées étaient pris en charge, il était possible de mettre à jour les binaires natifs et l’extension en même temps.</span><span class="sxs-lookup"><span data-stu-id="3f100-109">Previously when non-store based extensions were supported, it was possible to update the native binaries and the extension at the same time.</span></span>  <span data-ttu-id="3f100-110">À présent, ces extensions sont hébergées dans le magasin de modules extensions Microsoft Edge et les mises à jour sont réalisées à l’aide du même mécanisme que celui utilisé par Microsoft Edge, que vous ne pouvez pas contrôler.</span><span class="sxs-lookup"><span data-stu-id="3f100-110">Now, those extensions are hosted in the Microsoft Edge Add-ons store and updates are made using the same mechanism that Microsoft Edge uses, which you can't control.</span></span>  <span data-ttu-id="3f100-111">Soyez prudent lors de la mise à jour des extensions qui ont une dépendance sur les binaires natifs.</span><span class="sxs-lookup"><span data-stu-id="3f100-111">You should be careful when updating extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="3f100-112">Cette rubrique ne s’applique pas aux extensions publiées à l’aide du tableau [de bord de l’Centre][MicrosoftPartnerCenter] partenaires.</span><span class="sxs-lookup"><span data-stu-id="3f100-112">This topic does not apply to extensions published using the [Partner Center][MicrosoftPartnerCenter] dashboard.</span></span>  <span data-ttu-id="3f100-113">Vous pouvez utiliser le tableau de bord pour publier des versions mises à jour pour vos utilisateurs et dans le magasin de modules microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3f100-113">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>

## <a name="overview"></a><span data-ttu-id="3f100-114">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="3f100-114">Overview</span></span>  

<span data-ttu-id="3f100-115">Toutes les quelques heures, Microsoft Edge vérifie si chaque extension ou application installée dispose d’une URL de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-115">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="3f100-116">Les extensions peuvent spécifier une URL de mise à jour à l’aide du champ dans le manifeste, qui pointe vers un emplacement `update_url` pour effectuer une vérification de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-116">Extensions can specify an update URL using the `update_url` field in the manifest, which points to a location to perform an update check.</span></span>  <span data-ttu-id="3f100-117">Pour chaque `update_url` fichier manifeste, il envoie des demandes pour les fichiers XML de manifeste mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-117">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="3f100-118">Si le fichier XML de manifeste de mise à jour répertorie une version plus récente que celle installée, Microsoft Edge télécharge et installe la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="3f100-118">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="3f100-119">Le même processus fonctionne pour les mises à jour manuelles, où le nouveau fichier doit être signé avec la même clé privée que la `.crx` version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="3f100-119">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="3f100-120">Afin de maintenir la confidentialité des utilisateurs, Microsoft Edge n’envoie aucun en-tête avec des demandes de manifeste de mise à jour automatique et ignore les en-têtes dans les réponses à `Cookie` `Set-Cookie` ces demandes.</span><span class="sxs-lookup"><span data-stu-id="3f100-120">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="3f100-121">URL de mise à jour</span><span class="sxs-lookup"><span data-stu-id="3f100-121">Update URL</span></span>  

<span data-ttu-id="3f100-122">Si vous hébergez votre propre extension ou application, vous devez ajouter le `update_url` champ à votre `manifest.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="3f100-122">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="3f100-123">Examinez l’extrait de code suivant pour obtenir un exemple de `update_url` .</span><span class="sxs-lookup"><span data-stu-id="3f100-123">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="3f100-124">Manifeste mis à jour</span><span class="sxs-lookup"><span data-stu-id="3f100-124">Updated manifest</span></span>  

<span data-ttu-id="3f100-125">Le manifeste mis à jour renvoyé par le serveur doit être un document XML.</span><span class="sxs-lookup"><span data-stu-id="3f100-125">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="3f100-126">Examinez l’extrait de code suivant pour obtenir un exemple du fichier manifeste XML mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-126">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="3f100-127">Le tableau suivant décrit les attributs du fichier manifeste XML mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-127">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="3f100-128">Attribut</span><span class="sxs-lookup"><span data-stu-id="3f100-128">Attribute</span></span> | <span data-ttu-id="3f100-129">Détails</span><span class="sxs-lookup"><span data-stu-id="3f100-129">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="3f100-130">L’ID d’extension est généré en fonction d’un hachage de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="3f100-130">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="3f100-131">Pour trouver l’ID d’une extension, ouvrez Microsoft Edge et accédez à `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="3f100-131">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="3f100-132">URL du `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="3f100-132">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="3f100-133">Cette valeur d’attribut est utilisée par Microsoft Edge pour déterminer s’il doit télécharger le `.crx` fichier spécifié par `codebase` .</span><span class="sxs-lookup"><span data-stu-id="3f100-133">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="3f100-134">Elle doit correspondre à la valeur `version` du fichier `manifest.json` du `.crx` fichier.</span><span class="sxs-lookup"><span data-stu-id="3f100-134">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="3f100-135">Le fichier XML de manifeste de mise à jour peut contenir des informations sur plusieurs extensions en incluant plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="3f100-135">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="3f100-136">Test</span><span class="sxs-lookup"><span data-stu-id="3f100-136">Testing</span></span>  

<span data-ttu-id="3f100-137">La fréquence de vérification des mises à jour par défaut est de plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="3f100-137">The default update check frequency is several hours.</span></span>  <span data-ttu-id="3f100-138">Pour forcer une mise à jour, accédez au bouton Mettre à jour `edge://extensions` **les extensions et choisissez-le maintenant.**</span><span class="sxs-lookup"><span data-stu-id="3f100-138">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="3f100-139">Utilisation avancée : paramètres de requête</span><span class="sxs-lookup"><span data-stu-id="3f100-139">Advanced usage: request parameters</span></span>  

<span data-ttu-id="3f100-140">Le mécanisme de mise à jour automatique de base est aussi simple que de déposer un fichier XML statique sur n’importe quel serveur web tel qu’Apache et de mettre à jour le fichier XML lorsque vous publiez de nouvelles versions de vos extensions.</span><span class="sxs-lookup"><span data-stu-id="3f100-140">The basic auto-update mechanism is as easy as dropping a static XML file onto any web server such as Apache, and updating the XML file as you release new versions of your extensions.</span></span>  

<span data-ttu-id="3f100-141">Vous pouvez tirer parti du fait que des paramètres sont ajoutés à la demande de manifeste de mise à jour qui indiquent l’ID d’extension et la version.</span><span class="sxs-lookup"><span data-stu-id="3f100-141">You may take advantage of the fact that parameters are added to the update manifest request that indicate the extension ID and version.</span></span> <span data-ttu-id="3f100-142">Vous pouvez utiliser la même URL de mise à jour pour toutes vos extensions au lieu d’un fichier XML statique.</span><span class="sxs-lookup"><span data-stu-id="3f100-142">You can use the same update URL for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="3f100-143">Pour utiliser la même URL de mise à jour pour toutes vos extensions, pointez sur une URL qui exécute du code dynamique côté serveur pour tester ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="3f100-143">To use the same update URL for all your extensions, point to a URL that runs dynamic server-side code to test these parameters.</span></span>  

<span data-ttu-id="3f100-144">L’exemple suivant illustre le format des paramètres de requête de l’URL de mise à jour : `?x={extension_data}` .</span><span class="sxs-lookup"><span data-stu-id="3f100-144">The following example demonstrates the format of the request parameters of update URL: `?x={extension_data}`.</span></span>

<span data-ttu-id="3f100-145">Dans cet exemple, `{extension_data}` est une chaîne codée en URL qui utilise le format suivant : `id={id}&v={version}` .</span><span class="sxs-lookup"><span data-stu-id="3f100-145">In this example, `{extension_data}` is a URL-encoded string that uses the following format: `id={id}&v={version}`.</span></span>

<span data-ttu-id="3f100-146">Par exemple, les deux extensions suivantes pointent vers la même URL de mise à `http://contoso.com/extension_updates.php` jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-146">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*  <span data-ttu-id="3f100-147">Extension 1 - ID : « aaaaaaaaaaaaaaaaaaaa » Version : « 1.1 »</span><span class="sxs-lookup"><span data-stu-id="3f100-147">Extension 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"</span></span>
*  <span data-ttu-id="3f100-148">Extension 2 - ID : « bbbbbbbbbbbbbbbbbbbbbbbb » Version : « 0,4 »</span><span class="sxs-lookup"><span data-stu-id="3f100-148">Extension 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0.4"</span></span>


<span data-ttu-id="3f100-149">Voici les demandes de mise à jour de chaque extension.</span><span class="sxs-lookup"><span data-stu-id="3f100-149">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="3f100-150">Vous pouvez également ré lister plusieurs extensions dans une seule demande pour chaque URL de mise à jour unique.</span><span class="sxs-lookup"><span data-stu-id="3f100-150">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="3f100-151">L’exemple suivant fusionne les demandes précédentes en une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3f100-151">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="3f100-152">Si vous envoyez une seule demande et que le nombre d’extensions installées qui utilisent la même URL de mise à jour est trop long, la vérification de mise à jour envoie davantage de `GET` demandes.</span><span class="sxs-lookup"><span data-stu-id="3f100-152">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="3f100-153">Une `GET` URL de demande est trop longue si elle fait environ 2 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="3f100-153">A `GET` request URL is too long if it is approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="3f100-154">À l’avenir, une seule `POST` demande peut remplacer plusieurs `GET` demandes.</span><span class="sxs-lookup"><span data-stu-id="3f100-154">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="3f100-155">La `POST` demande peut contenir les paramètres de la demande dans le `POST` corps.</span><span class="sxs-lookup"><span data-stu-id="3f100-155">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="3f100-156">Utilisation avancée : version minimale du navigateur</span><span class="sxs-lookup"><span data-stu-id="3f100-156">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="3f100-157">À mesure que de nouvelles API sont publiées pour le système d’extensions Microsoft Edge, vous pouvez publier une version mise à jour de votre extension ou de votre application qui fonctionne uniquement avec les versions plus récentes de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3f100-157">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="3f100-158">Lorsque Microsoft Edge est mis à jour automatiquement, la mise à jour vers cette nouvelle version peut prendre quelques jours.</span><span class="sxs-lookup"><span data-stu-id="3f100-158">When Microsoft Edge is auto-updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="3f100-159">Pour vous assurer qu’une mise à jour spécifique s’applique uniquement aux versions de Microsoft Edge actuelles ou plus récentes qu’une version spécifique, ajoutez l’attribut `prodversionmin` dans votre manifeste de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3f100-159">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="3f100-160">Dans l’extrait de code suivant, la valeur d’attribut de spécifie que votre application se met automatiquement à jour vers la version uniquement lorsque l’utilisateur exécute Microsoft Edge ou `prodversionmin` `3.0.193.0` une version plus `2.0` `3.0.193.0` récente.</span><span class="sxs-lookup"><span data-stu-id="3f100-160">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app auto-updates to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> <span data-ttu-id="3f100-162">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f100-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3f100-163">La page d’origine se trouve [ici.](https://developer.chrome.com/docs/apps/autoupdate/)</span><span class="sxs-lookup"><span data-stu-id="3f100-163">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate/).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="3f100-165">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f100-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
