---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024527"
---
# Get-AzNotificationHubAuthorizationRule

## Áttekintés
Információt kap az értesítési központtal társított engedélyezési szabályokról.

## SZINTAXISA

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzNotificationHubAuthorizationRule** parancsmag információt kap az értesítési központhoz társított megosztott hozzáférés-aláírási engedélyekkel kapcsolatos szabályokról.
A parancsmag információt ad a hub-hoz társított összes szabályról, vagy a *AuthorizationRule* paraméterrel együtt az adott szabályra vonatkozó információkat.
Engedélyezési szabályok: hozzáférés kezelése az értesítési hubokhoz.
Egy engedélyezési szabály eltérő jogosultsági szinteken alapuló URI-ként hoz létre hivatkozásokat.
Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.
A figyelés engedéllyel rendelkező ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.
A **Get-AzNotificationHubAuthorizationRule** parancsmag csak az értesítési központtal társított engedélyezési szabályokról kap információkat.
Ha a középpontról szeretne információt kapni, használja a Get-AzNotificationHub.

## Példák

### 1. példa: információk kérése az értesítési központhoz rendelt összes engedélyezési szabályhoz
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Ez a parancs információt kap a ContosoInternalHub nevű értesítési központhoz rendelt összes engedélyezési szabályról a névtér ContosoNamespace.
Meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforráscsoport.

### 2. példa: információ kérése az értesítési központhoz rendelt engedélyezési szabályokról
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Ez a parancs információt kap a ContosoInternalHub nevű értesítési központhoz rendelt összes engedélyezési szabályról a névtér ContosoNamespace.
A parancs a *AuthorizationRule* paraméter használatával korlátozza a visszaadott adatot egy ListenRule nevű egyetlen engedélyezési szabályra.

## PARAMÉTEREK

### -AuthorizationRule
A SAS-hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.
A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.

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
Annak az értesítési csomópontnak a megadása, amelyhez a parancsmag engedélyezési szabályokat rendel.
Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.

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
Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.
Az erőforráscsoportok a Készletkezelés és az Azure-felügyelet egyszerűsítését segítő módon rendezheti az elemeket, például a névtereket, az értesítési hubokat és a engedélyezési szabályokat.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[Új – AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


