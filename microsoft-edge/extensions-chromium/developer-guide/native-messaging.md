---
description: Documentation de messagerie Native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088554"
---
# Messagerie native  

Les extensions peuvent communiquer avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de passage de messages. L’hôte d’application natif peut envoyer et recevoir des messages avec des extensions à l’aide d’entrées standard et d’une sortie standard. Les extensions utilisant la messagerie Native sont installées dans Microsoft Edge de la même façon que dans n’importe quelle autre extension. Toutefois, les applications natives ne sont pas installées ni gérées par Microsoft Edge.

Pour acquérir l’extension et l’hôte de l’application native, vous pouvez:

1. Empaquetez l’extension et l’hôte ensemble. Quand les utilisateurs installent le package, l’extension et l’hôte sont installés.
1. Installez l’extension à partir du [magasin de modules complémentaires Microsoft Edge][EdgeAddons]et demandez aux utilisateurs d’installer l’hôte. 

Reportez-vous aux étapes ci-dessous pour configurer votre extension pour envoyer et recevoir des messages avec des hôtes d’application natifs.

### Étape 1: ajouter des autorisations au manifeste de l’extension

Ajoutez l’autorisation nativeMessaging sur le fichier **manifest.js** de l’extension. Vous trouverez ci-dessous un exemple de manifest.jssur:

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

### Étape 2: créer le fichier de manifeste de votre hôte de messagerie natif
    
Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie natif. Ce fichier manifeste contient le chemin d’accès au fichier exécutable de l’hôte de messagerie natif, la méthode de communication avec l’extension et la liste des extensions autorisées avec lesquelles il peut communiquer. Le navigateur lit et valide le manifeste de l’hôte de messagerie natif, mais n’est jamais installé ou géré par le navigateur. Le fichier de manifeste hôte doit être un fichier JSON valide contenant les champs suivants.

    
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




| Nom | Description |  
|:--- |:--- |  
| `name` | Nom de l’hôte de messagerie natif. Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .  Ce nom doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.  Le nom ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point. |  
| `description` | Brève description de l’application. |  
| `path` | Chemin d’accès au fichier binaire de l’hôte de messagerie natif. Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs à l’annuaire qui contient le fichier manifeste. Sur macOS et Linux, le chemin d’accès doit être absolu. Le processus hôte est démarré avec le répertoire actif défini sur le répertoire contenant le fichier binaire hôte. Par exemple, si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif `C:\Application\` . |  
| `type` | Type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.  Il n’y a actuellement qu’une seule valeur possible pour ce paramètre: `stdio` .  Cette valeur indique que Microsoft Edge doit utiliser `stdin` et `stdout` communiquer avec l’hôte. |  
| `allowed_origins` |  Liste des extensions susceptibles d’avoir accès à l’hôte de messagerie natif.  Pour permettre à votre application d’identifier et de communiquer avec une extension, définissez `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif. |  


Pendant le développement, vous pouvez charger votre extension pour tester la messagerie native avec l’hôte:
1. Accédez à `edge://extensions` , puis activez le bouton bascule mode développeur. 
1. Sélectionnez charger le fichier non emballé, puis sélectionnez votre package d’extension pour charger.  
1. Choisissez OK.
1. Vérifiez que la `edge://extensions` page affiche désormais votre extension. 
1. Copiez la clé à partir de l’ID de la liste d’extensions sur la page.

Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez votre extension sur le magasin des modules complémentaires Microsoft Edge. L’ID de l’extension publiée doit être différent de l’ID utilisé lors de la chargement indépendant votre extension. Si l’ID a changé, mettez à jour `allowed_origins` le fichier de manifeste hôte avec l’ID de votre extension publiée. 



### Étape 3: copier le fichier manifeste de l’hôte de messagerie natif sur votre système

La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie natif sur votre ordinateur et à vérifier qu’il est correctement configuré. Suivez les étapes ci-dessous pour vous assurer que le fichier hôte de messagerie natif est placé à l’emplacement attendu, car il varie en fonction de la plateforme.
    
**Windows**. Le fichier manifeste est disponible n’importe où dans le système de fichiers. Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de cette clé sur le chemin d’accès complet du fichier manifeste. Les commandes suivantes sont des exemples de clés de registre.
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    ou  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`,  
    
Exécutez la commande suivante à l’invite de commandes pour ajouter une clé de Registre dans le dossier contenant le fichier manifeste.
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
Vous pouvez également copier la commande suivante dans un fichier. reg et l’exécuter pour ajouter la clé de registre. 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  Microsoft Edge interroge d’abord le registre 32, puis le registre 64 bits pour identifier les hôtes de messagerie natifs. Si vous exécutez le fichier. reg ci-dessus dans le cadre d’un script de commandes, assurez-vous de l’exécuter à l’aide d’une invite de commandes administrateur.


**MacOS**. Le fichier manifeste doit être stocké comme suit:

1. Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe. Par exemple, le fichier manifeste doit être stocké dans `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le sous-répertoire NativeMessagingHosts dans le répertoire du profil utilisateur. Par exemple, le fichier manifeste doit être stocké dans  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    où `ChannelName` il est possible que la fonction Canaries, dev ou beta. N’est pas nécessaire lors de l’utilisation du canal stable `ChannelName` .


**Linux** Le fichier manifeste doit être stocké comme suit:

1. Hôtes de messagerie native à l’échelle du système:  `~/.config/microsoft-edge/NativeMessagingHosts`

1. Hôtes de messagerie Native spécifiques de l’utilisateur:  `/etc/opt/edge/native-messaging-hosts`


> [!NOTE]
> Vérifiez que vous fournissez des autorisations de lecture sur le fichier manifeste et des autorisations d’exécution sur le fichier exécutable de l’hôte.


> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Modules complémentaires Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
