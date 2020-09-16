---
description: Différence de messagerie native de la documentation chrome
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 811468e5f92319107c60606bc9268a9f7a25e560
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015675"
---
# Messagerie native  

Microsoft Edge permet désormais d’installer une extension à partir du catalogue Microsoft Edge addons (Microsoft Edge addons) pour échanger des messages avec une application native utilisant des API de passage de messages.  Pour activer cette fonctionnalité, vous devez vous assurer que les éléments suivants sont implémentés lors de l’implémentation de l’hôte de messagerie natif de votre application native.  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  **Hôte de messagerie natif**:  
    
    Pour enregistrer un hôte de messagerie natif, l’application doit installer un fichier manifeste qui définit la configuration de l’hôte de messagerie natif.  Voici un exemple du fichier manifeste:  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
Le fichier manifeste de l’hôte de messagerie natif doit être JSON valide et contenir les champs suivants:  

| Nom | Description |  
|:--- |:--- |  
| `name` | Nom de l’hôte de messagerie natif. Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .  Ce nom doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.  Le nom ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point. |  
| `description` | Brève description de l’application. |  
| `path` | Chemin d’accès au fichier binaire de l’hôte de messagerie natif.  Sur Windows, le chemin d’accès peut être relatif au répertoire dans lequel se trouve le fichier manifeste.  Sur macOS, le chemin d’accès doit être absolu.  Le processus hôte est démarré avec le répertoire actif défini sur le répertoire contenant le fichier binaire hôte. Par exemple, si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif `C:\Application\` . |  
| `type` | Type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.  Il n’y a actuellement qu’une seule valeur possible pour ce paramètre: `stdio` .  Cette valeur indique que Chrome doit utiliser `stdin` et `stdout` communiquer avec l’hôte. |  
| `allowed_origins` |  liste d’extensions qui doivent pouvoir accéder à l’hôte de messagerie natif.  Pour permettre à votre application native d’identifier et de communiquer avec l’extension Microsoft Edge addons, définissez `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif. |  

1.  **Emplacement d’hébergement de messagerie Native**  
    
    L’emplacement du fichier manifeste dépend de la plateforme.  
    
    Sur Windows, le fichier manifeste est disponible n’importe où dans le système de fichiers.  Le programme d’installation de l’application doit créer une clé de Registre  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    ou  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`,  
    
    Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste.  Par exemple, à l’aide de la commande suivante:  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    ou en utilisant le fichier. reg suivant:  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    Lorsque Microsoft Edge recherche les hôtes de messagerie natifs, le registre 32 bits est interrogé en premier, puis le registre 64 bits.  

Sur macOS, les hôtes de messagerie natif à l’échelle du système sont examinés à un emplacement fixe, tandis que les hôtes de messagerie natifs de niveau utilisateur sont recherchés dans un sous-répertoire du répertoire de profil utilisateur appelé `NativeMessagingHosts` .  

Microsoft Edge sur macOS \ (système à l’échelle de la planète):  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

Microsoft Edge sur macOS \ (spécifique de l’utilisateur, chemin par défaut \):  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` Il est possible que la fonction «Canaries», «dev» ou «beta». Dans le cas d’un canal stable, `Microsoft Edge` il ne doit être utilisé qu' `<ChannelName`>'n’est pas nécessaire.

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
