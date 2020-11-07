---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669904"
---
# Get-AzNotificationHubsNamespace

## Áttekintés
Információt kap az értesítési hub névteréről.

## SZINTAXISA

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
**A Get-AzNotificationHubsNamespace** parancsmag információt kap az értesítési hub névteréről.
Ez a parancsmag lehetőséget nyújt arra, hogy az összes névtérre vonatkozóan információt kapjanak, és hogy a megadott erőforráscsoporthoz rendelt névterekre vonatkozóan milyen információkra van szükség. vagy egy adott névtérről szóló információk visszaadására.
A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.
Legalább egy értesítési hub-névtérnek kell lennie: minden értesítési hubot egy névtérhez kell rendelni.
Egyetlen névtérben több hub jelenhet meg, ami azt jelenti, hogy csak egy névtérre van szüksége a szervezetében.
Több névtér is használható azonban a hubok jobb rendszerezéséhez, vagy ha konkrét személyekre engedélyt szeretne adni a hubok kijelölt részhalmazának kezeléséhez.
A **Get-AzNotificationHubsNamespace** parancsmag a névtérre vonatkozó alapvető információkat ad eredményül.
Ha a névtérhez társított engedélyezési szabályokról szeretne információt kapni, használja a Get-AzNotificationHubsNamespaceAuthorizationRulest.

## Példák

### 1. példa: információk kérése az összes értesítési hub-névtérről
```
PS C:\>Get-AzNotificationHubsNamespace
```

Ez a parancs információt ad az összes értesítési hub-névtérről.

### 2. példa: információk beszerzése egyetlen értesítési központi névtérről
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Ez a parancs egyetlen értesítési hub-névtérről kap információt: ContosoNamespace.

### 3. példa: információk kérése egy adott névtérhez rendelt minden értesítési hubhoz
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Ez a parancs információt kap az erőforráscsoport ContosoNotificationsGroup társított összes értesítési hub-névtérről.

## PARAMÉTEREK

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
A névtér egyedi nevét adja meg.
A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.

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
Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.
Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespaceAuthorizationRules](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[Új – AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


