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
# <span data-ttu-id="25621-104">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-104">Payment Request API</span></span>

<span data-ttu-id="25621-105">Les ventes de commerce électronique continuent de croître à un rythme rapide.</span><span class="sxs-lookup"><span data-stu-id="25621-105">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="25621-106">D’après [eMarketer](https://www.emarketer.com/), les ventes numériques 2018 sont prévues pour une augmentation de 23% par rapport aux niveaux mesurés en 2013.</span><span class="sxs-lookup"><span data-stu-id="25621-106">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="25621-107">Si les particuliers et les entreprises jouissent de la commodité des ventes de commerce électronique, les problèmes persistent.</span><span class="sxs-lookup"><span data-stu-id="25621-107">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="25621-108">Dès à présent, chaque propriétaire de site Web d’e-commerce doit investir du temps pour développer des flux d’extraction de paiement et des règles de validation de grande qualité.</span><span class="sxs-lookup"><span data-stu-id="25621-108">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="25621-109">Les consommateurs doivent parcourir les différents flux d’extraction de paiement et entrer de nouveau les mêmes informations de paiement et d’expédition sur chaque site.</span><span class="sxs-lookup"><span data-stu-id="25621-109">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="25621-110">Cela peut prendre du temps et frustrant pour les particuliers, ce qui a pour principal taux d’abandon de panier d’achat et de diminution des ventes pour les commerçants.</span><span class="sxs-lookup"><span data-stu-id="25621-110">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="25621-111">L' [estimation](http://baymard.com/lists/cart-abandonment-rate) des commerçants entre 60% et 70% des paniers d’achat est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="25621-111">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="25621-112">L' [API de demande de paiement](https://w3.org/TR/payment-request/) standardise le processus de validation du paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-112">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="25621-113">Cette API nécessite moins de personnalisation pour les développeurs Web et offre une connaissance plus rapide, plus cohérente et donc plus déroutante pour les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="25621-113">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="25621-114">Dans la mesure où les consommateurs peuvent sélectionner des instruments de paiement et des adresses d’expédition à partir de leur compte Microsoft, il est nécessaire d’entrer moins de données pour effectuer des achats qui réduit le temps et la saisie de données requises pour effectuer un paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-114">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="25621-115">L' [API de demande de paiement](https://w3.org/TR/payment-request/) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et les modes de paiement (par exemple, cartes de crédit) stockés dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="25621-115">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="25621-116">En résumé, lors de l’utilisation de l' [API de demande de paiement](https://w3.org/TR/payment-request/), les clients achètent le site Web commerçant normalement.</span><span class="sxs-lookup"><span data-stu-id="25621-116">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="25621-117">Lorsque vous êtes prêt à payer, le site Web du commerçant appelle l’API de **demande de paiement** pour créer une **demande de paiement** et transmet les informations de paiement pertinentes (par exemple, modes de paiement pris en charge, montant de l’achat, devise, etc.) au navigateur.</span><span class="sxs-lookup"><span data-stu-id="25621-117">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Constitution d’une demande de paiement](./../media/payment_request_construct.png)

<span data-ttu-id="25621-119">Le navigateur authentifie l’utilisateur, permet à l’utilisateur de sélectionner un mode de paiement pris en charge sur un fichier et traite les détails du paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-119">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="25621-120">Le navigateur envoie ensuite les informations de paiement au site Web du commerçant pour que le commerçant puisse terminer le paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-120">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="25621-121">En plus de recevoir des informations de paiement, le commerçant peut également choisir de recevoir des informations d’expédition dans le cadre de la **demande de paiement**.</span><span class="sxs-lookup"><span data-stu-id="25621-121">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Construction de réponse de paiement](./../media/payment_response_construct.png)

