---
description: Documentation de messagerie Native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100251"
---
# Messagerie native  

Les extensions communiquent avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de passage de messages.  L’hôte d’application natif envoie et reçoit des messages avec des extensions à l’aide d’une entrée standard et d’une sortie standard.  Les extensions utilisant la messagerie Native sont installées dans Microsoft Edge de la même façon que dans n’importe quelle autre extension.  Toutefois, les applications natives ne sont pas installées ni gérées par Microsoft Edge.  

Pour acquérir l’extension et l’hôte d’application native, vous avez deux modèles de distribution.  

*   Emportez votre extension et l’hôte ensemble.  Lorsqu’un utilisateur installe le package, l’extension et l’hôte sont installés.
*   Installez votre extension à l’aide du [magasin de modules complémentaires Microsoft Edge][EdgeAddons]et votre extension invite les utilisateurs à installer l’hôte.  

Pour créer votre extension et envoyer et recevoir des messages avec des hôtes d’application natifs, reportez-vous aux étapes suivantes.  

## Étape 1: ajouter des autorisations au manifeste de l’extension  

Ajoutez l' `nativeMessaging` autorisation à la **manifest.jssur** le fichier de l’extension.  L’extrait de code suivant est un exemple de **manifest.jsactivé**.  

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```  

## Étape 2: créer le fichier de manifeste de votre hôte de messagerie natif  

Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie natif.  Le fichier manifeste contient le chemin d’accès au service d’exécution de l’hôte de messagerie natif, la méthode de communication avec l’extension et la liste des extensions autorisées auxquelles il communique.  Le navigateur lit et valide le manifeste de l’hôte de messagerie natif.  Le navigateur ne peut pas installer ou gérer le fichier manifeste de l’hôte de messagerie natif.  

```json
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

Le fichier de manifeste hôte doit être un fichier JSON valide contenant les clés suivantes.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Spécifie le nom de l’hôte de messagerie natif.  Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .  
      
      *   Cette valeur doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.  
      *   Cette valeur ne doit pas commencer ou se terminer par un point, et un point ne doit pas être suivi d’un autre point.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      Décrit l’application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      Spécifie le chemin d’accès au fichier binaire de l’hôte de messagerie natif.  
      
      *   Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs à l’annuaire qui contient le fichier manifeste.  
      *   Sur macOS et Linux, le chemin d’accès doit être absolu.  
      
      Le processus hôte commence par le répertoire actif défini sur le répertoire contenant le fichier binaire hôte.  Par exemple, \ (Windows \), si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif \ ( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Spécifie le type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.  Cette valeur indique à Microsoft Edge d’utiliser `stdin` et `stdout` de communiquer avec l’hôte.  
      La seule valeur acceptable est `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Spécifie la liste des extensions ayant accès à l’hôte de messagerie natif.  Pour permettre à votre application d’identifier et de communiquer avec une extension, dans votre fichier de manifeste d’hôte de messagerie natif, définissez la valeur suivante.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Charger-xxxxxxx xxxx xxxx xxxx xxxx xxxx xxxxxxx.  
Pour charger votre extension lors du développement et de la récupération `microsoft_catalog_extension_id` , procédez comme suit.  

1.  Accédez à `edge://extensions` , puis activez le bouton bascule mode développeur.  
1.  Sélectionnez **charger**le fichier non emballé, puis sélectionnez votre package d’extension pour charger.  
1.  Choisissez **OK**.
1.  Naviguez jusqu’à `edge://extensions` la page et vérifiez que votre extension figure dans la liste.  
1.  Copiez la clé à partir de `microsoft_catalog_extension_id` \ (ID \) à partir de la liste d’extensions sur la page.

Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez votre extension sur le magasin des modules complémentaires Microsoft Edge.  L’ID d’extension de l’extension publiée risque de différer de l’ID utilisé lors de la chargement indépendant de votre extension.  Si l’ID a changé, mettez à jour `allowed_origins` le fichier de manifeste hôte avec l’ID de votre extension publiée.  

## Étape 3: copier le fichier manifeste de l’hôte de messagerie natif sur votre système  

La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie natif sur votre ordinateur et à vérifier qu’il est correctement configuré.  Pour vous assurer que le fichier de votre manifeste est placé à l’emplacement attendu, procédez comme suit.  L’emplacement varie en fonction de la plateforme.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Le fichier manifeste est disponible n’importe où dans le système de fichiers.  Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de cette clé sur le chemin d’accès complet du fichier manifeste.  Les commandes suivantes sont des exemples de clés de registre.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Pour ajouter une clé de Registre à l’annuaire à l’aide de la clé de manifeste.  

*   Commande exécuter dans l’invite de commandes.    
    
    1.  Exécutez la commande suivante.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Créer un `.reg` fichier et l’exécuter.  
    
    1.  Copiez la commande suivante dans un `.reg` fichier.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Exécutez le `.reg` fichier.  
    
Microsoft Edge interroge d’abord le registre 32, puis le registre 64 bits pour identifier les hôtes de messagerie natifs.  Si vous exécutez le fichier ci-dessus `.reg` dans le cadre d’un script de commandes, assurez-vous de l’exécuter à l’aide d’une invite de commandes administrateur.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Pour stocker le fichier manifeste, effectuez l’une des actions suivantes.  

*   Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe.  Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant. 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le `NativeMessagingHosts` sous-répertoire dans le répertoire du profil utilisateur.  Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    La  `{Channel_Name}` `Microsoft Edge {Channel_Name}` figure de doit être l’une des valeurs suivantes.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Lors de l’utilisation du canal stable, `{Channel_Name}` n’est pas obligatoire.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Pour stocker le fichier manifeste, effectuez l’une des actions suivantes.  

*   Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe.  Le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le `NativeMessagingHosts` sous-répertoire dans le répertoire du profil utilisateur.  Le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Vérifiez que vous fournissez des autorisations de lecture sur le fichier manifeste et des autorisations d’exécution sur le runtime hôte.  

<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Modules complémentaires Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
