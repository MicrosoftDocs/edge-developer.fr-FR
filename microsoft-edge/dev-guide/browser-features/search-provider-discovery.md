---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Si vous êtes un fournisseur de recherche, voir comment s’assurer que Microsoft Edge prend en charge votre service.
title: Découverte du fournisseur de recherche-Guide du développeur
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 4ac8ea966e9c4736834a0be1130a8c2a8dfb2614
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941972"
---
# Découverte de moteur de recherche  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

L’intégration de recherche complète est intégrée à la barre d’adresses Microsoft Edge, y compris aux suggestions de recherche, aux résultats provenant du Web, à votre historique de navigation et aux favoris.  Microsoft Edge suit la spécification [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) pour découvrir et utiliser les fournisseurs de recherche Web.  Si vous êtes un fournisseur de recherche, procédez comme suit pour vous assurer que Microsoft Edge prend en charge votre service.  

> ESSENTIELLES Pour des informations sur la sécurité et la confidentialité des utilisateurs, Microsoft Edge nécessite que toutes les recherches soient effectuées via SSL.  

Les ressources suivantes doivent être spécifiées en tant qu' `https` URL pour permettre l’intégration de Microsoft Edge à votre moteur de recherche:  

*   Site contenant la référence au document de description.  
*   URL du document de description proprement dit  
*   Le modèle de requête de recherche  

1.  Fournissez un fichier de description OpenSearch contenant le nom du fournisseur de recherche et le modèle à utiliser pour créer la recherche.  Voici un exemple de document:  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  Ajoutez une référence à votre fichier de description OpenSearch dans la section d’en-tête de vos pages (il s’agit généralement de la page d’accueil du site et des pages de résultats de recherche), par exemple:  
    
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
    
Lorsqu’un utilisateur navigue vers votre service de recherche, votre description OpenSearch sera automatiquement sélectionnée et enregistrée pour une utilisation ultérieure.  L’utilisateur est alors en mesure d’accéder aux paramètres de Microsoft Edge et de choisir d’ajouter votre service de recherche à sa liste de fournisseurs de recherche pour la barre d’adresses Microsoft Edge.  

Pour plus d’informations sur la création de votre document de description OpenSearch, voir la spécification [1,1 de OpenSearch](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) .  
