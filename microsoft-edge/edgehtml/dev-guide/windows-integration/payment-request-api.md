---
description: Découvrez comment l’API de demande de paiement permet à Microsoft Edge d’agir en tant qu’intermédiaire entre commerçants, consommateurs et modes de paiement client stockés dans le Cloud.
title: API de demande de paiement-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: efcad701fec73f858fa9490f12b094259cd8c793
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233065"
---
# API de demande de paiement (EdgeHTML)  

> [!NOTE]
> Cet article décrit le flux de travail pris en charge dans la [version héritée de Microsoft Edge][MicrosoftSupport44533505].  Microsoft Edge \(chrome \) prend en charge l’API de demande de paiement avec une autre implémentation basée sur le projet de chrome.  

Les ventes de commerce électronique continuent de croître à un rythme rapide.  D’après [eMarketer](https://www.emarketer.com), les ventes numériques 2018 sont prévues pour une augmentation de 23% par rapport aux niveaux mesurés en 2013.  Si les particuliers et les entreprises jouissent de la commodité des ventes de commerce électronique, les problèmes persistent.  Dès à présent, chaque propriétaire de site Web d’e-commerce doit investir du temps pour développer des flux d’extraction de paiement et des règles de validation de grande qualité.  Les consommateurs doivent parcourir les différents flux d’extraction de paiement et entrer de nouveau les mêmes informations de paiement et d’expédition sur chaque site.  Cela peut prendre du temps et frustrant pour les particuliers, ce qui a pour principal taux d’abandon de panier d’achat et de diminution des ventes pour les commerçants.  L' [estimation](http://baymard.com/lists/cart-abandonment-rate) des commerçants entre 60% et 70% des paniers d’achat est abandonnée.  

L' [API de demande de paiement](https://w3.org/TR/payment-request) standardise le processus de validation du paiement.  Cette API nécessite moins de personnalisation pour les développeurs Web et offre une connaissance plus rapide, plus cohérente et donc plus déroutante pour les consommateurs.  Dans la mesure où les consommateurs peuvent sélectionner des instruments de paiement et des adresses d’expédition à partir de leur compte Microsoft, il est nécessaire d’entrer moins de données pour effectuer des achats qui réduit le temps et la saisie de données requises pour effectuer un paiement.  

L' [API de demande de paiement](https://w3.org/TR/payment-request) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et les modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.  
  
En résumé, lors de l’utilisation de l' [API de demande de paiement](https://w3.org/TR/payment-request), les clients achètent le site Web commerçant normalement.  Lorsque vous êtes prêt à payer, le site Web du commerçant appelle l’API de **demande de paiement** pour créer une **demande de paiement** et transmet les informations de paiement pertinentes (par exemple, modes de paiement pris en charge, montant de l’achat, devise, etc.) au navigateur.  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Constitution d’une demande de paiement" lightbox="../media/payment_request_construct.png":::
   Constitution d’une demande de paiement  
:::image-end:::  

Le navigateur authentifie l’utilisateur, permet à l’utilisateur de sélectionner un mode de paiement pris en charge sur un fichier et traite les détails du paiement.  Le navigateur envoie ensuite les informations de paiement au site Web du commerçant pour que le commerçant puisse terminer le paiement.  En plus de recevoir des informations de paiement, le commerçant peut également choisir de recevoir des informations d’expédition dans le cadre de la **demande de paiement**.  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construction de réponse de paiement" lightbox="../media/payment_response_construct.png":::
   Construction de réponse de paiement  
:::image-end:::  

Pour afficher une API de demande de paiement en action, et obtenir une vue d’ensemble de son utilisation, regardez cette vidéo.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> L’API de demande de paiement est prise en charge dans Microsoft Edge Build 14992 ou une version ultérieure.  

## Création d’une demande de paiement  

Les pages Web créent une **demande de paiement** en règle générale lorsque l’utilisateur démarre un processus de paiement en cliquant sur le bouton «acheter».  Le **** [constructeur](/previous-versions/mt790440(v=vs.85)) de votre demande de paiement inclut methodData, les détails et les options.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

Le paramètre [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contient une liste des modes de paiement et des réseaux acceptés par le site Web, ainsi que les données spécifiques du mode de paiement associé.  Dans Microsoft Edge, cette liste est mise en correspondance avec les modes de paiement pris en charge que l’acheteur a enregistrés sur son compte Microsoft et génère la liste «payer avec» dans l’interface utilisateur du paiement.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Liste payer avec dans l’interface utilisateur de Microsoft Wallet" lightbox="../media/pay_with.png":::
         Liste **payer avec** dans l’interface utilisateur de Microsoft Wallet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

Le paramètre [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contient des informations que le commerçant souhaite communiquer au client à propos de la transaction.  Il s’agit notamment des éléments de synthèse tels que total, taxe, montant d’expédition et autres niveaux de synthèse ayant un impact sur le montant du paiement.  Celles-ci ne sont pas destinées à être commandées.  
  
Le paramètre [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) permet également de définir les options d’expédition disponibles pour le client, le cas échéant.  Pour plus d’informations, reportez-vous à la section **paiement** avec la section expédition ci-dessous.  

Chaque ligne de [détail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) inclut une étiquette pour la devise et le montant.  

> [!NOTE]
> La **demande de paiement** ne calcule pas la somme ou le total de ces montants.  Il incombe au site Web du commerçant de s’assurer que le total de ses lignes est correct.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Détails du sous-total, de l’expédition, des taxes et du total" lightbox="../media/show_details.png":::
         Détails du sous-total, de l’expédition, des taxes et du total  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
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
   :::column-end:::
:::row-end:::  

[PaymentRequest](/previous-versions/mt790440(v=vs.85)) ne prend pas en charge le remboursement; les montants doivent donc toujours être positifs; les éléments de liste individuels peuvent être négatifs, tels que les remises.  

Le navigateur affiche les étiquettes lorsque vous les définissez et affiche automatiquement la mise en forme de devise appropriée selon les paramètres régionaux du client.  Notez que les étiquettes doivent être affichées dans la même langue que votre contenu.  

Le paramètre [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) définit les données souhaitées dans la page Web à partir de la **demande de paiement**.  Cela définit également les données qui doivent être collectées, notamment en cas d’expédition, d’adresse e-mail, de numéro de téléphone ou du tout.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Liste déroulante adresse e-mail" lightbox="../media/email_snippet.png":::
         Liste déroulante adresse e-mail  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## Affichage de la demande de paiement  

La méthode [Show ()](/previous-versions/mt790448(v=vs.85)) est appelée par la page Web pour permettre à l’utilisateur d’interagir avec l’interface utilisateur de la **demande de paiement** .  La méthode [Show ()](/previous-versions/mt790448(v=vs.85)) renvoie une promesse qui sera résolue lorsque l’utilisateur autorise la demande de paiement.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmer et payer les détails" lightbox="../media/pay_screen_default.png":::
         Confirmer et payer les détails  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## Abandon d’une demande de paiement  
 
La méthode [Abort ()](/previous-versions/mt790437(v=vs.85)) peut être appelée à tout moment après l’appel de la méthode [Show ()](/previous-versions/mt790448(v=vs.85)) , jusqu’à ce que la promesse soit résolue.  La méthode [Abort ()](/previous-versions/mt790437(v=vs.85)) a pour effet d’annuler la **demande de paiement** par le navigateur et de fermer l’interface utilisateur de votre demande de **paiement** .  Par exemple, une page Web est susceptible de se terminer si l’utilisateur n’a pas terminé la transaction dans la durée requise.  

```javascript
payment.abort();
```  

## Réponse de paiement  
Lorsque le client approuve la **demande de paiement**, une **réponse de paiement** est renvoyée au site Web.  Le **bordereau de réponse** comprend les éléments suivants:  

 Propriété      | Description | Requis | Informations supplémentaires
|---------------|-----------------|-------|-----------------|
[NomMéthode](/previous-versions/mt790656(v=vs.85)) | ID du mode de paiement sélectionné par l’utilisateur. | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Un objet JSON qui inclut toutes les données requises par le commerçant pour traiter la transaction à l’aide du mode de paiement sélectionné ou d’un jeton de paiement. | Y | [Carte de base](https://w3c.github.io/payment-method-basic-card) Dictionnaire: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
[shippingAddress](/previous-versions/mt790445(v=vs.85)) | Adresse d’expédition sélectionnée par l’utilisateur  |  Facultatif.  Obligatoire lorsque [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est `True`  | Dictionnaire d’adresses: pays; addressLine; Region urbains dependentLocality; CodePostal sortingCode; languageCode; société destinataire Répertoire |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | ID de l’option d’expédition sélectionnée | Facultatif.  Obligatoire lorsque [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est `True`  | |   
[payerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Nom fourni par l’utilisateur.  | Facultatif.  Obligatoire lorsque [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Adresse e-mail sélectionnée par l’utilisateur | Facultatif.  Obligatoire lorsque [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Le numéro de téléphone sélectionné par l’utilisateur | Facultatif.  Obligatoire lorsque [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est `True` | |  

L’objet JSON [Détails](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) de la **réponse au paiement** contient les données de paiement requises par le commerçant pour traiter un paiement.  Dans sa forme la plus simple, la réponse sera une charge utile de [carte de base](https://w3c.github.io/payment-method-basic-card) contenant les détails de la carte de paiement en clair.  Lorsque les commerçants disposent de contrats avec des partenaires passerelle/processeur supplémentaires pour leur permettre de prendre en charge des paiements, le commerçant peut nécessiter une charge utile que le processeur peut gérer.  Celles-ci peuvent prendre la forme d’un jeton de processeur/passerelle ou d’un instrument de paiement chiffré.  Ces modes de paiement font partie du cadre de ce document et seront couverts dans la documentation propre au processeur.  Par ailleurs, pour recevoir une réponse de base à une [carte](https://w3c.github.io/payment-method-basic-card) , aucun intégration supplémentaire à Microsoft n’est requise par le développeur, contrairement aux autres modes de paiement pour les processeurs et passerelles, qui pourraient nécessiter l’intégration de la clé de chiffrement ou la demande d’autorisation (OAuth \).  

Lors de la réception d’une **réponse de paiement**, le site Web transmet les informations de paiement à son processeur de paiement.  Le navigateur va afficher une page de compteur pendant le traitement du paiement.  

:::image type="complex" source="../media/loading_screen.png" alt-text="Page affichée lors du traitement du paiement" lightbox="../media/loading_screen.png":::
   Page affichée lors du traitement du paiement  
:::image-end:::  

Une fois le paiement terminé, la page Web appelle la méthode [Complete ()](/previous-versions/mt790642(v=vs.85)) et transmet une valeur de **réussite** ou d' **échec**.  La méthode [Complete ()](/previous-versions/mt790642(v=vs.85)) informe le navigateur que l’achat est terminé et l’écran de l’interface utilisateur de fin appropriée doit être affiché en fonction de la valeur de **Success** ou **Fail**.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Interface utilisateur affichée lors de la réussite de l’achat" lightbox="../media/response_payment-request_complete.png":::
         Interface utilisateur affichée lors de la réussite de l’achat  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Interface utilisateur affichée lors de l’échec de l’achat" lightbox="../media/response_payment-request_failure.png":::
         Interface utilisateur affichée lors de l’échec de l’achat  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Demande de paiement avec livraison  

### Adresse de livraison  

Pour les ventes qui nécessitent des produits physiques d’expédition, une adresse de livraison est requise.  Pour inclure une adresse d’expédition, définissez `requestShipping = True` le paramètre [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) de la requête.  

Lorsque l’utilisateur sélectionne ou met à jour l’adresse de livraison, l’événement [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) est exécuté.  Le site Web, à l’aide d’un écouteur d’événements, sera averti de la modification et pourra ensuite valider l’adresse, recalculer les coûts d’expédition et les taxes, et mettre à jour [shippingOptions](/previous-versions/mt790440(v=vs.85)) pour refléter les coûts et les options d’expédition disponibles pour l’adresse sélectionnée \(le cas échéant).  

### Options d’expédition  

Les options d’expédition peuvent être présentées au client en ajoutant [shippingOptions](/previous-versions/mt790440(v=vs.85)) au paramètre [Détails](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .  Vous pouvez établir une valeur par défaut en définissant l' `selected = True` une des options d’expédition.  
 
Lorsque l’utilisateur sélectionne ou met à jour le shippingOptions, l’événement [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) s’exécute.  Le site Web, à l’aide d’un écouteur d’événements, sera consciente du changement et peut mettre à jour le paramètre de [Détails](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) avec le montant d’expédition correct.  

```javascript
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

[API de demande de paiement](/previous-versions/mt790447(v=vs.85))  

## Spécifier
[API de demande de paiement](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Qu’est-ce que Microsoft Edge hérité?"  
