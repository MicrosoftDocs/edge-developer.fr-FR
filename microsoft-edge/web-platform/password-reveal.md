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
# Personnaliser le bouton d’révéler le mot de passe  

Le `password` type d’entrée dans Microsoft Edge inclut un contrôle **d’révéler le mot de** passe.  Un utilisateur peut choisir le bouton **d’entrée** de mot de passe pour révéler le **champ mot de** passe.  Le champ de mot **de passe** révélé permet à l’utilisateur de vérifier si le mot de passe est correct.  Une fois qu’un **** utilisateur a entré du **** texte dans le champ mot de passe, il peut choisir le bouton d’effet du mot de passe ou choisir de faire basculer la visibilité `Alt` + `F8` de l’entrée.  

:::row:::
   :::column span="":::
      Champ **de mot** de passe avec points masquant les caractères entrés par un utilisateur.  Le **bouton d’révéler** le mot de passe apparaît à droite du champ **mot de** passe.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="L’icône en forme d’œil apparaît en regard des points qui masquent le texte du mot de passe" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         L’icône en forme d’œil apparaît en regard des points qui masquent le texte du mot de passe  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="L’icône en forme d’œil est affichée avec une barre oblique et le texte du mot de passe d’origine s’affiche." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         L’icône en forme d’œil est affichée avec une barre oblique et le texte du mot de passe d’origine s’affiche. :::image-end:::  
   :::column-end:::
:::row-end:::  

Par défaut, le bouton **d’effet de mot** de passe s’insère dans le DOM d’ombre de tous les éléments HTML `input` avec la valeur définie sur `type` `"password"` .  À partir de La version 87 de Microsoft Edge, les utilisateurs ou les entreprises peuvent désactiver cette fonctionnalité globalement. [][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]  En tant que concepteurs web et développeurs, vous devez vous attendre à ce que la plupart des utilisateurs de Microsoft Edge utilisent l’expérience par défaut.  

## Supprimer le contrôle d’révéler le mot de passe  

Vous pouvez supprimer complètement le bouton **d’effet de mot de** passe en ciblant le `::-ms-reveal` pseudo-élément.  

```css
::-ms-reveal {
    display: none;
}
```  

Toutefois, vous devez envisager de tirer parti du bouton **d’effet de mot de** passe.  Le bouton **d’révéler le mot de** passe natif dispose de mesures [de sécurité importantes intégrées](#visibility-of-the-control) au comportement.  

## Personnaliser le style de contrôle  

Au lieu de supprimer entièrement le contrôle, vous **** pouvez modifier le style du bouton d’effet de mot de passe pour mieux correspondre au langage visuel du site web.  L’extrait de code suivant fournit un exemple de style de ce type.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Gardez les points suivants à l’esprit lorsque vous stylez le bouton **d’révéler le** mot de passe.  

*   L’icône de l’œil est implémentée en tant qu’image d’arrière-plan.  Pour ajouter une couleur **** d’arrière-plan au bouton d’effet de mot de passe, utilisez la propriété CSS au lieu de `background-color` la propriété `background` abrégée.  
*   Vous pouvez ajuster la taille et l’échelle du bouton **d’révéler le mot de** passe.  
    
    > [!NOTE]
    >Le navigateur masque tout dépassement en dehors des limites du contrôle d’entrée de mot de passe.  
    
*   Actuellement, aucun sélecteurs d’état n’est disponible pour le style de l’état bascule du bouton d’effet **de mot de** passe.  
    
## Visibilité du contrôle  

Le **bouton d’révéler** le mot de passe n’est pas disponible tant que l’utilisateur n’a pas entré de texte dans le **champ mot de** passe.  Pour sécuriser l’entrée de mot de passe de l’utilisateur, le navigateur supprime le bouton dans les scénarios suivants.

*   Si le focus s’éloigne du champ **mot** de passe, le navigateur supprime le bouton d’effet **du mot de** passe.  
*   Si les scripts modifient **le champ mot** de passe, le navigateur supprime le bouton d’effet de mot **de** passe.  
*   Si un utilisateur supprime le bouton d’affichage du **** mot de **** passe, il doit supprimer le contenu du champ mot de passe avant que le bouton d’affichage du mot de passe ne s’affiche à nouveau. ****  
    
    > [!NOTE]
    > Cette fonctionnalité empêche une personne d’effectuer un ajustement mineur pour afficher le mot de passe, si l’utilisateur s’éloigne d’un appareil déverrouillé.
    
Le bouton **d’révéler** le mot de passe n’est pas disponible si **le** champ mot de passe se remplit automatiquement à l’aide du gestionnaire des mots de passe.  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Stratégies | Documents Microsoft"  
