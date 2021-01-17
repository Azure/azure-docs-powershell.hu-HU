---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336233"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
Behozza az értesítési központ névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat.

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
A parancs futtatásakor szerepelnie kell annak az erőforráscsoportnak a nevével, amelyhez a névtér hozzá van rendelve.

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
A parancsmag által begyűlelt kapcsolati karakterláncokat tartalmazó névteret adja meg.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


