---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493388"
---
# New-AzureRmRedisCacheScheduleEntry

## Áttekintés
Ütemezési bejegyzés létrehozása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmRedisCacheScheduleEntry** parancsmag létrehoz egy **PSScheduleEntry** objektumot.
Az Azure Redis-gyorsítótár-javítás ütemezési parancsmagjai (például az New-AzureRmRedisCachePatchSchedule parancsmag) az ütemezési bejegyzés objektumait igénylik.

## Példák

### Példa 1: Ütemezési bejegyzés létrehozása hétvégekhez
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

Ez a parancs létrehoz egy **PSScheduleEntry** -objektumot, amely egy, a megadott kezdési időpontot és ablakot tartalmazó hétvégi ütemtervet képvisel.

## PARAMÉTEREK

### -DayOfWeek
Az ütemezési bejegyzéshez tartozó hét napját adja meg.
A paraméter elfogadható értékei a következők:

- Mindennapos 
- Hétvégén 
- Hétfő 
- Kedd 
- Szerda 
- Csütörtök 
- Péntek 
- Szombat 
- Vasárnap

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaintenanceWindow
A frissítésekhez engedélyezett időmennyiséget adja meg.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartHourUtc
Az ütemterv kezdési napját adja meg.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
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

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Microsoft. Azure. Command. RedisCache. models. PSScheduleEntry
Ez a parancsmag az ütemezési bejegyzés objektumát számítja ki.

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRedisCachePatchSchedule](./Get-AzureRmRedisCachePatchSchedule.md)

[Új – AzureRmRedisCachePatchSchedule](./New-AzureRmRedisCachePatchSchedule.md)

[Remove-AzureRmRedisCachePatchSchedule](./Remove-AzureRmRedisCachePatchSchedule.md)


