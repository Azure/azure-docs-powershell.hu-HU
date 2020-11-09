---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301367"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## Áttekintés
Információt kap az értesítési hub névteréhez társított engedélyezési szabályokról.

## SZINTAXISA

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzNotificationHubsNamespaceAuthorizationRule** parancsmag információt ad az értesítési hub névteréhez társított megosztott hozzáférés-aláírási szabályokról.
A névtérhez társított összes szabályról információt adhat vissza.
A másik lehetőség, hogy a *AuthorizationRule* paramétert is beleszámítva visszaadja az adott szabály adatait.
Engedélyezési szabályok: hozzáférés kezelése a névterekhez.
Ez a hivatkozás a különböző jogosultsági szintek alapján létrehozott URI-k létrehozásával végezhető el.
A platform szintjei az alábbiak lehetnek: 
- Hallgatni
- Küldése
- Az ügyfelek kezelése a megfelelő jogosultsági szint alapján a fenti URI-k egyikéhez van irányítva.
A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.
Ez a parancsmag csak a névtérhez társított engedélyezési szabályokat kapja meg.
Ha a névtérről szeretne információt kapni, használja a Get-AzNotificationHubsNamespace.

## Példák

### Példa 1: információk beszerzése a névterekhez rendelt összes engedélyezési szabályról
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Ez a parancs a névtér ContosoNamespace és a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes engedélyezési szabályról információt kap.

### 2. példa: az engedélyezési szabályokról szóló információk beszerzése
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Ez a parancs a ListenRule nevű egyetlen névtér-engedélyezési szabályról kap információkat.
Ha egy adott engedélyezési szabályról szeretne információt kapni, akkor a névteret és az erőforráscsoportot is be kell írnia.

## PARAMÉTEREK

### -AuthorizationRule
A SAS-hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel rendelkeznek a névtérhez.

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
Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.
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

### -ResourceGroup
Azt az erőforráscsoport-csoportot adja meg, amelyhez az engedélyezési szabályokat hozzárendelték.
Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.

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

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Új – AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