<span data-ttu-id="25621-123">Pour afficher une API de demande de paiement en action, et obtenir une vue d’ensemble de son utilisation, regardez cette vidéo.</span><span class="sxs-lookup"><span data-stu-id="25621-123">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="25621-124">L’API de demande de paiement est prise en charge dans Microsoft Edge Build 14992 +.</span><span class="sxs-lookup"><span data-stu-id="25621-124">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="25621-125">Création d’une demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-125">Creating a Payment Request</span></span> 
<span data-ttu-id="25621-126">Les pages Web créent une **demande de paiement** en règle générale lorsque l’utilisateur démarre un processus de paiement en cliquant sur le bouton «acheter».</span><span class="sxs-lookup"><span data-stu-id="25621-126">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="25621-127">Le **Payment Request** [constructeur](https://msdn.microsoft.com/library/mt790440) de votre demande de paiement inclut methodData, les détails et les options.</span><span class="sxs-lookup"><span data-stu-id="25621-127">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="25621-128">Ce [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre contient une liste des modes de paiement et des réseaux acceptés par le site Web et les données spécifiques du mode de paiement associé.</span><span class="sxs-lookup"><span data-stu-id="25621-128">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="25621-129">Dans Microsoft Edge, cette liste est mise en correspondance avec les modes de paiement pris en charge que l’acheteur a enregistrés sur son compte Microsoft et génère la liste «payer avec» dans l’interface utilisateur du paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-129">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

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

<span data-ttu-id="25621-131">Le [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre contient des informations que le commerçant souhaite communiquer au client à propos de la transaction.</span><span class="sxs-lookup"><span data-stu-id="25621-131">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="25621-132">Il s’agit notamment des éléments de synthèse tels que total, taxe, montant d’expédition et autres niveaux de synthèse ayant un impact sur le montant du paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-132">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="25621-133">Celles-ci ne sont pas destinées à être commandées.</span><span class="sxs-lookup"><span data-stu-id="25621-133">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="25621-134">Ce [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre permet également de définir les options d’expédition disponibles pour le client, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="25621-134">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="25621-135">Pour plus d’informations, reportez-vous à la section **paiement** avec la section expédition ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="25621-135">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="25621-136">Chaque [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) ligne inclut une étiquette pour la devise et le montant.</span><span class="sxs-lookup"><span data-stu-id="25621-136">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="25621-137">La **demande de paiement** ne calcule pas la somme ou le total de ces montants.</span><span class="sxs-lookup"><span data-stu-id="25621-137">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="25621-138">Il incombe au site Web du commerçant de s’assurer que le total de ses lignes est correct.</span><span class="sxs-lookup"><span data-stu-id="25621-138">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


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

<span data-ttu-id="25621-140">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)ne prend pas en charge le remboursement; les montants doivent donc toujours être positifs; les éléments de liste individuels peuvent être négatifs, tels que les remises.</span><span class="sxs-lookup"><span data-stu-id="25621-140">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="25621-141">Le navigateur affiche les étiquettes lorsque vous les définissez et affiche automatiquement la mise en forme de devise appropriée selon les paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="25621-141">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="25621-142">Notez que les étiquettes doivent être affichées dans la même langue que votre contenu.</span><span class="sxs-lookup"><span data-stu-id="25621-142">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="25621-143">Le [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre définit les données retournées par la page Web à partir de la **demande de paiement**.</span><span class="sxs-lookup"><span data-stu-id="25621-143">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="25621-144">Cela définit également les données qui doivent être collectées, notamment si la livraison, l’adresse de messagerie et/ou le numéro de téléphone sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="25621-144">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Liste déroulante adresse e-mail](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="25621-146">Affichage de la demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-146">Showing the Payment Request</span></span>

<span data-ttu-id="25621-147">La [`show()`](https://msdn.microsoft.com/library/mt790448) méthode est appelée par la page Web pour permettre à l’utilisateur d’interagir avec l’interface utilisateur de la **demande de paiement** .</span><span class="sxs-lookup"><span data-stu-id="25621-147">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="25621-148">La [`show()`](https://msdn.microsoft.com/library/mt790448) méthode renvoie une promesse qui sera résolue lorsque l’utilisateur autorise la demande de paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-148">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmer et payer les détails](./../media/pay_screen_default.png)

## <span data-ttu-id="25621-150">Abandon d’une demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-150">Aborting a Payment Request</span></span>
 
<span data-ttu-id="25621-151">La [`abort()`](https://msdn.microsoft.com/library/mt790437) méthode peut être appelée à tout moment après l’appel de la [`show()`](https://msdn.microsoft.com/library/mt790448) méthode, jusqu’à la date à laquelle la promesse est résolue.</span><span class="sxs-lookup"><span data-stu-id="25621-151">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="25621-152">La [`abort()`](https://msdn.microsoft.com/library/mt790437) méthode entraînera l’annulation de la **demande de paiement** par le navigateur, et la fermeture de l’interface utilisateur de votre **demande de paiement** .</span><span class="sxs-lookup"><span data-stu-id="25621-152">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="25621-153">Par exemple, une page Web est susceptible de se terminer si l’utilisateur n’a pas terminé la transaction dans la durée requise.</span><span class="sxs-lookup"><span data-stu-id="25621-153">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="25621-154">Réponse de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-154">Payment Response</span></span>
<span data-ttu-id="25621-155">Lorsque le client approuve la **demande de paiement**, une **réponse de paiement** est renvoyée au site Web.</span><span class="sxs-lookup"><span data-stu-id="25621-155">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="25621-156">Le **bordereau de réponse** comprend les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="25621-156">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="25621-157">Propriété</span><span class="sxs-lookup"><span data-stu-id="25621-157">Property</span></span>      | <span data-ttu-id="25621-158">Description</span><span class="sxs-lookup"><span data-stu-id="25621-158">Description</span></span> | <span data-ttu-id="25621-159">Requis</span><span class="sxs-lookup"><span data-stu-id="25621-159">Required</span></span> | <span data-ttu-id="25621-160">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="25621-160">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="25621-161">ID du mode de paiement sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="25621-161">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="25621-162">Y</span><span class="sxs-lookup"><span data-stu-id="25621-162">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="25621-163">Un objet JSON qui inclut toutes les données requises par le commerçant pour traiter la transaction à l’aide du mode de paiement sélectionné ou d’un jeton de paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-163">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="25621-164">Y</span><span class="sxs-lookup"><span data-stu-id="25621-164">Y</span></span> | <span data-ttu-id="25621-165">[Carte de base](https://go.microsoft.com/fwlink/?linkid=834965) Dictionnaire: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="25621-165">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="25621-166">Adresse d’expédition sélectionnée par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="25621-166">The shipping address selected by the user</span></span>  |  <span data-ttu-id="25621-167">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="25621-167">Optional.</span></span> <span data-ttu-id="25621-168">Obligatoire lorsque [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**</span><span class="sxs-lookup"><span data-stu-id="25621-168">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="25621-169">Dictionnaire d’adresses: pays; addressLine; Region urbains dependentLocality; CodePostal sortingCode; languageCode; société destinataire Répertoire</span><span class="sxs-lookup"><span data-stu-id="25621-169">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="25621-170">ID de l’option d’expédition sélectionnée</span><span class="sxs-lookup"><span data-stu-id="25621-170">The ID for the selected shipping option</span></span> | <span data-ttu-id="25621-171">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="25621-171">Optional.</span></span> <span data-ttu-id="25621-172">Obligatoire lorsque [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**</span><span class="sxs-lookup"><span data-stu-id="25621-172">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="25621-173">Nom fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="25621-173">The name provided by the user</span></span>  | <span data-ttu-id="25621-174">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="25621-174">Optional.</span></span> <span data-ttu-id="25621-175">Obligatoire lorsque [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**</span><span class="sxs-lookup"><span data-stu-id="25621-175">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="25621-176">Adresse e-mail sélectionnée par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="25621-176">The email address selected by the user</span></span> | <span data-ttu-id="25621-177">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="25621-177">Optional.</span></span> <span data-ttu-id="25621-178">Obligatoire lorsque [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**</span><span class="sxs-lookup"><span data-stu-id="25621-178">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="25621-179">Le numéro de téléphone sélectionné par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="25621-179">The phone number selected by the user</span></span> | <span data-ttu-id="25621-180">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="25621-180">Optional.</span></span> <span data-ttu-id="25621-181">Obligatoire lorsque [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) a la **valeur vrai**</span><span class="sxs-lookup"><span data-stu-id="25621-181">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="25621-182">L' [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objet JSON dans la **réponse de paiement** contient les données de paiement requises par le commerçant pour traiter un paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-182">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="25621-183">Dans sa forme la plus simple, la réponse sera une charge utile de [carte de base](https://go.microsoft.com/fwlink/?linkid=834965) contenant les détails de la carte de paiement en clair.</span><span class="sxs-lookup"><span data-stu-id="25621-183">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="25621-184">Lorsque les commerçants disposent de contrats avec des partenaires passerelle/processeur supplémentaires pour leur permettre de prendre en charge des paiements, le commerçant peut nécessiter une charge utile que le processeur peut gérer.</span><span class="sxs-lookup"><span data-stu-id="25621-184">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="25621-185">Celles-ci peuvent prendre la forme d’un jeton de processeur/passerelle ou d’un instrument de paiement chiffré.</span><span class="sxs-lookup"><span data-stu-id="25621-185">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="25621-186">Ces modes de paiement font partie du cadre de ce document et seront couverts dans la documentation propre au processeur.</span><span class="sxs-lookup"><span data-stu-id="25621-186">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="25621-187">Par ailleurs, pour recevoir une réponse de base à une [carte](https://go.microsoft.com/fwlink/?linkid=834965) , aucun intégration supplémentaire à Microsoft n’est requise par le développeur, contrairement aux autres modes de paiement pour les processeurs et les passerelles, qui pourraient nécessiter une autorisation d’intégration de clé de chiffrement ou de demande d’autorisation (OAuth).</span><span class="sxs-lookup"><span data-stu-id="25621-187">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="25621-188">Lors de la réception d’une **réponse de paiement**, le site Web transmet les informations de paiement à son processeur de paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-188">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="25621-189">Le navigateur va afficher une page de compteur pendant le traitement du paiement.</span><span class="sxs-lookup"><span data-stu-id="25621-189">The browser will display a spinner page while the payment is being processed.</span></span>

![Page affichée lors du traitement du paiement](./../media/loading_screen.png)

<span data-ttu-id="25621-191">Une fois le paiement terminé, la page Web appelle la [`complete()`](https://msdn.microsoft.com/library/mt790642) méthode et transmet une valeur de **réussite** ou d' **échec**.</span><span class="sxs-lookup"><span data-stu-id="25621-191">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="25621-192">La [`complete()`](https://msdn.microsoft.com/library/mt790642) méthode informe le navigateur que l’achat est terminé et l’écran de l’interface utilisateur de fin appropriée doit être affiché en fonction de la valeur de **Success** ou **Fail**.</span><span class="sxs-lookup"><span data-stu-id="25621-192">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="25621-193">Interface utilisateur affichée lors de la réussite de l’achat de l' ](./../media/response_payment-request_complete.png)
![ interface utilisateur lors de l’échec de l’achat</span><span class="sxs-lookup"><span data-stu-id="25621-193">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="25621-194">Demande de paiement avec livraison</span><span class="sxs-lookup"><span data-stu-id="25621-194">Payment Request with Shipping</span></span>

### <span data-ttu-id="25621-195">Adresse de livraison</span><span class="sxs-lookup"><span data-stu-id="25621-195">Shipping Address</span></span>

<span data-ttu-id="25621-196">Pour les ventes qui nécessitent des produits physiques d’expédition, une adresse de livraison est requise.</span><span class="sxs-lookup"><span data-stu-id="25621-196">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="25621-197">Pour inclure une adresse de livraison, définissez `requestShipping = True` le [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre de la requête.</span><span class="sxs-lookup"><span data-stu-id="25621-197">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="25621-198">Lorsque l’utilisateur sélectionne ou met à jour l’adresse de livraison, l' [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) événement s’exécute.</span><span class="sxs-lookup"><span data-stu-id="25621-198">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="25621-199">Le site Web, à l’aide d’un écouteur d’événements, sera considéré comme le changement et peut ensuite valider l’adresse, recalculer les coûts d’expédition et les taxes, et le mettre à jour [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) pour refléter les changements de coûts et les options d’expédition disponibles pour l’adresse sélectionnée (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="25621-199">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="25621-200">Options d’expédition</span><span class="sxs-lookup"><span data-stu-id="25621-200">Shipping Options</span></span> 

<span data-ttu-id="25621-201">Les options d’expédition peuvent être présentées au client en [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) l’ajoutant au [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre.</span><span class="sxs-lookup"><span data-stu-id="25621-201">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="25621-202">Vous pouvez établir une valeur par défaut en définissant l' `selected = True` une des options d’expédition.</span><span class="sxs-lookup"><span data-stu-id="25621-202">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="25621-203">Lorsque l’utilisateur sélectionne ou met à jour le shippingOptions, l' [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) événement s’exécute.</span><span class="sxs-lookup"><span data-stu-id="25621-203">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="25621-204">Le site Web, à l’aide d’un écouteur d’événements, est consciente de la modification et peut mettre à jour le [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) paramètre avec le montant d’expédition correct.</span><span class="sxs-lookup"><span data-stu-id="25621-204">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

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

## <span data-ttu-id="25621-205">Informations de référence sur les API</span><span class="sxs-lookup"><span data-stu-id="25621-205">API Reference</span></span>
[<span data-ttu-id="25621-206">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-206">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="25621-207">Spécifier</span><span class="sxs-lookup"><span data-stu-id="25621-207">Specification</span></span>
[<span data-ttu-id="25621-208">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="25621-208">Payment Request API</span></span>](https://w3.org/TR/payment-request/)
