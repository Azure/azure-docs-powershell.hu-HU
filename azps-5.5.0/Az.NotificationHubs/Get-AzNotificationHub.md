---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160498"
---
# Get-AzNotificationHub

## SYNOPSIS
Információkat kap az értesítési központokról.

## SZINTAXIS

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzNotificationHub** parancsmag információt kap egy megadott névtér értesítési központjáról, és hozzárendel egy adott erőforráscsoporthoz.
Információkat kaphat például a ContosoNamespace névtér összes értesítési központjáról, és hozzárendelheti őket a ContosoNotificationsGroup erőforráscsoporthoz.
Másik lehetőségként az *NotificationHub* paraméterrel korlátozhatja a visszaadott adatokat egy adott értesítési központ információira.
Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy milyen platformot használnak (például iOS, Android, Windows Phone 8 és Windows Áruház).
Ezek a központok nagyjából egyenértékűek az egyes alkalmazásokkal, és mindegyik alkalmazásnak általában saját értesítési központja lesz.
Ez a parancsmag csak a központról kap információt.
Más parancsmagokra, például a Get-AzNotificationHubAuthorizationRules, a Get-AzNotificationHubListKeys és a Get-AzNotificationHubPNSCredentials parancsmagra van szükség a központ engedélyezési szabályaival, kapcsolati karakterláncokkal és platformértesítési szolgáltatás hitelesítő adataival kapcsolatos információkhoz.

## PÉLDÁK

### 1. példa: Információ lekérte az adott névtér összes értesítési központját
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Ez a parancs információkat kap a ContosoNamespace nevű névtér összes, a ContosoNotificationsGroup erőforráscsoporthoz hozzárendelt értesítési központról.

### 2. példa

Információkat kap az értesítési központokról. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
A parancsmag értesítési központjának nevét adja meg.
Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


