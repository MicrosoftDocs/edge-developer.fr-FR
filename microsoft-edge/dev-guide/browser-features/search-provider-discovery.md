---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Si vous êtes un fournisseur de recherche, voir comment s’assurer que Microsoft Edge prend en charge votre service.
title: Guide de développement-découverte du fournisseur de recherche
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: ac23c2c62d436d5772b498208a56ad306eb8cb3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564698"
---
# <span data-ttu-id="6f6ec-104">Découverte du fournisseur de recherche</span><span class="sxs-lookup"><span data-stu-id="6f6ec-104">Search provider discovery</span></span>


<span data-ttu-id="6f6ec-105">L’intégration de recherche complète est intégrée à la barre d’adresses Microsoft Edge, y compris aux suggestions de recherche, aux résultats provenant du Web, à votre historique de navigation et aux favoris.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="6f6ec-106">Microsoft Edge suit la spécification [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) pour découvrir et utiliser les fournisseurs de recherche Web.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-106">Microsoft Edge follows the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification to discover and use web search providers.</span></span> <span data-ttu-id="6f6ec-107">Si vous êtes un fournisseur de recherche, procédez comme suit pour vous assurer que Microsoft Edge prend en charge votre service.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>

**<span data-ttu-id="6f6ec-108">Pour des informations sur la sécurité et la confidentialité des utilisateurs, Microsoft Edge nécessite que toutes les recherches soient effectuées via SSL.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-108">For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>** <span data-ttu-id="6f6ec-109">Les ressources suivantes doivent être spécifiées en tant qu' `https` URL pour permettre l’intégration de Microsoft Edge à votre moteur de recherche:</span><span class="sxs-lookup"><span data-stu-id="6f6ec-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>
* <span data-ttu-id="6f6ec-110">Site contenant la référence au document de description.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-110">The site that contains the reference to the description document</span></span>
* <span data-ttu-id="6f6ec-111">URL du document de description proprement dit</span><span class="sxs-lookup"><span data-stu-id="6f6ec-111">The URL to the description document itself</span></span>
* <span data-ttu-id="6f6ec-112">Le modèle de requête de recherche</span><span class="sxs-lookup"><span data-stu-id="6f6ec-112">The search query template</span></span> 

1.  <span data-ttu-id="6f6ec-113">Fournissez un fichier de description OpenSearch contenant le nom du fournisseur de recherche et le modèle à utiliser pour créer la recherche.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span> <span data-ttu-id="6f6ec-114">Voici un exemple de document:</span><span class="sxs-lookup"><span data-stu-id="6f6ec-114">Here is an example document:</span></span>

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  <span data-ttu-id="6f6ec-115">Ajoutez une référence à votre fichier de description OpenSearch dans la section d’en-tête de vos pages (il s’agit généralement de la page d’accueil du site et des pages de résultats de recherche), par exemple:</span><span class="sxs-lookup"><span data-stu-id="6f6ec-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>

    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```

<span data-ttu-id="6f6ec-116">Lorsqu’un utilisateur navigue vers votre service de recherche, votre description OpenSearch sera automatiquement sélectionnée et enregistrée pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span> <span data-ttu-id="6f6ec-117">L’utilisateur est alors en mesure d’accéder aux paramètres de Microsoft Edge et de choisir d’ajouter votre service de recherche à sa liste de fournisseurs de recherche pour la barre d’adresses Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6f6ec-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>

<span data-ttu-id="6f6ec-118">Pour plus d’informations sur la création de votre document de description OpenSearch, voir la spécification [1,1 de OpenSearch](https://go.microsoft.com/fwlink/p/?LinkID=208582) .</span><span class="sxs-lookup"><span data-stu-id="6f6ec-118">See the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification for further details on creating your OpenSearch description document.</span></span>