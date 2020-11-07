---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 9a17dfd649f35da3fa071eb7c6d2752d3a923398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669880"
---
# Set-AzNotificationHubsNamespace

## Áttekintés
Az értesítési hub-névtér tulajdonság-értékeit állítja be.

## SZINTAXISA

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzNotificationHubsNamespace** parancsmag a meglévő értesítési hub-névtér tulajdonság-értékeit állítja be.
A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.
Legalább egy értesítési hub-névtérnek kell lennie.
Emellett minden értesítési hub-nak rendelkeznie kell hozzárendelt névtérrel.
Ez a parancsmag elsősorban a névterek engedélyezéséhez és letiltásához használatos.
Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtérben lévő értesítési hubokhoz, és a rendszergazdák ezekkel a hubok segítségével küldhetnek leküldéses értesítéseket.
Ha újra engedélyezni szeretné egy letiltott névtér használatát, ezzel a parancsmaggal állítsa be az aktív névtér **állapot** tulajdonságát.
Ezt a parancsmagot is megadhatja kritikusként a névtér címkézéséhez.
Ez a beállítás megakadályozza a névtér törlését.
A kritikus névterek eltávolításához előbb el kell távolítania a kritikus címkét.

## Példák

### Példa 1: névtér letiltása
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Ez a parancs letiltja a ContosoPartners nevű névteret a West US Datacenter-ben, és a ContosoNotificationsGroup-erőforráscsoport számára van társítva.

### 2. példa: névtér engedélyezése
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Ez a parancs lehetővé teszi, hogy a ContosoPartners nevű névtér a West US-adatközpontban található, és a ContosoNotificationsGroup erőforráscsoport legyen társítva.

## PARAMÉTEREK

### -Kritikus
Azt jelzi, hogy a névtér a kritikus névtér-e.
A kritikus névterek nem törölhetők.
A kritikus névterek törléséhez a tulajdonság értékét false értékre kell állítania ahhoz, hogy a névteret nem kritikusként jelölje meg.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -Force
Ne kérjen megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A névteret működtető adatközpont megjelenítendő nevét adja meg.
Bár ezt a paramétert bármely érvényes Azure-helyre beállíthatja, így optimális teljesítményhez a felhasználók többségéhez közeli adatközpontot kell használnia.
Az Azure-helyek naprakész listáját az alábbi parancs futtatásával érheti el: `Get-AzLocation | Select-Object DisplayName`

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
A parancsmag által módosított névteret adja meg.
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

### -State (állami)
A névtér aktuális állapotát adja meg.
A paraméter elfogadható értékei a következők: aktív és le van tiltva.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.
A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.
Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.
Az egyéni címke két részből áll: a *név* és (tetszés szerint) az *érték*.
A részlegben például a címke neve részleg, a címke pedig az érték.
Címke hozzáadásához használja az ehhez hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016:-Tags @ {Name = "CalendarYear" kifejezést hozza létre. Value = "2016"} Ha több címkét szeretne hozzáadni ugyanabba a parancsba, válassza el az egyes címkéket vesszőkkel: – címke @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "pénzügyi év időszaka"; Value = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. NotificationHubs. models. NamespaceState

### System. Boolean

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Új – AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


