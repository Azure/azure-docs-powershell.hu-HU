---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504315"
---
# Get-AzureRmNotificationHubsNamespace

## Áttekintés
Információt kap az értesítési hub névteréről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
**A Get-AzureRmNotificationHubsNamespace** parancsmag információt kap az értesítési hub névteréről.
Ez a parancsmag lehetőséget nyújt arra, hogy az összes névtérre vonatkozóan információt kapjanak, és hogy a megadott erőforráscsoporthoz rendelt névterekre vonatkozóan milyen információkra van szükség. vagy egy adott névtérről szóló információk visszaadására.
A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.
Legalább egy értesítési hub-névtérnek kell lennie: minden értesítési hubot egy névtérhez kell rendelni.
Egyetlen névtérben több hub jelenhet meg, ami azt jelenti, hogy csak egy névtérre van szüksége a szervezetében.
Több névtér is használható azonban a hubok jobb rendszerezéséhez, vagy ha konkrét személyekre engedélyt szeretne adni a hubok kijelölt részhalmazának kezeléséhez.
A **Get-AzureRmNotificationHubsNamespace** parancsmag a névtérre vonatkozó alapvető információkat ad eredményül.
Ha a névtérhez társított engedélyezési szabályokról szeretne információt kapni, használja a Get-AzureRmNotificationHubsNamespaceAuthorizationRulest.

## Példák

### 1. példa: információk kérése az összes értesítési hub-névtérről
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

Ez a parancs információt ad az összes értesítési hub-névtérről.

### 2. példa: információk beszerzése egyetlen értesítési központi névtérről
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Ez a parancs egyetlen értesítési hub-névtérről kap információt: ContosoNamespace.

### 3. példa: információk kérése egy adott névtérhez rendelt minden értesítési hubhoz
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Ez a parancs információt kap az erőforráscsoport ContosoNotificationsGroup társított összes értesítési hub-névtérről.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Új – AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


