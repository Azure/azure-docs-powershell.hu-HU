---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504952"
---
# Add-AzureRmLogProfile

## Áttekintés
Új műveletnapló-profilt hoz létre. Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra. 

- **Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott. Lehet, hogy a kar vagy a klasszikus típus közül kell lennie. Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák. Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához. 

- **Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója. Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz. 

A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek. Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik. Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt. A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül. 

**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.** 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmLogProfile** parancsmag naplózó profilt hoz létre.

## Példák

### 1. példa: új log-profil hozzáadása a tevékenység naplójának exportálásához, amely a hely feltételéhez illő tárolási fiókhoz van illesztve
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMÉTEREK

### -Kategóriák
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

### -Helyek
A napló profiljának helyét adja meg.
Érvényes értékek: az alábbi parancsmagot futtatva érheti el a helyek legújabb listáját. 

Get-AzureLocation | A DisplayName elem választása

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSLogProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmLogProfile](./Get-AzureRmLogProfile.md)

[Remove-AzureRmLogProfile](./Remove-AzureRmLogProfile.md)


