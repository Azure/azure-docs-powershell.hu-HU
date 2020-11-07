---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846694"
---
# Get-AzNotificationHubsNamespaceListKey

## Áttekintés
Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.

## SZINTAXISA

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzNotificationHubsNamespaceListKey** parancsmag a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncait számítja ki az értesítési hub névteréhez rendelve.
Az engedélyezési szabályok a felhasználói jogokat az értesítési hub névteréhez kezelik.
Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.

## Példák

### Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule nevű engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncait ad eredményül.
A parancs futtatásakor tartalmaznia kell annak az erőforráscsoportnak a nevét, amelyhez a névtér hozzá van rendelve.

## PARAMÉTEREK

### -AuthorizationRule
A SAS-hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.

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
A parancsmag által kapott kapcsolati karakterláncokat tartalmazó névtér megadása.

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
Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.
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

### Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Get-AzNotificationHubsNamespaceAuthorizationRules](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


