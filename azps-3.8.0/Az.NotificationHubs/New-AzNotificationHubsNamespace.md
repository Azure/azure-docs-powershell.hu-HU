---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012780"
---
# New-AzNotificationHubsNamespace

## Áttekintés
Az értesítési hub névteret hozza létre.

## SZINTAXISA

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzNotificationHubsNamespace** parancsmag egy értesítési hub-névteret hoz létre.
A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.
Legalább egy értesítési hub-névtérnek kell lennie.
Egyetlen névtérben több hub is berendezhető.
Több névtér is megszervezhető a hubok rendszerezéséhez, vagy konkrét személyek számára engedélyt adhat a hubok kijelölt részhalmazának kezeléséhez.
Ha névteret szeretne létrehozni, győződjön meg arról, hogy a névtérhez egyedi nevet ad meg; adja meg azt az adatközpontot, ahol a névtér található; adja meg azt az erőforráscsoport-csoportot, amelyhez a névteret hozzá szeretné rendelni.
Miután létrehozta a névteret, az New-AzNotificationHubsNamespaceAuthorizationRules parancsmagot használva engedélyezési szabályokat rendelhet az adott névtérhez.
Az engedélyezési szabályok a névtér engedélyeinek kezelésére szolgálnak.

## Példák

### Példa 1: értesítési központ létrehozása
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Ez a parancs létrehoz egy ContosoPartners nevű értesítési hubot.
A névtér a Nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup-erőforráscsoporthoz van társítva.

### 2. példa: értesítési központ létrehozása címkékkel
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Ez a parancs létrehoz egy ContosoPartners nevű értesítési hubot.
A névtér a Nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup-erőforráscsoporthoz van társítva.
Emellett a parancs létrehoz egy címkét, amely a név célközönsége és az érték PartnerOrganizations, és a névtérhez van rendelve.
Ez a beállítás biztosítja, hogy a rendszer minden alkalommal megjelenítse a névteret, ha olyan elemeket szűr, amelyek PartnerOrganizations a célközönség címkéje van beállítva.

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

### -Hely
Annak az adatközpontnak a megjelenítendő nevét adja meg, amely a névteret fogja üzemeltetni.
Bár ezt a paramétert bármilyen érvényes helyre is beállíthatja, hogy optimális legyen, érdemes lehet egy olyan adatközpontot használni, amely a felhasználók többségéhez közel helyezkedik el.

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

### -Namespace
Az új névtér nevét adja meg.
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
Azt az erőforráscsoport-csoportot adja meg, amelyhez a névteret hozzá szeretné rendelni.
Az erőforráscsoportok olyan módon rendszerezik az elemeket, mint például a névterek, az értesítési hubok és az engedélyezési szabályok, amelyek megkönnyítik a Készletkezelés és a felügyelet kezelését.

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

### -SkuTier
A névtér SKU-szintjei

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.
A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.
Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.
Az egyéni címke két részből áll: a *név* és a tetszés szerinti *érték*.
Például a részlegben: a címke neve részleg, a címke pedig az érték.
Címke hozzáadásához használja az alábbihoz hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016 címkét hozza létre:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


