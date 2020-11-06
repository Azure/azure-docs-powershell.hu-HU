---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503988"
---
# Get-AzureRmRecoveryServicesAsrJob

## Áttekintés
A megadott ASR-feladat részleteit vagy a legutóbbi ASR-feladatok listáját a helyreállítási szolgáltatások pincéjében kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByParam (alapértelmezett)
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### ByObject
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesAsrJob** parancsmag Azure webhely-helyreállítási feladatokat kap.
Ezzel a parancsmaggal megtekintheti az ASR-feladatokat a helyreállítási szolgáltatások pincéjében.

## Példák

### Példa 1
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Egy adott ASR-objektum összes feladatát visszaadja (az ASR-objektumra (például a többszörözött elemre vagy a helyreállítási csomagra) az AZONOSÍTÓval.) 

## PARAMÉTEREK

### -A befejezési időpont
A feladatok befejezési időpontját adja meg.
Ez a parancsmag a megadott időpontig kezdődő összes feladatot beilleszti.
Ha egy **datetime** objektumot szeretne beolvasni ehhez a paraméterhez, használja az Get-Date parancsmagot.
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Az ASR-feladat objektumát adja meg, amely frissíti a részleteket.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Adja meg az ASR-feladatot név szerint.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kezdő időpont
A feladatok kezdési időpontját adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely a megadott idő után elindult.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State (állami)
Az ASR-feladat állapotát adja meg.
Ez a parancsmag minden olyan feladatra bekerül, amely megfelel a megadott állapotnak.
A paraméter elfogadható értékei a következők:

- NotStarted
- Előrehaladás
- Sikerességéről
- Más
- Sikertelen
- Lemondott
- Felfüggesztve

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Az objektum AZONOSÍTÓját adja meg. A megadott objektumon a feladatok keresésére szolgál.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Újraindítás – AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[Önéletrajz – AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[Stop-AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
