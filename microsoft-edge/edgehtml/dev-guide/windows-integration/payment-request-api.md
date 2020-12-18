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
# <span data-ttu-id="abb34-104">API de demande de paiement (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="abb34-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="abb34-105">Cet article décrit le flux de travail pris en charge dans la [version héritée de Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="abb34-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="abb34-106">Microsoft Edge \ (chrome \) prend en charge l’API de demande de paiement avec une autre implémentation basée sur le projet de chrome.</span><span class="sxs-lookup"><span data-stu-id="abb34-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="abb34-107">Les ventes de commerce électronique continuent de croître à un rythme rapide.</span><span class="sxs-lookup"><span data-stu-id="abb34-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="abb34-108">D’après [eMarketer](https://www.emarketer.com), les ventes numériques 2018 sont prévues pour une augmentation de 23% par rapport aux niveaux mesurés en 2013.</span><span class="sxs-lookup"><span data-stu-id="abb34-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="abb34-109">Si les particuliers et les entreprises jouissent de la commodité des ventes de commerce électronique, les problèmes persistent.</span><span class="sxs-lookup"><span data-stu-id="abb34-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="abb34-110">Dès à présent, chaque propriétaire de site Web d’e-commerce doit investir du temps pour développer des flux d’extraction de paiement et des règles de validation de grande qualité.</span><span class="sxs-lookup"><span data-stu-id="abb34-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="abb34-111">Les consommateurs doivent parcourir les différents flux d’extraction de paiement et entrer de nouveau les mêmes informations de paiement et d’expédition sur chaque site.</span><span class="sxs-lookup"><span data-stu-id="abb34-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="abb34-112">Cela peut prendre du temps et frustrant pour les particuliers, ce qui a pour principal taux d’abandon de panier d’achat et de diminution des ventes pour les commerçants.</span><span class="sxs-lookup"><span data-stu-id="abb34-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="abb34-113">L' [estimation](http://baymard.com/lists/cart-abandonment-rate) des commerçants entre 60% et 70% des paniers d’achat est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="abb34-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="abb34-114">L' [API de demande de paiement](https://w3.org/TR/payment-request) standardise le processus de validation du paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="abb34-115">Cette API nécessite moins de personnalisation pour les développeurs Web et offre une connaissance plus rapide, plus cohérente et donc plus déroutante pour les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="abb34-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="abb34-116">Dans la mesure où les consommateurs peuvent sélectionner des instruments de paiement et des adresses d’expédition à partir de leur compte Microsoft, il est nécessaire d’entrer moins de données pour effectuer des achats qui réduit le temps et la saisie de données requises pour effectuer un paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="abb34-117">L' [API de demande de paiement](https://w3.org/TR/payment-request) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et les modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="abb34-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="abb34-118">En résumé, lors de l’utilisation de l' [API de demande de paiement](https://w3.org/TR/payment-request), les clients achètent le site Web commerçant normalement.</span><span class="sxs-lookup"><span data-stu-id="abb34-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="abb34-119">Lorsque vous êtes prêt à payer, le site Web du commerçant appelle l’API de **demande de paiement** pour créer une **demande de paiement** et transmet les informations de paiement pertinentes (par exemple, modes de paiement pris en charge, montant de l’achat, devise, etc.) au navigateur.</span><span class="sxs-lookup"><span data-stu-id="abb34-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Constitution d’une demande de paiement" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="abb34-121">Constitution d’une demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="abb34-122">Le navigateur authentifie l’utilisateur, permet à l’utilisateur de sélectionner un mode de paiement pris en charge sur un fichier et traite les détails du paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="abb34-123">Le navigateur envoie ensuite les informations de paiement au site Web du commerçant pour que le commerçant puisse terminer le paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="abb34-124">En plus de recevoir des informations de paiement, le commerçant peut également choisir de recevoir des informations d’expédition dans le cadre de la **demande de paiement**.</span><span class="sxs-lookup"><span data-stu-id="abb34-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construction de réponse de paiement" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="abb34-126">Construction de réponse de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="abb34-127">Pour afficher une API de demande de paiement en action, et obtenir une vue d’ensemble de son utilisation, regardez cette vidéo.</span><span class="sxs-lookup"><span data-stu-id="abb34-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="abb34-128">L’API de demande de paiement est prise en charge dans Microsoft Edge Build 14992 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="abb34-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="abb34-129">Création d’une demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-129">Creating a Payment Request</span></span>  

