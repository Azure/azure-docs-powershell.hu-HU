---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679364"
---
# Restart-AzureRmRecoveryServicesAsrJob

## Áttekintés
Az Azure webhely-helyreállítási feladat újraindítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Újraindítás – AzureRmRecoveryServicesAsrJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.

## Példák

### Példa 1
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

A megadott ASR-feladat újraindítása, és az ASR-feladat frissített automatikus helyreállítási feladatát adja eredményül.

## PARAMÉTEREK

### -InputObject
A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amelyet az ASR-feladatnak megfelelően kell elindítani.
```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Adja meg a feladatot név szerint.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesAsrJob](./Get-AzureRmRecoveryServicesAsrJob.md)

[Önéletrajz – AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[Stop-AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
