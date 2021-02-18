---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410463"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
Egy értesítési központ névtér-engedélyezési szabályával társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.

## SZINTAXIS

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzNotificationHubsNamespaceListKey** parancsmag egy értesítési központ névterhez rendelt Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.
Az engedélyezési szabályok az értesítési központ névteréhez való felhasználói jogokat kezelik.
Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.

## PÉLDÁK

### 1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát adja vissza.
A parancs futtatásakor meg kell lennie annak az erőforráscsoportnak a nevével, amelyhez a névteret hozzárendelték.

## PARAMETERS

### -AuthorizationRule
Egy SAS-hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Az a névtér, amely a parancsmag által lekért kapcsolati karakterláncokat tartalmazza.

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

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)



