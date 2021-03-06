---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: aa8dde2683dcc939bb84e9f2026131cd8cc15b1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013600"
---
# Add-AzLogProfile

## Áttekintés
Új műveletnapló-profilt hoz létre. Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra. 

## SZINTAXISA

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Add-AzLogProfile** parancsmag naplózó profilt hoz létre.
- **Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott. Lehet, hogy a kar vagy a klasszikus típus közül kell lennie. Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák. Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához. 
- **Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója. Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz. A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek. Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik. Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt. A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül. 
**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.** Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.

## Példák

### 1. példa: új log-profil hozzáadása a tevékenység naplójának exportálásához, amely a hely feltételéhez illő tárolási fiókhoz van illesztve
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMÉTEREK

### -Category (kategória)
A kategóriák listáját adja meg.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Hely
A napló profiljának helyét adja meg.
Érvényes értékek: az alábbi parancsmagot futtatva érheti el a helyek legújabb listáját. Get-AzLocation | A DisplayName elem választása

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A profil nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
A napok szerinti adatmegőrzési házirendet adja meg. Ez az a napok száma, amelyekben a naplók megmaradnak a megadott tárolási fiókban. Ha meg szeretné őrizni az adatvesztést, a **0** értékre kell állítania. Ha nincs megadva, az alapértelmezett érték **0**. A normál normál tárterület vagy az esemény-hub számlázási díja az adatmegőrzésre érvényes lesz.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
A szolgáltatási busz szabályának AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
A tárolási fiók AZONOSÍTÓját adja meg. AZONOSÍTÓ: a tárolási fiók teljesen minősített erőforrás-azonosítója, például:  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSLogProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