<span data-ttu-id="abb34-130">Les pages Web créent une **demande de paiement** en règle générale lorsque l’utilisateur démarre un processus de paiement en cliquant sur le bouton «acheter».</span><span class="sxs-lookup"><span data-stu-id="abb34-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="abb34-131">Le \*\*\*\* [constructeur](/previous-versions/mt790440(v=vs.85)) de votre demande de paiement inclut methodData, les détails et les options.</span><span class="sxs-lookup"><span data-stu-id="abb34-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="abb34-132">Le paramètre [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contient une liste des modes de paiement et des réseaux acceptés par le site Web, ainsi que les données spécifiques du mode de paiement associé.</span><span class="sxs-lookup"><span data-stu-id="abb34-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="abb34-133">Dans Microsoft Edge, cette liste est mise en correspondance avec les modes de paiement pris en charge que l’acheteur a enregistrés sur son compte Microsoft et génère la liste «payer avec» dans l’interface utilisateur du paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Liste payer avec dans l’interface utilisateur de Microsoft Wallet" lightbox="../media/pay_with.png":::
         <span data-ttu-id="abb34-135">Liste **payer avec** dans l’interface utilisateur de Microsoft Wallet</span><span class="sxs-lookup"><span data-stu-id="abb34-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
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

<span data-ttu-id="abb34-136">Le paramètre [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contient des informations que le commerçant souhaite communiquer au client à propos de la transaction.</span><span class="sxs-lookup"><span data-stu-id="abb34-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="abb34-137">Il s’agit notamment des éléments de synthèse tels que total, taxe, montant d’expédition et autres niveaux de synthèse ayant un impact sur le montant du paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="abb34-138">Celles-ci ne sont pas destinées à être commandées.</span><span class="sxs-lookup"><span data-stu-id="abb34-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="abb34-139">Le paramètre [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) permet également de définir les options d’expédition disponibles pour le client, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="abb34-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="abb34-140">Pour plus d’informations, reportez-vous à la section **paiement** avec la section expédition ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="abb34-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="abb34-141">Chaque ligne de [détail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) inclut une étiquette pour la devise et le montant.</span><span class="sxs-lookup"><span data-stu-id="abb34-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="abb34-142">La **demande de paiement** ne calcule pas la somme ou le total de ces montants.</span><span class="sxs-lookup"><span data-stu-id="abb34-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="abb34-143">Il incombe au site Web du commerçant de s’assurer que le total de ses lignes est correct.</span><span class="sxs-lookup"><span data-stu-id="abb34-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Détails du sous-total, de l’expédition, des taxes et du total" lightbox="../media/show_details.png":::
         <span data-ttu-id="abb34-145">Détails du sous-total, de l’expédition, des taxes et du total</span><span class="sxs-lookup"><span data-stu-id="abb34-145">Subtotal, shipping, taxes, and total details</span></span>  
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

<span data-ttu-id="abb34-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) ne prend pas en charge le remboursement; les montants doivent donc toujours être positifs; les éléments de liste individuels peuvent être négatifs, tels que les remises.</span><span class="sxs-lookup"><span data-stu-id="abb34-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="abb34-147">Le navigateur affiche les étiquettes lorsque vous les définissez et affiche automatiquement la mise en forme de devise appropriée selon les paramètres régionaux du client.</span><span class="sxs-lookup"><span data-stu-id="abb34-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="abb34-148">Notez que les étiquettes doivent être affichées dans la même langue que votre contenu.</span><span class="sxs-lookup"><span data-stu-id="abb34-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="abb34-149">Le paramètre [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) définit les données souhaitées dans la page Web à partir de la **demande de paiement**.</span><span class="sxs-lookup"><span data-stu-id="abb34-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="abb34-150">Cela définit également les données qui doivent être collectées, notamment en cas d’expédition, d’adresse e-mail, de numéro de téléphone ou du tout.</span><span class="sxs-lookup"><span data-stu-id="abb34-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Liste déroulante adresse e-mail" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="abb34-152">Liste déroulante adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="abb34-152">Email address dropdown</span></span>  
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

## <span data-ttu-id="abb34-153">Affichage de la demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-153">Showing the Payment Request</span></span>  

<span data-ttu-id="abb34-154">La méthode [Show ()](/previous-versions/mt790448(v=vs.85)) est appelée par la page Web pour permettre à l’utilisateur d’interagir avec l’interface utilisateur de la **demande de paiement** .</span><span class="sxs-lookup"><span data-stu-id="abb34-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="abb34-155">La méthode [Show ()](/previous-versions/mt790448(v=vs.85)) renvoie une promesse qui sera résolue lorsque l’utilisateur autorise la demande de paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmer et payer les détails" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="abb34-157">Confirmer et payer les détails</span><span class="sxs-lookup"><span data-stu-id="abb34-157">Confirm and pay details</span></span>  
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

## <span data-ttu-id="abb34-158">Abandon d’une demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="abb34-159">La méthode [Abort ()](/previous-versions/mt790437(v=vs.85)) peut être appelée à tout moment après l’appel de la méthode [Show ()](/previous-versions/mt790448(v=vs.85)) , jusqu’à ce que la promesse soit résolue.</span><span class="sxs-lookup"><span data-stu-id="abb34-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="abb34-160">La méthode [Abort ()](/previous-versions/mt790437(v=vs.85)) a pour effet d’annuler la **demande de paiement** par le navigateur et de fermer l’interface utilisateur de votre demande de **paiement** .</span><span class="sxs-lookup"><span data-stu-id="abb34-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="abb34-161">Par exemple, une page Web est susceptible de se terminer si l’utilisateur n’a pas terminé la transaction dans la durée requise.</span><span class="sxs-lookup"><span data-stu-id="abb34-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="abb34-162">Réponse de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-162">Payment Response</span></span>  
<span data-ttu-id="abb34-163">Lorsque le client approuve la **demande de paiement**, une **réponse de paiement** est renvoyée au site Web.</span><span class="sxs-lookup"><span data-stu-id="abb34-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="abb34-164">Le **bordereau de réponse** comprend les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="abb34-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="abb34-165">Propriété</span><span class="sxs-lookup"><span data-stu-id="abb34-165">Property</span></span>      | <span data-ttu-id="abb34-166">Description</span><span class="sxs-lookup"><span data-stu-id="abb34-166">Description</span></span> | <span data-ttu-id="abb34-167">Requis</span><span class="sxs-lookup"><span data-stu-id="abb34-167">Required</span></span> | <span data-ttu-id="abb34-168">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="abb34-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="abb34-169">NomMéthode</span><span class="sxs-lookup"><span data-stu-id="abb34-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="abb34-170">ID du mode de paiement sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abb34-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="abb34-171">Y</span><span class="sxs-lookup"><span data-stu-id="abb34-171">Y</span></span> | |   
[<span data-ttu-id="abb34-172">details</span><span class="sxs-lookup"><span data-stu-id="abb34-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="abb34-173">Un objet JSON qui inclut toutes les données requises par le commerçant pour traiter la transaction à l’aide du mode de paiement sélectionné ou d’un jeton de paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="abb34-174">Y</span><span class="sxs-lookup"><span data-stu-id="abb34-174">Y</span></span> | <span data-ttu-id="abb34-175">[Carte de base](https://w3c.github.io/payment-method-basic-card) Dictionnaire: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="abb34-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="abb34-176">shippingAddress</span><span class="sxs-lookup"><span data-stu-id="abb34-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="abb34-177">Adresse d’expédition sélectionnée par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="abb34-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="abb34-178">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="abb34-178">Optional.</span></span>  <span data-ttu-id="abb34-179">Obligatoire lorsque [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est</span><span class="sxs-lookup"><span data-stu-id="abb34-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="abb34-180">Dictionnaire d’adresses: pays; addressLine; Region urbains dependentLocality; CodePostal sortingCode; languageCode; société destinataire Répertoire</span><span class="sxs-lookup"><span data-stu-id="abb34-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="abb34-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="abb34-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="abb34-182">ID de l’option d’expédition sélectionnée</span><span class="sxs-lookup"><span data-stu-id="abb34-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="abb34-183">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="abb34-183">Optional.</span></span>  <span data-ttu-id="abb34-184">Obligatoire lorsque [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est</span><span class="sxs-lookup"><span data-stu-id="abb34-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="abb34-185">payerName</span><span class="sxs-lookup"><span data-stu-id="abb34-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="abb34-186">Nom fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abb34-186">The name provided by the user</span></span>  | <span data-ttu-id="abb34-187">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="abb34-187">Optional.</span></span>  <span data-ttu-id="abb34-188">Obligatoire lorsque [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est</span><span class="sxs-lookup"><span data-stu-id="abb34-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="abb34-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="abb34-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="abb34-190">Adresse e-mail sélectionnée par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="abb34-190">The email address selected by the user</span></span> | <span data-ttu-id="abb34-191">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="abb34-191">Optional.</span></span>  <span data-ttu-id="abb34-192">Obligatoire lorsque [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est</span><span class="sxs-lookup"><span data-stu-id="abb34-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="abb34-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="abb34-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="abb34-194">Le numéro de téléphone sélectionné par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="abb34-194">The phone number selected by the user</span></span> | <span data-ttu-id="abb34-195">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="abb34-195">Optional.</span></span>  <span data-ttu-id="abb34-196">Obligatoire lorsque [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) est</span><span class="sxs-lookup"><span data-stu-id="abb34-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="abb34-197">L’objet JSON [Détails](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) de la **réponse au paiement** contient les données de paiement requises par le commerçant pour traiter un paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="abb34-198">Dans sa forme la plus simple, la réponse sera une charge utile de [carte de base](https://w3c.github.io/payment-method-basic-card) contenant les détails de la carte de paiement en clair.</span><span class="sxs-lookup"><span data-stu-id="abb34-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="abb34-199">Lorsque les commerçants disposent de contrats avec des partenaires passerelle/processeur supplémentaires pour leur permettre de prendre en charge des paiements, le commerçant peut nécessiter une charge utile que le processeur peut gérer.</span><span class="sxs-lookup"><span data-stu-id="abb34-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="abb34-200">Celles-ci peuvent prendre la forme d’un jeton de processeur/passerelle ou d’un instrument de paiement chiffré.</span><span class="sxs-lookup"><span data-stu-id="abb34-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="abb34-201">Ces modes de paiement font partie du cadre de ce document et seront couverts dans la documentation propre au processeur.</span><span class="sxs-lookup"><span data-stu-id="abb34-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="abb34-202">Par ailleurs, pour recevoir une réponse de base à une [carte](https://w3c.github.io/payment-method-basic-card) , aucun intégration supplémentaire à Microsoft n’est requise par le développeur, contrairement aux autres modes de paiement pour les processeurs et passerelles, qui pourraient nécessiter l’intégration de la clé de chiffrement ou la demande d’autorisation (OAuth \).</span><span class="sxs-lookup"><span data-stu-id="abb34-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="abb34-203">Lors de la réception d’une **réponse de paiement**, le site Web transmet les informations de paiement à son processeur de paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="abb34-204">Le navigateur va afficher une page de compteur pendant le traitement du paiement.</span><span class="sxs-lookup"><span data-stu-id="abb34-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="Page affichée lors du traitement du paiement" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="abb34-206">Page affichée lors du traitement du paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="abb34-207">Une fois le paiement terminé, la page Web appelle la méthode [Complete ()](/previous-versions/mt790642(v=vs.85)) et transmet une valeur de **réussite** ou d' **échec**.</span><span class="sxs-lookup"><span data-stu-id="abb34-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="abb34-208">La méthode [Complete ()](/previous-versions/mt790642(v=vs.85)) informe le navigateur que l’achat est terminé et l’écran de l’interface utilisateur de fin appropriée doit être affiché en fonction de la valeur de **Success** ou **Fail**.</span><span class="sxs-lookup"><span data-stu-id="abb34-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Interface utilisateur affichée lors de la réussite de l’achat" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="abb34-210">Interface utilisateur affichée lors de la réussite de l’achat</span><span class="sxs-lookup"><span data-stu-id="abb34-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Interface utilisateur affichée lors de l’échec de l’achat" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="abb34-212">Interface utilisateur affichée lors de l’échec de l’achat</span><span class="sxs-lookup"><span data-stu-id="abb34-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="abb34-213">Demande de paiement avec livraison</span><span class="sxs-lookup"><span data-stu-id="abb34-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="abb34-214">Adresse de livraison</span><span class="sxs-lookup"><span data-stu-id="abb34-214">Shipping Address</span></span>  

<span data-ttu-id="abb34-215">Pour les ventes qui nécessitent des produits physiques d’expédition, une adresse de livraison est requise.</span><span class="sxs-lookup"><span data-stu-id="abb34-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="abb34-216">Pour inclure une adresse d’expédition, définissez `requestShipping = True` le paramètre [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) de la requête.</span><span class="sxs-lookup"><span data-stu-id="abb34-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="abb34-217">Lorsque l’utilisateur sélectionne ou met à jour l’adresse de livraison, l’événement [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) est exécuté.</span><span class="sxs-lookup"><span data-stu-id="abb34-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="abb34-218">Le site Web, à l’aide d’un écouteur d’événements, sera averti de la modification et pourra ensuite valider l’adresse, recalculer les coûts d’expédition et les taxes, et mettre à jour [shippingOptions](/previous-versions/mt790440(v=vs.85)) pour refléter les coûts et les options d’expédition disponibles pour l’adresse sélectionnée \ (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="abb34-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="abb34-219">Options d’expédition</span><span class="sxs-lookup"><span data-stu-id="abb34-219">Shipping Options</span></span>  

<span data-ttu-id="abb34-220">Les options d’expédition peuvent être présentées au client en ajoutant [shippingOptions](/previous-versions/mt790440(v=vs.85)) au paramètre [Détails](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .</span><span class="sxs-lookup"><span data-stu-id="abb34-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="abb34-221">Vous pouvez établir une valeur par défaut en définissant l' `selected = True` une des options d’expédition.</span><span class="sxs-lookup"><span data-stu-id="abb34-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="abb34-222">Lorsque l’utilisateur sélectionne ou met à jour le shippingOptions, l’événement [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) s’exécute.</span><span class="sxs-lookup"><span data-stu-id="abb34-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="abb34-223">Le site Web, à l’aide d’un écouteur d’événements, sera consciente du changement et peut mettre à jour le paramètre de [Détails](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) avec le montant d’expédition correct.</span><span class="sxs-lookup"><span data-stu-id="abb34-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

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

## <span data-ttu-id="abb34-224">Informations de référence sur les API</span><span class="sxs-lookup"><span data-stu-id="abb34-224">API Reference</span></span>  

[<span data-ttu-id="abb34-225">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="abb34-226">Spécifier</span><span class="sxs-lookup"><span data-stu-id="abb34-226">Specification</span></span>
[<span data-ttu-id="abb34-227">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="abb34-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Qu’est-ce que Microsoft Edge hérité?"  
