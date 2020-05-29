---
description: Découvrez comment thePayment demande à APIenables Microsoft Edge d’agir en tant qu’intermédiaire entre commerçants, consommateurs et modes de paiement client stockés dans le Cloud.
title: Guide de développement-API de demande de paiement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 75c596570a222336a4ba0c371acb8770f97804ee
ms.sourcegitcommit: e690bb4d1cb9e73c93b468c9f55d91ea6fb6c654
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/10/2020
ms.locfileid: "10566678"
---
# API de demande de paiement

Les ventes de commerce électronique continuent de croître à un rythme rapide. D’après [eMarketer](https://www.emarketer.com/), les ventes numériques 2018 sont prévues pour une augmentation de 23% par rapport aux niveaux mesurés en 2013.  Si les particuliers et les entreprises jouissent de la commodité des ventes de commerce électronique, les problèmes persistent.  Dès à présent, chaque propriétaire de site Web d’e-commerce doit investir du temps pour développer des flux d’extraction de paiement et des règles de validation de grande qualité.  Les consommateurs doivent parcourir les différents flux d’extraction de paiement et entrer de nouveau les mêmes informations de paiement et d’expédition sur chaque site.  Cela peut prendre du temps et frustrant pour les particuliers, ce qui a pour principal taux d’abandon de panier d’achat et de diminution des ventes pour les commerçants. L' [estimation](http://baymard.com/lists/cart-abandonment-rate) des commerçants entre 60% et 70% des paniers d’achat est abandonnée.      

L' [API de demande de paiement](https://w3.org/TR/payment-request/) standardise le processus de validation du paiement. Cette API nécessite moins de personnalisation pour les développeurs Web et offre une connaissance plus rapide, plus cohérente et donc plus déroutante pour les consommateurs.  Dans la mesure où les consommateurs peuvent sélectionner des instruments de paiement et des adresses d’expédition à partir de leur compte Microsoft, il est nécessaire d’entrer moins de données pour effectuer des achats qui réduit le temps et la saisie de données requises pour effectuer un paiement.   

L' [API de demande de paiement](https://w3.org/TR/payment-request/) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et les modes de paiement (par exemple, cartes de crédit) stockés dans le Cloud. 
  
En résumé, lors de l’utilisation de l' [API de demande de paiement](https://w3.org/TR/payment-request/), les clients achètent le site Web commerçant normalement.  Lorsque vous êtes prêt à payer, le site Web du commerçant appelle l’API de **demande de paiement** pour créer une **demande de paiement** et transmet les informations de paiement pertinentes (par exemple, modes de paiement pris en charge, montant de l’achat, devise, etc.) au navigateur.

![Constitution d’une demande de paiement](./../media/payment_request_construct.png)

Le navigateur authentifie l’utilisateur, permet à l’utilisateur de sélectionner un mode de paiement pris en charge sur un fichier et traite les détails du paiement. Le navigateur envoie ensuite les informations de paiement au site Web du commerçant pour que le commerçant puisse terminer le paiement.  En plus de recevoir des informations de paiement, le commerçant peut également choisir de recevoir des informations d’expédition dans le cadre de la **demande de paiement**.  

![Construction de réponse de paiement](./../media/payment_response_construct.png)

Pour afficher une API de demande de paiement en action, et obtenir une vue d’ensemble de son utilisation, regardez cette vidéo.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> L’API de demande de paiement est prise en charge dans Microsoft Edge Build 14992 +.


## Création d’une demande de paiement 
Les pages Web créent une **demande de paiement** en règle générale lorsque l’utilisateur démarre un processus de paiement en cliquant sur le bouton «acheter».  Le **Payment Request** [constructeur](https://msdn.microsoft.com/library/mt790440) de votre demande de paiement inclut methodData, les détails et les options. 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

Ce [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre contient une liste des modes de paiement et des réseaux acceptés par le site Web et les données spécifiques du mode de paiement associé. Dans Microsoft Edge, cette liste est mise en correspondance avec les modes de paiement pris en charge que l’acheteur a enregistrés sur son compte Microsoft et génère la liste «payer avec» dans l’interface utilisateur du paiement.

![Liste «payer avec» dans l’interface utilisateur de Microsoft Wallet](./../media/pay_with.png)

```js
var supportedInstruments = [{
    supportedMethods: ['basic-card'],
    data: {
        supportedNetworks: ['visa', 'mastercard', 'amex'],
        supportedTypes: ['credit'] 
    }         
}]; 
```

Le [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre contient des informations que le commerçant souhaite communiquer au client à propos de la transaction.  Il s’agit notamment des éléments de synthèse tels que total, taxe, montant d’expédition et autres niveaux de synthèse ayant un impact sur le montant du paiement. Celles-ci ne sont pas destinées à être commandées. 
  
Ce [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre permet également de définir les options d’expédition disponibles pour le client, le cas échéant.  Pour plus d’informations, reportez-vous à la section **paiement** avec la section expédition ci-dessous. 

Chaque [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) ligne inclut une étiquette pour la devise et le montant.  

> [!NOTE]
> La **demande de paiement** ne calcule pas la somme ou le total de ces montants.  Il incombe au site Web du commerçant de s’assurer que le total de ses lignes est correct.   


![Détails du sous-total, de l’expédition, des taxes et du total](./../media/show_details.png)

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
        label: 'Subtotal',
        amount: {currency: 'USD', value: '174.99'}
    }, {
        label: 'Taxes',
        amount: {currency: "USD", value: '18.99'}
    }],
};  
```

[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)ne prend pas en charge le remboursement; les montants doivent donc toujours être positifs; les éléments de liste individuels peuvent être négatifs, tels que les remises. 

Le navigateur affiche les étiquettes lorsque vous les définissez et affiche automatiquement la mise en forme de devise appropriée selon les paramètres régionaux du client. Notez que les étiquettes doivent être affichées dans la même langue que votre contenu. 

Le [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre définit les données retournées par la page Web à partir de la **demande de paiement**. Cela définit également les données qui doivent être collectées, notamment si la livraison, l’adresse de messagerie et/ou le numéro de téléphone sont nécessaires.

![Liste déroulante adresse e-mail](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## Affichage de la demande de paiement

La [`show()`](https://msdn.microsoft.com/library/mt790448) méthode est appelée par la page Web pour permettre à l’utilisateur d’interagir avec l’interface utilisateur de la **demande de paiement** .  La [`show()`](https://msdn.microsoft.com/library/mt790448) méthode renvoie une promesse qui sera résolue lorsque l’utilisateur autorise la demande de paiement.  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmer et payer les détails](./../media/pay_screen_default.png)

## Abandon d’une demande de paiement
 
La [`abort()`](https://msdn.microsoft.com/library/mt790437) méthode peut être appelée à tout moment après l’appel de la [`show()`](https://msdn.microsoft.com/library/mt790448) méthode, jusqu’à la date à laquelle la promesse est résolue.  La [`abort()`](https://msdn.microsoft.com/library/mt790437) méthode entraînera l’annulation de la **demande de paiement** par le navigateur, et la fermeture de l’interface utilisateur de votre **demande de paiement** .  Par exemple, une page Web est susceptible de se terminer si l’utilisateur n’a pas terminé la transaction dans la durée requise.

```js
payment.abort();
``` 

## Réponse de paiement
Lorsque le client approuve la **demande de paiement**, une **réponse de paiement** est renvoyée au site Web. Le **bordereau de réponse** comprend les éléments suivants: 

 Propriété      | Description | Requis | Informations supplémentaires
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | ID du mode de paiement sélectionné par l’utilisateur. | Y | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | Un objet JSON qui inclut toutes les données requises par le commerçant pour traiter la transaction à l’aide du mode de paiement sélectionné ou d’un jeton de paiement. | Y | [Carte de base](https://go.microsoft.com/fwlink/?linkid=834965) Dictionnaire: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | Adresse d’expédition sélectionnée par l’utilisateur  |  Facultatif. Obligatoire lorsque [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**  | Dictionnaire d’adresses: pays; addressLine; Region urbains dependentLocality; CodePostal sortingCode; languageCode; société destinataire Répertoire |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | ID de l’option d’expédition sélectionnée | Facultatif. Obligatoire lorsque [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Nom fourni par l’utilisateur.  | Facultatif. Obligatoire lorsque [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai** | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Adresse e-mail sélectionnée par l’utilisateur | Facultatif. Obligatoire lorsque [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Le numéro de téléphone sélectionné par l’utilisateur | Facultatif. Obligatoire lorsque [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai** | |

L' [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objet JSON dans la **réponse de paiement** contient les données de paiement requises par le commerçant pour traiter un paiement. Dans sa forme la plus simple, la réponse sera une charge utile de [carte de base](https://go.microsoft.com/fwlink/?linkid=834965) contenant les détails de la carte de paiement en clair. Lorsque les commerçants disposent de contrats avec des partenaires passerelle/processeur supplémentaires pour leur permettre de prendre en charge des paiements, le commerçant peut nécessiter une charge utile que le processeur peut gérer. Celles-ci peuvent prendre la forme d’un jeton de processeur/passerelle ou d’un instrument de paiement chiffré. Ces modes de paiement font partie du cadre de ce document et seront couverts dans la documentation propre au processeur. Par ailleurs, pour recevoir une réponse de base à une [carte](https://go.microsoft.com/fwlink/?linkid=834965) , aucun intégration supplémentaire à Microsoft n’est requise par le développeur, contrairement aux autres modes de paiement pour les processeurs et les passerelles, qui pourraient nécessiter une autorisation d’intégration de clé de chiffrement ou de demande d’autorisation (OAuth). 

Lors de la réception d’une **réponse de paiement**, le site Web transmet les informations de paiement à son processeur de paiement.  Le navigateur va afficher une page de compteur pendant le traitement du paiement.

![Page affichée lors du traitement du paiement](./../media/loading_screen.png)

Une fois le paiement terminé, la page Web appelle la [`complete()`](https://msdn.microsoft.com/library/mt790642) méthode et transmet une valeur de **réussite** ou d' **échec**.  La [`complete()`](https://msdn.microsoft.com/library/mt790642) méthode informe le navigateur que l’achat est terminé et l’écran de l’interface utilisateur de fin appropriée doit être affiché en fonction de la valeur de **Success** ou **Fail**. 

![Interface utilisateur affichée lors de la réussite de l’achat de l' ](./../media/response_payment-request_complete.png)
![ interface utilisateur lors de l’échec de l’achat](./../media/response_payment-request_failure.png)

## Demande de paiement avec livraison

### Adresse de livraison

Pour les ventes qui nécessitent des produits physiques d’expédition, une adresse de livraison est requise.  Pour inclure une adresse de livraison, définissez `requestShipping = True` le [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre de la requête.   

Lorsque l’utilisateur sélectionne ou met à jour l’adresse de livraison, l' [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) événement s’exécute.  Le site Web, à l’aide d’un écouteur d’événements, sera considéré comme le changement et peut ensuite valider l’adresse, recalculer les coûts d’expédition et les taxes, et le mettre à jour [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) pour refléter les changements de coûts et les options d’expédition disponibles pour l’adresse sélectionnée (le cas échéant). 

### Options d’expédition 

Les options d’expédition peuvent être présentées au client en [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) l’ajoutant au [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre.  Vous pouvez établir une valeur par défaut en définissant l' `selected = True` une des options d’expédition. 
 
Lorsque l’utilisateur sélectionne ou met à jour le shippingOptions, l' [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) événement s’exécute.  Le site Web, à l’aide d’un écouteur d’événements, est consciente de la modification et peut mettre à jour le [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre avec le montant d’expédition correct.   

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
 
```

## Informations de référence sur les API
[API de demande de paiement](https://msdn.microsoft.com/library/mt790447)

## Spécifier
[API de demande de paiement](https://w3.org/TR/payment-request/)
