---
description: Fournit des conseils sur la personnalisation de l’affichage du bouton d’affichage du mot de passe
title: Personnaliser le bouton d’révéler le mot de passe
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, compatibilité, plateforme web, révéler le mot de passe, icône d’œil
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327713"
---
# <span data-ttu-id="40c97-104">Personnaliser le bouton d’révéler le mot de passe</span><span class="sxs-lookup"><span data-stu-id="40c97-104">Customize the password reveal button</span></span>  

<span data-ttu-id="40c97-105">Le `password` type d’entrée dans Microsoft Edge inclut un contrôle **d’révéler le mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="40c97-106">Un utilisateur peut choisir le bouton **d’entrée** de mot de passe pour révéler le **champ mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="40c97-107">Le champ de mot **de passe** révélé permet à l’utilisateur de vérifier si le mot de passe est correct.</span><span class="sxs-lookup"><span data-stu-id="40c97-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="40c97-108">Une fois qu’un  utilisateur a entré du  texte dans le champ mot de passe, il peut choisir le bouton d’effet du mot de passe ou choisir de faire basculer la visibilité `Alt` + `F8` de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="40c97-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="40c97-109">Champ **de mot** de passe avec points masquant les caractères entrés par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="40c97-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="40c97-110">Le **bouton d’révéler** le mot de passe apparaît à droite du champ **mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="L’icône en forme d’œil apparaît en regard des points qui masquent le texte du mot de passe" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="40c97-112">L’icône en forme d’œil apparaît en regard des points qui masquent le texte du mot de passe</span><span class="sxs-lookup"><span data-stu-id="40c97-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="40c97-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span><span class="sxs-lookup"><span data-stu-id="40c97-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="L’icône en forme d’œil est affichée avec une barre oblique et le texte du mot de passe d’origine s’affiche." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="40c97-115">L’icône en forme d’œil est affichée avec une barre oblique et le texte du mot de passe d’origine s’affiche.</span><span class="sxs-lookup"><span data-stu-id="40c97-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="40c97-116">Par défaut, le bouton **d’effet de mot** de passe s’insère dans le DOM d’ombre de tous les éléments HTML `input` avec la valeur définie sur `type` `"password"` .</span><span class="sxs-lookup"><span data-stu-id="40c97-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="40c97-117">À partir de La version 87 de Microsoft Edge, les utilisateurs ou les entreprises peuvent désactiver cette fonctionnalité globalement. [][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]</span><span class="sxs-lookup"><span data-stu-id="40c97-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="40c97-118">En tant que concepteurs web et développeurs, vous devez vous attendre à ce que la plupart des utilisateurs de Microsoft Edge utilisent l’expérience par défaut.</span><span class="sxs-lookup"><span data-stu-id="40c97-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <span data-ttu-id="40c97-119">Supprimer le contrôle d’révéler le mot de passe</span><span class="sxs-lookup"><span data-stu-id="40c97-119">Remove the password reveal control</span></span>  

<span data-ttu-id="40c97-120">Vous pouvez supprimer complètement le bouton **d’effet de mot de** passe en ciblant le `::-ms-reveal` pseudo-élément.</span><span class="sxs-lookup"><span data-stu-id="40c97-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="40c97-121">Toutefois, vous devez envisager de tirer parti du bouton **d’effet de mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="40c97-122">Le bouton **d’révéler le mot de** passe natif dispose de mesures [de sécurité importantes intégrées](#visibility-of-the-control) au comportement.</span><span class="sxs-lookup"><span data-stu-id="40c97-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <span data-ttu-id="40c97-123">Personnaliser le style de contrôle</span><span class="sxs-lookup"><span data-stu-id="40c97-123">Customize the control style</span></span>  

<span data-ttu-id="40c97-124">Au lieu de supprimer entièrement le contrôle, vous  pouvez modifier le style du bouton d’effet de mot de passe pour mieux correspondre au langage visuel du site web.</span><span class="sxs-lookup"><span data-stu-id="40c97-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="40c97-125">L’extrait de code suivant fournit un exemple de style de ce type.</span><span class="sxs-lookup"><span data-stu-id="40c97-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="40c97-126">Gardez les points suivants à l’esprit lorsque vous stylez le bouton **d’révéler le** mot de passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="40c97-127">L’icône de l’œil est implémentée en tant qu’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="40c97-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="40c97-128">Pour ajouter une couleur  d’arrière-plan au bouton d’effet de mot de passe, utilisez la propriété CSS au lieu de `background-color` la propriété `background` abrégée.</span><span class="sxs-lookup"><span data-stu-id="40c97-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="40c97-129">Vous pouvez ajuster la taille et l’échelle du bouton **d’révéler le mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="40c97-130">Le navigateur masque tout dépassement en dehors des limites du contrôle d’entrée de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="40c97-131">Actuellement, aucun sélecteurs d’état n’est disponible pour le style de l’état bascule du bouton d’effet **de mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <span data-ttu-id="40c97-132">Visibilité du contrôle</span><span class="sxs-lookup"><span data-stu-id="40c97-132">Visibility of the control</span></span>  

<span data-ttu-id="40c97-133">Le **bouton d’révéler** le mot de passe n’est pas disponible tant que l’utilisateur n’a pas entré de texte dans le **champ mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="40c97-134">Pour sécuriser l’entrée de mot de passe de l’utilisateur, le navigateur supprime le bouton dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="40c97-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="40c97-135">Si le focus s’éloigne du champ **mot** de passe, le navigateur supprime le bouton d’effet **du mot de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="40c97-136">Si les scripts modifient **le champ mot** de passe, le navigateur supprime le bouton d’effet de mot **de** passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="40c97-137">Si un utilisateur supprime le bouton d’affichage du  mot de  passe, il doit supprimer le contenu du champ mot de passe avant que le bouton d’affichage du mot de passe ne s’affiche à nouveau. </span><span class="sxs-lookup"><span data-stu-id="40c97-137">If a user removes the **password reveal** button, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="40c97-138">Cette fonctionnalité empêche une personne d’effectuer un ajustement mineur pour afficher le mot de passe, si l’utilisateur s’éloigne d’un appareil déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="40c97-138">This feature prevents someone from making a minor adjustment to view the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="40c97-139">Le bouton **d’révéler** le mot de passe n’est pas disponible si **le** champ mot de passe se remplit automatiquement à l’aide du gestionnaire des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="40c97-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Stratégies | Documents Microsoft"  
