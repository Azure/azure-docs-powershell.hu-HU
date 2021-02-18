---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206438"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Információkat kap egy értesítési központ névterről.

## SZINTAXIS

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
**A Get-AzNotificationHubsNamespace** parancsmag információt kap az értesítési központ névtereiről.
Ez a parancsmag lehetőséget nyújt arra, hogy információt kap az összes névtérről, valamint egy adott erőforráscsoporthoz rendelt névterek adatairól; vagy adott névtérről ad vissza információkat.
A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.
Legalább egy értesítési központ névterének meg kell lennie osztva: az összes értesítési központot hozzá kell rendelni egy névtérhez.
Egy névtér több központi központban is elterjedhet, ami azt jelenti, hogy a szervezetben lehet, hogy csak egy névterre van szüksége.
Több névteret is adhat azonban, hogy jobban rendszerezze a központokat, vagy hogy egyes személyeknek engedélyt adjon a központok kijelölt alcsoportja kezeléséhez.
A **Get-AzNotificationHubsNamespace** parancsmag alapvető információkat ad vissza a névtérről.
A névtérhez társított engedélyezési szabályokról a Get-AzNotificationHubsNamespaceAuthorizationRules használatával tud információt kapni.

## PÉLDÁK

### 1. példa: Információk lekérte az értesítési központ összes névterét
```
PS C:\>Get-AzNotificationHubsNamespace
```

Ez a parancs az értesítési központ összes névterének adatait adja vissza.

### 2. példa: Információ lekérte egy értesítési központ névterét
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Ez a parancs információt kap egyetlen értesítési központ névterére: ContosoNamespace.

### 3. példa: Információ az adott névtérhez rendelt összes értesítési központról
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Ez a parancs információkat kap a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes értesítési központ névterével kapcsolatban.

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
A névtér egyedi nevét adja meg.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

Required: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


