---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158763"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Információkat kap az értesítési központhoz társított engedélyezési szabályokról.

## SZINTAXIS

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzNotificationHubAuthorizationRule** parancsmag információkat kap az értesítési központhoz társított MEGOSZTOTT hozzáférés-aláírás (SAS) engedélyezési szabályairól.
A parancsmag információt ad a központhoz társított összes szabályról, vagy az *AuthorizationRule* paraméter megadva információkat kap egy adott szabályról.
Az engedélyezési szabályok kezelik az értesítési központokhoz való hozzáférést.
Az engedélyezési szabályok különböző engedélyszintek alapján hoznak létre hivatkozásokat URI-ként.
Az ügyfél a megfelelő jogosultsági szint alapján az alábbi URI-k egyikére irányítja az URI-ket.
A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.
A **Get-AzNotificationHubAuthorizationRule** parancsmag csak az értesítési központhoz társított engedélyezési szabályokkal kapcsolatos információkat kap.
Ha információt kap a központról, használja a Get-AzNotificationHubot.

## PÉLDÁK

### 1. példa: Információ kérése az értesítési központhoz rendelt összes engedélyezési szabályról
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Ez a parancs információkat kap a ContosoNamespace névtéren található ContosoInternalHub értesítési központhoz rendelt összes engedélyezési szabályról.
Meg kell adnia azt a névteret, ahol a központ található, valamint azt az erőforráscsoportot, amelyhez a központ hozzá lett rendelve.

### 2. példa: Információ kérése egy értesítési központhoz rendelt engedélyezési szabályokkal kapcsolatban
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Ez a parancs információkat kap a ContosoNamespace névtéren található ContosoInternalHub értesítési központhoz rendelt összes engedélyezési szabályról.
A parancs az *AuthorizationRule paraméterrel* korlátozza a visszaadott adatokat egyetlen, ListenRule nevű engedélyezési szabályra.

## PARAMETERS

### -AuthorizationRule
Egy SAS-hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
Megadja azt az értesítési központot, amelyhez ez a parancsmag engedélyezési szabályokat rendel.
Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy milyen platformot használnak az adott ügyfél által használt platformon.

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

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét megkönnyítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


